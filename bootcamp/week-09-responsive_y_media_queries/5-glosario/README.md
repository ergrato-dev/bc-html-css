# Glosario — Semana 09: Responsive & Media Queries

Términos clave ordenados alfabéticamente.

---

## A

### `auto-fit`

Valor de `repeat()` en CSS Grid que crea las columnas necesarias para llenar el contenedor y colapsa las columnas vacías. Útil para grids *truly responsive* sin media queries.

```css
grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
```

---

## B

### Breakpoint

Valor de ancho de viewport en el que el diseño cambia mediante una Media Query. Los breakpoints más comunes en este bootcamp son `480px`, `768px` y `1024px`.

---

## C

### `clamp()`

Función CSS que retorna un valor entre un mínimo y un máximo, escalando de forma fluida con un valor preferido (generalmente en `vw`).

```css
/* mínimo: 1.75rem — preferido: 5vw — máximo: 3.5rem */
font-size: clamp(1.75rem, 5vw, 3.5rem);
```

### Container

Patrón CSS para centrar y limitar el ancho del contenido:

```css
.container {
  width: 90%;
  max-width: 1200px;
  margin: 0 auto;
  padding: 0 1rem;
}
```

---

## D

### Desktop-first

Estrategia de desarrollo que empieza por la versión de escritorio y usa `@media (max-width)` para adaptar a pantallas más pequeñas. **No recomendada** — genera CSS más complejo.

### `dvh` (Dynamic Viewport Height)

Unidad moderna que representa la altura del viewport *real* del navegador, incluyendo aparecer/desaparecer de la barra de dirección en móviles. Alternativa más robusta a `vh` en contextos móviles.

---

## E

### `em`

Unidad relativa al `font-size` del elemento padre. Se acumula en elementos anidados.

```css
.btn {
  padding: 0.65em 1.3em; /* escala con el font-size del botón */
}
```

---

## F

### Fluid Typography

Técnica donde el tamaño del texto escala automáticamente entre dos valores según el ancho del viewport, usando `clamp()` o funciones `calc()` con `vw`.

---

## M

### `@media`

Regla CSS que aplica un bloque de estilos solo cuando se cumple una condición de media. En este bootcamp se usan `@media (min-width: Xpx)` (Mobile-first).

```css
@media (min-width: 768px) {
  .grid { grid-template-columns: repeat(2, 1fr); }
}
```

### `min-width`

Feature de media query que se cumple cuando el viewport es igual o mayor al valor especificado. Base del enfoque Mobile-first.

### Mobile-first

Estrategia de desarrollo CSS donde los estilos base se escriben para pantallas pequeñas (320px) y se expanden progresivamente con `@media (min-width)`. Genera código más limpio y performático.

---

## O

### Overflow (horizontal)

Problema común en responsive cuando un elemento excede el ancho del viewport. Se previene con `max-width: 100%` en imágenes y `min-width: 0` en elementos de grid/flex.

---

## P

### `prefers-color-scheme`

Media query de preferencia del sistema. Detecta si el usuario tiene configurado el modo oscuro:

```css
@media (prefers-color-scheme: dark) { /* overrides de variables */ }
```

### `prefers-reduced-motion`

Media query de accesibilidad que detecta si el usuario ha solicitado reducir movimiento en su sistema operativo:

```css
@media (prefers-reduced-motion: reduce) {
  * { transition: none !important; animation: none !important; }
}
```

---

## R

### `rem`

Unidad CSS relativa al `font-size` del elemento raíz (`html`). Si `html { font-size: 100%; }`, entonces `1rem = 16px`. No se acumula como `em`.

### Responsive Design

Enfoque de diseño web en que el layout y la tipografía se adaptan fluidamente a cualquier tamaño de viewport mediante Media Queries, unidades relativas y layouts flexibles (Flex, Grid).

---

## V

### Viewport

El área visible de la ventana del navegador. Su tamaño varía según el dispositivo y el zoom del usuario.

### `<meta viewport>`

Etiqueta HTML obligatoria para activar el comportamiento responsive en dispositivos móviles:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

Sin ella, el navegador móvil simula un viewport de escritorio y el diseño responsive no funciona.

### `vw` / `vh`

Unidades del viewport: `1vw` = 1% del ancho del viewport; `1vh` = 1% de la altura. Útiles para secciones hero (100vh) y tipografía fluida.

---

## %

### Porcentaje (`%`)

Unidad relativa al elemento padre. Comúnmente usada para anchos fluidos de contenedores:

```css
.container { width: 90%; } /* 90% del ancho del padre */
```
