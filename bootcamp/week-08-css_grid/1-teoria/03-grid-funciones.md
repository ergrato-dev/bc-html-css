# CSS Grid — Funciones Avanzadas: repeat(), minmax(), auto-fit

Las funciones de CSS Grid permiten crear layouts **totalmente responsive sin media queries** para la rejilla de items.

---

## 🎯 Objetivos

- Generar columnas repetidas con `repeat()`
- Definir rangos de tamaño con `minmax()`
- Crear grids automáticamente responsive con `auto-fit` y `auto-fill`
- Aplicar tamaños fluidos con `clamp()`

---

## 1. repeat()

`repeat(n, tamaño)` evita escribir el mismo valor múltiples veces.

```css
/* Sin repeat: verboso */
.grid { grid-template-columns: 1fr 1fr 1fr 1fr; }

/* Con repeat: limpio */
.grid { grid-template-columns: repeat(4, 1fr); }

/* Con patrón: repite el patrón N veces */
.grid { grid-template-columns: repeat(3, 1fr 2fr); }
/* Resultado: 1fr 2fr  1fr 2fr  1fr 2fr → 6 columnas */
```

---

## 2. minmax(mínimo, máximo)

Define un rango de tamaño. La columna no será menor que `mínimo` ni mayor que `máximo`.

```css
/* Columna de mínimo 200px, máximo 1fr */
.grid {
  grid-template-columns: repeat(3, minmax(200px, 1fr));
}

/* Fila de mínimo 100px, máximo contenido */
.grid {
  grid-auto-rows: minmax(100px, auto);
}
```

Casos comunes:

```css
minmax(200px, 1fr)  /* mínimo 200px, crece hasta fr */
minmax(0, 1fr)      /* sin mínimo, solo crece (útil para evitar overflow) */
minmax(auto, 1fr)   /* mínimo = tamaño del contenido */
```

---

## 3. auto-fit: grid responsive sin media queries

`auto-fit` con `minmax()` es el patrón más usado en CSS Grid responsive. Crea tantas columnas como quepan en el ancho disponible.

```css
/* Cards totalmente responsive: sin una sola media query */
.card-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(240px, 1fr));
  gap: 1.5rem;
}
```

Comportamiento:
- En pantalla ancha (1200px): caben ~4 columnas de 240px → **4 columnas**
- En tablet (768px): caben ~2 columnas → **2 columnas**
- En móvil (400px): solo cabe 1 columna → **1 columna de 400px (>240px)**

> 🎯 `auto-fit` colapsa las columnas vacías. Si hay 3 items en un grid de 4 posibles columnas, los 3 items crecen hasta `1fr` para llenar el espacio.

---

## 4. auto-fill vs. auto-fit

La diferencia es sutil pero importante:

```css
/* auto-fill: mantiene columnas vacías reservando espacio */
.grid-fill { grid-template-columns: repeat(auto-fill, minmax(200px, 1fr)); }

/* auto-fit: colapsa columnas vacías (items ocupan todo el ancho) */
.grid-fit  { grid-template-columns: repeat(auto-fit,  minmax(200px, 1fr)); }
```

Con 2 items en un contenedor ancho:
- `auto-fill`: `[item1][item2][vacío][vacío]` — items no se expanden
- `auto-fit`: `[    item1    ][    item2    ]` — items se expanden a 1fr

📌 **Cuándo usar cada uno:**
- `auto-fit`: cuando quieres que los pocos items existentes llenen el ancho
- `auto-fill`: cuando quieres mantener el tamaño de item aunque sobren celdas

---

## 5. clamp() para columnas fluidas

`clamp(mínimo, preferido, máximo)` crea columnas que crecen fluidamente entre un mínimo y máximo.

```css
.fluid-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(clamp(200px, 30%, 350px), 1fr));
  gap: 1rem;
}
```

Equivale a: mínimo 200px, preferido 30% del contenedor, máximo 350px.

---

## 6. Patrones prácticos

### Gallery de imágenes

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
  grid-auto-rows: 180px; /* filas cuadradas */
  gap: 0.5rem;
}

.gallery img {
  width: 100%;
  height: 100%;
  object-fit: cover; /* rellena sin deformar */
}
```

### Dashboard de stats cards

```css
.stats {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
}
```

### Layout de página completa

```css
.page {
  display: grid;
  grid-template-areas:
    "header"
    "main"
    "footer";
  grid-template-rows: auto 1fr auto;
  min-height: 100vh;
}

@media (min-width: 768px) {
  .page {
    grid-template-columns: 240px 1fr;
    grid-template-areas:
      "header  header"
      "sidebar main"
      "footer  footer";
  }
}
```

---

## 📚 Recursos Adicionales

- [MDN — repeat()](https://developer.mozilla.org/es/docs/Web/CSS/repeat)
- [MDN — minmax()](https://developer.mozilla.org/es/docs/Web/CSS/minmax)
- [CSS-Tricks — auto-fill vs auto-fit](https://css-tricks.com/auto-sizing-columns-css-grid-auto-fill-vs-auto-fit/)

---

## ✅ Checklist

- [ ] `repeat(3, 1fr)` genera 3 columnas iguales
- [ ] `minmax(200px, 1fr)` limita el tamaño de una columna
- [ ] `repeat(auto-fit, minmax(220px, 1fr))` crea un grid responsive sin media queries
- [ ] `auto-fit` colapsa columnas vacías; `auto-fill` las reserva
- [ ] `grid-auto-rows: minmax(100px, auto)` controla filas implícitas
