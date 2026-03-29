# Ejercicio 01 — El Box Model

## 🎯 Objetivo

Visualizar y modificar las 4 capas del Box Model: content, padding, border y margin. Comparar `content-box` vs `border-box`.

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css`. Descomenta cada bloque y observa cómo cambia el tamaño de los elementos en el navegador.

---

## Paso 1: Observar el Box Model por defecto

Sin estilos, los elementos tienen el comportamiento por defecto del navegador. Abre DevTools (`F12`) → panel **Elements** → selecciona un elemento → panel **Computed** → desplázate hacia abajo para ver el diagrama del Box Model.

**Descomenta el bloque `/* PASO 1 */`** para aplicar un reset base.

---

## Paso 2: content-box vs border-box

Con `content-box` (defecto), el padding **agrega espacio** al ancho declarado. Con `border-box` el ancho declarado incluye el padding.

```css
/* content-box: el div mide 200 + 40 + 4 = 244px en pantalla */
.box-content {
  box-sizing: content-box;
  width: 200px;
  padding: 20px;
  border: 2px solid #264de4;
}

/* border-box: el div mide exactamente 200px en pantalla */
.box-border {
  box-sizing: border-box;
  width: 200px;
  padding: 20px;
  border: 2px solid #3fb950;
}
```

**Descomenta el bloque `/* PASO 2 */`** y mide los dos elementos con DevTools.

---

## Paso 3: Margin y padding shorthand

```css
/* 1 valor: igual en todos los lados */
.card { margin: 1rem; }

/* 2 valores: vertical | horizontal */
.card { padding: 1rem 2rem; }

/* 4 valores: top | right | bottom | left */
.card { padding: 1rem 2rem 1.5rem 2rem; }
```

**Descomenta el bloque `/* PASO 3 */`** para aplicar espaciado shorthand a las tarjetas.

---

## Paso 4: Centra con margin auto

Un elemento block con `width` definido se centra horizontalmente con `margin: 0 auto`.

```css
.centered {
  width: 400px;
  max-width: 100%;
  margin: 0 auto;
}
```

**Descomenta el bloque `/* PASO 4 */`** y observa cómo el contenedor se centra.

---

## ✅ Verificación

- [ ] En DevTools: puedes ver las 4 capas en el diagrama Computed
- [ ] `.box-content` mide más de 200px (244px si padding=20px, border=2px)
- [ ] `.box-border` mide exactamente 200px
- [ ] El contenedor `.centered` aparece centrado en la página
