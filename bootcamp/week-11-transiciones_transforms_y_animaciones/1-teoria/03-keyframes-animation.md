# @keyframes y Animation

## 🎯 Objetivos

- Definir secuencias de animación con `@keyframes`
- Dominar el shorthand `animation` y sus 8 sub-propiedades
- Entender `animation-fill-mode` y `animation-iteration-count`
- Saber cuándo usar animación vs transición

---

## 1. Diferencia: Transition vs Animation

| | `transition` | `animation` |
|--|-------------|------------|
| **Disparador** | Necesita cambio de estado (`:hover`, clase JS) | Se ejecuta sola al cargar |
| **Complejidad** | Un estado → otro estado | Múltiples fotogramas clave |
| **Control** | Limitado (inicio y fin) | Total (velocidad, pausa, vuelta atrás, infinito) |
| **Uso típico** | Hover, focus, toggle | Loaders, entradas, llamadas de atención |

---

## 2. `@keyframes`

Define la secuencia de fotogramas de la animación.

```css
/* Forma sencilla: from / to */
@keyframes fade-in {
  from { opacity: 0; }
  to   { opacity: 1; }
}

/* Forma precisa: porcentajes */
@keyframes slide-up {
  0%   { opacity: 0; transform: translateY(20px); }
  100% { opacity: 1; transform: translateY(0); }
}

/* Múltiples paradas */
@keyframes pulse {
  0%, 100% { transform: scale(1); }
  50%       { transform: scale(1.05); }
}

/* Spinner */
@keyframes spin {
  from { transform: rotate(0deg); }
  to   { transform: rotate(360deg); }
}
```

---

## 3. El Shorthand `animation`

```
animation: nombre duración easing retraso iteraciones dirección fill-mode play-state
```

```css
.elemento {
  animation: fade-in 400ms ease-out 0ms 1 normal forwards running;
}

/* Forma abreviada (omitiendo valores por defecto comunes) */
.elemento {
  animation: fade-in 400ms ease-out forwards;
}
```

---

## 4. Las 8 Sub-propiedades

### `animation-name`
Nombre del `@keyframes` a usar.

### `animation-duration`
Cuánto dura un ciclo. Debe ser siempre mayor que `0s`.

### `animation-timing-function`
Curva de velocidad (igual que en transitions: `ease`, `ease-out`, `linear`…).

### `animation-delay`
Tiempo que espera antes de comenzar. Acepta valores negativos (comienza en medio).

```css
/* Comienza como si ya hubieran pasado 200ms */
animation-delay: -200ms;
```

### `animation-iteration-count`
Número de repeticiones. `infinite` = sin fin.

```css
animation-iteration-count: 1;        /* una vez */
animation-iteration-count: 3;        /* tres veces */
animation-iteration-count: infinite; /* loop infinito */
```

### `animation-direction`

| Valor | Comportamiento |
|-------|---------------|
| `normal` | Siempre de 0% a 100% (por defecto) |
| `reverse` | Siempre de 100% a 0% |
| `alternate` | 0→100 luego 100→0 luego 0→100... |
| `alternate-reverse` | Inverso del anterior |

### `animation-fill-mode`

| Valor | Comportamiento |
|-------|---------------|
| `none` | Sin efecto fuera de la animación (por defecto) |
| `forwards` | Mantiene el estado del **último** fotograma |
| `backwards` | Aplica el estado del **primer** fotograma durante el delay |
| `both` | Combina forwards y backwards |

```css
/* Al terminar, el elemento se queda en el estado final */
animation: slide-up 400ms ease-out forwards;
```

### `animation-play-state`
`running` (por defecto) | `paused`. Útil para pausar con JavaScript.

---

## 5. Animaciones Escalonadas con `animation-delay`

```css
/* Entrada escalonada de tarjetas */
.card:nth-child(1) { animation: slide-up 400ms ease-out forwards; }
.card:nth-child(2) { animation: slide-up 400ms ease-out 100ms forwards; }
.card:nth-child(3) { animation: slide-up 400ms ease-out 200ms forwards; }

/* Con Custom Properties para mantener la consistencia */
.card {
  opacity: 0; /* estado inicial antes de la animación */
  animation: slide-up 400ms ease-out forwards;
  animation-delay: calc(var(--card-index, 0) * 100ms);
}
```

---

## 6. Tokens para Animaciones

```css
:root {
  --duration-fast:    150ms;
  --duration-base:    300ms;
  --duration-slow:    600ms;
  --duration-xslow:  1200ms;

  --ease-out:         ease-out;
  --ease-in-out:      ease-in-out;

  --anim-fade-in:     fade-in  var(--duration-base) var(--ease-out) forwards;
  --anim-slide-up:    slide-up var(--duration-base) var(--ease-out) forwards;
  --anim-spin:        spin     var(--duration-slow)  linear         infinite;
}
```

---

## 7. Accesibilidad

```css
/* Elimina animaciones cuando el usuario lo prefiere */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration:        0.01ms !important;
    animation-iteration-count: 1      !important;
    transition-duration:       0.01ms !important;
    scroll-behavior:           auto   !important;
  }
}
```

---

## ✅ Checklist

- [ ] `@keyframes` con nombre descriptivo en kebab-case
- [ ] `animation-fill-mode: forwards` cuando se quiere mantener el estado final
- [ ] `opacity: 0` en el elemento antes de la animación de entrada
- [ ] Animaciones infinitas solo en elementos funcionales (spinners, loaders)
- [ ] `prefers-reduced-motion: reduce` implementado

---

## 📚 Recursos

- [MDN — @keyframes](https://developer.mozilla.org/es/docs/Web/CSS/@keyframes)
- [MDN — animation](https://developer.mozilla.org/es/docs/Web/CSS/animation)
- [MDN — animation-fill-mode](https://developer.mozilla.org/es/docs/Web/CSS/animation-fill-mode)
- [Animate.css](https://animate.style/) — biblioteca de referencia de animaciones
- [web.dev — CSS animations](https://web.dev/learn/css/animations)
