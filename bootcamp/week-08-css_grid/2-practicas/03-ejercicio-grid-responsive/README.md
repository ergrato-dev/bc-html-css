# Ejercicio 03 — Grid Responsive

Compara columnas fijas con `auto-fill` y `auto-fit`, y controla la altura de las filas con `grid-auto-rows`.

---

## Paso 1: Columnas fijas con `repeat(3, 1fr)`

Con columnas fijas, la grilla siempre tiene exactamente 3 columnas sin importar el ancho de la ventana:

```css
.grid-fixed {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}
```

**Abre `starter/css/styles.css`** y descomenta la sección del PASO 1. Redimensiona la ventana: los ítems se comprimen pero el número de columnas no cambia.

---

## Paso 2: `auto-fill` — reserva columnas vacías

`auto-fill` calcula cuántas columnas de al menos `200px` caben y **reserva el espacio** aunque no haya ítems:

```css
.grid-fill {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
  gap: 1rem;
}
```

**Descomenta la sección del PASO 2**. Con pocos ítems, las columnas vacías mantienen su espacio.

---

## Paso 3: `auto-fit` — colapsa columnas vacías

`auto-fit` hace lo mismo que `auto-fill` pero **colapsa** las columnas sin contenido, permitiendo que los ítems existentes crezcan:

```css
.grid-fit {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 1rem;
}
```

**Descomenta la sección del PASO 3**. Con 3 ítems en pantalla ancha, los 3 se expanden equitativamente.

---

## Paso 4: `grid-auto-rows` — filas de altura uniforme

Controla la altura mínima de todas las filas implícitas:

```css
.grid-rows-control {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  grid-auto-rows: minmax(160px, auto);
  gap: 1rem;
}
```

**Descomenta la sección del PASO 4**. Todos los ítems tendrán al menos `160px` de alto, pero se expandirán si el contenido es mayor.
