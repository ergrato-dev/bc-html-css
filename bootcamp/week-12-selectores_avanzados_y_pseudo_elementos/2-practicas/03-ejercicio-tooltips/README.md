# Ejercicio 03 — Tooltips CSS Puro

> **Semana 12 · Práctica 03** — Construir un sistema de tooltips sin JavaScript usando `[data-tooltip]` y `::after`.

---

## 🎯 Objetivos

- Leer atributos HTML desde CSS con la función `attr()`
- Posicionar el tooltip con `position: absolute` y `position: relative`
- Animar la aparición del tooltip con `opacity` y `visibility` (no con `display`)
- Hacer el tooltip accesible con `aria-label`

---

## 📋 Descripción

La página muestra un conjunto de botones de acción con iconos. Cada botón tiene un atributo `data-tooltip` con la descripción de la acción. Tú implementarás el tooltip puro en CSS.

Abre `starter/css/styles.css` y descomenta los bloques paso a paso.

---

## Paso 1 — Contenedor relativo y tooltip invisible

Establecer el contexto de posicionamiento y crear el `::after` con `content: attr(data-tooltip)`, invisible por defecto.

```css
[data-tooltip] {
  position: relative; /* contexto para el ::after */
}

[data-tooltip]::after {
  content: attr(data-tooltip);  /* lee el atributo HTML */
  position: absolute;
  bottom: calc(100% + 8px);
  left: 50%;
  transform: translateX(-50%);
  /* Invisible por defecto con visibility (no display:none) */
  opacity: 0;
  visibility: hidden;
  /* Estilos visuales del tooltip */
  background: hsl(220 14% 14%);
  color: hsl(220 18% 88%);
  font-size: 0.75rem;
  white-space: nowrap;
  padding: 0.4em 0.8em;
  border-radius: 6px;
  border: 1px solid hsl(220 12% 24%);
  pointer-events: none;
}
```

**Abre `starter/css/styles.css`** y descomenta `PASO 1`.

---

## Paso 2 — Mostrar el tooltip en `:hover` y `:focus`

Hacer visible el tooltip cuando el botón recibe hover o foco de teclado.

```css
[data-tooltip]:hover::after,
[data-tooltip]:focus::after {
  opacity: 1;
  visibility: visible;
}
```

**Descomenta `PASO 2`** en el CSS.

---

## Paso 3 — Transición suave

Añadir transiciones a `opacity` y `visibility` para que el tooltip aparezca y desaparezca suavemente.

```css
[data-tooltip]::after {
  /* Añadir al bloque existente del Paso 1 */
  transition:
    opacity    150ms ease-out,
    visibility 150ms ease-out;
}
```

**Descomenta `PASO 3`** en el CSS.

---

## Paso 4 — Flecha decorativa con `::before`

Añadir un pequeño triángulo debajo del tooltip como "cola" apuntando al botón.

```css
[data-tooltip]::before {
  content: "";
  position: absolute;
  bottom: calc(100% + 2px);
  left: 50%;
  transform: translateX(-50%);
  border: 5px solid transparent;
  border-top-color: hsl(220 12% 24%);
  opacity: 0;
  visibility: hidden;
  transition: opacity 150ms ease-out, visibility 150ms ease-out;
  pointer-events: none;
}

[data-tooltip]:hover::before,
[data-tooltip]:focus::before {
  opacity: 1;
  visibility: visible;
}
```

**Descomenta `PASO 4`** en el CSS.

---

## ✅ Resultado esperado

- Cada botón muestra un tooltip con su descripción al hacer hover
- Los tooltips también aparecen al navegar con Tab (accesibilidad de teclado)
- La aparición y desaparición son suaves gracias a la transición
- Los tooltips tienen una pequeña flecha apuntando al botón
- No se usa ninguna línea de JavaScript
