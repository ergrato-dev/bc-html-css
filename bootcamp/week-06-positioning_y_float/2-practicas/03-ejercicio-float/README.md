# Ejercicio 03 — Float y Clearfix

## 🎯 Objetivo

Practicar `float`, `clear`, clearfix y `display: flow-root` para envolver texto alrededor de imágenes.

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css`. Descomenta cada bloque siguiendo los pasos.

---

## Paso 1: Imagen flotando a la izquierda

`float: left` hace que el elemento salga parcialmente del flujo y el texto inline lo rodee.

```css
.float-image {
  float: left;
  margin-right: 1.5rem;
  margin-bottom: 1rem;
  width: 200px;
}
```

**Descomenta el bloque `/* PASO 1 */`** y observa cómo el texto rodea la imagen.

---

## Paso 2: El problema del contenedor colapsado

Sin clearfix, el contenedor no abraza el float y su altura colapsa a cero.

```css
/* Ver en DevTools: el .article-box tiene height: 0 */
```

**Descomenta el bloque `/* PASO 2 */`** para aplicar clearfix clásico.

---

## Paso 3: Clearfix clásico con `::after`

```css
.clearfix::after {
  content: "";
  display: block;
  clear: both;
}
```

**Descomenta el bloque `/* PASO 3 */`** para el clearfix con pseudoelemento.

---

## Paso 4: `display: flow-root` — solución moderna

La forma más limpia: crea un Block Formatting Context (BFC) automáticamente.

```css
.article-box {
  display: flow-root;
}
```

**Descomenta el Paso 4 y comenta el Paso 3** para comparar ambas soluciones.

---

## ✅ Verificación

- [ ] El texto fluye alrededor de la imagen flotante
- [ ] Sin clearfix el contenedor colapsa (verificar en DevTools)
- [ ] Con clearfix `::after` el contenedor abraza el float
- [ ] `display: flow-root` logra el mismo resultado de forma más limpia
