# Rúbrica de Evaluación — Semana 12

> **Selectores Avanzados y Pseudo-elementos CSS**
> Distribución: Conocimiento 30% · Desempeño 40% · Producto 30%

---

## 🧠 Conocimiento (30 puntos)

Cuestionario escrito o verbal al inicio/cierre de la sesión.

| # | Pregunta | Pts |
|---|----------|-----|
| 1 | ¿Cuál es la diferencia entre `:nth-child(2)` y `:nth-of-type(2)`? Da un ejemplo donde producen resultados distintos. | 6 |
| 2 | ¿Por qué `::before` y `::after` requieren la propiedad `content`? ¿Qué sucede si se omite? | 6 |
| 3 | ¿Cuál es la diferencia de especificidad entre `:is(h1, h2)` y `:where(h1, h2)`? | 6 |
| 4 | Escribe un selector CSS que aplique estilos a un `<form>` solo cuando contiene un `<input>` con el atributo `required`. | 6 |
| 5 | ¿Para qué sirve `:focus-within` y en qué se diferencia de `:focus`? | 6 |

---

## 💪 Desempeño (40 puntos)

Evaluación en tiempo real durante los ejercicios prácticos.

### Ejercicio 01 — Patrones con `:nth-child` (14 pts)

| Criterio | Pts |
|----------|-----|
| Zebra stripes aplicados correctamente con `:nth-child(even/odd)` | 4 |
| Primer y último elemento con estilos diferenciados (`:first-child`, `:last-child`) | 3 |
| Patrón `3n+1` implementado correctamente en la grilla | 4 |
| No se usan clases extra en el HTML para lograr los estilos | 3 |

### Ejercicio 02 — Pseudo-elementos decorativos (13 pts)

| Criterio | Pts |
|----------|-----|
| `::before` con `content` no vacío y posicionamiento correcto | 4 |
| `::after` usado para decoración sin modificar el HTML | 4 |
| El ribbon diagonal usa `position: absolute` en el pseudo-elemento | 3 |
| Los pseudo-elementos no rompen el layout (overflow controlado) | 2 |

### Ejercicio 03 — Tooltips CSS puro (13 pts)

| Criterio | Pts |
|----------|-----|
| Tooltip aparece correctamente en `:hover` sin JS | 5 |
| Usa `[data-tooltip]` + `attr()` para leer el texto dinámico | 4 |
| Tooltip con `visibility: hidden` / `opacity: 0` (no `display: none`) para transición | 2 |
| `aria-label` u otro atributo de accesibilidad presente en el elemento | 2 |

---

## 📦 Producto (30 puntos)

Proyecto **Component Showcase** entregado y funcional.

| Criterio | Pts |
|----------|-----|
| Tabla con zebra stripes, primera fila destacada con `:first-child` | 5 |
| Checkboxes custom construidos solo con CSS (`<input>` + `<label>` + `:checked ~ ::before`) | 7 |
| Al menos un ribbon o badge implementado con `::before`/`::after` | 5 |
| Sistema de tooltips funcional para todos los botones de acción | 6 |
| Se usa `:has()` en al menos un selector del proyecto | 4 |
| Zero JavaScript — ningún `<script>` en el HTML ni inline | 3 |

---

## 📊 Escala de Calificación

| Puntos | Nivel |
|--------|-------|
| 90–100 | ⭐ Excelente — dominio sólido de selectores avanzados |
| 75–89  | ✅ Competente — comprensión buena con detalles menores |
| 60–74  | 📚 En desarrollo — necesita reforzar pseudo-elementos y `:has()` |
| < 60   | ⚠️ Insuficiente — requiere revisión de selectores fundamentales |

### Criterios de Aprobación

- Mínimo **70%** en cada categoría por separado
- El producto debe funcionar **sin ninguna línea de JavaScript**
- HTML válido (W3C Validator sin errores)
