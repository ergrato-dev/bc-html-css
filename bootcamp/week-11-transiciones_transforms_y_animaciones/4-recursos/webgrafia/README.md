# 📖 Webgrafía — Transiciones, Transforms y Animaciones CSS

> Recursos en línea seleccionados para profundizar en los temas de la semana.

---

## 🔀 Transiciones (`transition`)

| Recurso | Descripción |
|---------|-------------|
| [MDN — transition](https://developer.mozilla.org/es/docs/Web/CSS/transition) | Referencia completa: shorthand, sub-propiedades y valores |
| [MDN — transition-timing-function](https://developer.mozilla.org/es/docs/Web/CSS/transition-timing-function) | Funciones de easing: ease, cubic-bezier, steps |
| [MDN — Using CSS transitions](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_transitions/Using_CSS_transitions) | Guía oficial con ejemplos interactivos |
| [cubic-bezier.com](https://cubic-bezier.com/) | Herramienta visual para diseñar curvas cúbicas personalizadas |

---

## 🔄 Transforms 2D y 3D

| Recurso | Descripción |
|---------|-------------|
| [MDN — transform](https://developer.mozilla.org/es/docs/Web/CSS/transform) | Lista de todas las funciones: translate, rotate, scale, skew, perspective |
| [MDN — transform-origin](https://developer.mozilla.org/es/docs/Web/CSS/transform-origin) | Pivot point: valores de posición en 2D y 3D |
| [MDN — perspective](https://developer.mozilla.org/en-US/docs/Web/CSS/perspective) | Perspectiva en el padre para efectos 3D |
| [MDN — transform-style: preserve-3d](https://developer.mozilla.org/en-US/docs/Web/CSS/transform-style) | Conservar contexto 3D en elementos hijos |
| [CSS-Tricks — transform](https://css-tricks.com/almanac/properties/t/transform/) | Guía visual concisa con demos de cada función |

---

## 🎬 Animaciones (`@keyframes` + `animation`)

| Recurso | Descripción |
|---------|-------------|
| [MDN — @keyframes](https://developer.mozilla.org/es/docs/Web/CSS/@keyframes) | Sintaxis de `from/to` y porcentajes |
| [MDN — animation](https://developer.mozilla.org/es/docs/Web/CSS/animation) | Shorthand: todas las 8 sub-propiedades explicadas |
| [MDN — animation-fill-mode](https://developer.mozilla.org/es/docs/Web/CSS/animation-fill-mode) | `forwards`, `backwards`, `both`, `none` — casos de uso |
| [MDN — animation-play-state](https://developer.mozilla.org/es/docs/Web/CSS/animation-play-state) | `running` / `paused` para control desde JS |
| [web.dev — Learn CSS: Animations](https://web.dev/learn/css/animations) | Módulo completo con ejercicios interactivos |
| [web.dev — Learn CSS: Transitions](https://web.dev/learn/css/transitions) | Módulo de transiciones del curso Learn CSS |

---

## ♿ Accesibilidad: `prefers-reduced-motion`

| Recurso | Descripción |
|---------|-------------|
| [MDN — prefers-reduced-motion](https://developer.mozilla.org/es/docs/Web/CSS/@media/prefers-reduced-motion) | Media query de accesibilidad, sintaxis y detección |
| [web.dev — Prefers reduced motion](https://web.dev/articles/prefers-reduced-motion) | Best practices para animaciones accesibles con ejemplos |
| [WCAG 2.3.3 — Animation from Interactions](https://www.w3.org/WAI/WCAG21/Understanding/animation-from-interactions.html) | Requisito de accesibilidad WCAG 2.1 criterio 2.3.3 |

---

## 🛠 Herramientas

| Herramienta | Descripción |
|-------------|-------------|
| [Easing functions cheat sheet](https://easings.net/es) | Referencia visual de 30+ curvas de easing listas para copiar |
| [cubic-bezier.com](https://cubic-bezier.com/) | Editor interactivo de curvas `cubic-bezier()` |
| [Animista](https://animista.net/) | Generador de animaciones CSS listas para usar y personalizar |
| [Keyframes.app](https://keyframes.app/animate/) | Editor visual de @keyframes con exportación CSS |
| [Chrome DevTools — Animations panel](https://developer.chrome.com/docs/devtools/css/animations) | Depurar y ajustar animaciones en tiempo real en el navegador |

---

## 📐 Rendimiento

| Recurso | Descripción |
|---------|-------------|
| [web.dev — Rendering performance](https://web.dev/articles/rendering-performance) | Por qué `transform` y `opacity` son compositor-only |
| [CSS-Triggers (referencia)](https://csstriggers.com/) | Qué propiedades causan layout, paint o composite |

---

> 💡 **Tip:** Cuando experimentes con `cubic-bezier`, usa las DevTools del navegador (panel Animations) para ajustar la curva visualmente sobre la animación en vivo.
