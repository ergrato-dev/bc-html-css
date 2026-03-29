# Semana 06 — Positioning y Float

## 🎯 Objetivos de aprendizaje

Al finalizar esta semana, el estudiante será capaz de:

- Comprender el flujo normal del documento y cómo `position` lo altera
- Aplicar `position: relative`, `absolute`, `fixed` y `sticky` correctamente
- Identificar el *containing block* de cada elemento posicionado
- Controlar el apilamiento visual con `z-index` y el *stacking context*
- Usar `float` y la técnica de *clearfix* cuando sea necesario
- Saber cuándo **no** usar float (y por qué Flexbox/Grid lo reemplaza)

---

## 📚 Requisitos previos

- Semana 05: CSS Box Model y Display
- Conocer `display: block`, `inline`, `inline-block`
- Entender `margin`, `padding`, `overflow`

---

## 🗂️ Estructura de la semana

```
week-06-positioning_y_float/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
│   ├── 01-position-contexts.svg
│   └── 02-stacking-context.svg
├── 1-teoria/
│   ├── 01-position.md
│   ├── 02-z-index-y-stacking.md
│   └── 03-float-y-clearfix.md
├── 2-practicas/
│   ├── 01-ejercicio-position/
│   ├── 02-ejercicio-z-index/
│   └── 03-ejercicio-float/
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
|---------|------|
| [01-position.md](1-teoria/01-position.md) | `static`, `relative`, `absolute`, `fixed`, `sticky` y el *containing block* |
| [02-z-index-y-stacking.md](1-teoria/02-z-index-y-stacking.md) | `z-index`, stacking context y orden visual |
| [03-float-y-clearfix.md](1-teoria/03-float-y-clearfix.md) | `float`, `clear`, clearfix moderno y alternativas |

### Prácticas

| Ejercicio | Concepto |
|-----------|---------|
| [01-ejercicio-position](2-practicas/01-ejercicio-position/) | Tarjetas con badges absolutos, modal overlay, header sticky |
| [02-ejercicio-z-index](2-practicas/02-ejercicio-z-index/) | Capas y orden de apilamiento |
| [03-ejercicio-float](2-practicas/03-ejercicio-float/) | Texto alrededor de imagen, clearfix, `display: flow-root` |

---

## ⏱️ Distribución del tiempo (8 horas)

| Actividad | Tiempo |
|-----------|--------|
| Teoría: position contexts | 1.5 h |
| Teoría: z-index y float | 1 h |
| Práctica 01: position | 1.5 h |
| Práctica 02: z-index | 1 h |
| Práctica 03: float | 1 h |
| Proyecto: Navbar + Overlays | 2 h |

---

## 📌 Entregables

- ✅ Ejercicios completados (descomenta bloques paso a paso)
- ✅ Proyecto iniciado: **NavLayout** — Navbar sticky + card con badge + modal overlay

---

## 🎓 Conceptos clave

- **Flujo normal**: cómo los elementos se colocan por defecto (block de arriba a abajo, inline de izquierda a derecha)
- **Containing block**: ancestro posicionado más cercano (`position != static`) que sirve de referencia para `absolute`
- **Stacking context**: contexto de apilamiento creado por `position + z-index`, `opacity < 1`, `transform`, etc.
- **Clearfix**: técnica para que un contenedor abarque sus hijos flotantes

---

## ✅ Checklist de verificación

- [ ] Puedo posicionar un badge sobre una imagen con `absolute`
- [ ] Entiendo la diferencia entre `fixed` (relativo al viewport) y `sticky` (relativo al scroll)
- [ ] Sé qué elemento es el *containing block* de un `absolute`
- [ ] Puedo crear un header sticky que no tape el contenido principal
- [ ] Entiendo cuándo `z-index` no funciona (sin contexto de apilamiento)
- [ ] Puedo hacer que un contenedor abarque floats con clearfix o `flow-root`

---

## 🔗 Navegación

← [Semana 05 — CSS Box Model y Display](../week-05-css_box_model_y_display/README.md) &nbsp;|&nbsp; [Semana 07 — Flexbox](../week-07-flexbox/README.md) →
