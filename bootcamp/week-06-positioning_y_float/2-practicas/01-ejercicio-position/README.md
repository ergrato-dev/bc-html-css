# Ejercicio 01 — Position: Tarjetas, Header Sticky y Modal

## 🎯 Objetivo

Practicar `position: relative`, `absolute`, `fixed` y `sticky` en contextos reales de UI.

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css`. Descomenta cada bloque de estilos siguiendo los pasos del README.

---

## Paso 1: Badge sobre imagen con `absolute`

Para posicionar un elemento **encima** de otro, el padre debe ser el *containing block* (`position: relative`) y el hijo usa `position: absolute`.

```css
/* Ejemplo: badge posicionado en la esquina superior izquierda */
.card-wrapper {
  position: relative; /* ← containing block */
}

.badge {
  position: absolute;
  top: 0.75rem;
  left: 0.75rem;
}
```

**Abre `starter/css/styles.css`** y descomenta el bloque `/* PASO 1 */`.

---

## Paso 2: Header sticky

Con `position: sticky` el header sigue el flujo normal hasta que el usuario hace scroll — entonces se "pega" al tope del viewport.

```css
.site-header {
  position: sticky;
  top: 0;
  z-index: 100;
}
```

**Descomenta el bloque `/* PASO 2 */`** en `styles.css`.

---

## Paso 3: Overlay oscuro con `fixed`

Un overlay de fondo usa `position: fixed` para cubrir todo el viewport independientemente del scroll.

```css
.modal-overlay {
  position: fixed;
  inset: 0; /* top:0; right:0; bottom:0; left:0 */
  background-color: rgba(0, 0, 0, 0.7);
  z-index: 200;
}
```

**Descomenta el bloque `/* PASO 3 */`** en `styles.css`.

---

## Paso 4: Dialog centrado sobre el overlay

El dialog modal se centra usando `position: fixed` con `transform: translate(-50%, -50%)`:

```css
.modal-dialog {
  position: fixed;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  z-index: 300;
}
```

**Descomenta el bloque `/* PASO 4 */`** en `styles.css`.

---

## ✅ Verificación

- [ ] El badge aparece en la esquina superior izquierda de la imagen
- [ ] El header permanece visible al hacer scroll
- [ ] El overlay oscurece toda la página
- [ ] El dialog aparece centrado sobre el overlay
