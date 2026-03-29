# Ejercicio 03 — Display y Overflow

## 🎯 Objetivo

Experimentar con `display: block`, `inline`, `inline-block`, `none` y `visibility: hidden`. Aplicar `overflow` para controlar el desbordamiento de contenido.

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css`. Descomenta cada bloque y observa el comportamiento en el navegador.

---

## Paso 1: block vs inline vs inline-block

```css
/* block: ocupa todo el ancho, genera salto de línea */
.tag-block {
  display: block;
  width: 180px;
}

/* inline: fluye en el texto, ignora width/height */
.tag-inline {
  display: inline;
}

/* inline-block: fluye en línea Y acepta width/height */
.tag-inline-block {
  display: inline-block;
  width: 120px;
  height: 40px;
}
```

**Descomenta el bloque `/* PASO 1 */`** y observa la diferencia visual entre los tres comportamientos.

---

## Paso 2: display none vs visibility hidden

```css
/* none: el elemento desaparece y no ocupa espacio */
.hidden-none {
  display: none;
}

/* hidden: el elemento es invisible pero sigue en el layout */
.hidden-visibility {
  visibility: hidden;
}
```

**Descomenta el bloque `/* PASO 2 */`** para activar la clase que oculta el elemento central. Observa la diferencia con cada método.

---

## Paso 3: overflow — controlar el desbordamiento

```css
/* Texto largo truncado con ellipsis */
.truncated {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  max-width: 250px;
}

/* Caja con scroll cuando el texto excede la altura */
.scrollable {
  height: 80px;
  overflow: auto;
}
```

**Descomenta el bloque `/* PASO 3 */`** y observa cómo el texto largo se corta en la primera caja y es scrolleable en la segunda.

---

## Paso 4: overflow hidden activa BFC

`overflow: hidden` en un contenedor crea un **Block Formatting Context**, lo que hace que contenga sus floats hijos (útil antes de Flexbox).

```css
.clearfix {
  overflow: hidden; /* contiene los floats internos */
}
```

**Descomenta el bloque `/* PASO 4 */`** y observa cómo el `overflow: hidden` hace que el contenedor rodee correctamente su contenido.

---

## ✅ Verificación

- [ ] Los tres badges (block/inline/inline-block) muestran comportamientos distintos
- [ ] `display: none` elimina el espacio del elemento
- [ ] `visibility: hidden` conserva el espacio del elemento
- [ ] El texto de `.truncated` muestra `...` cuando no cabe
- [ ] `.scrollable` tiene scroll interno sin desbordar
