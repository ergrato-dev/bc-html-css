# CSS Grid — Contenedor y Unidad fr

CSS Grid es el sistema de layout **bidimensional** de CSS: controla filas y columnas al mismo tiempo, a diferencia de Flexbox que es unidimensional.

![Conceptos de CSS Grid](../0-assets/01-grid-conceptos.svg)

---

## 🎯 Objetivos

- Activar CSS Grid con `display: grid`
- Definir columnas con `grid-template-columns`
- Controlar filas con `grid-template-rows`
- Usar la unidad `fr` (fracción)
- Añadir espacio con `gap`

---

## 1. display: grid

`display: grid` convierte el elemento en un **grid container**. Sus hijos directos se convierten en **grid items** y se colocan automáticamente en las celdas del grid.

```css
.container {
  display: grid;
  /* Por defecto: una sola columna, filas automáticas */
}
```

> A diferencia de Flexbox, el grid actúa en dos ejes simultáneamente: columnas (eje inline) y filas (eje block).

---

## 2. grid-template-columns

Define el número y tamaño de las columnas.

```css
/* Tres columnas de igual tamaño */
.grid-3-equal {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  /* equivale a: repeat(3, 1fr) */
}

/* Sidebar fija + contenido flexible */
.layout-sidebar {
  display: grid;
  grid-template-columns: 240px 1fr;
}

/* Tres columnas: fija, flexible, fija */
.layout-mixed {
  display: grid;
  grid-template-columns: 200px 1fr 300px;
}
```

---

## 3. La unidad fr (fracción)

`fr` representa una **fracción del espacio disponible** en el grid, después de restar los valores fijos y los gaps.

```css
.grid {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  /* Total 4fr: primera columna = 1/4, segunda = 2/4, tercera = 1/4 */
  gap: 1rem;
}
```

Equivalencia visual: `1fr 2fr 1fr` → 25% / 50% / 25% del espacio disponible.

```css
/* Comparación con unidades fijas */
.bad  { grid-template-columns: 300px auto 200px; } /* auto puede ser impredecible */
.good { grid-template-columns: 300px 1fr 200px;  } /* 1fr ocupa exactamente el resto */
```

---

## 4. grid-template-rows

Define el tamaño de las filas. Si no se especifica, las filas tienen altura automática (igual al contenido más alto).

```css
.grid-with-rows {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-template-rows: 80px auto 60px; /* header / contenido / footer */
  min-height: 100vh;
}
```

---

## 5. gap (row-gap + column-gap)

`gap` añade espacio entre celdas del grid. Es la forma moderna de `grid-gap` (obsoleto).

```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1.5rem;          /* igual en filas y columnas */
  gap: 1rem 2rem;       /* row-gap col-gap */
  row-gap: 1rem;        /* solo entre filas */
  column-gap: 1.5rem;   /* solo entre columnas */
}
```

---

## 6. Colocación automática

Los grid items se colocan automáticamente de izquierda a derecha, llenando celdas y creando nuevas filas según sea necesario.

```css
/* 6 items en un grid de 3 columnas → 2 filas automáticas */
.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}
/* Los 6 <article> hijos se distribuyen automáticamente */
```

> Esto es **colocación implícita**: el grid crea filas nuevas cuando se acaban las definidas. `grid-auto-rows` controla su tamaño.

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  grid-auto-rows: 200px; /* todas las filas implícitas miden 200px */
  gap: 1rem;
}
```

---

## 7. Grid vs. Flexbox: ¿cuándo usar cada uno?

| Criterio | Flexbox | CSS Grid |
|----------|---------|----------|
| Dirección | Una dimensión (fila o columna) | Dos dimensiones (ambas) |
| Control de layout | Items controlan su tamaño | Contenedor define la estructura |
| Caso de uso | Navbar, botones, cards en fila | Layouts de página, galleries, dashboards |
| Responsive | `flex-wrap` + `flex: 1 1 Xpx` | `auto-fit` + `minmax()` |

📌 **Regla práctica:** Si piensas en filas Y columnas simultáneamente, usa Grid. Si solo necesitas una dirección, usa Flexbox.

---

## 📚 Recursos Adicionales

- [MDN — CSS Grid Layout](https://developer.mozilla.org/es/docs/Web/CSS/CSS_grid_layout)
- [CSS-Tricks — A Complete Guide to Grid](https://css-tricks.com/snippets/css/complete-guide-grid/)

---

## ✅ Checklist

- [ ] `display: grid` activa el contexto de grid en el contenedor
- [ ] `grid-template-columns: repeat(3, 1fr)` crea 3 columnas iguales
- [ ] La unidad `fr` distribuye el espacio disponible proporcionalmente
- [ ] `gap` añade espacio consistente entre celdas
- [ ] Las filas se crean automáticamente según el número de items
