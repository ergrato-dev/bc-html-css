# Ejercicio 02 — Grid Areas

Practica `grid-template-areas`, `grid-area`, spanning con líneas y responsive changes.

---

## Paso 1: Definir layout con `grid-template-areas`

El contenedor `.page-grid` tiene cuatro hijos: header, sidebar, main y footer. Activa CSS Grid y define las áreas:

```css
.page-grid {
  display: grid;
  grid-template-columns: 220px 1fr;
  grid-template-rows: auto 1fr auto;
  grid-template-areas:
    "header  header"
    "sidebar main"
    "footer  footer";
  min-height: 100vh;
}
```

**Abre `starter/css/styles.css`** y descomenta la sección del PASO 1.

---

## Paso 2: Asignar `grid-area` a cada hijo

Cada hijo tiene que declarar en qué área vive:

```css
.pg-header  { grid-area: header; }
.pg-sidebar { grid-area: sidebar; }
.pg-main    { grid-area: main; }
.pg-footer  { grid-area: footer; }
```

**Descomenta la sección del PASO 2**.

---

## Paso 3: Spanning con líneas de grid

El elemento `.featured` debe ocupar toda la anchura disponible dentro de `.pg-main`:

```css
/* span usando número de línea */
.featured { grid-column: 1 / -1; }

/* equivalente con span */
.featured { grid-column: span 2; }
```

**Descomenta la sección del PASO 3**. Observa cómo `.featured` se extiende por todas las columnas internas del área main.

---

## Paso 4: Responsive — cambiar áreas en mobile

En pantallas pequeñas, sidebar se coloca debajo del main:

```css
@media (max-width: 767px) {
  .page-grid {
    grid-template-columns: 1fr;
    grid-template-areas:
      "header"
      "main"
      "sidebar"
      "footer";
  }
}
```

**Descomenta la sección del PASO 4**. Redimensiona la ventana y observa el reordenamiento sin tocar el HTML.
