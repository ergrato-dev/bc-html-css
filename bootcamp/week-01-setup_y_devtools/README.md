# 🛠️ Semana 1: Setup y DevTools

## 🎯 Objetivos de Aprendizaje

Al finalizar esta semana, serás capaz de:

- ✅ Instalar y configurar VS Code con las extensiones esenciales para desarrollo web
- ✅ Personalizar tu entorno: atajos, snippets y settings óptimos
- ✅ Usar Live Server para ver cambios en tiempo real en el navegador
- ✅ Organizar correctamente la estructura de archivos de un proyecto HTML/CSS
- ✅ Navegar con fluidez por los paneles de DevTools: Elements, Styles, Computed y Console
- ✅ Inspeccionar y editar HTML y CSS directamente desde el navegador
- ✅ Depurar problemas de layout usando DevTools
- ✅ Medir y analizar el rendimiento básico de una página

---

## 📚 Requisitos Previos

- **VS Code** instalado ([Descargar](https://code.visualstudio.com/))
- **Chrome** o **Firefox** (versión reciente, para DevTools)
- **Git** instalado y configurado ([Descargar](https://git-scm.com/))
- Sin conocimientos previos de HTML o CSS — ¡empezamos de cero!

---

## 🗂️ Estructura de la Semana

```
week-01-setup_y_devtools/
├── README.md                        # Este archivo
├── rubrica-evaluacion.md            # Criterios de evaluación
├── 0-assets/                        # Diagramas y recursos visuales
│   ├── vscode-interfaz.svg
│   └── devtools-panels.svg
├── 1-teoria/                        # Material teórico
│   ├── 01-vscode-setup.md
│   ├── 02-live-server-y-estructura.md
│   ├── 03-devtools-elements-y-styles.md
│   └── 04-devtools-computed-y-debug.md
├── 2-practicas/                     # Ejercicios guiados
│   ├── 01-ejercicio-vscode/
│   ├── 02-ejercicio-live-server/
│   ├── 03-ejercicio-devtools-inspect/
│   └── 04-ejercicio-debug-layout/
├── 3-proyecto/                      # Proyecto semanal
│   ├── README.md
│   ├── starter/
│   └── solution/                    # Solo instructores
├── 4-recursos/
│   ├── ebooks-free/
│   ├── videografia/
│   └── webgrafia/
└── 5-glosario/
    └── README.md
```

---

## 📝 Contenidos

### 1️⃣ Teoría (2–2.5 horas)

| Tema | Duración | Descripción |
| ---- | -------- | ----------- |
| [VS Code: Setup y Extensiones](1-teoria/01-vscode-setup.md) | 40 min | Instalar extensiones, atajos clave, configuración recomendada |
| [Live Server y Estructura de Proyecto](1-teoria/02-live-server-y-estructura.md) | 30 min | Recarga automática, organización de archivos HTML/CSS |
| [DevTools: Elements y Styles](1-teoria/03-devtools-elements-y-styles.md) | 40 min | Inspeccionar y editar HTML/CSS en vivo desde el navegador |
| [DevTools: Computed, Console y Debug](1-teoria/04-devtools-computed-y-debug.md) | 30 min | Panel Computed, depurar layouts, medir rendimiento |

### 2️⃣ Prácticas (3.5–4 horas)

| Ejercicio | Duración | Nivel | Objetivo |
| --------- | -------- | ----- | -------- |
| [Configurar VS Code](2-practicas/01-ejercicio-vscode/) | 45 min | Básico | Instalar y personalizar el entorno de trabajo |
| [Primera página con Live Server](2-practicas/02-ejercicio-live-server/) | 60 min | Básico | Crear proyecto y ver cambios en tiempo real |
| [Inspeccionar y Editar con DevTools](2-practicas/03-ejercicio-devtools-inspect/) | 60 min | Básico | Modificar HTML y CSS directamente en el navegador |
| [Depurar un Layout con DevTools](2-practicas/04-ejercicio-debug-layout/) | 60 min | Básico | Identificar y corregir problemas de maquetado |

### 3️⃣ Proyecto (1.5–2 horas)

**Mi Página de Presentación**

Construir una página web personal sencilla que demuestre el dominio del entorno:
- Estructura HTML básica bien formada
- CSS aplicado desde archivo externo
- Desarrollada completamente con VS Code + Live Server
- Validada e inspeccionada con DevTools

---

## ⏱️ Distribución del Tiempo (8 horas)

```
📖 Teoría:     2–2.5h  (25–31%)
💻 Prácticas:  3.5–4h  (44–50%)
🚀 Proyecto:   1.5–2h  (19–25%)
```

### Cronograma Sugerido

| Sesión | Actividad | Tiempo |
| ------ | --------- | ------ |
| **Sesión 1** | Teoría: VS Code + Live Server | 1.5h |
| **Sesión 2** | Práctica 1 + Práctica 2 | 1.75h |
| **Sesión 3** | Teoría: DevTools (paneles) | 1.5h |
| **Sesión 4** | Práctica 3 + Práctica 4 | 2h |
| **Sesión 5** | Proyecto final | 1.5h |

---

## 📌 Entregable

**Proyecto: [Mi Página de Presentación](3-proyecto/)**

Una página web personal con:

- [ ] Estructura HTML válida (DOCTYPE, `<html>`, `<head>`, `<body>`)
- [ ] CSS en archivo externo (`css/styles.css`) vinculado correctamente
- [ ] Al menos un encabezado, párrafo e imagen
- [ ] Inspeccionada con DevTools (sin errores en consola)
- [ ] Desarrollada con VS Code + Live Server

---

## 🎓 Conceptos Clave

- **VS Code**: Editor de código fuente gratuito y de código abierto de Microsoft
- **Extensión**: Plugin que agrega funcionalidad a VS Code
- **Live Server**: Extensión que recarga el navegador automáticamente al guardar
- **DevTools**: Herramientas del desarrollador integradas en el navegador
- **Panel Elements**: Vista del árbol DOM del documento HTML
- **Panel Styles**: Reglas CSS aplicadas al elemento seleccionado
- **Panel Computed**: Valores CSS finales calculados tras la cascada
- **Panel Console**: Mensajes, errores y ejecución de JavaScript en tiempo real
- **DOM** (Document Object Model): Representación del HTML como árbol de nodos
- **Inspector**: Herramienta para seleccionar y examinar elementos en la página

---

## ✅ Checklist de Verificación

Antes de pasar a la Semana 2, asegúrate de:

- [ ] VS Code instalado con Live Server, Prettier y las extensiones recomendadas
- [ ] Puedes abrir un proyecto y ver cambios en tiempo real con Live Server
- [ ] Conoces la estructura de carpetas de un proyecto HTML/CSS básico
- [ ] Puedes abrir DevTools con `F12` o `Ctrl+Shift+I`
- [ ] Sabes seleccionar un elemento en la página y ver su HTML en el panel Elements
- [ ] Sabes modificar CSS en el panel Styles y ver el resultado al instante
- [ ] Entiendes la diferencia entre el panel Styles y el panel Computed
- [ ] Puedes identificar errores en el panel Console
- [ ] Completaste todos los ejercicios prácticos
- [ ] Entregaste el proyecto funcional
- [ ] Alcanzaste mínimo 70% en cada tipo de evidencia

---

## 🔗 Navegación

⬅️ **Anterior**: [Inicio del Bootcamp](../../README.md)  
➡️ **Siguiente**: [Semana 2: HTML Fundamentos](../week-02-html_fundamentos/README.md)

---

## 💡 Consejos para Esta Semana

> 💡 **DevTools es tu mejor amigo**: Más del 80% del tiempo de debugging en frontend se hace con DevTools. Aprenderlo bien desde el inicio te ahorrará horas.

> 🎯 **Live Server desde el minuto 1**: Nunca abras el HTML con doble clic. Siempre usa Live Server — simula un servidor real y evita problemas con rutas de archivos.

> 🔍 **Inspect antes de escribir**: Cuando algo no se ve como quieres, primero inspecciona con DevTools antes de cambiar el código.

> 🤝 **Experimenta sin miedo**: Los cambios que hagas en DevTools son temporales — al recargar, se borran. Es el lugar perfecto para probar ideas.

---

<p align="center">
  <strong>¡Bienvenido al Bootcamp HTML + CSS! 🎉</strong><br>
  <em>Esta semana sentarás las bases de tu entorno de trabajo</em>
</p>

<p align="center">
  <a href="1-teoria/01-vscode-setup.md">📖 Comenzar con Teoría</a> •
  <a href="2-practicas/">💻 Ir a Prácticas</a> •
  <a href="3-proyecto/">🚀 Ver Proyecto</a>
</p>
