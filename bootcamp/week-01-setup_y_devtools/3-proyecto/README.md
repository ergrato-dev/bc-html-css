# Proyecto Semana 01 — Mi Página de Presentación

## Descripción

En este proyecto crearás tu **primera página web personal**: una presentación simple
con tu nombre, una breve bio y links a tus redes o proyectos.

El objetivo es aplicar todo lo visto en la semana: estructura HTML5 semántica,
vinculación de CSS externo, uso de Live Server y DevTools para iterar.

---

## 🎯 Objetivos

Al completar este proyecto serás capaz de:

- Crear un proyecto web con estructura de carpetas correcta
- Escribir HTML5 semántico con etiquetas `<header>`, `<main>`, `<footer>`
- Vincular un CSS externo y ver los cambios en vivo con Live Server
- Usar DevTools para inspeccionar y ajustar estilos

---

## 📋 Requisitos del proyecto

### HTML (`index.html`)

- [ ] DOCTYPE, `<html lang="es">`, `<meta charset>`, `<meta viewport>`, `<title>`
- [ ] `<header>` con tu nombre en un `<h1>` y tu título profesional en un `<p>`
- [ ] `<main>` con al menos dos secciones semánticas (`<section>`)
- [ ] Una sección "Sobre mí" con `<h2>` y un párrafo de presentación
- [ ] Una sección "Mis habilidades" con una lista `<ul>` de al menos 3 items
- [ ] Al menos un enlace `<a>` con `href` real (GitHub, LinkedIn, correo, etc.)
- [ ] `<footer>` con tu nombre y el año

### CSS (`css/styles.css`)

- [ ] Variables CSS en `:root` para colores y espaciados
- [ ] Reset mínimo con `box-sizing: border-box`
- [ ] Estilos para `body`, `header`, `main`, `footer`
- [ ] Al menos un estado `:hover` en algún elemento interactivo
- [ ] Sin errores en el [Validador CSS W3C](https://jigsaw.w3.org/css-validator/)

### Calidad

- [ ] Sin errores en el [Validador HTML W3C](https://validator.w3.org/)
- [ ] Sin errores en la Console de DevTools (sin 404)
- [ ] La página se ve bien en el navegador abierta con Live Server

---

## 📁 Estructura esperada de entrega

```
starter/
├── index.html
├── css/
│   └── styles.css
└── assets/
    └── images/
        └── (imagen de perfil o placeholder)
```

---

## 🚀 Instrucciones

1. Trabaja dentro de la carpeta `starter/`
2. Abre VS Code apuntando a `starter/` como carpeta raíz
3. Activa Live Server haciendo clic en `⚡ Go Live`
4. Implementa los TODOs en `index.html` y `css/styles.css`
5. Usa DevTools para inspeccionar y ajustar estilos en vivo
6. Valida tu HTML en [https://validator.w3.org/](https://validator.w3.org/)

---

## 📊 Criterios de evaluación

| Criterio | Puntos |
| -------- | ------ |
| Estructura HTML5 semántica completa | 30 |
| CSS con Custom Properties y estilos aplicados | 30 |
| Sin errores en W3C Validator (HTML y CSS) | 20 |
| Sin errores 404 en la Console de DevTools | 10 |
| Buena presentación visual (legible, organizado) | 10 |
| **Total** | **100** |

---

## 💡 Tips

- Empieza por el HTML completo antes de tocar el CSS
- Usa Emmet: `!` + `Tab` genera la plantilla HTML5 en segundos
- Para el color: elige una paleta de 2-3 colores y defínela como variables en `:root`
- Inspecciona páginas reales con DevTools para ver cómo están construidas

---

> 🔗 Recursos útiles:
> - [MDN — Etiquetas HTML semánticas](https://developer.mozilla.org/es/docs/Glossary/Semantics#semántica_en_html)
> - [W3C HTML Validator](https://validator.w3.org/)
> - [W3C CSS Validator](https://jigsaw.w3.org/css-validator/)
