# Semana 02 — HTML Fundamentos

## 🎯 Objetivos de aprendizaje

Al terminar esta semana serás capaz de:

- Escribir la estructura base de cualquier documento HTML5
- Distinguir entre etiquetas semánticas y genéricas
- Jerarquizar correctamente los headings (h1→h6)
- Crear listas ordenadas, no ordenadas y de descripción
- Insertar enlaces con rutas relativas y absolutas
- Incluir imágenes con atributos de accesibilidad correctos

## 📚 Requisitos previos

- Semana 01 completada (VS Code + Live Server funcionando)

## 🗂️ Estructura de la semana

```
week-02-html_fundamentos/
├── 0-assets/               ← diagramas SVG de apoyo
├── 1-teoria/
│   ├── 01-estructura-html.md
│   ├── 02-textos-y-listas.md
│   └── 03-enlaces-e-imagenes.md
├── 2-practicas/
│   ├── 01-ejercicio-estructura/
│   ├── 02-ejercicio-semantica/
│   └── 03-ejercicio-contenido/
├── 3-proyecto/             ← "Mi CV en HTML"
├── 4-recursos/
└── 5-glosario/
```

## 📝 Contenidos

| # | Archivo | Tema |
|---|---------|------|
| 1 | `01-estructura-html.md` | DOCTYPE, head/body, etiquetas semánticas |
| 2 | `02-textos-y-listas.md` | Headings, párrafos, strong/em, listas |
| 3 | `03-enlaces-e-imagenes.md` | a, img, rutas relativas, figure |

## ⏱️ Distribución del tiempo (8 horas)

| Actividad | Tiempo |
|-----------|--------|
| Teoría (3 archivos) | 2 h |
| Prácticas (3 ejercicios) | 3.5 h |
| Proyecto "Mi CV en HTML" | 2 h |
| Revisión y validación W3C | 0.5 h |

## 📌 Entregables

- [ ] Los 3 ejercicios de prácticas funcionan en el navegador
- [ ] El proyecto "Mi CV en HTML" validado en W3C sin errores
- [ ] HTML semántico: sin `<div>` donde exista etiqueta semántica

## 🎓 Conceptos clave

`DOCTYPE` · `<html lang>` · `<head>` · `<meta>` · `<header>` · `<main>` · `<footer>` · `<nav>` · `<section>` · `<article>` · `heading hierarchy` · `<ul>` · `<ol>` · `<a>` · `<img>` · `alt` · rutas relativas

## ✅ Checklist de verificación

- [ ] El documento comienza con `<!DOCTYPE html>`
- [ ] `<html>` tiene atributo `lang="es"`
- [ ] `<head>` incluye charset, viewport y title
- [ ] Solo un `<h1>` por página
- [ ] Headings en orden jerárquico (no salta de h2 a h4)
- [ ] Toda `<img>` tiene atributo `alt`
- [ ] Los `<a>` externos tienen `rel="noopener noreferrer"`
- [ ] Sin errores en [validator.w3.org](https://validator.w3.org)

## 🔗 Navegación

← [Semana 01 — Setup y DevTools](../week-01-setup_y_devtools/README.md) | [Semana 03 — HTML Formularios y Multimedia](../week-03-html_formularios_y_multimedia/README.md) →
