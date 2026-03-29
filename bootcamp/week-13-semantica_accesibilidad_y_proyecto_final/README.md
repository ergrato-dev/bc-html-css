# Semana 13 — Semántica, Accesibilidad y Proyecto Final

> **Bootcamp HTML + CSS Zero to Hero** · Semana 13 de 13

---

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana serás capaz de:

1. Estructurar documentos HTML5 usando **etiquetas semánticas** de forma correcta y profunda
2. Comprender y aplicar el árbol de accesibilidad y los **roles ARIA** fundamentales
3. Implementar **accesibilidad de teclado**: skip links, `tabindex`, `:focus-visible`
4. Escribir HTML que cumpla **WCAG 2.1 AA**: contraste, alternativas de texto, navegación
5. Aplicar **SEO on-page** básico: estructura de headings, meta tags, open graph
6. Construir un **portfolio personal completo** integrando todos los conceptos del bootcamp

---

## 📚 Requisitos Previos

- Semana 12 completada (selectores avanzados y pseudo-elementos)
- Dominio de Flexbox y CSS Grid (semanas 7 y 8)
- Diseño responsive y Custom Properties (semanas 9 y 10)
- Transiciones y animaciones (semana 11)

---

## 🗂️ Estructura de la Semana

```
week-13-semantica_accesibilidad_y_proyecto_final/
├── README.md                         ← Este archivo
├── rubrica-evaluacion.md             ← Criterios de evaluación
├── 0-assets/
│   ├── 01-aria-roles.svg             ← Diagrama de roles ARIA landmark
│   └── 02-semantic-structure.svg    ← Árbol de estructura HTML5 semántica
├── 1-teoria/
│   ├── 01-semantica-html5.md         ← Etiquetas semánticas en profundidad
│   ├── 02-accesibilidad-aria.md      ← ARIA, WCAG, teclado, :focus-visible
│   └── 03-seo-y-rendimiento.md       ← Meta tags, OG, Core Web Vitals
├── 2-practicas/
│   ├── 01-ejercicio-semantica/       ← Convertir div-soup a HTML semántico
│   ├── 02-ejercicio-aria/            ← Añadir ARIA a formulario y modal
│   └── 03-ejercicio-keyboard/        ← Skip link + focus management
├── 3-proyecto/
│   ├── README.md                     ← Instrucciones del portfolio capstone
│   ├── starter/                      ← Código inicial con TODOs
│   └── solution/                     ← ⚠️ Solo instructores
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
| [01-semantica-html5.md](1-teoria/01-semantica-html5.md) | Landmarks, `<figure>`, `<time>`, `<address>`, jerarquía heading | 45 min |
| [02-accesibilidad-aria.md](1-teoria/02-accesibilidad-aria.md) | ARIA roles/labels, tabindex, :focus-visible, skip links, WCAG AA | 45 min |
| [03-seo-y-rendimiento.md](1-teoria/03-seo-y-rendimiento.md) | Meta tags, Open Graph, Core Web Vitals, performance checklist | 30 min |

### Prácticas

| Ejercicio | Tema | Tiempo |
|-----------|------|--------|
| [01-ejercicio-semantica](2-practicas/01-ejercicio-semantica/) | "Div soup" → HTML5 semántico correcto | 45 min |
| [02-ejercicio-aria](2-practicas/02-ejercicio-aria/) | ARIA labels en formulario y botón de modal | 40 min |
| [03-ejercicio-keyboard](2-practicas/03-ejercicio-keyboard/) | Skip link + jerarquía de tabindex + :focus-visible | 35 min |

### Proyecto

| Entregable | Descripción | Tiempo |
|------------|-------------|--------|
| [Portfolio Personal Completo](3-proyecto/README.md) | Capstone: portfolio responsive con todo lo aprendido | 2 h |

---

## ⏱️ Distribución del Tiempo (8 horas)

```
📖 Teoría (3 archivos):       2 h      (25%)
💻 Prácticas (3 ejercicios):  2 h      (25%)
🚀 Proyecto capstone:         2 h      (25%)
🔍 Revisión y refino:         2 h      (25%)
```

---

## 🎓 Conceptos Clave

| Concepto | Descripción |
|----------|-------------|
| `<main>` | Contenido principal único por página |
| `<article>` | Contenido autocontenido y redistribuible |
| `<section>` | Sección temática con su propio heading |
| `<aside>` | Contenido complementario |
| `<nav>` | Bloque de navegación (puede haber varios) |
| `<figure>` + `<figcaption>` | Imagen/gráfico con descripción asociada |
| `<time datetime="">` | Fecha/hora legible por máquina |
| `<address>` | Información de contacto del autor |
| `role="banner"` | Landmark: encabezado del sitio |
| `role="main"` | Landmark: contenido principal |
| `role="navigation"` | Landmark: región de navegación |
| `role="contentinfo"` | Landmark: pie de página |
| `aria-label` | Nombre accesible cuando no hay texto visible |
| `aria-labelledby` | Referencia a otro elemento como etiqueta |
| `aria-describedby` | Descripción adicional de un elemento |
| `aria-hidden="true"` | Excluir de lectores de pantalla |
| `tabindex="0"` | Añade elemento al orden de tabulación |
| `tabindex="-1"` | Permite foco programático, no en tab |
| `:focus-visible` | Foco del teclado (no mouse) — WCAG 2.1 |
| Skip link | Enlace "Saltar al contenido" para usuarios de teclado |
| WCAG 2.1 AA | Contraste mínimo 4.5:1 texto normal, 3:1 texto grande |
| Open Graph | Meta tags para compartir en redes sociales |

---

## 📌 Entregables

- [ ] 3 ejercicios prácticos completados
- [ ] Portfolio personal funcional y responsive (semana 13 · proyecto capstone)
- [ ] HTML validado en [W3C Validator](https://validator.w3.org/)
- [ ] Sin errores de accesibilidad en [axe DevTools](https://www.deque.com/axe/devtools/)

---

## ✅ Checklist de Verificación

**Semántica:**
- [ ] Uso correcto de landmarks: `<header>`, `<nav>`, `<main>`, `<footer>`
- [ ] Solo un `<h1>` por página
- [ ] Jerarquía de headings sin saltos (`h1 → h2 → h3`)
- [ ] `<img>` con `alt` descriptivo (vacío si decorativa)
- [ ] Formularios con `<label>` vinculado a cada `<input>`

**Accesibilidad:**
- [ ] Contraste mínimo 4.5:1 para texto normal
- [ ] Contraste mínimo 3:1 para texto grande (18px+ o 14px+ bold)
- [ ] Skip link visible al recibir foco
- [ ] Todos los elementos interactivos accesibles por teclado
- [ ] Sin `tabindex` positivo (solo 0 o -1)
- [ ] `aria-label` en botones icono
- [ ] `lang="es"` en `<html>`

**SEO:**
- [ ] `<title>` único y descriptivo
- [ ] `<meta name="description">` específica y < 160 caracteres
- [ ] Open Graph tags presentes
- [ ] URL canónica con `<link rel="canonical">`

**Código:**
- [ ] Sin errores en W3C Validator
- [ ] Sin `display:none` para contenido accesible (usar `.visually-hidden`)
- [ ] `prefers-reduced-motion` respetado en animaciones

---

## 🔗 Navegación

← [Semana 12 — Selectores Avanzados y Pseudo-elementos](../week-12-selectores_avanzados_y_pseudo_elementos/README.md) | **Fin del Bootcamp** 🎓

---

> **¡Felicidades!** Esta es la última semana del Bootcamp HTML + CSS Zero to Hero.  
> Al completar el proyecto capstone tendrás un portfolio profesional listo para mostrar.
