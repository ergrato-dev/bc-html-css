# Semana 08 — CSS Grid

Domina el sistema de layout bidimensional más potente de CSS: **CSS Grid**. Construirás layouts complejos con filas y columnas de forma declarativa, sin hacks ni floats.

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana serás capaz de:

- ✅ Activar CSS Grid con `display: grid`
- ✅ Definir columnas y filas con `grid-template-columns` / `grid-template-rows`
- ✅ Crear layouts con áreas nombradas (`grid-template-areas`)
- ✅ Posicionar items explícitamente con `grid-column` / `grid-row`
- ✅ Crear grids responsive con `repeat()`, `auto-fit`, `auto-fill` y `minmax()`
- ✅ Distinguir cuándo usar Grid vs. Flexbox

---

## 📚 Requisitos Previos

- Semana 05 — Box Model y Display
- Semana 07 — Flexbox (especialmente `flex-direction` y `align-items`)

---

## 🗂️ Estructura de la Semana

```
week-08-css_grid/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
│   ├── 01-grid-conceptos.svg
│   └── 02-grid-areas.svg
├── 1-teoria/
│   ├── 01-grid-container.md
│   ├── 02-grid-areas.md
│   └── 03-grid-funciones.md
├── 2-practicas/
│   ├── 01-ejercicio-grid-container/
│   ├── 02-ejercicio-grid-areas/
│   └── 03-ejercicio-grid-responsive/
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

| # | Archivo | Descripción |
|---|---------|-------------|
| 1 | [01-grid-container.md](1-teoria/01-grid-container.md) | display:grid, columnas, filas, gap, fr unit |
| 2 | [02-grid-areas.md](1-teoria/02-grid-areas.md) | grid-template-areas, grid-column/row, spanning |
| 3 | [03-grid-funciones.md](1-teoria/03-grid-funciones.md) | repeat(), minmax(), auto-fit, auto-fill, clamp() |

---

## ⏱️ Distribución del Tiempo (8 horas)

| Actividad | Tiempo |
|-----------|--------|
| Teoría: Grid container y fr unit | 1.5h |
| Teoría: Grid areas y posicionamiento | 1h |
| Teoría: Funciones avanzadas | 0.5h |
| Práctica 01: Grid container | 1h |
| Práctica 02: Grid areas | 1h |
| Práctica 03: Grid responsive | 1h |
| Proyecto: AdminGrid | 1.5h |

---

## 📌 Entregables

- [ ] Tres ejercicios prácticos completados
- [ ] Proyecto AdminGrid funcional y responsive
- [ ] Layout con `grid-template-areas` correcto en desktop y mobile

---

## 🎓 Conceptos Clave

| Concepto | Descripción |
|----------|-------------|
| `display: grid` | Activa CSS Grid en el contenedor |
| `fr` | Fracción del espacio disponible |
| `grid-template-areas` | Layout visual declarativo con nombres |
| `repeat()` | Repite columnas/filas |
| `minmax(min, max)` | Tamaño adaptable con límites |
| `auto-fit` | Crea tantas columnas como quepan |
| `gap` | Espacio entre celdas |

---

## ✅ Checklist de Verificación

- [ ] Activar `display: grid` y definir columnas con `fr`
- [ ] Gap funciona como espacio entre celdas
- [ ] `grid-template-areas` dibuja el layout correctamente
- [ ] Un item ocupa varias celdas con `grid-column: span 2`
- [ ] `auto-fit` + `minmax()` crea columnas responsivas automáticamente
- [ ] El layout se reorganiza correctamente en móvil

---

## 🔗 Navegación

← [Semana 07 — Flexbox](../week-07-flexbox/README.md) | [Semana 09 — Responsive y Media Queries](../week-09-responsive_y_media_queries/README.md) →
