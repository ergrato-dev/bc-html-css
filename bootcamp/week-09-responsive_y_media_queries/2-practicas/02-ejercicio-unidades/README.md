# Ejercicio 02 — Unidades Relativas

Practica `rem`, `em`, `vw`, `vh`, `%` y `clamp()` en un entorno real.

---

## Paso 1: Tipografía con `rem`

Reemplaza los tamaños de texto fijos (`px`) por `rem`:

```css
h1 { font-size: 2rem; }      /* 32px */
h2 { font-size: 1.5rem; }    /* 24px */
p  { font-size: 1rem; }      /* 16px */
small { font-size: 0.875rem; } /* 14px */
```

**Abre `starter/css/styles.css`** y descomenta la sección del PASO 1. Prueba cambiar el zoom del navegador — todo el texto escala proporcionalmente.

---

## Paso 2: Espaciados con `rem` y `em` en botones

```css
/* rem para spacing global */
.section { padding: 2rem 0; }

/* em para padding de botón (escala con el texto del botón) */
.btn { padding: 0.65em 1.3em; }
```

**Descomenta la sección del PASO 2**. Cambia el `font-size` del `.btn` y observa cómo el padding escala.

---

## Paso 3: Hero con `vw` y `vh`

```css
.hero {
  min-height: 100vh; /* ocupa toda la pantalla */
  display: flex;
  align-items: center;
}
```

**Descomenta la sección del PASO 3**. Observa cómo el hero ocupa exactamente la altura del viewport.

---

## Paso 4: Tipografía fluida con `clamp()`

```css
h1 {
  font-size: clamp(1.75rem, 5vw, 3rem);
}

.hero-subtitle {
  font-size: clamp(1rem, 2.5vw, 1.25rem);
}
```

**Descomenta la sección del PASO 4**. Redimensiona la ventana lentamente — el texto crece y encoge de forma fluida sin saltos.
