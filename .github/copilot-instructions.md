# 🤖 Instrucciones para GitHub Copilot

## 📋 Contexto del Bootcamp

Este es un Bootcamp de HTML + CSS Zero to Hero estructurado para llevar a estudiantes de cero a héroe en el desarrollo de interfaces web modernas, semánticas y accesibles.

### 📊 Datos del Bootcamp

- **Duración:** 13 semanas (~3 meses)
- **Dedicación semanal:** 8 horas
- **Total de horas:** ~104 horas
- **Nivel de salida:** Frontend Developer Junior (HTML + CSS)
- **Enfoque:** HTML5 semántico + CSS3 moderno, sin frameworks (Tailwind cubierto en bootcamp aparte)
- **Stack:** HTML5, CSS3, CSS Custom Properties, Flexbox, Grid, DevTools del navegador, VS Code + Live Server

---

## 🎯 Objetivos de Aprendizaje

Al finalizar el bootcamp, los estudiantes serán capaces de:

- ✅ Configurar el entorno de desarrollo (VS Code, Live Server, DevTools)
- ✅ Inspeccionar, depurar y experimentar con HTML/CSS desde el navegador
- ✅ Escribir HTML5 semántico, estructurado y accesible
- ✅ Crear formularios, tablas y multimedia correctamente
- ✅ Dominar el modelo de caja (Box Model) y los modos de display
- ✅ Construir layouts con Flexbox y CSS Grid
- ✅ Implementar diseño responsive con Mobile-first y Media Queries
- ✅ Usar CSS Custom Properties, tipografía web y paletas de color
- ✅ Aplicar transiciones, transforms y animaciones CSS
- ✅ Usar selectores avanzados, pseudo-clases y pseudo-elementos
- ✅ Cumplir estándares de accesibilidad (ARIA, a11y) y SEO básico
- ✅ Construir un portfolio completo como proyecto final

---

## 📚 Estructura del Bootcamp

### Distribución por Etapas

#### Setup & DevTools (Semana 1) — 8 horas

- VS Code: extensiones esenciales, atajos, configuración
- Entorno de trabajo: Live Server, estructura de archivos, Git básico
- DevTools del navegador: paneles Elements, Styles, Computed, Console
- Inspeccionar y editar HTML/CSS en vivo, depurar layouts, medir rendimiento

#### HTML Fundamentos (Semanas 2–3) — 16 horas

- Estructura HTML, DOCTYPE, etiquetas esenciales, semántica básica
- Listas, links, tablas, formularios, multimedia (img, video, audio, iframe)

#### CSS Fundamentos (Semanas 4–5) — 16 horas

- Sintaxis CSS, selectores, especificidad, cascada y herencia
- Box Model (margin, border, padding, content), display, overflow

#### Layout (Semanas 6–8) — 24 horas

- Positioning (static / relative / absolute / fixed / sticky) y float
- Flexbox: ejes, alineación, flex-wrap, gap, flex-grow/shrink/basis
- CSS Grid: grid-template, áreas nombradas, auto-fit/fill, minmax

#### Responsive & Estilizado (Semanas 9–10) — 16 horas

- Mobile-first, breakpoints, unidades relativas (rem, em, vw, vh, %)
- Tipografía web (Google Fonts), gradientes, CSS Custom Properties, `calc()`

#### CSS Avanzado (Semanas 11–12) — 16 horas

- `transition`, `transform` (2D y 3D), `@keyframes`, `animation`
- `:nth-child`, `:not()`, `:has()`, `::before`, `::after`, atributos

#### Producción (Semana 13) — 8 horas

- HTML5 semántico profundo, ARIA, accesibilidad (a11y), SEO básico
- Proyecto final: portfolio completo responsive

### 📅 Nombres de Carpeta por Semana

