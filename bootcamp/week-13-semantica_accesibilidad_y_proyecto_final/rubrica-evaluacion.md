# Rúbrica de Evaluación — Semana 13

> Semántica, Accesibilidad y Proyecto Final

---

## 📊 Distribución de Evidencias

| Evidencia | Peso | Puntos |
|-----------|------|--------|
| 🧠 Conocimiento (cuestionario) | 30% | 30 pts |
| 💪 Desempeño (ejercicios prácticos) | 40% | 40 pts |
| 📦 Producto (proyecto capstone) | 30% | 30 pts |
| **Total** | **100%** | **100 pts** |

**Mínimo para aprobar:** 70 pts totales con al menos 21 pts en cada evidencia.

---

## 🧠 Conocimiento — 30 puntos

Cuestionario de 5 preguntas de opción múltiple y respuesta corta.

| # | Pregunta | Pts |
|---|----------|-----|
| 1 | ¿Cuál es la diferencia entre `<section>` y `<article>`? | 6 |
| 2 | Escribe el código HTML completo de un skip link funcional. | 6 |
| 3 | ¿Cuál es el contraste mínimo WCAG 2.1 AA para texto normal? | 6 |
| 4 | ¿Qué diferencia hay entre `aria-label` y `aria-labelledby`? | 6 |
| 5 | ¿Por qué se usa `:focus-visible` en lugar de `:focus` para estilos de outline? | 6 |

---

## 💪 Desempeño — 40 puntos

### Ejercicio 01 — Semántica HTML5 (14 pts)

Convertir un documento con "div soup" a HTML5 semántico correcto.

| Criterio | Pts |
|----------|-----|
| Uso correcto de `<header>`, `<nav>`, `<main>`, `<footer>` | 4 |
| `<article>` y `<section>` con su heading correspondiente | 3 |
| `<figure>` + `<figcaption>` para imagen con descripción | 3 |
| `<time datetime="">` con valor correcto | 2 |
| Jerarquía de headings sin saltos | 2 |

### Ejercicio 02 — ARIA (13 pts)

Añadir atributos ARIA a un formulario y un botón de modal.

| Criterio | Pts |
|----------|-----|
| `aria-label` correcto en botón sin texto visible | 3 |
| `aria-labelledby` vinculando `<legend>` o `<h2>` al `<form>` | 3 |
| `aria-describedby` para mensajes de error de input | 3 |
| `aria-hidden="true"` en icono decorativo | 2 |
| `role="alert"` para mensajes dinámicos de error | 2 |

### Ejercicio 03 — Navegación por Teclado (13 pts)

Implementar skip link, jerarquía tabindex y `:focus-visible`.

| Criterio | Pts |
|----------|-----|
| Skip link visible al recibir foco y funcional | 4 |
| `.visually-hidden` implementado correctamente (no `display:none`) | 3 |
| `:focus-visible` con outline claro en todos los interactivos | 3 |
| Orden lógico de tabulación (sin `tabindex` positivo) | 3 |

---

## 📦 Producto — 30 puntos

### Portfolio Personal Capstone

| Criterio | Pts |
|----------|-----|
| **HTML semántico** — landmarks correctos, un solo `<h1>`, jerarquía de headings | 5 |
| **CSS responsive** — mobile-first, 3 breakpoints mínimo, sin desbordamientos | 5 |
| **Accesibilidad** — contraste AA, alt en imágenes, labels en form, skip link | 5 |
| **CSS avanzado** — Custom Properties, Flexbox/Grid en layout, transiciones CSS | 5 |
| **SEO básico** — `<title>`, `<meta description>`, Open Graph, `lang="es"` | 4 |
| **Calidad del código** — sin errores W3C, organizado, sin `!important` | 3 |
| **Entrega puntual** — entregado antes del plazo | 3 |

---

## 🔢 Escala de Calificación

| Rango | Calificación |
|-------|-------------|
| 90–100 | Excelente — Listo para portfolio profesional |
| 80–89 | Muy bien — Solo detalles menores a mejorar |
| 70–79 | Aprobado — Cumple los requisitos básicos |
| 60–69 | Insuficiente — Requiere repaso y reentrega |
| < 60 | No aprobado — Semana a repetir |
