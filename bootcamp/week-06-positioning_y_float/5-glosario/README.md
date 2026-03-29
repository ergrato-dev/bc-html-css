# 📖 Glosario — Semana 06: Positioning y Float

Términos técnicos clave ordenados alfabéticamente.

---

## A

**`absolute` (position)**
Valor de `position` que saca el elemento del flujo normal. Se posiciona respecto a su *containing block* (el ancestro posicionado más cercano). Sus vecinos actúan como si no existiera.

---

## B

**BFC (Block Formatting Context)**
Contexto de formateo de bloque. Zona de renderización independiente que contiene sus floats, evita la fusión de márgenes con el exterior y establece su propio eje de apilamiento. Se activa con `display: flow-root`, `overflow != visible`, `position: absolute/fixed`, entre otros.

---

## C

**`clear`**
Propiedad que indica que un elemento no puede colocarse al lado de un float. Valores: `left`, `right`, `both`, `none`. Se usa en clearfix.

**Clearfix**
Técnica para que un contenedor abarque sus hijos flotantes. Implementación clásica: `::after { content:""; display:block; clear:both; }`. Solución moderna: `display: flow-root`.

**Containing Block**
El cuadro de referencia respecto al cual se posiciona un elemento `absolute`. Es el ancestro posicionado más cercano (`position != static`). Si no hay ninguno, es el bloque inicial (elemento `<html>`).

---

## F

**`fixed` (position)**
Valor de `position` que posiciona el elemento respecto al viewport. No se mueve al hacer scroll. Saca el elemento del flujo normal.

**`float`**
Propiedad CSS que permite que un elemento flote a la izquierda o derecha de su contenedor y que el texto inline lo rodee. Valores: `left`, `right`, `none`.

**`flow-root` (display)**
Valor de display que crea un Block Formatting Context (BFC). La forma moderna de contener floats sin necesitar clearfix con pseudoelementos.

---

## I

**`inset`**
Propiedad shorthand para `top`, `right`, `bottom` y `left` juntas. `inset: 0` equivale a `top: 0; right: 0; bottom: 0; left: 0`. Muy útil para overlays.

**`isolation: isolate`**
Propiedad CSS que crea un nuevo stacking context sin necesitar `z-index` numérico. Ideal para aislar componentes de UI en design systems.

---

## O

**Overlay**
Elemento `position: fixed` con `inset: 0` y fondo semitransparente que cubre todo el viewport. Usado en modales, drawers y lightboxes.

---

## R

**`relative` (position)**
Valor de `position` que desplaza el elemento desde su posición original usando `top`, `right`, `bottom`, `left`. El elemento permanece en el flujo normal y su espacio original se conserva. El uso más común es crear un *containing block*.

---

## S

**Stacking Context**
Contexto de apilamiento. Jerarquía visual independiente en el eje Z. Los `z-index` dentro de un contexto solo compiten entre sí. Se crea con `position + z-index != auto`, `opacity < 1`, `transform`, `filter`, `isolation: isolate`, entre otros.

**`static` (position)**
Valor por defecto de `position`. El elemento sigue el flujo normal. `top`, `right`, `bottom`, `left` y `z-index` son ignorados.

**`sticky` (position)**
Combina `relative` y `fixed`. El elemento sigue el flujo normal hasta llegar al umbral definido (`top`, `left`, etc.), momento en que se "pega" mientras su contenedor sea visible. No saca el elemento del flujo.

---

## Z

**`z-index`**
Propiedad que controla el orden de apilamiento en el eje Z. Solo funciona en elementos con `position != static`. Un valor mayor queda encima de un valor menor. Solo es significativo dentro del mismo stacking context.
