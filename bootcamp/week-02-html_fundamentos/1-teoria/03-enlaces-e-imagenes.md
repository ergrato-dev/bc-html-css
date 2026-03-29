# 03 — Enlaces e imágenes

## 🎯 Objetivos

- Crear enlaces internos y externos con `<a>`
- Distinguir rutas relativas de absolutas
- Insertar imágenes accesibles con `<img>`
- Usar `<figure>` y `<figcaption>` correctamente

---

## 1. La etiqueta `<a>` — hipervínculo

El elemento `<a>` (anchor) crea hipervínculos. El atributo `href` define el destino.

```html
<!-- Enlace externo -->
<a href="https://developer.mozilla.org" target="_blank" rel="noopener noreferrer">
  MDN Web Docs
</a>

<!-- Enlace interno (anchor a sección de la misma página) -->
<a href="#sobre-mi">Ir a Sobre mí</a>
<section id="sobre-mi">...</section>

<!-- Enlace a otra página del mismo proyecto -->
<a href="about.html">Acerca de</a>

<!-- Enlace de correo electrónico -->
<a href="mailto:contacto@ejemplo.com">Enviar email</a>

<!-- Enlace a número de teléfono -->
<a href="tel:+34600000000">Llamar</a>
```

> ⚠️ **Buena práctica — `mailto:` en producción:** el atributo `mailto:` es útil para aprender
> el protocolo de enlace, pero exponer una dirección de correo en el HTML la hace
> vulnerable al rastreo por **bots de spam**. En proyectos reales, **prefiere
> un formulario de contacto** (`<form>`) en su lugar.

### Atributos importantes de `<a>`:

| Atributo | Valor | Para qué |
|----------|-------|---------|
| `href` | URL o ruta | Destino del enlace |
| `target="_blank"` | `_blank` | Abre en pestaña nueva |
| `rel="noopener noreferrer"` | — | Seguridad: evita acceso al `window.opener` |
| `download` | — | Descarga el archivo en lugar de abrirlo |

> ⚠️ **Seguridad**: todo `target="_blank"` debe ir acompañado de `rel="noopener noreferrer"` para evitar ataques de tabnapping.

---

## 2. Rutas relativas vs absolutas

```html
<!-- Ruta ABSOLUTA: incluye el protocolo y dominio -->
<a href="https://github.com/ergrato-dev">GitHub</a>
<img src="https://ejemplo.com/foto.jpg" alt="foto" />

<!-- Ruta RELATIVA: parte desde la ubicación del archivo actual -->
<a href="about.html">Acerca de</a>           <!-- misma carpeta -->
<a href="pages/contact.html">Contacto</a>    <!-- subcarpeta -->
<a href="../index.html">Inicio</a>           <!-- carpeta padre -->
<img src="assets/images/perfil.jpg" alt="Mi foto" />
```

### Regla de los puntos:

```
./archivo.html    = misma carpeta (el ./ es opcional)
../archivo.html   = carpeta padre (sube un nivel)
../../archivo     = sube dos niveles
```

---

## 3. La etiqueta `<img>` — imagen

```html
<!-- Obligatorio: src (ruta) + alt (texto alternativo) -->
<img
  src="assets/images/perfil.jpg"
  alt="Fotografía de Ana García sonriendo"
  width="300"
  height="300"
  loading="lazy"
/>
```

### Atributos de `<img>`:

| Atributo | Descripción |
|----------|-------------|
| `src` | Ruta al archivo de imagen |
| `alt` | Texto alternativo para accesibilidad/carga fallida |
| `width` / `height` | Dimensiones en píxeles (evita "layout shift") |
| `loading="lazy"` | Carga diferida para imágenes fuera del viewport inicial |

### Reglas del atributo `alt`:

```html
<!-- ✅ Imagen con contenido informativo: describir lo que muestra -->
<img src="grafico.png" alt="Gráfico de barras: ventas Q1 2026 superan 50k€" />

<!-- ✅ Imagen decorativa: alt vacío (no omitir el atributo, dejarlo vacío) -->
<img src="fondo-decorativo.svg" alt="" />

<!-- ❌ INCORRECTO: alt con nombre de archivo o "imagen de..." -->
<img src="foto.jpg" alt="foto.jpg" />
<img src="foto.jpg" alt="imagen de una persona" />
```

---

## 4. `<figure>` y `<figcaption>`

Cuando una imagen necesita una leyenda o descripción visible, se usa `<figure>`:

```html
<figure>
  <img
    src="assets/images/box-model.png"
    alt="Diagrama del Box Model CSS: content, padding, border y margin"
    width="600"
    height="400"
  />
  <figcaption>
    El Box Model de CSS define cuánto espacio ocupa un elemento.
    — Diagrama de MDN Web Docs
  </figcaption>
</figure>
```

`<figure>` también se usa para bloques de código, citas, tablas y cualquier contenido autocontenido con leyenda.

---

## 5. Formatos de imagen para web

| Formato | Mejor para | Transparencia |
|---------|-----------|---------------|
| JPEG / JPG | Fotografías | No |
| PNG | Gráficos, iconos con transparencia | Sí |
| SVG | Vectores, iconos escalables | Sí |
| WebP | Todo (moderno, menor tamaño) | Sí |
| AVIF | Fotografías modernas (máxima compresión) | Sí |

> Regla práctica: fotografías → JPEG/WebP · iconos/logos → SVG · screenshots → PNG

---

## ✅ Checklist

- [ ] Todo enlace externo tiene `rel="noopener noreferrer"`
- [ ] Los anchor links internos tienen `id` en el elemento destino
- [ ] Toda `<img>` tiene atributo `alt` (vacío si es decorativa)
- [ ] Imágenes fuera del viewport inicial tienen `loading="lazy"`
- [ ] Se especifica `width` y `height` en `<img>` para evitar reflow
- [ ] Se usa `<figure>` cuando la imagen necesita leyenda visible
