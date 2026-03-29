# Ejercicio 03 — Contenido semántico: textos, listas, enlaces e imágenes

## 🎯 Objetivo

Practicar el uso de etiquetas de contenido: headings, párrafos, texto enriquecido, listas, enlaces e imágenes dentro de una estructura HTML semántica.

## 📋 Instrucciones

Abre `starter/index.html` en VS Code con Live Server activo y sigue los pasos descomentando el código en orden.

---

### Paso 1: Jerarquía de headings

Los headings `<h1>`–`<h6>` definen la jerarquía del contenido. Reglas clave:

- Solo **un `<h1>`** por página (el título principal)
- No saltar niveles: después de `<h2>` va `<h3>`, no `<h4>`
- Los headings describen **estructura**, no tamaño de fuente

**Descomenta** la sección `PASO 1` en el archivo starter.

---

### Paso 2: Texto enriquecido

```html
<!-- strong = importancia semántica; b = solo visual (evitar) -->
<strong>Importante</strong>

<!-- em = énfasis semántico; i = solo visual (evitar) -->
<em>Con énfasis</em>

<!-- mark resalta texto como si fuera un marcador -->
<p>Usa <mark>CSS Custom Properties</mark> para colores reutilizables.</p>
```

**Descomenta** la sección `PASO 2`.

---

### Paso 3: Listas

```html
<!-- Lista no ordenada (orden no importa) -->
<ul>
  <li>HTML</li>
  <li>CSS</li>
</ul>

<!-- Lista ordenada (orden sí importa) -->
<ol>
  <li>Abrir VS Code</li>
  <li>Instalar Live Server</li>
</ol>

<!-- Lista de definición (términos y descripciones) -->
<dl>
  <dt>HTML</dt>
  <dd>Lenguaje de marcado para estructurar contenido web.</dd>
</dl>
```

**Descomenta** la sección `PASO 3`.

---

### Paso 4: Enlaces e imágenes

```html
<!-- target="_blank" abre en pestaña nueva; rel='noopener noreferrer' es obligatorio por seguridad -->
<a href="https://developer.mozilla.org/es/" target="_blank" rel="noopener noreferrer">
  MDN Web Docs
</a>

<!-- alt siempre presente: describe la imagen para lectores de pantalla -->
<img src="assets/html5-logo.png" alt="Logo de HTML5 de color naranja" width="80" height="80" loading="lazy" />
```

**Descomenta** la sección `PASO 4`.

---

## ✅ Verificación

- [ ] Los headings siguen jerarquía lógica (h1 → h2 → h3)
- [ ] `<strong>` y `<em>` se usan con intención semántica, no visual
- [ ] Las listas usan la etiqueta correcta según el contexto
- [ ] Todos los enlaces externos tienen `rel="noopener noreferrer"`
- [ ] Todas las imágenes tienen atributo `alt` descriptivo
