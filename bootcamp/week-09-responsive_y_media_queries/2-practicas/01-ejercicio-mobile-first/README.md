# Ejercicio 01 — Mobile-first

Construye estilos base para mobile y escala hacia tablet y desktop usando `@media (min-width)`.

---

## Paso 1: Estilos base (mobile 320px+)

Sin ninguna media query, los estilos base se aplican a todos los tamaños. Define:

```css
.site-nav {
  display: flex;
  flex-direction: column; /* links apilados */
  gap: 0.5rem;
}

.cards-grid {
  display: grid;
  grid-template-columns: 1fr; /* 1 columna */
  gap: 1rem;
}
```

**Abre `starter/css/styles.css`** y descomenta la sección del PASO 1.

---

## Paso 2: Tablet pequeña `@media (min-width: 480px)`

En 480px o más, el grid pasa a 2 columnas:

```css
@media (min-width: 480px) {
  .cards-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

**Descomenta la sección del PASO 2**. Redimensiona la ventana para ver el cambio.

---

## Paso 3: Tablet `@media (min-width: 768px)`

En 768px, la navegación pasa a horizontal y el hero crece:

```css
@media (min-width: 768px) {
  .site-nav {
    flex-direction: row;
    gap: 1.5rem;
  }

  .hero-title {
    font-size: 2.5rem;
  }
}
```

**Descomenta la sección del PASO 3**.

---

## Paso 4: Desktop `@media (min-width: 1024px)`

En desktop, 3 columnas y un hero más grande:

```css
@media (min-width: 1024px) {
  .cards-grid {
    grid-template-columns: repeat(3, 1fr);
  }

  .hero-title {
    font-size: 3rem;
  }

  .container {
    max-width: 1100px;
  }
}
```

**Descomenta la sección del PASO 4**. Comprara el resultado en DevTools Device Toolbar.
