# Rúbrica de Evaluación — Semana 06: Positioning y Float

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
| ¿Cuál es la diferencia entre `position: relative` y `position: absolute`? | 4 |
| ¿Qué es el *containing block* de un elemento `absolute`? | 4 |
| ¿En qué se diferencia `position: fixed` de `position: sticky`? | 4 |
| ¿Cuándo se crea un nuevo *stacking context*? Nombra 3 formas. | 4 |
| ¿Por qué se recomienda no usar `float` para layouts? | 4 |

### Identificación visual en DevTools (10 pts)

| Tarea | Pts |
|-------|-----|
| Localizar el *containing block* de un `absolute` en el panel Elements | 5 |
| Verificar el valor de `z-index` computado de dos elementos superpuestos | 5 |

---

## 💪 Desempeño (40 pts)

### Ejercicio 01 — Position (14 pts)

| Criterio | Pts |
|----------|-----|
| Badge posicionado correctamente sobre la imagen con `absolute` | 4 |
| Header sticky que permanece visible al hacer scroll | 4 |
| Modal overlay centrado con `fixed` y fondo semitransparente | 6 |

### Ejercicio 02 — Z-index (12 pts)

| Criterio | Pts |
|----------|-----|
| Capas apiladas en el orden correcto con `z-index` | 4 |
| Comprende que `z-index` sin `position != static` no tiene efecto | 4 |
| Demuestra un *stacking context* independiente | 4 |

### Ejercicio 03 — Float y clearfix (14 pts)

| Criterio | Pts |
|----------|-----|
| Imagen flotando con texto alrededor usando `float: left/right` | 4 |
| Contenedor que abraza los floats con clearfix o `flow-root` | 6 |
| Transición a `display: flow-root` como solución moderna | 4 |

---

## 📦 Producto — NavLayout (30 pts)

**Proyecto: NavLayout — Navbar sticky + card con badge + modal overlay**

### Nivel 4 — Excelente (27–30 pts)

- Navbar sticky funcional que no desplaza el contenido
- Badge absoluto perfectamente posicionado sobre la imagen de tarjeta
- Modal overlay centrado con `fixed`, fondo semitransparente y contenido centrado
- Uso correcto del *containing block* (el padre tiene `position: relative`)
- Código limpio, variables CSS, comentarios educativos

### Nivel 3 — Bueno (21–26 pts)

- Navbar sticky y badge implementados correctamente
- Modal overlay presente aunque el centrado tenga pequeñas imprecisiones
- Containing block configurado correctamente en la mayoría de casos
- CSS organizado con variables

### Nivel 2 — En desarrollo (15–20 pts)

- Al menos dos de los tres componentes (navbar, badge, modal) funcionan
- Algunos posicionamientos son incorrectos o tienen valores mágicos
- Sin uso de variables CSS

### Nivel 1 — Insuficiente (0–14 pts)

- Solo uno o ningún componente funciona correctamente
- `z-index` usado sin comprensión del contexto
- Código desordenado, sin estructura semántica

---

## 📋 Evidencias requeridas

1. Captura del navbar sticky en scroll
2. Captura del badge sobre la tarjeta
3. Captura del modal overlay activo
4. Enlace al repositorio o archivo ZIP con el código fuente
