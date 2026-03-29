# Ejercicio 03 — Galería Multimedia

## 🎯 Objetivo

Integrar diferentes elementos multimedia en una página HTML: imágenes con `<figure>`, video nativo, audio nativo e iframe embebido de forma accesible.

## 📋 Instrucciones

Abre `starter/index.html` con Live Server y descomenta cada sección.

---

### Paso 1: Galería de imágenes con `<figure>`

```html
<figure>
  <img
    src="https://picsum.photos/400/250?random=1"
    alt="Fotografía paisajística generada aleatoriamente número 1"
    width="400"
    height="250"
    loading="lazy"
  />
  <figcaption>Fotografía 1 — ejemplo de imagen con figure y figcaption</figcaption>
</figure>
```

**Descomenta** el `PASO 1` (incluye 3 imágenes).

---

### Paso 2: Video nativo

```html
<figure>
  <video width="560" height="315" controls poster="portada.jpg" preload="metadata">
    <source src="video/demo.mp4" type="video/mp4" />
    <p>Tu navegador no soporta video HTML5. <a href="#">Descárgalo aquí</a>.</p>
  </video>
  <figcaption>Video de demostración</figcaption>
</figure>
```

> Para esta práctica usaremos un video de `sample-videos.com` o similar.

**Descomenta** el `PASO 2`.

---

### Paso 3: Audio nativo

```html
<figure>
  <audio controls preload="metadata" aria-describedby="desc-audio">
    <source src="audio/podcast.mp3" type="audio/mpeg" />
    Tu navegador no soporta audio HTML5.
  </audio>
  <figcaption id="desc-audio">Episodio de ejemplo</figcaption>
</figure>
```

**Descomenta** el `PASO 3`.

---

### Paso 4: iframe de YouTube

```html
<figure>
  <iframe
    src="https://www.youtube.com/embed/kUMe1FH4CHE"
    title="Aprende HTML en 15 minutos"
    width="560"
    height="315"
    frameborder="0"
    allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
    allowfullscreen
    loading="lazy"
  ></iframe>
  <figcaption>Video: Introducción a HTML — YouTube</figcaption>
</figure>
```

**Descomenta** el `PASO 4`.

---

## ✅ Verificación

- [ ] Todas las imágenes tienen `alt` descriptivo
- [ ] Imágenes envueltas en `<figure>` con `<figcaption>`
- [ ] Video con `controls`, `poster` y fuente `<source>`
- [ ] Audio con `controls` y `aria-describedby`
- [ ] iframe con `title` descriptivo y `loading="lazy"`
