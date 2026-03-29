# Multimedia en HTML

## 🎯 Objetivos

- Insertar video y audio nativos con `<video>` y `<audio>`
- Proveer formatos alternativos con `<source>` para compatibilidad
- Incrustar contenido externo de forma segura con `<iframe>`
- Optimizar imágenes con `loading="lazy"`, `srcset` y `sizes`

---

## 1. Imágenes avanzadas

Más allá de `<img src alt>`, HTML ofrece opciones para imágenes responsivas:

```html
<!-- Imagen básica: siempre con alt, width y height -->
<img
  src="assets/images/portada.jpg"
  alt="Vista aérea de una ciudad al atardecer"
  width="800"
  height="450"
  loading="lazy"
/>

<!-- srcset: proporciona versiones de distinto tamaño al navegador -->
<img
  src="imagen-800.jpg"
  srcset="imagen-400.jpg 400w, imagen-800.jpg 800w, imagen-1200.jpg 1200w"
  sizes="(max-width: 600px) 400px, (max-width: 900px) 800px, 1200px"
  alt="Fotografía del equipo de desarrollo"
  width="800"
  height="450"
  loading="lazy"
/>

<!-- picture: imágenes diferentes según contexto (viewport o formato) -->
<picture>
  <!-- WebP para navegadores que lo soportan (más ligero) -->
  <source srcset="imagen.webp" type="image/webp" />
  <!-- AVIF si el navegador lo soporta (aún más ligero) -->
  <source srcset="imagen.avif" type="image/avif" />
  <!-- Fallback para todos los navegadores -->
  <img src="imagen.jpg" alt="Descripción de la imagen" width="800" height="450" />
</picture>
```

---

## 2. Video nativo

```html
<!-- Video básico con controles del navegador -->
<video
  src="video/presentacion.mp4"
  width="640"
  height="360"
  controls
  poster="video/portada.jpg"
>
  <!-- Texto de fallback para navegadores muy antiguos -->
  Tu navegador no soporta video HTML5.
</video>

<!-- Video con múltiples formatos y accesibilidad -->
<figure>
  <video
    width="640"
    height="360"
    controls
    preload="metadata"
    poster="video/portada.jpg"
    aria-describedby="desc-video"
  >
    <!-- MP4 es compatible con todos los navegadores modernos -->
    <source src="video/presentacion.mp4" type="video/mp4" />
    <!-- WebM como fallback (más comprimido en Firefox/Chrome) -->
    <source src="video/presentacion.webm" type="video/webm" />
    <!-- track: subtítulos para accesibilidad (formato WebVTT) -->
    <track
      src="video/subtitulos-es.vtt"
      kind="subtitles"
      srclang="es"
      label="Español"
      default
    />
    <p>Tu navegador no soporta el elemento video.
      <a href="video/presentacion.mp4">Descarga el video aquí</a>.
    </p>
  </video>
  <figcaption id="desc-video">
    Presentación del bootcamp HTML + CSS Zero to Hero
  </figcaption>
</figure>
```

**Atributos importantes de `<video>`:**

| Atributo | Descripción |
|----------|-------------|
| `controls` | Muestra los controles del reproductor |
| `autoplay` | Reproduce automáticamente (evitar: malo para accesibilidad) |
| `loop` | Repite el video en bucle |
| `muted` | Silencia el audio (requerido para autoplay en Chrome) |
| `poster` | Imagen a mostrar antes de reproducir |
| `preload="none\|metadata\|auto"` | Controla cuánto se carga al abrir la página |

---

## 3. Audio nativo

```html
<figure>
  <audio controls preload="metadata" aria-describedby="desc-audio">
    <source src="audio/podcast.mp3" type="audio/mpeg" />
    <source src="audio/podcast.ogg" type="audio/ogg" />
    <p>Tu navegador no soporta audio HTML5.
      <a href="audio/podcast.mp3">Descarga el audio aquí</a>.
    </p>
  </audio>
  <figcaption id="desc-audio">
    Episodio 01 — Introducción al desarrollo web moderno
  </figcaption>
</figure>
```

---

## 4. iframes (contenido embebido)

```html
<!-- YouTube: siempre con title para accesibilidad -->
<iframe
  src="https://www.youtube.com/embed/VIDEO_ID"
  title="Curso completo de HTML5 para principiantes"
  width="560"
  height="315"
  frameborder="0"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
  allowfullscreen
  loading="lazy"
></iframe>

<!-- Google Maps -->
<iframe
  src="https://www.google.com/maps/embed?pb=..."
  title="Mapa de ubicación de nuestra oficina en Ciudad de México"
  width="600"
  height="450"
  style="border:0"
  loading="lazy"
  referrerpolicy="no-referrer-when-downgrade"
></iframe>
```

> **Seguridad con iframes:** Añade `sandbox` para restricciones: `sandbox="allow-scripts allow-same-origin"` limita lo que puede hacer el contenido incrustado.

---

## 5. Formatos y compatibilidad

| Formato | Tipo | Compatibilidad | Nota |
|---------|------|----------------|------|
| `.jpg` / `.jpeg` | Imagen | Todos | Fotos, alta compresión |
| `.png` | Imagen | Todos | Transparencia, iconos |
| `.webp` | Imagen | Chrome, Firefox, Safari 14+ | 30% más pequeño que JPG |
| `.avif` | Imagen | Chrome, Firefox | Aún más pequeño, soporte creciente |
| `.svg` | Vector | Todos | Ideal para iconos y logos |
| `.mp4` (H.264) | Video | Todos | Formato universal |
| `.webm` | Video | Chrome, Firefox | Más comprimido |
| `.mp3` | Audio | Todos | Formato universal |
| `.ogg` | Audio | Chrome, Firefox | Alternativa libre |

---

## ✅ Checklist de verificación

- [ ] Video y audio tienen `controls` visible
- [ ] `<track>` con subtítulos si el video tiene voz o sonido
- [ ] Múltiples `<source>` para compatibilidad de navegadores
- [ ] `<iframe>` siempre tiene `title` descriptivo
- [ ] Imágenes con `loading="lazy"` si están fuera del viewport inicial
- [ ] `<figure>` + `<figcaption>` para multimedia con descripción

## 📚 Recursos

- [MDN — `<video>`](https://developer.mozilla.org/es/docs/Web/HTML/Element/video)
- [MDN — `<audio>`](https://developer.mozilla.org/es/docs/Web/HTML/Element/audio)
- [MDN — `<iframe>`](https://developer.mozilla.org/es/docs/Web/HTML/Element/iframe)
