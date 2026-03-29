# Semana 12 — Selectores Avanzados y Pseudo-elementos CSS

> **Bootcamp HTML + CSS · Semana 12 de 13**

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana serás capaz de:

- ✅ Usar `:nth-child()`, `:nth-of-type()` y `:nth-last-child()` para seleccionar elementos por posición
- ✅ Filtrar elementos con `:not()`, `:is()` y `:where()` para agrupar reglas y reducir repetición
- ✅ Aplicar el selector parental `:has()` para estilar contenedores según su contenido
- ✅ Crear contenido decorativo con `::before` y `::after` usando la propiedad `content`
- ✅ Usar selectores de atributos (`[attr=value]`, `[attr^=]`, `[attr*=]`) para estilar por datos
- ✅ Construir interfaces sin JavaScript: tooltips, custom checkboxes, badges dinámicos
- ✅ Controlar el estado de formularios con `:checked`, `:focus-within`, `:valid`, `:invalid`

---

## 📚 Requisitos Previos

- ✔ Semanas 1–11 completadas
- ✔ Dominio de CSS Custom Properties (semana 10)
- ✔ Conocimiento de transiciones y transforms (semana 11)
- ✔ Comprensión de especificidad CSS (semana 4)

---

## 🗂 Estructura de la Semana

```
week-12-selectores_avanzados_y_pseudo_elementos/
├── README.md
├── rubrica-evaluacion.md
├── 0-assets/
│   ├── 01-pseudo-elements.svg         # ::before/::after concept diagram
│   └── 02-advanced-selectors.svg      # :nth-child, :has, :not visual guide
├── 1-teoria/
│   ├── 01-pseudo-clases-posicion.md   # :nth-child, :nth-of-type, :last-child
│   ├── 02-pseudo-elementos.md         # ::before, ::after, ::marker, ::selection
│   └── 03-selectores-avanzados.md     # :has, :is, :where, :not, [attr], :checked
├── 2-practicas/
│   ├── 01-ejercicio-nth/              # Tablas y grids con zebra stripes
│   ├── 02-ejercicio-pseudo-elements/  # Bullets, badges y ribbons decorativos
│   └── 03-ejercicio-tooltips/         # Tooltips data-* + ::after (sin JS)
├── 3-proyecto/
│   ├── README.md
│   ├── starter/                       # Custom Form y Component Showcase
│   └── solution/                      # ⚠️ Solo instructores
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

| Archivo | Tema | Tiempo |
|---------|------|--------|
| [01-pseudo-clases-posicion.md](1-teoria/01-pseudo-clases-posicion.md) | `:nth-child`, `:nth-of-type`, `:last-child`, `:first-child` | 45 min |
| [02-pseudo-elementos.md](1-teoria/02-pseudo-elementos.md) | `::before`, `::after`, `::marker`, `::selection`, `::placeholder` | 45 min |
| [03-selectores-avanzados.md](1-teoria/03-selectores-avanzados.md) | `:has()`, `:is()`, `:where()`, `:not()`, `[attr]`, estados de formulario | 45 min |

### Prácticas

| Ejercicio | Tema | Tiempo |
|-----------|------|--------|
| [01-ejercicio-nth](2-practicas/01-ejercicio-nth/) | Zebra stripes, highlight impar/par, grid patterns con `:nth-child` | 50 min |
| [02-ejercicio-pseudo-elements](2-practicas/02-ejercicio-pseudo-elements/) | Bullets custom, badges `::before`, ribbon decorativo `::after` | 55 min |
| [03-ejercicio-tooltips](2-practicas/03-ejercicio-tooltips/) | Sistema de tooltips CSS puro con `[data-tooltip]` + `::after` | 55 min |

### Proyecto

| Entregable | Descripción |
|-----------|-------------|
| [Component Showcase](3-proyecto/README.md) | Tabla estilizada, checkboxes custom, tooltips y ribbon — sin JavaScript |

---

## ⏱ Distribución del Tiempo (8 horas)

```
📖 Teoría          2h 15min  ▓▓▓▓▓▓▓▓▓░░░░░░░░░░░░
💻 Prácticas       3h 25min  ▓▓▓▓▓▓▓▓▓▓▓▓▓▓░░░░░░░
🚀 Proyecto        2h 20min  ▓▓▓▓▓▓▓▓▓░░░░░░░░░░░░
```

---

## 🎓 Conceptos Clave

| Concepto | Descripción corta |
|----------|-------------------|
| `:nth-child(n)` | Selecciona el elemento en posición `n` dentro de su padre |
| `:nth-child(even/odd)` | Selecciona elementos en posición par o impar |
| `:nth-child(An+B)` | Fórmula: cada A elementos, empezando desde B |
| `:not(selector)` | Excluye elementos que coincidan con el selector |
| `:is()` | Agrupa selectores con la especificidad del más alto |
| `:where()` | Equivalente a `:is()` pero con especificidad cero |
| `:has()` | Selector parental: selecciona padre si contiene el hijo dado |
| `::before` | Crea un pseudo-elemento antes del contenido real |
| `::after` | Crea un pseudo-elemento después del contenido real |
| `content` | Propiedad obligatoria en `::before`/`::after` (valor mínimo: `""`) |
| `[attr=value]` | Selecciona elementos con un atributo de valor exacto |
| `[attr^=value]` | Atributo que **empieza** con el valor dado |
| `[attr*=value]` | Atributo que **contiene** el valor dado |
| `:checked` | Estado activo de `<input type="checkbox/radio">` |
| `:focus-within` | Padre que tiene un descendiente con foco |

---

## 📌 Entregables

1. Completar los 3 ejercicios guiados (descomentando código paso a paso)
2. Entregar el **Component Showcase** (`3-proyecto/starter/`) completo y funcional
3. La solución debe funcionar **sin ninguna línea de JavaScript**

---

## ✅ Checklist de Verificación

- [ ] Las tablas tienen zebra stripes con `:nth-child(even)`
- [ ] Al menos un `::before` y un `::after` con contenido decorativo real
- [ ] El tooltip funciona solo con CSS (`[data-tooltip]` + `::after` + `:hover`)
- [ ] Los checkboxes custom no usan `<input>` oculto ni JS
- [ ] Se usa `:has()` en al menos un caso práctico
- [ ] El código **no** usa `!important` innecesariamente
- [ ] Se mantiene especificidad baja con `:is()` o `:where()` donde aplique
- [ ] Todos los elementos interactivos tienen estilos `:focus-visible`
- [ ] HTML válido (sin errores en W3C Validator)

---

## 🔗 Navegación

← [Semana 11 — Transiciones, Transforms y Animaciones](../week-11-transiciones_transforms_y_animaciones/README.md)
→ [Semana 13 — Semántica, Accesibilidad y Proyecto Final](../week-13-semantica_accesibilidad_y_proyecto_final/README.md)
