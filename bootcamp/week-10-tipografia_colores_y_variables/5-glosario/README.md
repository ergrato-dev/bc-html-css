# Glosario — Semana 10: Tipografía, Colores y CSS Variables

Términos técnicos en orden alfabético.

---

## @font-face

Regla CSS que permite registrar fuentes personalizadas (locales o remotas) para usarlas con `font-family`.

```css
@font-face {
  font-family: 'MiFuente';
  src: url('fuentes/mi-fuente.woff2') format('woff2');
  font-display: swap;
}
```

---

## `calc()`

Función CSS que realiza cálculos matemáticos (+, -, *, /) directamente en los estilos. Puede mezclar unidades y Custom Properties.

```css
.elemento {
  width: calc(100% - var(--sidebar-width));
  padding: calc(var(--space-4) * 2);
}
```

---

## Cascada de colores (color-scheme)

Propiedad CSS que indica al navegador si el elemento prefiere el modo claro u oscuro, afectando colores de UI del sistema.

```css
:root { color-scheme: light dark; }
```

---

## CSS Custom Property (`--variable`)

Variable definida por el desarrollador que almacena un valor reutilizable. Se declara con `--` y se consume con `var()`.

```css
:root { --color-primary: hsl(225 73% 52%); }
.btn  { background: var(--color-primary); }
```

---

## Design Token

Unidad mínima de un sistema de diseño expresada como variable nombrada. Existen dos niveles: tokens **primitivos** (valores concretos) y tokens **semánticos** (valores con intención).

---

## `em`

Unidad relativa al `font-size` del elemento padre. Útil para padding/margin proporcional al tamaño de texto del componente.

```css
.btn { padding: 0.625em 1.25em; } /* se escala con font-size */
```

---

## FOIT (Flash of Invisible Text)

Comportamiento del navegador donde el texto permanece invisible mientras carga la fuente web. Comportamiento de `font-display: block`.

---

## FOUT (Flash of Unstyled Text)

Comportamiento donde el texto se muestra en la fuente de respaldo antes de que cargue la fuente web. Comportamiento de `font-display: swap`.

---

## `font-display`

Propiedad de `@font-face` que controla cómo se carga la fuente web:

| Valor | Comportamiento |
|-------|---------------|
| `swap` | FOUT — fuente de respaldo inmediata (**recomendado**) |
| `block` | FOIT — texto invisible hasta 3s |
| `fallback` | Mezcla: 100ms invisible, luego swap solo si carga rápido |
| `optional` | El navegador decide según la conexión |

---

## Google Fonts

Servicio de fuentes web gratuito de Google. Integración con `<link>` + `preconnect` para mayor rendimiento.

```html
<link rel="preconnect" href="https://fonts.googleapis.com" />
<link href="https://fonts.googleapis.com/css2?family=Inter&display=swap" rel="stylesheet" />
```

---

## HSL

Formato de color **Hue / Saturation / Lightness**. Intuitivo para crear paletas y variar el contraste sin cambiar el tono.

```css
/* Hue: 0-360° | Saturation: 0-100% | Lightness: 0-100% */
--color-primary: hsl(225 73% 52%);
```

---

## Hue (tono)

Primer parámetro de HSL. Valor entre 0° y 360° que representa el ángulo en la rueda de color (0=rojo, 120=verde, 240=azul).

---

## Lightness (luminosidad)

Tercer parámetro de HSL. 0% = negro, 50% = color puro, 100% = blanco. Permite generar paletas de claro a oscuro con el mismo hue.

---

## `linear-gradient()`

Función CSS que crea un degradé entre dos o más colores a lo largo de una dirección.

```css
background: linear-gradient(135deg, hsl(225 73% 52%), hsl(270 60% 50%));
```

---

## Magic Number (anti-patrón)

Valor numérico literal en CSS sin contexto ni variable. Dificulta el mantenimiento y la coherencia del sistema.

```css
/* ❌ Magic number */
.card { padding: 24px; }

/* ✅ Token semántico */
.card { padding: var(--space-6); }
```

---

## oklch

Formato de color moderno basado en percepción humana (Lightness, Chroma, Hue). Produce colores perceptualmente uniformes y evita el problema del "gris sucio" de HSL.

```css
--color-primary: oklch(55% 0.18 260);
```

---

## Paleta semántica

Sistema de colores donde los nombres reflejan su **función** (no su apariencia): `--color-primary`, `--color-danger`, `--color-muted`.

---

## `preconnect`

Directiva HTML que inicia la conexión con un servidor externo antes de que el navegador la necesite, reduciendo la latencia de fuentes web.

```html
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
```

---

## Token primitivo

Token que almacena el **valor concreto**: `--blue-500: hsl(225 73% 52%)`. Base de la escala de color.

---

## Token semántico

Token que almacena la **intención**: `--color-primary: var(--blue-500)`. Facilita los temas (dark/light) sin cambiar el HTML ni el CSS de los componentes.

---

## Razón modular (type scale ratio)

Factor multiplicador entre niveles de una escala tipográfica. La razón **1.25 (Major Third)** es la más usada:

```
base × 1.25 = md
base × 1.25² = lg
base × 1.25³ = xl   ...y así sucesivamente
```

---

## `rem`

Unidad relativa al `font-size` del elemento `<html>` (root). Estable e independiente de anidamiento. `1rem = 16px` si no se modifica la raíz.

---

## `:root`

Pseudo-clase que selecciona el elemento raíz del documento (`<html>`). Tiene mayor especificidad que `html {}`. Lugar estándar para declarar Custom Properties globales.

---

## Saturation (saturación)

Segundo parámetro de HSL. 0% = gris (sin color), 100% = color puro y vivo.

---

## Token

Ver **Design Token**.

---

## `var()`

Función CSS que consume el valor de una Custom Property. Acepta un valor de respaldo (fallback):

```css
color: var(--color-primary, hsl(225 73% 52%));
```
