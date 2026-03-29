# Glosario — Semana 07: Flexbox

Términos clave de Flexbox ordenados alfabéticamente.

---

## A

### align-content
Alinea las **líneas** de un contenedor flex con `flex-wrap: wrap` en el **eje cruzado**. Solo tiene efecto cuando hay más de una línea. Valores: `flex-start`, `flex-end`, `center`, `space-between`, `space-around`, `stretch`.

```css
.container {
  display: flex;
  flex-wrap: wrap;
  align-content: space-between; /* distribuye las filas */
}
```

### align-items
Alinea los flex items en el **eje cruzado** dentro de su línea. Afecta a todos los items del contenedor. Por defecto es `stretch`.

```css
.container {
  display: flex;
  align-items: center; /* centra verticalmente (en row) */
}
```

### align-self
Sobreescribe `align-items` para un **item individual**. Útil para destacar un elemento del resto.

```css
.item-especial {
  align-self: flex-end; /* solo este item va al fondo */
}
```

---

## C

### cross axis (eje cruzado)
El eje **perpendicular** al eje principal. Si `flex-direction: row`, el eje cruzado es vertical. `align-items` y `align-self` actúan sobre este eje.

---

## D

### display: flex
Activa el **contexto de formato flexible** en un elemento, convirtiendo sus hijos directos en flex items.

```css
.container { display: flex; }
```

---

## F

### flex (shorthand)
Forma corta que combina `flex-grow`, `flex-shrink` y `flex-basis`. El valor más común es `flex: 1` (equivale a `1 1 0%`).

```css
.item { flex: 1; }           /* crece para llenar */
.item { flex: 0 0 200px; }   /* tamaño fijo */
.item { flex: 1 1 250px; }   /* mínimo 250px + crece */
```

### flex-basis
Define el **tamaño inicial** del flex item antes de distribuir el espacio libre. Puede ser un valor fijo (`200px`), porcentaje, `auto` (usa width/height) o `0%`.

### flex container
El elemento que tiene `display: flex` o `display: inline-flex`. Establece el contexto Flexbox para sus hijos directos.

### flex-direction
Define la dirección del **eje principal**: `row` (horizontal, por defecto), `row-reverse`, `column` (vertical), `column-reverse`. Cambia en qué eje actúa `justify-content`.

### flex-grow
Factor de crecimiento proporcional. `flex-grow: 1` distribuye el espacio libre igualmente. `flex-grow: 2` absorbe el doble que `flex-grow: 1`. Por defecto es `0` (no crece).

### flex item
Cada hijo directo de un flex container. Se convierte automáticamente en flex item al aplicar `display: flex` al padre.

### flex-shrink
Factor de encogimiento. `flex-shrink: 0` evita que el item se reduzca cuando no hay espacio suficiente. Por defecto es `1` (puede encoger).

### flex-wrap
Controla si los items se colocan en una sola línea (`nowrap`, por defecto) o pueden saltar a varias líneas (`wrap`). `wrap-reverse` invierte el orden de las líneas.

---

## G

### gap
Espacio entre flex items (y entre líneas en `flex-wrap`). Equivale a `row-gap` + `column-gap`. Preferible a `margin` porque no afecta a los bordes del contenedor.

```css
.container {
  display: flex;
  gap: 1rem;           /* igual en filas y columnas */
  gap: 1rem 1.5rem;    /* row-gap col-gap */
}
```

---

## J

### justify-content
Distribuye los flex items en el **eje principal**. Valores: `flex-start` (por defecto), `flex-end`, `center`, `space-between`, `space-around`, `space-evenly`.

```css
.navbar {
  display: flex;
  justify-content: space-between; /* logo ← → nav */
}
```

---

## M

### main axis (eje principal)
El eje en que se colocan los flex items por defecto. Horizontal (`row`) o vertical (`column`). `justify-content` actúa sobre este eje.

---

## O

### order
Cambia el **orden visual** de un flex item sin modificar el DOM. Por defecto todos tienen `order: 0`. `order: -1` coloca el item antes de todos.

> ⚠️ Puede afectar la accesibilidad al desacoplar el orden visual del orden del DOM.

---

## W

### wrap
Ver `flex-wrap`. El contenedor con `flex-wrap: wrap` permite que los items salten a la siguiente línea cuando no caben en una sola.
