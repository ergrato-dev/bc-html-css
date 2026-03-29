# Glosario — Semana 04: CSS Fundamentos y Selectores

Términos técnicos clave de esta semana en orden alfabético.

---

## A

**Atributo selector** (`[attr]`)
Selector que apunta a elementos según la presencia o valor de un atributo HTML. Ejemplo: `a[href^="https"]` selecciona todos los enlaces que empiezan con `https`.

---

## B

**Block (display)**
Modo de visualización de un elemento que ocupa todo el ancho disponible y genera un salto de línea antes y después. `<div>`, `<p>`, `<h1>` son block por defecto.

---

## C

**Cascada (Cascade)**
Algoritmo de CSS que determina qué regla se aplica cuando hay múltiples reglas que afectan al mismo elemento. Considera origen, especificidad y orden de aparición.

**Combinador (Combinator)**
Símbolo entre selectores que define una relación de parentesco. Los 4 combinadores son: descendiente (espacio), hijo directo (`>`), hermano adyacente (`+`) y hermano general (`~`).

---

## D

**Declaración (Declaration)**
Par de `propiedad: valor` dentro de una regla CSS. Ejemplo: `color: red` es una declaración.

---

## E

**Especificidad (Specificity)**
Puntaje `(A, B, C)` que el navegador asigna a cada selector para decidir cuál prevalece. A = IDs, B = clases/atributos/pseudo-clases, C = elementos/pseudo-elementos.

---

## H

**Herencia (Inheritance)**
Mecanismo por el cual ciertos valores CSS del elemento padre fluyen automáticamente hacia sus hijos. Las propiedades tipográficas (`color`, `font-*`, `line-height`) heredan; las de caja (`margin`, `padding`, `border`) no.

---

## I

**`inherit`**
Palabra clave CSS que fuerza a una propiedad a tomar el valor de su elemento padre, aunque normalmente no herede.

**`initial`**
Palabra clave CSS que devuelve una propiedad a su valor inicial tal como lo define la especificación CSS.

---

## P

**Propiedad (Property)**
La característica visual que se quiere modificar. Ejemplos: `color`, `font-size`, `margin`, `display`.

**Pseudo-clase**
Selector que apunta a un estado especial de un elemento. Ejemplos: `:hover`, `:focus`, `:focus-visible`, `:active`, `:visited`, `:nth-child()`.

**Pseudo-elemento**
Permite estilizar una parte específica de un elemento o insertar contenido decorativo. Ejemplos: `::before`, `::after`, `::first-line`, `::placeholder`.

---

## R

**Reset CSS**
Conjunto de reglas CSS que eliminan o normalizan los estilos por defecto del navegador, garantizando una base consistente en todos los navegadores.

**Regla CSS (CSS Rule)**
Bloque de código CSS compuesto por un **selector** y un **bloque de declaraciones** encerrado en `{}`.

---

## S

**Selector**
Patrón que identifica qué elemento(s) HTML serán afectados por las declaraciones CSS. Existen selectores de tipo, clase, ID, atributo, combinadores, pseudo-clases y pseudo-elementos.

**Selector de clase (`.clase`)**
Selecciona todos los elementos que tienen ese valor en su atributo `class`. Puede reutilizarse en múltiples elementos. Especificidad `(0,1,0)`.

**Selector de ID (`#id`)**
Selecciona el único elemento con ese `id` en la página. Especificidad `(1,0,0)`. Usar con moderación; preferir clases.

**Selector de tipo**
Selecciona todos los elementos de ese nombre de etiqueta. Ejemplo: `p`, `h1`, `a`. Especificidad `(0,0,1)`.

**Selector universal (`*`)**
Selecciona todos los elementos del DOM. Especificidad `(0,0,0)`.

---

## U

**`unset`**
Palabra clave CSS que se comporta como `inherit` si la propiedad hereda, o como `initial` si no hereda.

---

## V

**Valor (Value)**
El dato asignado a una propiedad en una declaración CSS. Puede ser una palabra clave (`red`, `auto`), un número con unidad (`1.5rem`, `50%`) o una función (`rgb()`, `calc()`).

---

## :

**`:focus-visible`**
Pseudo-clase que aplica estilos de enfoque solo cuando el elemento fue enfocado mediante teclado o navegación no táctil. Recomendada sobre `:focus` por razones de experiencia de usuario.

**`:nth-child(n)`**
Pseudo-clase que selecciona un elemento dependiendo de su posición entre sus hermanos. Acepta fórmulas: `odd`, `even`, `2n+1`, `3n`, etc.

**`!important`**
Modificador de una declaración CSS que la eleva por encima de cualquier otra regla en la cascada. Debe evitarse salvo en casos muy específicos (utility classes, sobrescritura de estilos de terceros).
