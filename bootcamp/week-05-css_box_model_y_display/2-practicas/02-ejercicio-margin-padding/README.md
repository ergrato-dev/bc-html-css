# Ejercicio 02 — Margin y Padding Avanzados

## 🎯 Objetivo

Practicar el shorthand de 4 valores, centrado con `margin: auto`, colapso de márgenes y margin negativo.

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css`. Descomenta cada bloque y observa los efectos en el layout.

---

## Paso 1: El colapso de márgenes en acción

Cuando dos elementos block adyacentes tienen `margin-bottom` y `margin-top`, el espacio entre ellos es el **mayor** de los dos, no la suma.

```css
/* Ambas secciones tienen margin 2rem, el espacio entre ellas será 2rem, no 4rem */
.section-a { margin-bottom: 2rem; }
.section-b { margin-top: 2rem; }
```

**Descomenta el bloque `/* PASO 1 */`** y mide el espacio en DevTools → Box Model.

**Para evitar el colapso** (cuando lo necesitas), usa `overflow: hidden` o `padding` en el padre.

---

## Paso 2: Colapso padre-hijo

Si un padre no tiene `padding-top` ni `border-top`, el `margin-top` del primer hijo se "escapa" al padre.

```css
/* ❌ El margin del hijo escapa al padre */
.parent { background-color: #161b22; }
.child  { margin-top: 3rem; }

/* ✅ Solución: padding en el padre */
.parent { padding-top: 0.1px; }
```

**Descomenta el bloque `/* PASO 2 */`** para ver el efecto y la solución.

---

## Paso 3: Margin negativo para superposición

El margin negativo acerca o superpone elementos. Es útil para efectos de diseño como imágenes que sobresalen.

```css
/* La imagen sobresale 2rem hacia arriba */
.featured-image {
  margin-top: -2rem;
  position: relative;
  z-index: 1;
}
```

**Descomenta el bloque `/* PASO 3 */`**.

---

## Paso 4: max-width + margin auto — layout de contenido

El patrón más usado para layout de página:

```css
.page-content {
  max-width: 720px;
  margin: 0 auto;
  padding: 0 1rem; /* padding lateral para móvil */
}
```

**Descomenta el bloque `/* PASO 4 */`** y ajusta el ancho del navegador para ver cómo el contenido responde.

---

## ✅ Verificación

- [ ] Puedo explicar por qué el espacio entre `.section-a` y `.section-b` es 2rem y no 4rem
- [ ] Veo el efecto del colapso padre-hijo antes y después del fix
- [ ] El elemento con margin negativo se superpone al elemento anterior
- [ ] El contenedor `.page-content` está centrado y nunca supera 720px
