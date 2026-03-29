# Patrones comunes con Flexbox

## 🎯 Objetivos

- Reconocer y aplicar los patrones de Flexbox más usados en proyectos reales
- Construir navbars, centrado perfecto, layouts sidebar y grids de cards

---

## 📋 Contenido

### 1. Patrón: Navbar (logo izquierda, links derecha)

```css
.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;  /* logo ← → links */
  padding: 0.75rem 2rem;
}

.nav-links {
  display: flex;
  gap: 1.5rem;
  list-style: none;
}
```

```html
<header class="navbar">
  <span class="logo">MiSitio</span>
  <nav>
    <ul class="nav-links">
      <li><a href="#home">Inicio</a></li>
      <li><a href="#about">Sobre mí</a></li>
      <li><a href="#contact">Contacto</a></li>
    </ul>
  </nav>
</header>
```

---

### 2. Patrón: Centrado perfecto

Centrar un elemento exactamente en el centro de su contenedor:

```css
.centered-wrapper {
  display: flex;
  justify-content: center;  /* centro horizontal */
  align-items: center;      /* centro vertical */
  min-height: 100vh;        /* viewport completo */
}
```

```html
<div class="centered-wrapper">
  <div class="hero-card">Contenido centrado</div>
</div>
```

---

### 3. Patrón: Sidebar + Main

Layout de dos columnas donde el sidebar tiene ancho fijo y el main ocupa el resto:

```css
.layout {
  display: flex;
  min-height: calc(100vh - 60px); /* descontar header */
}

.sidebar {
  flex: 0 0 240px;   /* no crece, no encoge, 240px fijo */
  border-right: 1px solid #30363d;
  padding: 1.5rem;
}

.main-content {
  flex: 1;           /* ocupa todo el espacio libre */
  padding: 1.5rem;
  overflow-y: auto;
}
```

---

### 4. Patrón: Cards responsivas (Holy Grail)

Grid de cards que se adaptan automáticamente sin media queries:

```css
.cards-grid {
  display: flex;
  flex-wrap: wrap;     /* permite múltiples filas */
  gap: 1.5rem;
}

.card {
  flex: 1 1 280px;     /* base 280px, crece y encoge */
  /* Cuando el viewport es pequeño, queda 1 por fila */
  /* Cuando es grande, caben 2, 3 o más por fila */
}
```

---

### 5. Patrón: Footer pegado al fondo (sticky footer)

Footer que se mueve al fondo aunque el contenido sea corto:

```css
body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

main {
  flex: 1;  /* ocupa todo el espacio libre → empuja el footer hacia abajo */
}

footer {
  /* sin flex: el footer queda al final automáticamente */
  padding: 1rem;
}
```

---

### 6. Patrón: Ícono + texto en línea (media object)

```css
.media-object {
  display: flex;
  align-items: flex-start;  /* alinear arriba */
  gap: 1rem;
}

.media-icon {
  flex-shrink: 0;   /* el ícono no se reduce */
  width: 48px;
  height: 48px;
}

.media-body {
  flex: 1;          /* el texto ocupa el espacio restante */
}
```

---

## 📚 Recursos adicionales

- [Every Layout — Sidebar](https://every-layout.dev/layouts/sidebar/)
- [CSS-Tricks — Flexbox Patterns](https://css-tricks.com/snippets/css/a-guide-to-flexbox/#aa-prefixing-flexbox)
- [Flexbox Defense](http://www.flexboxdefense.com/) — juego online de práctica

---

## ✅ Checklist de verificación

- [ ] Puedo construir una navbar con logo y links usando `space-between`
- [ ] Puedo centrar un elemento perfectamente con `justify-content + align-items`
- [ ] Puedo crear un layout sidebar + main con `flex: 0 0 240px` y `flex: 1`
- [ ] Puedo hacer que un grid de cards sea responsive con `flex-wrap + flex: 1 1 Xpx`
- [ ] Puedo crear un sticky footer con `flex-direction: column` en el body
