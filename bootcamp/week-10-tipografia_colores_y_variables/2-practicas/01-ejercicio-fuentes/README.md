# Ejercicio 01 — Fuentes Web con Google Fonts

## 🎯 Objetivo

Cargar una fuente de Google Fonts usando el método `<link>` con `preconnect`, y aplicarla al proyecto mediante CSS Custom Properties.

---

## 📋 Pasos

### Paso 1: Preconnect y link de Google Fonts

Abre `starter/index.html`. Las etiquetas `<link>` de Google Fonts ya están en el `<head>`.

Observa la URL: incluye `display=swap` al final — esto activa `font-display: swap` automáticamente.

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&family=Fira+Code:wght@400&display=swap" rel="stylesheet" />
```

**Objetivo:** Comprobar en DevTools → Network que las fuentes se cargan.

### Paso 2: Declarar las fuentes como Custom Properties

Abre `starter/css/styles.css`. Descomenta la sección **PASO 2**.

Verás las variables `--font-body`, `--font-mono` con sus stacks de fallback.

### Paso 3: Aplicar las fuentes al documento

Descomenta la sección **PASO 3**.

`body` usará `var(--font-body)` e `.code-sample` usará `var(--font-mono)`.

### Paso 4: Escalar con font-weight

Descomenta la sección **PASO 4**.

Las variables `--font-regular`, `--font-semibold` y `--font-bold` se aplicarán a heading, labels y párrafos.

---

## ✅ Resultado Esperado

Al completar los 4 pasos, la tipografía del sitio debe variar visiblemente respecto al fallback del sistema (`Arial` o `Helvetica`). Verifica abriendo las DevTools → tab **Computed** → propiedad `font-family`.
