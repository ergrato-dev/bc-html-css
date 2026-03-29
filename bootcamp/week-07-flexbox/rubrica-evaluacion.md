# Rúbrica de Evaluación — Semana 07: Flexbox

## 📊 Distribución de la evaluación

| Tipo | Porcentaje | Puntos |
|------|-----------|--------|
| 🧠 Conocimiento | 30% | 30 pts |
| 💪 Desempeño | 40% | 40 pts |
| 📦 Producto | 30% | 30 pts |
| **Total** | **100%** | **100 pts** |

> **Mínimo para aprobar:** 70 pts globales con al menos 21/30 en cada categoría.

---

## 🧠 Conocimiento (30 pts)

### Cuestionario teórico (20 pts)

| Pregunta | Pts |
|----------|-----|
| ¿Cuál es la diferencia entre el eje principal y el eje cruzado de un flex container? | 4 |
| ¿Qué hace `justify-content: space-between`? ¿En qué eje actúa? | 4 |
| Explica la diferencia entre `align-items` y `align-self` | 4 |
| ¿Qué significa `flex: 1 1 200px`? Explica cada valor. | 4 |
| ¿Por qué se prefiere `gap` sobre `margin` en flex containers? | 4 |

### Identificación en DevTools (10 pts)

| Tarea | Pts |
|-------|-----|
| Abrir el panel de Flexbox en DevTools y leer los valores actuales de `justify-content` | 5 |
| Modificar `flex-basis` en tiempo real desde el panel Computed | 5 |

---

## 💪 Desempeño (40 pts)

### Ejercicio 01 — Flex Container (14 pts)

| Criterio | Pts |
|----------|-----|
| Cambia la dirección con `flex-direction: column` y observa el cambio de ejes | 4 |
| Usa `justify-content` para distribuir 5 valores distintos | 5 |
| Aplica `flex-wrap: wrap` con un `gap` adecuado | 5 |

### Ejercicio 02 — Flex Items (12 pts)

| Criterio | Pts |
|----------|-----|
| Usa `flex-grow` para que un item ocupe el espacio restante | 4 |
| Aplica `align-self` para alinear un item de forma independiente | 4 |
| Usa `order` para reordenar visualmente sin cambiar el HTML | 4 |

### Ejercicio 03 — Patrones (14 pts)

| Criterio | Pts |
|----------|-----|
| Navbar con logo a la izquierda y nav a la derecha | 5 |
| Elemento centrado perfectamente con `justify-content + align-items` | 4 |
| Layout sidebar + main con proporciones controladas | 5 |

---

## 📦 Producto — FlexDash (30 pts)

**Proyecto: FlexDash — Dashboard con Flexbox**

### Nivel 4 — Excelente (27–30 pts)

- Navbar sticky con logo y links (Flexbox)
- Layout principal: sidebar fijo (240px) + area de contenido que crece (`flex: 1`)
- Grid de tarjetas con `flex-wrap: wrap` y `flex: 1 1 220px`
- Tarjetas con altura uniforme usando `align-items: stretch`
- Footer centrado
- Variables CSS, código semántico, sin valores mágicos

### Nivel 3 — Bueno (21–26 pts)

- Navbar y layout sidebar + main implementados
- Cards con wrap aunque sin flex-basis controlado
- Pequeñas inconsistencias en alineación

### Nivel 2 — En desarrollo (15–20 pts)

- Solo el navbar o el layout sidebar implementados
- Items sin `gap`, usando margin individual

### Nivel 1 — Insuficiente (0–14 pts)

- Flexbox aplicado incorrectamente o sin comprensión de los ejes
- Sin estructura semántica

---

## 📋 Evidencias requeridas

1. Captura del navbar (logo izquierda, links derecha)
2. Captura del layout sidebar + main
3. Captura del grid de tarjetas en distintos anchos (responsive)
4. Enlace al repo o ZIP del proyecto