| #   | Carpeta                                            | Tema principal                                          |
| --- | -------------------------------------------------- | ------------------------------------------------------- |
| 01  | `week-01-setup_y_devtools`                         | VS Code, Live Server, DevTools del navegador            |
| 02  | `week-02-html_fundamentos`                         | Estructura HTML, etiquetas esenciales, semántica básica |
| 03  | `week-03-html_formularios_y_multimedia`            | Formularios, tablas, img, video, audio, iframe          |
| 04  | `week-04-css_fundamentos_y_selectores`             | Sintaxis CSS, selectores, especificidad, cascada        |
| 05  | `week-05-css_box_model_y_display`                  | Box Model, margin/padding, display, overflow            |
| 06  | `week-06-positioning_y_float`                      | static/relative/absolute/fixed/sticky, z-index, float   |
| 07  | `week-07-flexbox`                                  | Ejes, alineación, flex-wrap, gap, flex-grow/shrink      |
| 08  | `week-08-css_grid`                                 | grid-template, áreas nombradas, auto-fit/fill, minmax   |
| 09  | `week-09-responsive_y_media_queries`               | Mobile-first, breakpoints, rem/em/vw/vh                 |
| 10  | `week-10-tipografia_colores_y_variables`           | Google Fonts, gradientes, Custom Properties, `calc()`   |
| 11  | `week-11-transiciones_transforms_y_animaciones`    | `transition`, `transform`, `@keyframes`, `animation`    |
| 12  | `week-12-selectores_avanzados_y_pseudo_elementos`  | `:nth-child`, `:not()`, `:has()`, `::before`, `::after` |
| 13  | `week-13-semantica_accesibilidad_y_proyecto_final` | HTML5 semántico, ARIA, a11y, SEO, portfolio completo    |

---

## 🗂️ Estructura de Carpetas

Cada semana sigue esta estructura estándar:

```
bootcamp/week-XX-tema_principal/
├── README.md                 # Descripción y objetivos de la semana
├── rubrica-evaluacion.md     # Criterios de evaluación detallados
├── 0-assets/                 # Imágenes, diagramas y recursos visuales (SVG preferido)
├── 1-teoria/                 # Material teórico (archivos .md)
├── 2-practicas/              # Ejercicios guiados paso a paso
├── 3-proyecto/               # Proyecto semanal integrador
│   ├── README.md             # Instrucciones del proyecto
│   ├── starter/              # Código inicial para el estudiante
│   └── solution/             # ⚠️ OCULTA - Solo para instructores (.gitignore)
├── 4-recursos/               # Recursos adicionales
│   ├── ebooks-free/          # Libros electrónicos gratuitos
│   ├── videografia/          # Videos y tutoriales recomendados
│   └── webgrafia/            # Enlaces y documentación
└── 5-glosario/               # Términos clave de la semana (A-Z)
    └── README.md
```

### 📁 Carpetas Raíz

- `_assets/`: Recursos visuales globales (logos, headers, banners del bootcamp)
- `_docs/`: Documentación general que aplica a todo el bootcamp
- `_scripts/`: Scripts de automatización y utilidades
- `bootcamp/`: Contenido semanal del bootcamp

---

## 🎓 Componentes de Cada Semana

### 1. Teoría (`1-teoria/`)

- Archivos markdown con explicaciones conceptuales
- Ejemplos de código HTML/CSS con comentarios claros
- Diagramas y visualizaciones SVG cuando sea necesario
- Referencias a MDN Web Docs y especificaciones W3C / WHATWG

### 2. Prácticas (`2-practicas/`)

- Ejercicios guiados paso a paso
- Incremento progresivo de dificultad
- Soluciones comentadas
- Casos de uso del mundo real

#### 📋 Formato de Ejercicios

Los ejercicios son tutoriales guiados, **NO tareas con TODOs**. El estudiante aprende descomentando código:

**README.md del ejercicio:**

````markdown
### Paso 1: Crear un enlace de navegación accesible

Explicación del concepto con ejemplo:

```html
<!-- Ejemplo explicativo -->
<nav aria-label="Navegación principal">
  <a href="/inicio">Inicio</a>
</nav>
```
````

**Abre `starter/index.html`** y descomenta la sección correspondiente.

````

**starter/index.html:**

