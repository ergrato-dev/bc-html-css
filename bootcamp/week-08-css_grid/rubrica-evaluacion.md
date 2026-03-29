# Rúbrica de Evaluación — Semana 08: CSS Grid

## 📊 Distribución de Evidencias

| Tipo | Peso | Descripción |
|------|------|-------------|
| 🧠 Conocimiento | 30% | Cuestionario teórico + DevTools |
| 💪 Desempeño | 40% | Tres ejercicios prácticos |
| 📦 Producto | 30% | Proyecto AdminGrid |

---

## 🧠 Conocimiento (30 puntos)

### Preguntas de Evaluación

1. ¿Cuál es la diferencia entre `display: flex` y `display: grid`?
   - Flex: unidimensional (fila O columna); Grid: bidimensional (filas Y columnas simultáneamente)

2. ¿Qué es la unidad `fr`?
   - Fracción del espacio disponible en el grid después de restar gaps y tamaños fijos

3. ¿Para qué sirve `grid-template-areas`?
   - Para definir el layout visual de manera declarativa asignando nombres a las celdas

4. ¿Cuál es la diferencia entre `auto-fit` y `auto-fill`?
   - `auto-fit`: colapsa columnas vacías; `auto-fill`: mantiene las columnas vacías reservando su espacio

5. ¿Qué hace `minmax(200px, 1fr)`?
   - El item tiene un mínimo de 200px y puede crecer hasta 1fr del espacio disponible

### Tarea DevTools

- Abrir el inspector de grid en Chrome DevTools (ícono cuadrícula junto al elemento)
- Visualizar las líneas de grid numeradas
- Identificar las áreas nombradas en un layout con `grid-template-areas`

---

## 💪 Desempeño (40 puntos)

### Ejercicio 01 — Grid Container (14 puntos)

| Criterio | Puntos |
|----------|--------|
| `display: grid` activo | 3 |
| Columnas con `fr` correctas | 4 |
| `gap` entre celdas | 3 |
| `grid-template-rows` correcta | 4 |

### Ejercicio 02 — Grid Areas (12 puntos)

| Criterio | Puntos |
|----------|--------|
| `grid-template-areas` correcta | 4 |
| Items asignados con `grid-area` | 4 |
| Item que centra con `span` | 4 |

### Ejercicio 03 — Grid Responsive (14 puntos)

| Criterio | Puntos |
|----------|--------|
| `repeat(auto-fit, minmax(...))` funcional | 6 |
| Cards se reorganizan sin media queries | 4 |
| `minmax()` con límites correctos | 4 |

---

## 📦 Producto (30 puntos) — Proyecto AdminGrid

### Descripción
Dashboard de administración con **CSS Grid** como sistema de layout principal. El layout debe usar `grid-template-areas` para la estructura global y `auto-fit` para las grids de contenido.

### Rúbrica del Proyecto

| Criterio | Excelente (100%) | Suficiente (70%) | Insuficiente (<50%) |
|----------|------------------|------------------|---------------------|
| **Layout global (areas)** | `grid-template-areas` correcto con header/sidebar/main/footer | Areas definidas pero con errores menores | Sin `grid-template-areas` |
| **Cards responsive** | `auto-fit` + `minmax()` sin media queries | Responsive con media queries | Sin responsive |
| **Spanning** | Items que ocupan varias celdas (`span`) | Un solo span correcto | Sin span |
| **Custom Properties** | Variables para colores, gaps y breakpoints | Variables parciales | Sin variables |
| **Semántica HTML** | Etiquetas correctas (`<header>`, `<aside>`, `<main>`, `<footer>`) | Semántica parcial | `<div>` sin semántica |

### Puntuación Producto

| Criterio | Puntos |
|----------|--------|
| Layout global con `grid-template-areas` | 10 |
| Cards con `auto-fit` + `minmax()` | 8 |
| Al menos un item con `span` | 4 |
| CSS Custom Properties | 4 |
| HTML semántico correcto | 4 |

---

## ✅ Criterios de Aprobación

- Mínimo **21/30** en conocimiento
- Mínimo **28/40** en desempeño
- Mínimo **21/30** en producto
- Código HTML válido (sin errores W3C)
- Layout funcional en desktop y móvil
