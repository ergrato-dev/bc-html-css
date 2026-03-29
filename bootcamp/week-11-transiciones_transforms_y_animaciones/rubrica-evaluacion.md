# Rúbrica de Evaluación — Semana 11
## Transiciones, Transforms y Animaciones CSS

---

## 🧠 Conocimiento (30 pts)

Cuestionario teórico al final de la semana.

| # | Pregunta | Pts |
|---|----------|-----|
| 1 | ¿Cuál es la diferencia entre `transition` y `animation`? Menciona al menos 2 diferencias. | 6 |
| 2 | Explica qué hace cada valor de `animation-fill-mode`: `none`, `forwards`, `backwards`, `both`. | 6 |
| 3 | ¿Por qué se recomienda animar `transform` y `opacity` en vez de `top`/`left` o `width`? | 6 |
| 4 | Escribe un `@keyframes` llamado `fade-in` que vaya de opacidad 0 a 1. | 6 |
| 5 | ¿Qué hace `prefers-reduced-motion: reduce` y por qué es importante? | 6 |

---

## 💪 Desempeño (40 pts)

Evaluación de los tres ejercicios prácticos.

### Ejercicio 01 — Hover Transitions (14 pts)

| Criterio | Pts |
|----------|-----|
| Transición suave en tarjeta (shadow + translateY) | 4 |
| Variable `--transition-base` en `:root` | 3 |
| Botón con cambio de color y escala en hover | 4 |
| No usa `transition: all` (especifica propiedades) | 3 |

### Ejercicio 02 — Transform Playground (12 pts)

| Criterio | Pts |
|----------|-----|
| Demuestra `translate()` con eje X e Y | 3 |
| Demuestra `rotate()` y `scale()` | 3 |
| Demuestra `skewX()` o `skewY()` | 3 |
| Aplica `transform-origin` en al menos un caso | 3 |

### Ejercicio 03 — Keyframe Animations (14 pts)

| Criterio | Pts |
|----------|-----|
| Animación `fade-in` con `@keyframes` | 4 |
| Animación `slide-up` (translateY + opacity) | 4 |
| Spinner con `rotate` y `animation: infinite` | 4 |
| Usa `animation-fill-mode: forwards` correctamente | 2 |

---

## 📦 Producto (30 pts)

Proyecto: **Animated Portfolio Card**

| Criterio | Pts |
|----------|-----|
| Animación de entrada (`@keyframes`) con `fill-mode: forwards` | 8 |
| Hover con `transform` + `transition` suave | 7 |
| Spinner o loader animado con `@keyframes infinite` | 5 |
| Variables CSS para duración/easing (`--duration-base`, `--ease-out`) | 5 |
| `prefers-reduced-motion` desactiva/reduce animaciones | 5 |

---

## 📊 Calificación Final

| Sección | Pts | % |
|---------|-----|---|
| Conocimiento | /30 | 30% |
| Desempeño | /40 | 40% |
| Producto | /30 | 30% |
| **Total** | **/100** | **100%** |

**Mínimo para aprobar:** 70 puntos totales, mínimo 21/30 en Producto.
