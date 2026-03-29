# Semana 11: Transiciones, Transforms y Animaciones CSS

> **Duración:** 8 horas | **Nivel:** Intermedio-Avanzado  
> **Prerequisitos:** Box Model, Flexbox, CSS Custom Properties

Aprende a dar vida a tus interfaces con movimiento controlado: transiciones suaves en hover, transformaciones geométricas de elementos y animaciones completas con `@keyframes`.

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana serás capaz de:

1. Aplicar `transition` para cambios de estado fluidos
2. Usar `transform` en 2D: mover, rotar, escalar e inclinar elementos
3. Crear perspectiva 3D con `perspective` y `rotateX/Y`
4. Definir secuencias de animación con `@keyframes`
5. Controlar `animation` con sus 8 sub-propiedades
6. Usar `animation-fill-mode` para mantener el estado final
7. Respetar la accesibilidad con `prefers-reduced-motion`
8. Identificar cuándo usar transición vs animación

---

## 📋 Requisitos Previos

- CSS Custom Properties (`var()`, `:root`)
- Box Model y display
- Pseudo-clases (`:hover`, `:focus`)

---

## 🗂️ Estructura de la Semana

```
week-11-transiciones_transforms_y_animaciones/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
│   ├── 01-timing-functions.svg    # Curvas ease-in/out/in-out/linear
│   └── 02-transform-2d.svg        # Grid visual de funciones 2D
├── 1-teoria/
│   ├── 01-transitions.md          # transition shorthand y propiedades
│   ├── 02-transforms.md           # transform 2D y 3D + perspective
│   └── 03-keyframes-animation.md  # @keyframes y animation
├── 2-practicas/
│   ├── 01-ejercicio-hover/        # Transiciones en tarjetas y botones
│   ├── 02-ejercicio-transforms/   # Transform playground
│   └── 03-ejercicio-keyframes/    # Animaciones de entrada y spinner
├── 3-proyecto/
│   ├── README.md
│   ├── starter/
│   └── solution/
├── 4-recursos/
│   ├── ebooks-free/
│   ├── videografia/
│   └── webgrafia/
└── 5-glosario/
    └── README.md
```

---

## 📝 Contenidos

| # | Teoría | Tema |
|---|--------|------|
| 01 | [Transitions](1-teoria/01-transitions.md) | `transition` shorthand, propiedades, timing functions |
| 02 | [Transforms](1-teoria/02-transforms.md) | `transform` 2D/3D, `perspective`, orden de funciones |
| 03 | [Keyframes & Animation](1-teoria/03-keyframes-animation.md) | `@keyframes`, `animation` y sus 8 sub-propiedades |

| # | Práctica | Objetivo |
|---|----------|---------|
| 01 | [Hover Transitions](2-practicas/01-ejercicio-hover/) | Cards con lift + botones con color/shadow |
| 02 | [Transform Playground](2-practicas/02-ejercicio-transforms/) | Explorar translate/rotate/scale/skew en vivo |
| 03 | [Keyframe Animations](2-practicas/03-ejercicio-keyframes/) | fade-in, slide-up, spinner con @keyframes |

---

## ⏱️ Distribución del Tiempo (8 horas)

| Actividad | Tiempo |
|-----------|--------|
| 📖 Teoría (3 archivos) | 2h |
| 💻 Práctica 01 — Hover Transitions | 1.5h |
| 💻 Práctica 02 — Transform Playground | 1h |
| 💻 Práctica 03 — Keyframe Animations | 1h |
| 🚀 Proyecto — Animated Card | 2.5h |

---

## 📌 Entregables

- [ ] Ejercicio 01: tarjeta con hover lift y botones animados
- [ ] Ejercicio 02: playground con los 4 transforms 2D
- [ ] Ejercicio 03: tres animaciones de entrada + spinner
- [ ] Proyecto: Animated Portfolio Card completo

---

## 🎓 Conceptos Clave

| Concepto | Propiedad / Función |
|----------|-------------------|
| Transición suave | `transition: property duration easing delay` |
| Curvas de tiempo | `ease`, `ease-in`, `ease-out`, `ease-in-out`, `linear`, `cubic-bezier()` |
| Mover | `transform: translate(x, y)` |
| Rotar | `transform: rotate(deg)` |
| Escalar | `transform: scale(n)` |
| Inclinar | `transform: skewX(deg)` |
| Perspectiva 3D | `perspective: 600px` + `rotateY(deg)` |
| Secuencia | `@keyframes nombre { from {} to {} }` |
| Animar | `animation: nombre duración easing delay iteraciones dirección fill-mode play-state` |
| Accesibilidad | `@media (prefers-reduced-motion: reduce)` |

---

## ✅ Checklist de Verificación

- [ ] Las transiciones usan `var(--transition-base)` (no valores mágicos)
- [ ] `will-change: transform` solo en elementos que realmente animan
- [ ] `transform-origin` ajustado cuando el punto de pivote importa
- [ ] `animation-fill-mode: forwards` cuando se quiere mantener el estado final
- [ ] Todo el movimiento respeta `prefers-reduced-motion: reduce`
- [ ] No se animan propiedades que causan reflow (`width`, `height`, `top`, `left`)
- [ ] Se usan `transform` y `opacity` (propiedades que solo afectan el compositor)

---

## 🔗 Navegación

[← Semana 10: Tipografía, Colores y Variables](../week-10-tipografia_colores_y_variables/README.md) | [Semana 12: Selectores Avanzados →](../week-12-selectores_avanzados_y_pseudo_elementos/README.md)
