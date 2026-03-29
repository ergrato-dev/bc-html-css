# 🤝 Guía de Contribución

¡Gracias por tu interés en contribuir al **Bootcamp HTML + CSS — Zero to Hero**! Este documento proporciona las pautas para contribuir al proyecto.

## 📋 Tabla de Contenidos

- [Código de Conducta](#código-de-conducta)
- [¿Cómo Puedo Contribuir?](#cómo-puedo-contribuir)
- [Configuración del Entorno](#configuración-del-entorno)
- [Flujo de Trabajo](#flujo-de-trabajo)
- [Convenciones de Código](#convenciones-de-código)
- [Commits](#commits)
- [Pull Requests](#pull-requests)

---

## 📜 Código de Conducta

Este proyecto se adhiere al [Código de Conducta](CODE_OF_CONDUCT.md). Al participar, se espera que respetes este código. Por favor, reporta comportamientos inaceptables.

---

## 🎯 ¿Cómo Puedo Contribuir?

### 🐛 Reportar Bugs

Si encuentras un error, por favor abre un [Issue](https://github.com/ergrato-dev/bc-html-css/issues/new?template=bug_report.md) incluyendo:

- Descripción clara del problema
- Pasos para reproducirlo
- Comportamiento esperado vs actual
- Screenshots o capturas de DevTools si aplica
- Información del entorno (OS, navegador y versión, VS Code versión)

### 💡 Sugerir Mejoras

Las sugerencias son bienvenidas. Abre un [Issue](https://github.com/ergrato-dev/bc-html-css/issues/new?template=feature_request.md) describiendo:

- El problema que resuelve
- La solución propuesta
- Alternativas consideradas
- Contexto adicional

### 📚 Mejorar Documentación

- Correcciones ortográficas o gramaticales
- Clarificación de explicaciones conceptuales
- Nuevos ejemplos de código HTML/CSS
- Mejoras en ejercicios de práctica
- Traducciones al inglés

### ✨ Contribuir Contenido

- Nuevos ejercicios o prácticas guiadas
- Mejoras en el código HTML/CSS existente
- Recursos visuales (diagramas SVG en tema dark)
- Recursos adicionales (ebooks, videos, webgrafía)
- Mejoras al glosario de términos

---

## ⚙️ Configuración del Entorno

### Prerrequisitos

- [VS Code](https://code.visualstudio.com/) con la extensión [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- Git
- Navegador moderno: Chrome, Firefox o Edge (para DevTools)

> ℹ️ Este bootcamp **no requiere** Node.js, npm, Docker ni ningún build tool. Solo HTML, CSS y un editor de texto.

### Setup

```bash
# 1. Fork del repositorio en GitHub

# 2. Clonar tu fork
git clone https://github.com/TU-USUARIO/bc-html-css.git
cd bc-html-css

# 3. Agregar upstream
git remote add upstream https://github.com/ergrato-dev/bc-html-css.git

# 4. Abrir en VS Code
code .
```

### Verificar la Instalación

1. Abre cualquier archivo `index.html` de `bootcamp/`
2. Haz clic en **"Go Live"** en la barra de estado de VS Code (Live Server)
3. El archivo debe abrirse en el navegador con recarga automática

---

## 🔄 Flujo de Trabajo

### 1. Sincronizar con upstream

```bash
git fetch upstream
git checkout main
git merge upstream/main
```

### 2. Crear una rama

```bash
# Para nuevas funcionalidades o contenido
git checkout -b feature/nombre-descriptivo

# Para correcciones
git checkout -b fix/descripcion-del-problema

# Para documentación
git checkout -b docs/que-se-documenta
```

### 3. Hacer cambios

- Sigue las [convenciones de código](#convenciones-de-código)
- Valida tu HTML en [W3C Validator](https://validator.w3.org/)
- Verifica que el CSS funcione en Chrome, Firefox y Edge
- Actualiza la documentación si es necesario

### 4. Commit y Push

```bash
git add .
git commit -m "tipo(scope): descripción breve"
git push origin nombre-de-tu-rama
```

### 5. Crear Pull Request

- Ve a GitHub y crea un PR hacia `main`
- Completa la plantilla del PR
- Espera la revisión

---

## 📝 Convenciones de Código

### HTML

```html
<!-- ✅ CORRECTO — semántico, accesible, lang en inglés del código -->
<header role="banner">
  <nav aria-label="Main navigation">
    <ul>
      <li><a href="#about">About</a></li>
    </ul>
  </nav>
</header>

<!-- ❌ INCORRECTO — divitis, sin semántica -->
<div class="header">
  <div class="nav">
    <div class="item"><a href="#about">About</a></div>
  </div>
</div>
```

### CSS

```css
/* ✅ CORRECTO — Custom Properties, Mobile-first, unidades relativas */
:root {
  --color-primary: #3b82f6;
  --spacing-md: 1.5rem;
}

.card {
  padding: var(--spacing-md);
}

@media (min-width: 768px) {
  .card {
    padding: calc(var(--spacing-md) * 1.5);
  }
}

/* ❌ INCORRECTO — valores mágicos, desktop-first */
.card {
  padding: 24px;
}

@media (max-width: 768px) {
  .card {
    padding: 16px;
  }
}
```

### Reglas Generales

| Elemento          | Convención                              |
| ----------------- | --------------------------------------- |
| Clases CSS        | `kebab-case` (`.nav-item`, `.btn-primary`) |
| IDs HTML          | `kebab-case`, solo anchors/accesibilidad |
| Archivos          | `kebab-case` (`index.html`, `styles.css`) |
| Carpetas          | `kebab-case` (`2-practicas/`, `0-assets/`) |
| Código            | **Inglés** (clases, IDs, nombres de archivo) |
| Documentación     | **Español** (READMEs, teoría, guías) |
| Comentarios educativos | **Español** (explican conceptos) |

### Assets SVG

- **Formato**: SVG preferido para todos los diagramas e iconos
- **Tema**: Dark mode (`#0d1117` de fondo)
- **Sin degradés** (gradients)
- **Fuentes**: Sans-serif únicamente (Inter, Roboto, System UI)
- Vinculados en archivos de teoría: `![Descripción](../0-assets/nombre.svg)`

---

## 💬 Commits

Usamos [Conventional Commits](https://www.conventionalcommits.org/):

```
tipo(scope): descripción breve

¿Qué se hizo?
¿Para qué / por qué?
¿Cuál es el impacto?
```

### Tipos Permitidos

| Tipo       | Descripción                            |
| ---------- | -------------------------------------- |
| `feat`     | Nuevo contenido o funcionalidad        |
| `fix`      | Corrección de error                    |
| `docs`     | Solo documentación                     |
| `style`    | Formato (no afecta el código)          |
| `refactor` | Refactorización sin cambio funcional   |
| `chore`    | Tareas de mantenimiento                |

### Ejemplos

```bash
feat(week-03): add form validation exercises
fix(week-07): correct flexbox axis diagram labels
docs(readme): update quick start section
chore(assets): optimize SVG file sizes
```

---

## 🔀 Pull Requests

### Checklist

Antes de crear un PR, asegúrate de:

- [ ] El HTML valida sin errores en [W3C Validator](https://validator.w3.org/)
- [ ] El CSS funciona en Chrome, Firefox y Edge
- [ ] Sigue las convenciones de nomenclatura del proyecto
- [ ] La documentación está en español (excepto el código)
- [ ] Los commits siguen Conventional Commits
- [ ] Has probado los cambios con Live Server
- [ ] Los assets SVG usan tema dark sin gradients
- [ ] No hay conflictos con `main`

### Plantilla

Al crear un PR, completa la plantilla proporcionada:

- **Descripción**: ¿Qué hace este PR?
- **Tipo de cambio**: `feat` / `fix` / `docs` / etc.
- **Testing**: ¿En qué navegadores se probó?
- **Screenshots**: Si hay cambios visuales
- **Issues relacionados**: `Closes #123`

### Revisión

- Al menos 1 aprobación requerida
- El HTML debe validar en W3C
- Sin conflictos de merge

---

## ❓ ¿Preguntas?

- 💬 [GitHub Discussions](https://github.com/ergrato-dev/bc-html-css/discussions)
- 🐛 [GitHub Issues](https://github.com/ergrato-dev/bc-html-css/issues)

---

¡Gracias por contribuir! 🚀
