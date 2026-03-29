# Ejercicio 01 — Flex Container

Aprende a activar Flexbox en un contenedor y a controlar cómo se distribuyen y alinean los elementos en los dos ejes.

![Ejes de Flexbox](../../0-assets/01-flex-ejes.svg)

---

## 🎯 Objetivos

- Activar `display: flex` en un contenedor
- Controlar la dirección con `flex-direction`
- Distribuir espacio con `justify-content`
- Alinear elementos con `align-items`
- Gestionar el desbordamiento con `flex-wrap` y `gap`

---

## Paso 1: Activar display flex

Sin Flexbox, los elementos `<div>` son de bloque y se apilan verticalmente.  
Añadir `display: flex` los coloca en fila por defecto.

```css
.container {
  display: flex;
  /* Los hijos directos se convierten en flex items */
  /* Por defecto: flex-direction: row  (eje principal horizontal) */
}
```

**Abre `starter/css/styles.css`** y descomenta la sección **PASO 1**.

---

## Paso 2: Cambiar dirección con flex-direction

`flex-direction: column` cambia el eje principal a vertical.  
Importante: cuando la dirección es columna, `justify-content` actúa en vertical y `align-items` en horizontal.

```css
.container-column {
  display: flex;
  flex-direction: column;
}
```

**Descomenta** la sección **PASO 2** en `starter/css/styles.css`.

---

## Paso 3: Distribuir espacio con justify-content

```css
/* flex-start: todos al inicio (por defecto) */
.jc-start   { justify-content: flex-start; }

/* center: todos al centro */
.jc-center  { justify-content: center; }

/* space-between: espacio entre elementos, sin espacio en bordes */
.jc-between { justify-content: space-between; }

/* space-around: espacio alrededor de cada elemento */
.jc-around  { justify-content: space-around; }

/* space-evenly: espacio idéntico entre todos (incluidos bordes) */
.jc-evenly  { justify-content: space-evenly; }
```

**Descomenta** la sección **PASO 3** en `starter/css/styles.css`.

---

## Paso 4: Alinear en el eje cruzado y permitir salto de línea

```css
.container-wrap {
  display: flex;
  flex-wrap: wrap;        /* permite saltar a la línea siguiente */
  gap: 1rem;              /* espacio entre filas y columnas */
  align-items: center;    /* centra verticalmente en cada línea */
}
```

**Descomenta** la sección **PASO 4** en `starter/css/styles.css`.

---

## ✅ Verificación

- [ ] Los items se colocan en fila al activar `display: flex`
- [ ] `flex-direction: column` los apila verticalmente
- [ ] `justify-content` cambia la distribución horizontal
- [ ] `flex-wrap: wrap` hace que los items salten de línea
- [ ] `gap` añade espacio consistente entre los items