```html
<!-- ============================================ -->
<!-- PASO 1: Enlace de navegación accesible       -->
<!-- ============================================ -->

<!-- Descomenta las siguientes líneas: -->
<!-- <nav aria-label="Navegación principal"> -->
<!--   <a href="/inicio">Inicio</a>          -->
<!-- </nav>                                  -->
````

> ⚠️ **IMPORTANTE:** Los ejercicios **NO tienen** carpeta `solution/`. El estudiante aprende descomentando el código y verificando el resultado en el navegador.

#### ❌ NO usar este formato en ejercicios:

```html
<!-- ❌ INCORRECTO - Este formato es para PROYECTOS, no ejercicios -->
<nav>
  <!-- TODO: Añadir enlace de navegación -->
</nav>
```

#### ✅ Usar este formato en ejercicios:

```html
<!-- ✅ CORRECTO - Código comentado para descomentar -->
<!-- Descomenta las siguientes líneas: -->
<!-- <nav aria-label="Navegación principal"> -->
<!--   <a href="/inicio">Inicio</a>          -->
<!-- </nav>                                  -->
```

### 3. Proyecto (`3-proyecto/`)

- Proyecto integrador que consolida lo aprendido en la semana
- `README.md` con instrucciones claras
- Código inicial en `starter/`
- Carpeta `solution/` oculta (en `.gitignore`) solo para instructores
- Criterios de evaluación específicos

#### 📋 Formato de Proyecto (con TODOs)

A diferencia de los ejercicios, el proyecto **SÍ usa TODOs** para que el estudiante implemente desde cero:

**starter/index.html:**

```html
<!-- ============================================ -->
<!-- SECCIÓN: Hero del portfolio                  -->
<!-- Crea la sección principal con nombre,        -->
<!-- título profesional y llamada a la acción.    -->
<!-- ============================================ -->

<!-- TODO: Implementar la sección hero            -->
<!-- 1. Agregar un <header> semántico             -->
<!-- 2. Incluir <h1> con tu nombre                -->
<!-- 3. Agregar <p> con tu título profesional     -->
<!-- 4. Incluir un <a> como botón CTA             -->
```

> 📁 Estructura del proyecto:
>
> ```
> 3-proyecto/
> ├── README.md          # Instrucciones del proyecto
> ├── starter/           # Código inicial para el estudiante
> └── solution/          # ⚠️ OCULTA - Solo para instructores
> ```
>
> La carpeta `solution/` está en `.gitignore` y **NO se sube** al repositorio público.

### 4. Recursos (`4-recursos/`)

- `ebooks-free/`: Libros gratuitos relevantes (HTML, CSS, a11y, etc.)
- `videografia/`: Videos tutoriales complementarios
- `webgrafia/`: Enlaces a MDN, CSS-Tricks, web.dev, can-i-use, etc.

### 5. Glosario (`5-glosario/`)

- Términos técnicos ordenados alfabéticamente
- Definiciones claras y concisas
- Ejemplos de código HTML/CSS cuando aplique

---

## 📝 Convenciones de Código

### HTML — Buenas Prácticas

```html
<!-- ✅ BIEN - HTML semántico con atributos de accesibilidad -->
<header role="banner">
  <nav aria-label="Navegación principal">
    <ul>
      <li><a href="#about">Sobre mí</a></li>
    </ul>
  </nav>
</header>

<main id="main-content">
  <article>
    <h1>Título principal</h1>
    <p>Contenido descriptivo.</p>
  </article>
</main>

<!-- ❌ MAL - divitis sin semántica ni accesibilidad -->
<div class="header">
  <div class="nav">
    <div class="nav-item"><a href="#about">Sobre mí</a></div>
  </div>
</div>
```

### CSS — Buenas Prácticas

```css
/* ✅ BIEN - Custom Properties y unidades relativas */
:root {
  --color-primary: #3b82f6;
  --color-text: #1f2937;
  --font-size-base: 1rem;
  --spacing-md: 1.5rem;
}

.card {
  padding: var(--spacing-md);
  font-size: var(--font-size-base);
  color: var(--color-text);
  border-radius: 0.5rem;
}

