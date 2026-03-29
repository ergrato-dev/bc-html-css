# Margin y Padding

## 🎯 Objetivos

- Usar la notación shorthand de margin y padding
- Centrar bloques con `margin: 0 auto`
- Entender y anticipar el colapso de márgenes verticales
- Usar margin negativo para efectos de superposición

---

## 1. Sintaxis shorthand

Tanto `margin` como `padding` aceptan 1, 2, 3 o 4 valores:

```css
/* 1 valor → igual en los 4 lados */
margin: 1rem;

/* 2 valores → top/bottom  left/right */
margin: 1rem 2rem;

/* 3 valores → top  left/right  bottom */
margin: 1rem 2rem 0.5rem;

/* 4 valores → top  right  bottom  left  (sentido horario) */
margin: 1rem 2rem 0.5rem 0;

/* Propiedades individuales (más explícito) */
margin-top: 2rem;
margin-right: 1rem;
margin-bottom: 2rem;
margin-left: 1rem;
```

El mismo principio aplica para `padding`.

---

## 2. Centrado horizontal con `margin: auto`

Un elemento de bloque con `width` definido se puede centrar horizontalmente:

```css
/* ✅ Centrar un contenedor */
.container {
  width: 900px;
  max-width: 100%;    /* nunca más ancho que la pantalla */
  margin: 0 auto;     /* auto distribuye el espacio sobrante entre izq y der */
}
```

> **Importante:** `margin: auto` solo centra horizontalmente en elementos `block` con `width` definido. No funciona para centrar verticalmente (para eso usa Flexbox o Grid).

---

## 3. Colapso de márgenes (Margin Collapse)

Cuando dos márgenes **verticales** de elementos adyacentes se encuentran, **no se suman — se colapsan** en el mayor de los dos.

```html
<!-- Estos dos párrafos tienen margin-bottom/top de 1rem cada uno -->
<!-- El espacio entre ellos será 1rem, NO 2rem -->
<p style="margin-bottom: 1rem;">Párrafo 1</p>
<p style="margin-top: 1rem;">Párrafo 2</p>
```

### Reglas del colapso

```css
/* Caso 1: Hermanos adyacentes — gana el mayor */
.a { margin-bottom: 2rem; }
.b { margin-top: 1rem; }
/* Espacio resultante = 2rem (no 3rem) */

/* Caso 2: Padre e hijo — si el padre no tiene padding ni border */
.parent { margin-top: 2rem; }
.child  { margin-top: 3rem; }
/* El hijo "escapa" y el padre toma margin-top: 3rem */

/* ✅ Solución: añadir padding o border al padre */
.parent {
  padding-top: 1px;  /* evita el colapso */
}
```

### Cuándo NO ocurre el colapso

- Elementos con `display: flex` o `display: grid` (hijos no colapsan)
- Elementos con `overflow: hidden` o `overflow: auto`
- Elementos con `float` o `position: absolute/fixed`
- Márgenes horizontales (nunca colapsan)

---

## 4. Margin negativo

El margen negativo acerca los elementos, incluso solapándolos:

```css
/* Pull de una imagen hacia afuera del contenedor */
.pull-left {
  margin-left: -2rem;
}

/* Efecto de overlap entre secciones */
.hero + .section {
  margin-top: -4rem;
  position: relative; /* necesario para z-index */
  z-index: 1;
}
```

---

## 5. Espaciado con gap vs margin

En Flexbox y Grid, usa `gap` en el **contenedor** en vez de `margin` en cada hijo:

```css
/* ✅ BIEN — gap en el contenedor */
.cards {
  display: flex;
  gap: 1.5rem;
}

/* ❌ EVITAR — margin en cada hijo genera problemas */
.card {
  margin-right: 1.5rem; /* exceso en el último elemento */
}
```

---

## ✅ Checklist de verificación

- [ ] Uso shorthand de 4 valores en sentido horario
- [ ] Sé centrar un bloque con `max-width` + `margin: 0 auto`
- [ ] Puedo predecir qué espacio habrá entre dos elementos adyacentes
- [ ] Sé cómo prevenir el colapso de márgenes padre-hijo

## 📚 Recursos

- [MDN — margin](https://developer.mozilla.org/es/docs/Web/CSS/margin)
- [MDN — Mastering margin collapsing](https://developer.mozilla.org/es/docs/Web/CSS/CSS_box_model/Mastering_margin_collapsing)
