# Glosario — CSS Grid (Semana 08)

Términos clave de CSS Grid en orden alfabético.

---

## A

**auto-fill**
Valor de `repeat()` que genera tantas columnas (o filas) como quepan según el tamaño mínimo declarado. Mantiene las columnas vacías como espacio reservado si los ítems no las ocupan.
```css
grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
```

**auto-fit**
Similar a `auto-fill`, pero colapsa las columnas vacías y permite que los ítems existentes se expandan para llenar todo el espacio disponible.
```css
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
```

---

## C

**celda (cell)**
La intersección de una fila y una columna en el grid. Es la unidad mínima del grid. Un ítem ocupa al menos una celda.

**columna (grid column)**
Una pista (track) vertical del grid definida por `grid-template-columns`. Las columnas están numeradas de izquierda a derecha empezando en 1 (o de derecha a izquierda empezando en -1).

---

## D

**display: grid**
Propiedad que convierte un elemento en un contenedor grid. Sus hijos directos se convierten automáticamente en ítems del grid.
```css
.container { display: grid; }
```

---

## E

**explicit grid (grid explícito)**
Las filas y columnas definidas explícitamente con `grid-template-columns` y `grid-template-rows`. Los ítems que no caben en el grid explícito crean el grid implícito.

---

## F

**fr (fracción)**
Unidad de medida exclusiva de CSS Grid que representa una fracción del espacio disponible en el contenedor, calculada después de descontar tamaños fijos y gaps.
```css
/* 3 columnas: 25% / 50% / 25% del espacio libre */
grid-template-columns: 1fr 2fr 1fr;
```

---

## G

**gap**
Espacio entre filas y columnas del grid. Es la forma moderna de `grid-gap`. Se puede especificar como `gap: row-gap column-gap`.
```css
gap: 1rem;         /* igual en ambos ejes */
gap: 1rem 2rem;    /* fila / columna */
```

**grid area**
Una zona rectangular del grid formada por una o más celdas. Las áreas pueden nombrarse con `grid-template-areas` para posicionar ítems semánticamente.

**grid-area**
Propiedad que asigna un ítem a un área nombrada (con `grid-template-areas`) o define su posición con líneas de grid (`grid-row-start / grid-column-start / grid-row-end / grid-column-end`).
```css
.sidebar { grid-area: sidebar; }
```

**grid container**
El elemento padre con `display: grid`. Establece el contexto de formato grid para sus hijos directos.

**grid-template-areas**
Propiedad del contenedor que define las áreas del grid con un mapa visual en texto. Cada string representa una fila; cada palabra, una celda nombrada; `.` equivale a celda vacía.
```css
grid-template-areas:
  "header  header"
  "sidebar main"
  "footer  footer";
```

**grid-template-columns**
Define el número y tamaño de las columnas del grid. Acepta longitudes, porcentajes, `fr`, `auto`, `repeat()`, `minmax()`.
```css
grid-template-columns: 240px 1fr 1fr;
```

---

## I

**implicit grid (grid implícito)**
Las filas (o columnas) que CSS Grid crea automáticamente cuando los ítems desbordan el grid explícito. Su tamaño se controla con `grid-auto-rows` / `grid-auto-columns`.

**item (grid item)**
Cada hijo directo del contenedor grid. Se coloca automáticamente o manualmente con propiedades de línea o área.

---

## L

**línea (grid line)**
Las líneas verticales y horizontales que dividen el grid. Se numeran desde 1 hasta `n+1` (donde n es el número de tracks). `-1` siempre apunta a la última línea.

---

## M

**minmax()**
Función que fija un rango de tamaño para una pista: tamaño mínimo y máximo. Fundamental para diseños responsivos sin media queries.
```css
grid-auto-rows: minmax(120px, auto);
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
```

---

## R

**repeat()**
Función que simplifica la declaración de tracks repetidos.
```css
repeat(3, 1fr)             /* 3 columnas iguales */
repeat(auto-fit, 200px)    /* columnas responsivas */
```

**fila (grid row)**
Una pista (track) horizontal del grid definida por `grid-template-rows`. Las filas están numeradas de arriba a abajo empezando en 1.

---

## S

**span**
Palabra clave que indica cuántas celdas debe ocupar un ítem en la dirección indicada.
```css
.wide-card { grid-column: span 2; }       /* ocupa 2 columnas */
.tall-card { grid-row: span 3; }          /* ocupa 3 filas */
.full-row  { grid-column: 1 / -1; }       /* toda la anchura */
```

---

## T

**track**
Cada columna o fila del grid. Un track es el espacio entre dos líneas de grid consecutivas.