/* ❌ MAL - valores mágicos sin variables */
.card {
  padding: 24px;
  font-size: 16px;
  color: #1f2937;
  border-radius: 8px;
}
```

```css
/* ✅ BIEN - Mobile-first con Media Queries */
.grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 1rem;
}

@media (min-width: 768px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

/* ❌ MAL - Desktop-first (dificulta el responsive) */
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
}

@media (max-width: 768px) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```

### Nomenclatura

- **Clases CSS:** `kebab-case` (`.nav-item`, `.hero-title`, `.btn-primary`)
- **IDs HTML:** `kebab-case`, usar solo para anchors y accesibilidad (`#main-content`)
- **Archivos:** `kebab-case` (`index.html`, `styles.css`, `about-page.css`)
- **Carpetas:** `kebab-case` (`2-practicas/`, `4-recursos/`)
- **Idioma del código:** inglés (clases, IDs, nombres de archivo)
- **Idioma de documentación:** español (READMEs, teoría, comentarios educativos)

### Estructura de Proyecto HTML/CSS

```
proyecto/
├── index.html           # Página principal
├── about.html           # Página secundaria (si aplica)
├── css/
│   ├── reset.css        # Reset / normalize
│   ├── variables.css    # CSS Custom Properties
│   └── styles.css       # Estilos principales
├── assets/
│   ├── images/          # Imágenes optimizadas
│   └── fonts/           # Fuentes locales (si aplica)
└── README.md            # Instrucciones del proyecto
```

---

## 🌐 Idioma y Nomenclatura

### Código y Clases

```html
<!-- ✅ CORRECTO - inglés en código -->
<section class="hero-section" id="hero">
  <h1 class="hero-title">My Portfolio</h1>
  <p class="hero-subtitle">Frontend Developer</p>
</section>

<!-- ❌ INCORRECTO - español en clases/IDs -->
<section class="seccion-hero" id="hero">
  <h1 class="titulo-hero">Mi Portfolio</h1>
  <p class="subtitulo-hero">Desarrollador Frontend</p>
</section>
```

### Documentación

- ✅ Documentación en español (READMEs, teoría, guías)
- ✅ Explicaciones y tutoriales en español
- ✅ Comentarios educativos en español cuando expliquen conceptos

```html
<!-- ✅ CORRECTO - código en inglés, comentario educativo en español -->
<figure class="profile-card">
  <!-- La etiqueta <figure> es semántica: agrupa contenido autocontenido como imágenes con su descripción -->
  <img src="assets/images/profile.jpg" alt="Foto de perfil de Ana García" />
  <figcaption>Ana García — Frontend Developer</figcaption>
</figure>
```

---

## 🎨 Recursos Visuales y Estándares de Diseño

### Formato de Assets

- ✅ Preferir **SVG** para todos los diagramas, iconos y gráficos
- ❌ NO usar ASCII art para diagramas o visualizaciones
- ✅ Usar PNG/JPG solo para screenshots o fotografías reales
- ✅ Optimizar imágenes antes de incluirlas (`alt` siempre presente)

### Criterio para Assets SVG por Semana

Los assets SVG en `0-assets/` de cada semana tienen un propósito educativo específico:

- ✅ Apoyo visual para comprensión de conceptos teóricos
- ✅ Diagramas del Box Model, Flexbox, Grid, etc.
- ✅ Visualización de flujos (cascada CSS, especificidad, responsive breakpoints)
- ✅ Headers de semana para identificación visual

Reglas de vinculación:

1. Todo SVG debe estar vinculado en al menos un archivo de teoría o práctica
2. Usar sintaxis markdown: `![Descripción](../0-assets/nombre.svg)`
3. Incluir texto alternativo descriptivo para accesibilidad
4. Nombrar archivos descriptivamente: `box-model.svg`, `flexbox-axes.svg`, `grid-areas.svg`

```markdown
<!-- Ejemplo de vinculación correcta en teoría -->

## Box Model

![Diagrama del Box Model CSS](../0-assets/box-model.svg)

Como se observa en el diagrama, el Box Model define...
```

### Tema Visual

