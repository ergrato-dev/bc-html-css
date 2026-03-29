# 📊 Rúbrica de Evaluación — Semana 1

## Setup y DevTools

---

## 🎯 Competencias a Evaluar

| Competencia | Descripción |
| ----------- | ----------- |
| **C1** | Configurar VS Code con extensiones y settings óptimos para HTML/CSS |
| **C2** | Usar Live Server y organizar la estructura de un proyecto web |
| **C3** | Navegar e inspeccionar elementos con DevTools (Elements + Styles) |
| **C4** | Depurar layouts y analizar estilos con DevTools (Computed + Console) |

---

## 🧠 Conocimiento (30%)

### Cuestionario Teórico (20%)

| Criterio | Excelente (100%) | Bueno (80%) | Suficiente (70%) | Insuficiente (<70%) |
| -------- | ---------------- | ----------- | ---------------- | ------------------- |
| **VS Code** | Explica extensiones, atajos y settings; justifica cada elección | Conoce extensiones y atajos principales | Conoce Live Server y una extensión más | No conoce el entorno |
| **Live Server** | Explica recarga automática, diferencia con apertura directa, rutas | Entiende su función y cómo activarlo | Sabe instalar y abrir con Live Server | No sabe usarlo |
| **DevTools: Elements/Styles** | Explica DOM, box model visual, selector de elementos, cascada en Styles | Entiende inspección básica y edición de estilos | Sabe abrir DevTools y seleccionar elementos | No maneja DevTools |
| **DevTools: Computed/Console** | Explica valores computados, diferencia con Styles, errores en Console | Entiende panel Computed y mensajes de consola | Sabe que existe el panel Computed | No conoce estos paneles |

### Identificación en Pantalla (10%)

| Criterio | Puntos |
| -------- | ------ |
| Identifica correctamente los 4 paneles de DevTools en una captura | 100% |
| Identifica 3 de 4 paneles | 80% |
| Identifica 2 de 4 paneles | 70% |
| Identifica menos de 2 paneles | <70% |

---

## 💪 Desempeño (40%)

### Ejercicios Prácticos

| Ejercicio | Peso | Criterios de Evaluación |
| --------- | ---- | ----------------------- |
| **Configurar VS Code** | 10% | Extensiones instaladas, settings aplicados, Live Server funciona |
| **Primera página con Live Server** | 10% | Proyecto con estructura correcta, recarga automática activa |
| **Inspeccionar y Editar con DevTools** | 10% | Modifica HTML y CSS en DevTools, entiende los cambios temporales |
| **Depurar Layout con DevTools** | 10% | Identifica y describe los problemas de maquetado encontrados |

### Criterios por Ejercicio

| Nivel | Descripción | Porcentaje |
| ----- | ----------- | ---------- |
| **Excelente** | Completa el ejercicio, explica lo que hace en comentarios, va más allá | 100% |
| **Bueno** | Completa todos los pasos del ejercicio correctamente | 80% |
| **Suficiente** | Completa los pasos esenciales con algún error menor | 70% |
| **Insuficiente** | Incompleto o con errores que impiden el funcionamiento | <70% |

---

## 📦 Producto (30%)

### Proyecto: Mi Página de Presentación

| Criterio | Peso | Excelente (100%) | Bueno (80%) | Suficiente (70%) | Insuficiente (<70%) |
| -------- | ---- | ---------------- | ----------- | ---------------- | ------------------- |
| **Estructura HTML** | 8% | DOCTYPE, `<html lang>`, `<head>` completo, `<body>` semántico | Estructura válida con `<head>` y `<body>` | Estructura básica funcional | HTML inválido o incompleto |
| **CSS externo** | 8% | Archivo CSS vinculado, reglas organizadas con comentarios | CSS vinculado y funcionando | CSS vinculado aunque mínimo | CSS inline o ausente |
| **Contenido** | 5% | Encabezado, párrafo, imagen con `alt`, lista — todo con sentido | Encabezado, párrafo e imagen | Encabezado y párrafo | Solo texto sin estructura |
| **Sin errores en Console** | 5% | Sin errores ni advertencias en la consola del navegador | Sin errores (puede haber warnings) | Un error de recurso menor | Múltiples errores |
| **Uso del entorno** | 4% | Evidencia de uso de Live Server y revisión con DevTools | Usa Live Server correctamente | Abre con Live Server | No usa Live Server |

---

## 📋 Checklist de Entrega

### Estructura Esperada del Proyecto

```
mi-pagina-presentacion/
├── index.html
├── css/
│   └── styles.css
├── assets/
│   └── images/
│       └── (imagen de perfil u otra)
└── README.md
```

### Requisitos Mínimos

- [ ] `index.html` con DOCTYPE y estructura `<html>`, `<head>`, `<body>`
- [ ] `<meta charset="UTF-8">` y `<meta name="viewport">` en `<head>`
- [ ] `<title>` descriptivo en `<head>`
- [ ] CSS en archivo externo vinculado con `<link>`
- [ ] Al menos un `<h1>`, un `<p>` y un `<img>` con atributo `alt`
- [ ] Sin errores en la consola del navegador
- [ ] Proyecto revisado con DevTools antes de entregar

---

## 🏆 Escala de Calificación

| Calificación | Rango | Descripción |
| ------------ | ----- | ----------- |
| **Sobresaliente** | 90–100% | Supera expectativas; entorno perfectamente configurado y documentado |
| **Notable** | 80–89% | Cumple todos los requisitos correctamente |
| **Aprobado** | 70–79% | Cumple los requisitos mínimos |
| **No Aprobado** | <70% | No cumple los requisitos mínimos |

---

## ⚠️ Criterios de No Aprobación Automática

- Proyecto que no abre en el navegador
- Plagio detectado
- Entrega fuera de plazo sin justificación
- CSS incrustado en `<style>` o en atributos `style=""` en lugar de archivo externo
- Sin evidencia de uso de DevTools

---

## 📝 Formato de Entrega

1. **Repositorio**: Fork del bootcamp o repositorio personal
2. **Branch**: `week-01-proyecto`
3. **Commit message**: `feat(week-01): complete mi-pagina-presentacion project`
4. **Fecha límite**: Según el calendario del bootcamp

---

## 🔄 Retroalimentación

Después de la evaluación recibirás:

- ✅ Puntuación por cada criterio
- 💬 Comentarios específicos sobre el HTML y CSS
- 📈 Sugerencias de mejora para la siguiente semana
- 🎯 Puntos fuertes identificados
