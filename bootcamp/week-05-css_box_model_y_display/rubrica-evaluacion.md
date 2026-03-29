# Rúbrica de Evaluación — Semana 05: CSS Box Model y Display

## Distribución de puntos

| Tipo de evidencia | Porcentaje | Puntos |
|-------------------|-----------|--------|
| 🧠 Conocimiento | 30% | 30 pts |
| 💪 Desempeño | 40% | 40 pts |
| 📦 Producto | 30% | 30 pts |
| **Total** | **100%** | **100 pts** |

---

## 🧠 Conocimiento (30 pts)

### Cuestionario teórico (20 pts)

| # | Pregunta | Pts |
|---|----------|-----|
| 1 | ¿Cuáles son los 4 componentes del Box Model en orden de adentro hacia afuera? | 3 |
| 2 | ¿Qué diferencia hay entre `box-sizing: content-box` y `box-sizing: border-box`? | 4 |
| 3 | ¿Qué es el colapso de márgenes (margin collapse)? ¿Cuándo ocurre? | 4 |
| 4 | ¿Para qué sirve `margin: 0 auto` y en qué condiciones funciona? | 3 |
| 5 | ¿Qué valor de `display` permite aplicar width/height a un elemento inline? | 3 |
| 6 | ¿Qué hace `overflow: hidden` y en qué casos lo usarías? | 3 |

### Identificación visual (10 pts)

El instructor muestra capturas del panel DevTools → Computed con el diagrama del Box Model. El estudiante debe:
- Identificar qué valor corresponde a cada capa (4 pts)
- Calcular el ancho total del elemento en `content-box` dado sus valores (3 pts)
- Indicar qué cambia si se aplica `border-box` (3 pts)

---

## 💪 Desempeño (40 pts)

### Ejercicio 01 — Box Model (14 pts)

| Criterio | Pts |
|----------|-----|
| Descomenta correctamente los pasos 1–4 sin errores de sintaxis | 4 |
| El diagrama visual del Box Model muestra claramente las 4 capas | 4 |
| `box-sizing: border-box` aplicado y el layout no se rompe | 3 |
| Verifica el resultado en DevTools → Computed | 3 |

### Ejercicio 02 — Margin y Padding (12 pts)

| Criterio | Pts |
|----------|-----|
| Usa shorthand de margin/padding correctamente | 3 |
| Centra un bloque con `margin: 0 auto` | 3 |
| Explica el colapso de márgenes observado entre dos secciones | 3 |
| Usa margin negativo para un efecto de superposición | 3 |

### Ejercicio 03 — Display y Overflow (14 pts)

| Criterio | Pts |
|----------|-----|
| Convierte elementos inline a `inline-block` con dimensiones | 4 |
| Aplica `display: none` y `visibility: hidden` y nota la diferencia | 4 |
| Controla el overflow de un contenedor con texto largo | 3 |
| No usa `float` para la tarea (sancionar) | 3 |

---

## 📦 Producto (30 pts)

### Proyecto: Tarjetas de Producto

| Criterio | Excelente (100%) | Bueno (75%) | Suficiente (50%) | Insuficiente (0%) |
|----------|-----------------|-------------|-----------------|-------------------|
| **Box Model correcto** (8 pts) | Padding/border/margin calculados con `border-box`, sin desbordamiento | Aplica border-box pero hay pequeños desajustes | Paddings inconsistentes | Sin box-sizing definido |
| **Layout de cards** (7 pts) | 3 columnas uniformes con gap correcto en todos los tamaños | 3 columnas pero gap irregular | Layout funciona solo en desktop | Cards se superponen |
| **Espaciado consistente** (6 pts) | Usa variables CSS para todos los espaciados | >75% de espaciados con variables | Solo algunos con variables | Sin variables |
| **Overflow controlado** (5 pts) | Texto largo truncado con ellipsis, imágenes no se desbordan | Imágenes controladas pero texto desbordado | Solo overflow básico | Contenido desbordado visible |
| **Validación CSS** (4 pts) | 0 errores W3C Validator | 1–2 warnings | 3–5 errores menores | Errores graves |

---

## 📊 Tabla de calificaciones

| Rango | Calificación |
|-------|-------------|
| 90–100 | Excelente |
| 80–89 | Bueno |
| 70–79 | Suficiente |
| < 70 | Insuficiente (requiere retroalimentación) |