- 🌙 Tema **dark** para todos los assets visuales del bootcamp
- ❌ Sin degradés (gradients) en diseños de assets educativos
- ✅ Colores sólidos y contrastes claros
- ✅ Paleta consistente basada en el color primario del bootcamp

### Tipografía en Assets

- ✅ Fuentes sans-serif exclusivamente
- ✅ Recomendadas: Inter, Roboto, Open Sans, System UI
- ❌ NO usar fuentes serif (Times, Georgia, etc.)
- ✅ Mantener jerarquía visual clara

---

## 🔐 Mejores Prácticas

### HTML Semántico y Accesibilidad

- Usar etiquetas semánticas: `<header>`, `<main>`, `<nav>`, `<section>`, `<article>`, `<aside>`, `<footer>`
- Todo `<img>` debe tener atributo `alt` descriptivo (vacío solo si es decorativa)
- Formularios: `<label>` vinculado a cada `<input>` con `for`/`id`
- Orden lógico de headings (`h1` → `h2` → `h3`, sin saltar niveles)
- Usar `aria-label` y `aria-describedby` cuando el contexto visual no sea suficiente
- Contraste de color mínimo: 4.5:1 (WCAG AA) para texto normal

### CSS Limpio

- CSS Custom Properties para todos los valores reutilizables (colores, espaciados, tipografías)
- Mobile-first siempre (estilos base para móvil, `@media (min-width)` para pantallas mayores)
- Evitar `!important` salvo casos extremadamente justificados
- Evitar selectores excesivamente específicos (máximo 2–3 niveles)
- Preferir `rem` y `em` sobre `px` para tipografía y espaciados
- Usar `gap` (en Flex/Grid) sobre `margin` para espaciado entre elementos

### Rendimiento y Código

- Imágenes con `loading="lazy"` cuando no estén en la vista inicial
- Fuentes web con `font-display: swap`
- CSS crítico (above the fold) inline o en `<head>`, resto diferido
- No incluir CSS no utilizado

### 🔒 Dependencias Externas — Reglas de Oro

> ⚠️ Este bootcamp es **100% HTML + CSS estático sin build tools**. No existe ni existirá `package.json`, `requirements.txt`, `Gemfile` ni ningún manifiesto de dependencias. Estas reglas aplican a cualquier herramienta de soporte (linters, scripts de automatización) que se agregue en el futuro.

#### Política de versiones (OBLIGATORIO)

| ❌ PROHIBIDO | ✅ CORRECTO |
|---|---|
| `"eslint": "^8.0.0"` | `"eslint": "8.57.1"` |
| `"prettier": ">=3.0.0"` | `"prettier": "3.3.3"` |
| `"stylelint": "~15.0"` | `"stylelint": "16.9.0"` |
| `"node": ">=18"` | `"node": "22.11.0"` |

**Regla de oro**: SIEMPRE versión exacta. NUNCA `^`, `~`, `>=`, `>`, `*` ni rangos de ningún tipo.

Razón: Los rangos permiten actualizaciones automáticas silenciosas que pueden introducir CVEs, breaking changes o comportamiento no reproducible. Una versión exacta garantiza builds deterministas y auditorías trazables.

#### Gestión de paquetes

- Package manager: **pnpm exclusivamente** (NUNCA npm, yarn, bun)
- Lockfile: siempre commitear `pnpm-lock.yaml` — NUNCA ignorarlo en `.gitignore`
- Actualización: manual y deliberada, con revisión del changelog y CVEs antes de cada bump

#### Dependencias externas en HTML/CSS (estado auditado: abril 2026)

| Recurso | Tipo | Estado | Notas |
|---|---|---|---|
| `fonts.googleapis.com` | Fuentes web | ✅ Aceptado | Servicio gestionado por Google; sin CVEs trazables. `crossorigin` aplicado. |
| `fonts.gstatic.com` | Fuentes web | ✅ Aceptado | Preconnect con `crossorigin`. |
| `placehold.co` | Imágenes demo | ✅ Solo educativo | Contenido de ejemplo, no producción. |
| `i.pravatar.cc` / `picsum.photos` | Imágenes demo | ✅ Solo educativo | Ídem. |
| `ui-avatars.com` | Avatares demo | ✅ Solo educativo | Ídem. |
| Librerías JS (jQuery, Bootstrap…) | — | 🚫 Prohibido | Este bootcamp NO carga librerías JS externas. |

