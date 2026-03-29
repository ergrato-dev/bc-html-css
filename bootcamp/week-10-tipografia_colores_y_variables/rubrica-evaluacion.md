# Rúbrica de Evaluación — Semana 10: Tipografía, Colores y Variables CSS

## 📊 Distribución de Evidencias

| Tipo | Porcentaje | Descripción |
|---|---|---|
| 🧠 Conocimiento | 30% | Comprensión conceptual evaluada mediante preguntas |
| 💪 Desempeño | 40% | Ejercicios prácticos realizados en clase |
| 📦 Producto | 30% | Proyecto Design Tokens Page |

---

## 🧠 Conocimiento (30 puntos)

### Preguntas de Evaluación

1. **(6 pts)** ¿Qué es `font-display: swap` y por qué es importante para el rendimiento web? Describe qué ocurre sin este atributo.

2. **(6 pts)** Explica los tres parámetros del modelo de color HSL: `hue`, `saturation` y `lightness`. ¿Qué ventaja tiene HSL sobre HEX para crear paletas programáticamente?

3. **(6 pts)** ¿Cuál es la diferencia entre una variable CSS (`--mi-variable`) y una variable de un preprocesador como SASS? Menciona dos ventajas de las CSS Custom Properties.

4. **(6 pts)** ¿Qué hace `calc()`? Escribe un ejemplo donde sea necesario combinar dos unidades diferentes.

5. **(6 pts)** ¿Cómo funciona un sistema de escala tipográfica modular? Si la base es `1rem` y la razón es `1.25`, ¿cuál es el valor de los niveles `md`, `lg` y `xl`?

---

## 💪 Desempeño (40 puntos)

### Ejercicio 01 — Fuentes Web (12 pts)

| Criterio | Puntos |
|---|---|
| Google Fonts importada correctamente (con `display=swap`) | 3 |
| Fuente asignada mediante CSS Custom Property (`--font-body`) | 3 |
| `font-display: swap` presente | 3 |
| Fallback stack definido correctamente | 3 |

### Ejercicio 02 — Escala Tipográfica (14 pts)

| Criterio | Puntos |
|---|---|
| Escala de 5+ niveles con valores `rem` coherentes | 4 |
| Todos los valores declarados como variables CSS | 4 |
| Aplicación correcta de `font-weight` y `line-height` | 3 |
| Escala visible y legible en el navegador | 3 |

### Ejercicio 03 — Design Tokens (14 pts)

| Criterio | Puntos |
|---|---|
| Variables de color en HSL | 4 |
| Variables de espaciado en `rem` | 4 |
| Variables de tipografía (sizes + families) | 3 |
| Variables de `border-radius` y bordes | 3 |

---

## 📦 Producto (30 puntos)

### Proyecto — Design Tokens Page

| Criterio | Puntos |
|---|---|
| Sistema completo de variables en `:root` (colores, tipo, espaciados, radios) | 8 |
| Paleta de colores en HSL con 3+ variantes por color | 6 |
| Escala tipográfica aplicada correctamente | 6 |
| Tema oscuro con `prefers-color-scheme: dark` | 5 |
| `calc()` usado en al menos 2 lugares | 3 |
| Sin valores mágicos en el CSS (todo usa `var()`) | 2 |

---

## ✅ Criterios de Aprobación

- Mínimo **21/30** en Conocimiento (70%)
- Mínimo **28/40** en Desempeño (70%)
- Mínimo **21/30** en Producto (70%)
- Sin errores de validación W3C en HTML y CSS
