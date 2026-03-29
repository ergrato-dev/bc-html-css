# Rúbrica de Evaluación — Semana 03: HTML Formularios y Multimedia

## 📊 Distribución de puntos

| Tipo de evidencia | Porcentaje | Puntos |
|-------------------|------------|--------|
| 🧠 Conocimiento | 30% | 30 pts |
| 💪 Desempeño | 40% | 40 pts |
| 📦 Producto | 30% | 30 pts |
| **Total** | **100%** | **100 pts** |

---

## 🧠 Conocimiento (30 pts)

### Cuestionario teórico (20 pts)

| # | Pregunta | Pts |
|---|----------|-----|
| 1 | ¿Cuál es la diferencia entre `<input type="submit">` y `<button type="submit">`? | 3 |
| 2 | ¿Por qué es obligatorio asociar `<label>` con `<input>` usando `for`/`id`? | 3 |
| 3 | ¿Cuándo se usa `<fieldset>` y `<legend>`? | 2 |
| 4 | ¿Qué diferencia hay entre `<th>` y `<td>`? ¿Qué es `scope`? | 3 |
| 5 | ¿Cuál es la diferencia entre `colspan` y `rowspan`? | 2 |
| 6 | ¿Por qué `<iframe>` necesita el atributo `title`? | 3 |
| 7 | ¿Qué hace el atributo `required` en un formulario HTML? | 2 |
| 8 | ¿Para qué sirve el elemento `<source>` dentro de `<video>` o `<audio>`? | 2 |

### Identificación visual (10 pts)

El instructor mostrará HTML de formularios o tablas con errores de accesibilidad o semántica. El estudiante deberá identificarlos y proponer la corrección.

---

## 💪 Desempeño (40 pts)

### Ejercicio 01 — Formulario de contacto (14 pts)

| Criterio | Pts |
|----------|-----|
| Estructura correcta con `<form>`, `action` y `method` | 3 |
| Todos los campos con `<label>` asociado (for/id) | 4 |
| Tipos de input correctos (email, tel, text, textarea) | 4 |
| `required` y validación básica presente | 3 |

### Ejercicio 02 — Tabla de horarios (12 pts)

| Criterio | Pts |
|----------|-----|
| Estructura completa: `<thead>`, `<tbody>`, `<tfoot>` | 4 |
| `<th scope="col">` en encabezados de columna | 4 |
| Uso correcto de `colspan` o `rowspan` | 4 |

### Ejercicio 03 — Galería multimedia (14 pts)

| Criterio | Pts |
|----------|-----|
| Imágenes con `alt` descriptivo y dentro de `<figure>` | 4 |
| Video con atributos `controls` y texto alternativo | 4 |
| Audio con `controls` y fuente correcta | 3 |
| iframe con `title` y `loading="lazy"` | 3 |

---

## 📦 Producto (30 pts) — Formulario de Registro con Multimedia

| Criterio | Nivel 4 (Excelente) | Nivel 3 (Bien) | Nivel 2 (Regular) | Nivel 1 (Insuficiente) | Pts máx |
|----------|---------------------|----------------|-------------------|------------------------|---------|
| Estructura del formulario | Secciones con fieldset/legend, todos los campos con label | Labelsy tipos correctos, sin fieldset | Labels presentes pero sin asociar | Sin labels | 10 |
| Validación HTML5 | required, pattern, minlength/maxlength en todos los campos relevantes | required en la mayoría | Solo en algunos campos | Sin validación | 8 |
| Tabla de tarifas | Thead/tbody/tfoot, th con scope, colspan correcto | Thead/tbody presentes | Solo estructura básica | Sin semántica de tabla | 6 |
| Multimedia | Video + audio con controls + fallback, iframe con title | Video o audio presentes | Solo imágenes | Sin multimedia | 6 |
