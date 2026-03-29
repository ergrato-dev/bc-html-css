# Ejercicio 02 — Transform Playground

Explora las cuatro funciones de `transform` 2D en un entorno interactivo. Cada sección demuestra una función por separado.

---

## 🎯 Objetivos

- Observar el efecto visual de cada función transform
- Combinar transforms en el mismo elemento
- Usar `transform-origin` para cambiar el punto de pivote
- Comparar el mismo transform con distintos orígenes

---

## PASO 1 — translate: mover sin afectar el flujo

```css
/* El espacio original del elemento se mantiene */
.box-translate {
  transform: translate(20px, -10px);
  /* o por separado: */
  transform: translateX(20px);
  transform: translateY(-10px);
}
```

**Abre `starter/css/styles.css`** y descomenta la sección PASO 1. Observa que el espacio original queda vacío (el elemento se movió).

---

## PASO 2 — rotate: rotar sobre el eje Z

```css
.box-rotate { transform: rotate(15deg); }       /* sentido horario */
.box-rotate-neg { transform: rotate(-15deg); }  /* antihorario */
```

**Descomenta** PASO 2. Ajusta los grados en DevTools para ver distintos ángulos.

---

## PASO 3 — scale: escalar (sin reflow)

```css
.box-scale-up   { transform: scale(1.3); }   /* 30% más grande */
.box-scale-down { transform: scale(0.7); }   /* 30% más pequeño */
```

**Descomenta** PASO 3. Nota: escalar con `transform` no afecta el espacio del layout.

---

## PASO 4 — transform-origin + rotate combo

Misma rotación, distinto punto de pivote:

```css
.box-origin-tl { transform-origin: top left;   transform: rotate(20deg); }
.box-origin-br { transform-origin: bottom right; transform: rotate(20deg); }
.box-origin-center { transform-origin: center; transform: rotate(20deg); } /* default */
```

**Descomenta** PASO 4 y observa cómo el pivote cambia radicalmente el resultado visual.
