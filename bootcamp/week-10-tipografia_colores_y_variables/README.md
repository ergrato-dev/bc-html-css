# Semana 10 — Tipografía, Colores y Variables CSS

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, serás capaz de:

- ✅ Cargar fuentes web con `@font-face` y Google Fonts (`font-display: swap`)
- ✅ Construir un sistema de escala tipográfica basado en una razón modular (1.25)
- ✅ Entender el modelo de color HSL y crear paletas coherentes
- ✅ Aplicar gradientes CSS (`linear-gradient`, `radial-gradient`, `conic-gradient`)
- ✅ Declarar y usar CSS Custom Properties (variables CSS) con `:root` y fallbacks
- ✅ Calcular valores dinámicos con `calc()`
- ✅ Construir un sistema de Design Tokens documentado como proyecto final

---

## 📚 Requisitos Previos

- Semana 04: selectores CSS y especificidad
- Semana 05: Box Model y display
- Semana 09: CSS Custom Properties (introducidas en contexto responsive)

---

## 🗂️ Estructura de la Semana

```
week-10-tipografia_colores_y_variables/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
│   ├── 01-type-scale.svg       # Escala tipográfica modular 1.25
│   └── 02-color-hsl.svg        # Modelo HSL + paleta de variables
├── 1-teoria/
│   ├── 01-tipografia-web.md    # @font-face, Google Fonts, font-display
│   ├── 02-colores-gradientes.md # HSL, oklch, gradientes
│   └── 03-custom-properties.md # CSS Variables, :root, fallbacks, calc()
├── 2-practicas/
│   ├── 01-ejercicio-fuentes/   # Cargar y aplicar Google Fonts
│   ├── 02-ejercicio-type-scale/ # Escala modular con rem
│   └── 03-ejercicio-tokens/    # Sistema de design tokens con variables
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

### Teoría

| Archivo | Tema |
|---|---|
| [01-tipografia-web.md](1-teoria/01-tipografia-web.md) | @font-face, Google Fonts, font-display, font-weight |
| [02-colores-gradientes.md](1-teoria/02-colores-gradientes.md) | HSL, oklch, gradientes CSS, opacidad |
| [03-custom-properties.md](1-teoria/03-custom-properties.md) | CSS Custom Properties, :root, fallbacks, calc(), tema oscuro |

### Prácticas

| Ejercicio | Descripción |
|---|---|
| [01 — Fuentes Web](2-practicas/01-ejercicio-fuentes/README.md) | Cargar Google Fonts e integrarlas con CSS Custom Properties |
| [02 — Escala Tipográfica](2-practicas/02-ejercicio-type-scale/README.md) | Crear sistema de tamaños basado en razón 1.25 |
| [03 — Tokens CSS](2-practicas/03-ejercicio-tokens/README.md) | Sistema completo de design tokens: colors, type, spacing, radius |

### Proyecto

[Design Tokens Page](3-proyecto/README.md) — Página que documenta y demuestra su propio sistema de design tokens usando CSS Custom Properties.

---

## ⏱️ Distribución del Tiempo (8 horas)

| Actividad | Tiempo |
|---|---|
| 📖 Teoría (3 archivos) | 2h |
| 💻 Práctica 01 — Fuentes | 1h |
| 💻 Práctica 02 — Type Scale | 1h |
| 💻 Práctica 03 — Tokens | 1.5h |
| 🚀 Proyecto | 2h |
| ✅ Revisión y checklist | 30min |

---

## 📌 Entregables

1. Ejercicios 01, 02 y 03 completados (código descomentado y funcional)
2. Proyecto **Design Tokens Page** con sistema completo de variables

---

## 🎓 Conceptos Clave

| Concepto | Ejemplo |
|---|---|
| Google Fonts | `@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;700&display=swap')` |
| `font-display: swap` | Evita FOIT (Flash of Invisible Text) |
| Type Scale 1.25 | base → ×1.25 → ×1.563 → ×1.953 → ×2.441 |
| HSL | `hsl(220, 90%, 56%)` — hue / saturation / lightness |
| `linear-gradient` | `linear-gradient(135deg, #264de4, #e34f26)` |
| CSS Custom Property | `--color-primary: hsl(220, 90%, 56%);` |
| `:root` | Selector del elemento raíz para variables globales |
| Fallback | `color: var(--color-text, #0f172a)` |
| `calc()` | `width: calc(100% - 2rem)` |

---

## ✅ Checklist de Verificación

- [ ] Google Fonts cargando correctamente (sin FOIT)
- [ ] Escala tipográfica coherente y progresiva
- [ ] Colores definidos en HSL con variables CSS
- [ ] Todos los espaciados usando `var()` con valores `rem`
- [ ] `calc()` aplicado en al menos un caso práctico
- [ ] Tema oscuro funcionando con `prefers-color-scheme`
- [ ] Sin valores mágicos ("magic numbers") en el CSS
- [ ] Variables organizadas en categorías semánticas en `:root`

---

## 🔗 Navegación

← [Semana 09 — Responsive & Media Queries](../week-09-responsive_y_media_queries/README.md)
→ [Semana 11 — Transiciones, Transforms y Animaciones](../week-11-transiciones_transforms_y_animaciones/README.md)
