# Rúbrica de Evaluación — Semana 09

## Responsive & Media Queries

**Puntaje total: 100 pts** · Mínimo para aprobar: 70 pts

---

## 🧠 Conocimiento (30%) — 30 pts

### Cuestionario teórico (20 pts)

| # | Pregunta | Pts |
|---|----------|-----|
| 1 | ¿Qué significa Mobile-first y por qué es preferible a Desktop-first? | 4 |
| 2 | ¿Cuál es la diferencia entre `rem` y `em`? Da un ejemplo de cuándo usar cada uno | 4 |
| 3 | ¿Cuándo usar `vw`/`vh` y cuándo usar `%`? ¿En qué se diferencian? | 4 |
| 4 | Explica `clamp(min, val, max)`. ¿Para qué se usa en tipografía responsiva? | 4 |
| 5 | ¿Por qué se usa `@media (min-width)` en Mobile-first en vez de `@media (max-width)`? | 4 |

### DevTools responsive (10 pts)

| Acción | Pts |
|--------|-----|
| Activar Device Toolbar y simular iPhone SE (375px) | 3 |
| Cambiar viewport manualmente a 768px e identificar qué media query aplica | 4 |
| Usar la regla "responsive" arrastrando para encontrar el breakpoint de quiebre | 3 |

---

## 💪 Desempeño (40%) — 40 pts

### Ejercicio 01 — Mobile-first (14 pts)

| Criterio | Pts |
|----------|-----|
| Estilos base correctos para móvil sin media queries | 4 |
| `@media (min-width: 768px)` aplica estilos tablet correctamente | 5 |
| `@media (min-width: 1024px)` aplica estilos desktop correctamente | 5 |

### Ejercicio 02 — Unidades relativas (12 pts)

| Criterio | Pts |
|----------|-----|
| `rem` aplicado a tipografía y espaciados | 4 |
| `vw`/`vh` aplicado a elementos de viewport | 4 |
| `clamp()` implementado para tipografía fluida | 4 |

### Ejercicio 03 — Breakpoints con Grid/Flex (14 pts)

| Criterio | Pts |
|----------|-----|
| Grid de 1 columna en mobile → 2 en tablet → 3+ en desktop | 6 |
| Navegación horizontal → vertical en mobile con Flexbox | 4 |
| Sin scroll horizontal en ningún breakpoint probado | 4 |

---

## 📦 Producto (30%) — 30 pts

### Responsive Landing Page

| Criterio | Pts |
|----------|-----|
| Layout mobile (320px–767px): 1 columna, legible, sin desbordamiento | 8 |
| Layout tablet (768px–1023px): adaptación correcta de grid y navegación | 8 |
| Layout desktop (1024px+): uso completo del espacio horizontal | 6 |
| Tipografía fluida con `rem` o `clamp()` | 4 |
| Sin `px` fijos en tipografía ni espaciados principales | 4 |

---

## ⚠️ Penalizaciones

| Infracción | Penalización |
|------------|--------------|
| Scroll horizontal en cualquier viewport | −5 pts |
| `@media (max-width)` en lugar de mobile-first | −3 pts por ocurrencia |
| Uso de `px` en tipografía | −2 pts |
| HTML no válido (errores W3C) | −5 pts |
