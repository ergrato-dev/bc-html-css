# Glosario — Semana 12: Selectores Avanzados & Pseudo-elementos

Términos clave de la semana ordenados alfabéticamente.

---

## A

### `::after`
Pseudo-elemento que inserta contenido **después** del contenido real de un elemento. Requiere la propiedad `content`. No se crea en el DOM real y no es accesible para lectores de pantalla.

```css
.card::after {
  content: "↗";
  position: absolute;
  top: 1rem;
  right: 1rem;
}
```

### `attr()`
Función CSS que lee el valor de un atributo HTML del elemento y lo inserta como contenido de texto. Se usa principalmente en `content` con pseudo-elementos.

```css
[data-tooltip]::after {
  content: attr(data-tooltip); /* Lee data-tooltip="Guardar" */
}
```

---

## B

### `::before`
Pseudo-elemento que inserta contenido **antes** del contenido real de un elemento. Requiere `content`. Igual que `::after`, no está en el DOM y no es accesible.

```css
.feature-item::before {
  content: "▸";
  color: var(--color-primary);
  margin-right: 0.5rem;
}
```

---

## C

### `:checked`
Pseudo-clase que aplica estilos cuando un `<input type="checkbox">` o `<input type="radio">` está seleccionado. Fundamental para controles de formulario custom sin JavaScript.

```css
input[type="checkbox"]:checked + label::before {
  background-color: var(--color-primary);
}
```

### `content`
Propiedad CSS obligatoria para `::before` y `::after`. Sin ella el pseudo-elemento no se renderiza. Acepta: `""`, texto, `attr()`, `url()`, `counter()`, o combinaciones.

```css
.element::before {
  content: "";        /* Cadena vacía — necesaria aunque sin texto */
  display: block;
  width: 2px;
  height: 100%;
  background: red;
}
```

---

## E

### Especificidad
Valor numérico que determina qué regla CSS tiene prioridad cuando varias reglas se aplican al mismo elemento. Los pseudo-elementos y pseudo-clases tienen especificidad `(0, 1, 0)`. La pseudo-clase `:where()` tiene especificidad `(0, 0, 0)`.

---

## F

### `:first-child`
Pseudo-clase que selecciona un elemento solo si es el **primer hijo** de su padre.

```css
li:first-child { font-weight: bold; }
```

### `:first-of-type`
Pseudo-clase que selecciona el **primer elemento de su tipo** (etiqueta HTML) dentro de su padre, independientemente de otros tipos de hijos.

### `:focus-within`
Pseudo-clase que activa estilos en un elemento cuando **él mismo o cualquier descendiente** tiene el foco del teclado. Muy útil para resaltar formularios.

```css
.form-group:focus-within {
  border-color: var(--color-primary);
}
```

---

## H

### `:has()`
Pseudo-clase funcional (CSS Selectors Level 4) que selecciona un elemento si **contiene** un descendiente que coincide con el argumento. Funciona como "selector de padre". Soporte: Chrome 105+, Firefox 121+, Safari 15.4+.

```css
/* Selecciona .card si contiene un img */
.card:has(img) { padding-top: 0; }

/* Selecciona .form-group si tiene algún input:checked */
.form-group:has(input:checked) { border-color: green; }
```

---

## I

### `:invalid`
Pseudo-clase que aplica cuando un `<input>` no supera la validación HTML5 (required vacío, email mal formado, etc.).

### `:is()`
Pseudo-clase funcional que agrupa una lista de selectores. La especificidad resultante es la del selector **más específico** del grupo.

```css
/* Equivale a: h1, h2, h3, h4 */
:is(h1, h2, h3, h4) { line-height: 1.2; }
```

---

## L

### `:last-child`
Pseudo-clase que selecciona un elemento solo si es el **último hijo** de su padre.

```css
li:last-child { border-bottom: none; }
```

### `:last-of-type`
Selecciona el **último elemento de su tipo** dentro de su padre.

---

## M

### `::marker`
Pseudo-elemento que representa el **marcador** (bullet o número) de los elementos de lista `<li>`. Permite cambiar su color, tamaño y contenido sin JavaScript.

```css
li::marker {
  color: var(--color-primary);
  font-size: 1.2em;
}
```

---

## N

### `:not()`
Pseudo-clase que excluye elementos que coincidan con el argumento. Muy útil para evitar aplicar estilos al último elemento.

```css
li:not(:last-child) { border-bottom: 1px solid #ccc; }
img:not([alt])      { outline: 3px solid red; } /* Detecta imágenes sin alt */
```

### `:nth-child()`
Pseudo-clase que selecciona elementos según su **posición entre todos los hijos** del padre, usando la fórmula `An+B`. Palabras clave: `even` (pares), `odd` (impares).

```css
tr:nth-child(even) { background-color: #f5f5f5; }
li:nth-child(3n+1) { color: blue; }
```

### `:nth-last-child()`
Igual que `:nth-child()` pero contando **desde el final**.

```css
/* Los últimos 3 items */
li:nth-last-child(-n+3) { opacity: 0.5; }
```

### `:nth-of-type()`
Similar a `:nth-child()` pero selecciona por posición **entre elementos del mismo tipo** (misma etiqueta HTML). Útil en padres con hijos de tipos mixtos.

---

## P

### `::placeholder`
Pseudo-elemento para estilizar el texto de placeholder de los inputs.

```css
input::placeholder { color: #aaa; font-style: italic; }
```

### Pseudo-clase
Selector que aplica estilos basándose en el **estado** o **posición** de un elemento: `:hover`, `:focus`, `:nth-child()`, `:checked`, `:not()`, etc. Especificidad: `(0, 1, 0)`.

### Pseudo-elemento
Selector que crea o apunta a una **parte específica** de un elemento. Se escribe con `::` doble: `::before`, `::after`, `::marker`, `::selection`. Especificidad: `(0, 0, 1)`.

---

## S

### `::selection`
Pseudo-elemento que estiliza el texto cuando el usuario lo **selecciona** con el ratón.

```css
::selection {
  background-color: var(--color-primary);
  color: white;
}
```

### Selectores de atributo
Selectores que apuntan a elementos según el valor de sus atributos HTML.

| Selector | Descripción |
|----------|-------------|
| `[attr]` | Tiene el atributo (sin importar valor) |
| `[attr="val"]` | Valor exacto igual a `val` |
| `[attr^="val"]` | Valor empieza con `val` |
| `[attr$="val"]` | Valor termina con `val` |
| `[attr*="val"]` | Valor contiene `val` |
| `[attr~="val"]` | Valor es una lista separada por espacios que incluye `val` |

---

## V

### `:valid`
Pseudo-clase que aplica cuando un `<input>` supera la validación HTML5.

---

## W

### `:where()`
Pseudo-clase funcional equivalente a `:is()` pero con **especificidad siempre cero** `(0, 0, 0)`. Ideal para estilos base o resets que no deben bloquear sobreescrituras.

```css
/* No suma especificidad — fácil de sobreescribir */
:where(h1, h2, h3, h4) { font-family: var(--font-sans); }
```
