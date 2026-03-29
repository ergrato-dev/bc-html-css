# 📖 Glosario — Semana 05: CSS Box Model y Display

Términos técnicos clave ordenados alfabéticamente.

---

## A

**`auto` (margin)**
Valor especial para `margin-left` y `margin-right` que hace que el navegador calcule el margen automáticamente. Usado en el patrón `margin: 0 auto` para centrar un elemento en línea horizontalmente.

---

## B

**`block` (display)**
Valor de `display` que hace que el elemento ocupe todo el ancho disponible, genera un salto de línea antes y después, y respeta `width` y `height`.

**`border-box` (box-sizing)**
Modelo de caja donde `width` y `height` incluyen el `padding` y el `border`. El área de contenido se reduce para compensar. `100px` siempre ocupa `100px` independientemente viendo del padding o border.

**`border` (Box Model)**
Segunda capa del Box Model. Línea opcional alrededor del `padding`. Su grosor se suma al tamaño total del elemento en `content-box`.

**`box-sizing`**
Propiedad CSS que define cómo se calcula el `width` y `height` de un elemento. Valores: `content-box` (por defecto) y `border-box`.

**BFC (Block Formatting Context)**
Contexto de formatos de bloque. Zona de renderización independiente que evita la fusión de márgenes con su contenedor y contiene los floats. Se activa con `overflow: hidden`, `display: flow-root`, etc.

---

## C

**Cascade (Cascada CSS)**
Algoritmo que determina qué declaración CSS prevalece cuando hay conflictos. Considera: origen, especificidad y orden de aparición.

**`content-box` (box-sizing)**
Modelo de caja por defecto. `width` y `height` solo miden el área de contenido. El `padding` y `border` se añaden encima, aumentando el tamaño total del elemento.

**`content` (Box Model)**
Capa más interna del Box Model. Es donde se renderiza el texto e imágenes. Su tamaño está definido por `width` y `height`.

---

## D

**`display`**
Propiedad CSS que controla cómo un elemento genera su caja y cómo interactúa con otros elementos. Valores comunes: `block`, `inline`, `inline-block`, `flex`, `grid`, `none`.

---

## F

**`flex` (display)**
Activa el modelo Flexbox en el contenedor. Sus hijos directos se convierten en flex items, organizados en ejes principal y cruzado. Tema de la semana 07.

---

## H

**`height`**
Propiedad que define la altura del área de contenido (o del elemento completo si `box-sizing: border-box`). En `display: inline`, se ignora.

---

## I

**`inline` (display)**
Valor que hace que el elemento fluya dentro del texto. No acepta `width`, `height` ni `margin` vertical. Solo respeta padding horizontal.

**`inline-block` (display)**
Combina lo mejor de `block` e `inline`: fluye en línea con el texto pero acepta `width`, `height` y todos los márgenes.

---

## M

**`margin`**
Capa externa del Box Model. Espacio transparente fuera del `border`. Separa el elemento de su entorno. Puede ser negativo.

**Margin Collapse (colapsado de márgenes)**
Fenómeno CSS donde dos márgenes verticales adyacentes se fusionan en uno solo (el mayor de los dos). Ocurre entre hermanos y entre padre e hijo. No ocurre en contextos flex/grid ni con overflow != visible.

---

## N

**`none` (display)**
Elimina el elemento del flujo del documento y de la pantalla. No ocupa espacio. Diferente de `visibility: hidden`, que oculta pero mantiene el espacio.

---

## O

**`object-fit`**
Controla cómo una imagen o video se ajusta dentro de su caja. `cover` rellena sin deformar (recortando), `contain` cabe completo (con espacios). Muy útil con imágenes de tamaño fijo.

**`overflow`**
Controla qué ocurre con el contenido que desborda la caja. Valores: `visible` (por defecto), `hidden` (recorta), `scroll` (siempre scrollbar), `auto` (scrollbar solo si necesario).

---

## P

**`padding`**
Tercera capa del Box Model. Espacio interno entre el `border` y el `content`. Hereda el fondo (`background`) del elemento.

---

## R

**Reset CSS**
Hoja de estilos que anula los estilos por defecto del navegador para garantizar consistencia entre diferentes navegadores. La regla `* { box-sizing: border-box; margin: 0; padding: 0; }` es la base de todo reset moderno.

---

## S

**Shorthand (propiedad abreviada)**
Propiedad CSS que agrupa varias propiedades en una. Ejemplo: `margin: 10px 20px 15px 5px` equivale a top/right/bottom/left. Para 1 valor: todos lados; 2 valores: vertical / horizontal; 3 valores: top / horizontal / bottom.

---

## T

**`text-overflow`**
Controla cómo se muestra el texto que desborda su contenedor. El valor `ellipsis` muestra `...` al final. Requiere `white-space: nowrap` y `overflow: hidden` para funcionar.

---

## V

**`visibility`**
Controla la visibilidad de un elemento. `hidden` lo oculta visualmente pero mantiene su espacio en el layout (a diferencia de `display: none`).

---

## W

**`width`**
Propiedad que define el ancho del área de contenido (o del elemento completo si `box-sizing: border-box`). En `display: inline`, se ignora.
