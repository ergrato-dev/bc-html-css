# Ejercicio 03 — Breakpoints con Grid y Flex

Combina CSS Grid, Flexbox y `@media (min-width)` para un layout completamente responsive.

---

## Paso 1: Layout base (mobile 320px+)

Empieza con la estructura más simple: navegación vertical, hero en 1 columna, cards en 1 columna:

```css
.main-nav  { flex-direction: column; }
.page-grid { grid-template-columns: 1fr; }
```

**Abre `starter/css/styles.css`** y descomenta la sección del PASO 1.

---

## Paso 2: Tablet `@media (min-width: 768px)`

En tablet, la navegación pasa a horizontal y el grid a 2 columnas:

```css
@media (min-width: 768px) {
  .main-nav { flex-direction: row; }
  .page-grid { grid-template-columns: repeat(2, 1fr); }
}
```

**Descomenta la sección del PASO 2**.

---

## Paso 3: Desktop `@media (min-width: 1024px)`

El layout pasa a sidebar + contenido principal con grid-template-areas:

```css
@media (min-width: 1024px) {
  .app-layout {
    display: grid;
    grid-template-columns: 240px 1fr;
    grid-template-areas: "sidebar content";
    min-height: calc(100vh - 60px);
  }

  .app-sidebar { grid-area: sidebar; }
  .app-content { grid-area: content; }
  .page-grid   { grid-template-columns: repeat(3, 1fr); }
}
```

**Descomenta la sección del PASO 3**.

---

## Paso 4: Sin scroll horizontal

Asegura que no haya overflow en ningún tamaño:

```css
img, video { max-width: 100%; height: auto; }
```

**Descomenta la sección del PASO 4**. Inspecciona en DevTools con 320px de ancho y verifica que no haya scroll horizontal.