#### SRI (Subresource Integrity)

- Para cualquier recurso CSS o JS externo que NO sea Google Fonts API: **OBLIGATORIO** añadir atributo `integrity` con hash SHA-384.
- Google Fonts API queda exento porque genera CSS dinámico por user-agent (SRI incompatible por diseño).

```html
<!-- ✅ CORRECTO — recurso externo con SRI -->
<link
  rel="stylesheet"
  href="https://example.com/lib.css"
  integrity="sha384-HASH_AQUI"
  crossorigin="anonymous"
/>

<!-- ❌ INCORRECTO — recurso externo sin SRI -->
<link rel="stylesheet" href="https://example.com/lib.css" />
```

#### Auditoría de CVEs

- Antes de agregar cualquier dependencia nueva: consultar [osv.dev](https://osv.dev) y [nvd.nist.gov](https://nvd.nist.gov/)
- Para paquetes npm/pnpm: ejecutar `pnpm audit --audit-level=moderate` antes de cada commit que toque dependencias

---

## 📖 Documentación

### README.md de Semana

Debe incluir:

1. Título y descripción
2. 🎯 Objetivos de aprendizaje
3. 📚 Requisitos previos
4. 🗂️ Estructura de la semana
5. 📝 Contenidos (con enlaces a teoría/prácticas)
6. ⏱️ Distribución del tiempo (8 horas)
7. 📌 Entregables
8. 🎓 Conceptos clave
9. ✅ Checklist de verificación
10. 🔗 Navegación (semana anterior / siguiente)

### Archivos de Teoría

```markdown
# Título del Tema

## 🎯 Objetivos

- Objetivo 1
- Objetivo 2

## 📋 Contenido

### 1. Introducción

### 2. Conceptos Clave

### 3. Ejemplos Prácticos

### 4. Casos de Uso

## 📚 Recursos Adicionales

## ✅ Checklist de Verificación
```

---

## 📊 Evaluación

Cada semana incluye tres tipos de evidencias:

1. **Conocimiento 🧠 (30%):** Cuestionarios y evaluaciones teóricas
2. **Desempeño 💪 (40%):** Ejercicios prácticos en clase
3. **Producto 📦 (30%):** Proyecto entregable funcional (código HTML/CSS)

### Criterios de Aprobación

- Mínimo 70% en cada tipo de evidencia
- Entrega puntual de proyectos
- Código validado (sin errores en W3C Validator)
- Diseño responsive funcional (móvil, tablet y escritorio)

---

## 🚀 Metodología de Aprendizaje

### Estrategias Didácticas

- **Aprendizaje Basado en Proyectos (ABP):** Proyectos semanales integradores
- **Práctica Deliberada:** Ejercicios incrementales
- **Build & Break:** Construir y romper layouts para entender el comportamiento
- **Inspect & Learn:** Uso intensivo de DevTools del navegador
- **Live Coding:** Sesiones en vivo de maquetado

### Distribución del Tiempo (8h/semana)

```
📖 Teoría:           2–2.5h  (25–31%)
💻 Prácticas:        3.5–4h  (44–50%)
🚀 Proyecto:         1.5–2h  (19–25%)
```

---

## 🤖 Instrucciones para Copilot

Cuando trabajes en este proyecto:

### Límites de Respuesta

1. **Divide respuestas largas**
   - ❌ NUNCA generar respuestas que superen los límites de tokens
   - ✅ SIEMPRE dividir contenido extenso en múltiples entregas
   - ✅ Crear contenido por secciones, esperar confirmación del usuario
   - ✅ Priorizar calidad sobre cantidad en cada entrega
   - Razón: Evitar pérdida de contenido y garantizar completitud

2. **Estrategia de División**
   - Para semanas completas: dividir por carpetas (`1-teoria` → `2-practicas` → `3-proyecto`)
   - Para archivos grandes: dividir por secciones lógicas
   - Siempre indicar claramente qué parte se entrega y qué falta
   - Esperar confirmación del usuario antes de continuar

### Generación de Código

1. **HTML5 moderno y semántico siempre**
   - Etiquetas semánticas obligatorias (`<header>`, `<main>`, `<nav>`, etc.)
   - `lang` en `<html>` siempre presente (`<html lang="es">`)
   - `meta charset`, `meta viewport` en todo `<head>`
   - `alt` en toda `<img>`, `<label>` en todo `<input>`

2. **CSS con Custom Properties**
   - Declarar variables en `:root` para colores, tipografías y espaciados
   - Mobile-first en todos los estilos responsive

3. **Entorno de Desarrollo**
   - ✅ VS Code + extensión **Live Server** para recarga en vivo
   - ✅ DevTools del navegador (Chrome/Firefox) para inspección y debug
   - ✅ W3C Validator para validar HTML: [https://validator.w3.org/](https://validator.w3.org/)
   - ✅ W3C CSS Validator: [https://jigsaw.w3.org/css-validator/](https://jigsaw.w3.org/css-validator/)
   - ❌ NO se requiere Node.js, npm ni build tools para este bootcamp

4. **Comenta el código de manera educativa**
   - Explica conceptos para principiantes
   - Incluye referencias a MDN cuando sea útil
   - Usa comentarios que enseñen, no solo que describan

   ```css
   /* ✅ CORRECTO - código en inglés, explicación en español */
   .flex-container {
     display: flex;
     /* justify-content alinea los items en el eje principal (horizontal por defecto) */
     justify-content: space-between;
     /* align-items alinea los items en el eje cruzado (vertical por defecto) */
     align-items: center;
   }
   ```

5. **Proporciona ejemplos completos y funcionales**
   - HTML que se pueda abrir directamente en el navegador
   - CSS que produzca resultados visibles e inmediatos
   - Muestra tanto lo correcto como lo que se debe evitar

### Creación de Contenido

1. **Estructura clara y progresiva**
   - De lo simple a lo complejo
   - Conceptos construidos sobre conocimientos previos
   - Repetición espaciada de conceptos clave

2. **Ejemplos del mundo real**
   - Componentes de UI reales: headers, cards, formularios, grids de galería, navbars
   - Proyectos que los estudiantes puedan mostrar en portfolios
   - Problemas de maquetado que encontrarán en el trabajo real

3. **Enfoque moderno**
   - No mencionar características obsoletas (`<font>`, `<center>`, `float` para layouts, `table` para maquetado)
   - Enfocarse en Flexbox y Grid como sistemas de layout primarios
   - Usar CSS Custom Properties, `gap`, `clamp()`, `aspect-ratio`, etc.

### Respuestas y Ayuda

1. **Explicaciones claras**
   - Lenguaje simple y directo
   - Evitar jerga innecesaria
   - Proporcionar analogías visuales cuando sea útil (ej: el Box Model como una caja de regalo)

2. **Código comentado**
   - Explicar cada regla CSS importante
   - Destacar propiedades que suelen confundir (especificidad, `z-index`, `position`, `stacking context`)
   - Señalar errores comunes (márgenes colapsados, overflow oculto, unidades incorrectas)

3. **Recursos adicionales**
   - Referencias a MDN Web Docs (fuente de verdad)
   - CSS-Tricks para guías visuales (Flexbox/Grid)
   - can-i-use para compatibilidad de navegadores
   - web.dev para rendimiento y accesibilidad

---

## 📚 Referencias Oficiales

- **MDN HTML:** [https://developer.mozilla.org/es/docs/Web/HTML](https://developer.mozilla.org/es/docs/Web/HTML)
- **MDN CSS:** [https://developer.mozilla.org/es/docs/Web/CSS](https://developer.mozilla.org/es/docs/Web/CSS)
- **W3C HTML Spec:** [https://html.spec.whatwg.org/](https://html.spec.whatwg.org/)
- **CSS Specifications:** [https://www.w3.org/Style/CSS/](https://www.w3.org/Style/CSS/)
- **CSS-Tricks Flexbox:** [https://css-tricks.com/snippets/css/a-guide-to-flexbox/](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- **CSS-Tricks Grid:** [https://css-tricks.com/snippets/css/complete-guide-grid/](https://css-tricks.com/snippets/css/complete-guide-grid/)
- **web.dev (Google):** [https://web.dev/](https://web.dev/)
- **Can I Use:** [https://caniuse.com/](https://caniuse.com/)
- **WCAG 2.1:** [https://www.w3.org/TR/WCAG21/](https://www.w3.org/TR/WCAG21/)

---

## 🔗 Enlaces Importantes

- **Repositorio:** [https://github.com/ergrato-dev/bc-html-css](https://github.com/ergrato-dev/bc-html-css)
- **Documentación general:** [\_docs/README.md](../_docs/README.md)
- **Primera semana:** [bootcamp/week-01-html_fundamentos/README.md](../bootcamp/week-01/README.md)

---

## 📋 Orden de Creación de Contenidos

Al crear o completar una semana, seguir **estrictamente este orden**:

1. **`README.md` principal de la semana** — objetivos, estructura, distribución del tiempo, checklist y navegación
2. **`rubrica-evaluacion.md`** — criterios de evaluación detallados (conocimiento, desempeño, producto)
3. **Archivos de teoría** (`1-teoria/`) — explicaciones conceptuales con ejemplos de código comentados
4. **Assets SVG** (`0-assets/`) — diagramas de apoyo a la teoría; vincularlos en los archivos de teoría correspondientes usando `![Descripción](../0-assets/nombre.svg)`
5. **Prácticas** (`2-practicas/`) — ejercicios guiados en formato "descomentar", basados en la teoría ya creada
6. **Proyecto** (`3-proyecto/`) — `README.md` del proyecto + `starter/` con TODOs + `solution/` (oculta)
7. **Recursos** (`4-recursos/`) — `ebooks-free/`, `videografia/` y `webgrafia/` completos
8. **Glosario** (`5-glosario/README.md`) — todos los términos clave de la semana en orden alfabético

> ⚠️ **IMPORTANTE:** No avanzar al siguiente paso sin completar el anterior. Los assets SVG deben crearse **después** de la teoría para saber exactamente qué conceptos necesitan apoyo visual, y vincularse **antes** de crear las prácticas para que los ejercicios puedan referenciarlos.

---

## ✅ Checklist para Nuevas Semanas

Cuando crees contenido para una nueva semana:

- [ ] Crear estructura de carpetas completa (`week-XX-tema_principal/`)
- [ ] `README.md` principal con objetivos, estructura y navegación
- [ ] `rubrica-evaluacion.md` con criterios de conocimiento, desempeño y producto
- [ ] Archivos de teoría en `1-teoria/`
- [ ] Assets SVG en `0-assets/` vinculados en los archivos de teoría correspondientes
- [ ] Ejercicios guiados en `2-practicas/` (formato descomentar, no TODOs)
- [ ] Proyecto integrador en `3-proyecto/` (con `starter/` y `solution/`)
- [ ] Recursos completos en `4-recursos/` (ebooks, videografía, webgrafía)
- [ ] Glosario de términos en `5-glosario/README.md`
- [ ] Verificar coherencia con semanas anteriores
- [ ] Revisar progresión de dificultad
- [ ] Validar HTML de ejemplos en W3C Validator
- [ ] Verificar que el CSS funciona en Chrome, Firefox y Safari

---

## 💡 Notas Finales

- **Prioridad:** Claridad sobre brevedad
- **Enfoque:** Aprendizaje práctico sobre teoría abstracta
- **Objetivo:** Preparar desarrolladores frontend capaces de maquetar cualquier diseño
- **Filosofía:** HTML semántico y CSS moderno desde el día 1 — sin atajos que generen malos hábitos
- **Fuera de scope:** Tailwind CSS, SASS/SCSS, Bootstrap y otros frameworks (cubiertos en bootcamps separados)

---

_Última actualización: Marzo 2026 · Versión: 1.0_
