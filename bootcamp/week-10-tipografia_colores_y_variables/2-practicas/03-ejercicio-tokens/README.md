# Ejercicio 03 — Sistema de Design Tokens

## 🎯 Objetivo

Construir un sistema completo de **design tokens** usando CSS Custom Properties, con paleta de colores en HSL, espaciados en `rem`, y uso de `calc()` para valores derivados.

---

## 📋 Pasos

### Paso 1: Tokens de color primitivos y semánticos

Abre `starter/css/styles.css` y descomenta la sección **PASO 1**.

Se declaran los hue base y la paleta primitiva, más los tokens semánticos que hacen referencia a los primitivos:

```css
:root {
  --hue-brand: 225;
  --blue-500:  hsl(var(--hue-brand) 73% 52%);
  --color-primary: var(--blue-500);
}
```

Cambiar `--hue-brand` actualiza toda la paleta automáticamente.

### Paso 2: Tokens de espaciado y tipografía

Descomenta la sección **PASO 2**.

Variables para tipografía (`--font-*`, `--text-*`) y escalas de espaciado (`--space-1` a `--space-16`).

### Paso 3: Tokens de forma (border-radius y shadow)

Descomenta la sección **PASO 3**.

Variables para `--radius-*` y `--shadow-*`.

### Paso 4: Override de tema oscuro

Descomenta la sección **PASO 4**.

`@media (prefers-color-scheme: dark)` redefine solo los tokens semánticos de color — el resto permanece igual.

---

## ✅ Resultado Esperado

Al completar los 4 pasos, las tarjetas de la demo deben mostrar los tokens aplicados visualmente. Activa/desactiva el modo oscuro del SO para ver el cambio de tema automático.
