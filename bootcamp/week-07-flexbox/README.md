# Semana 07 — Flexbox

## 🎯 Objetivos de aprendizaje

Al finalizar esta semana, el estudiante será capaz de:

- Activar un contenedor flex y comprender los ejes principal y cruzado
- Controlar la dirección, envoltura y espaciado con propiedades del contenedor flex
- Alinear y distribuir elementos con `justify-content` y `align-items`
- Controlar el tamaño de los flex items con `flex-grow`, `flex-shrink` y `flex-basis`
- Construir patrones de UI comunes: navbars, cards, centrado, sidebar

---

## 📚 Requisitos previos

- Semana 05: CSS Box Model y Display (`display: block/inline`)
- Semana 06: Positioning (para superponer elementos si se requiere)

---

## 🗂️ Estructura de la semana

```
week-07-flexbox/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
│   ├── 01-flex-ejes.svg
│   └── 02-flex-propiedades.svg
├── 1-teoria/
│   ├── 01-flex-container.md
│   ├── 02-flex-items.md
│   └── 03-flex-patrones.md
├── 2-practicas/
│   ├── 01-ejercicio-flex-container/
│   ├── 02-ejercicio-flex-items/
│   └── 03-ejercicio-flex-patrones/
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
| [01-flex-container.md](1-teoria/01-flex-container.md) | `display: flex`, `flex-direction`, `flex-wrap`, `justify-content`, `align-items`, `gap` |
| [02-flex-items.md](1-teoria/02-flex-items.md) | `flex-grow`, `flex-shrink`, `flex-basis`, shorthand `flex`, `align-self`, `order` |
| [03-flex-patrones.md](1-teoria/03-flex-patrones.md) | Patrones: navbar, centrado perfecto, cards iguales, sidebar + main |

### Prácticas

| Ejercicio | Concepto |
|-----------|---------|
| [01-ejercicio-flex-container](2-practicas/01-ejercicio-flex-container/) | Ejes, dirección, wrap, gap, justify y align |
| [02-ejercicio-flex-items](2-practicas/02-ejercicio-flex-items/) | grow, shrink, basis, order, align-self |
| [03-ejercicio-flex-patrones](2-practicas/03-ejercicio-flex-patrones/) | Navbar + hero centrado + grid de tarjetas + sidebar |

---

## ⏱️ Distribución del tiempo (8 horas)

| Actividad | Tiempo |
|-----------|--------|
| Teoría: flex container | 1.5 h |
| Teoría: flex items y patrones | 1 h |
| Práctica 01: container | 1.5 h |
| Práctica 02: items | 1 h |
| Práctica 03: patrones | 1 h |
| Proyecto: FlexDash | 2 h |

---

## 📌 Entregables

- ✅ Ejercicios completados (descomenta bloques paso a paso)
- ✅ Proyecto: **FlexDash** — layout de dashboard con Flexbox

---

## 🎓 Conceptos clave

- **Eje principal (main axis):** dirección de `flex-direction` (por defecto: horizontal)
- **Eje cruzado (cross axis):** perpendicular al eje principal
- **`justify-content`:** distribuye items **en el eje principal**
- **`align-items`:** alinea items **en el eje cruzado**
- **`flex: 1`:** shorthand para `flex-grow:1; flex-shrink:1; flex-basis:0%` — reparte espacio igualmente
- **`gap`:** espacio entre flex items (no en los bordes externos)

---

## ✅ Checklist de verificación

- [ ] Entiendo la diferencia entre eje principal y eje cruzado
- [ ] Puedo cambiar la dirección con `flex-direction`
- [ ] Uso `justify-content: space-between` para separar items en una fila
- [ ] Uso `align-items: center` para alinear verticalmente en una fila
- [ ] Conozco la diferencia entre `flex: 1` y `flex: 1 1 200px`
- [ ] Puedo crear un layout de sidebar + main solo con Flexbox
- [ ] Uso `gap` en lugar de márgenes para espacio entre items

---

## 🔗 Navegación

← [Semana 06 — Positioning y Float](../week-06-positioning_y_float/README.md) &nbsp;|&nbsp; [Semana 08 — CSS Grid](../week-08-css_grid/README.md) →
