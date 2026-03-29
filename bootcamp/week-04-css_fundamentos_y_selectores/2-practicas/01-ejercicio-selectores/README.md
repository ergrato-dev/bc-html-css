# Ejercicio 01 — Selectores CSS

## 🎯 Objetivo

Practicar selectores de tipo, clase, ID, atributo, combinadores y pseudo-clases para apuntar a elementos HTML con precisión.

## 📋 Instrucciones

Abre `starter/index.html` y `starter/css/styles.css` en VS Code con Live Server activo. Descomenta cada bloque siguiendo los pasos del README.

---

## Paso 1: Selectores básicos (tipo, clase, ID)

Seleccionamos elementos por su nombre de etiqueta, clase o identificador único.

```css
/* Selector de tipo: aplica a todos los párrafos */
p {
  color: #c9d1d9;
  line-height: 1.6;
}

/* Selector de clase: aplica a cualquier elemento con class="highlight" */
.highlight {
  background-color: #264de4;
  color: white;
}

/* Selector de ID: aplica solo al elemento con id="main-title" */
#main-title {
  font-size: 2rem;
  color: #58a6ff;
}
```

**Abre `starter/css/styles.css`** y descomenta el bloque `/* PASO 1 */`.

---

## Paso 2: Selectores de atributo

Seleccionamos elementos según el valor de sus atributos HTML.

```css
/* Todos los enlaces externos */
a[href^="https"] {
  color: #3fb950;
}

/* Todos los inputs de tipo email */
input[type="email"] {
  border-color: #264de4;
}

/* Imágenes con alt que contiene "logo" */
img[alt*="logo"] {
  width: 120px;
}
```

**Descomenta el bloque `/* PASO 2 */`** en `styles.css`.

---

## Paso 3: Combinadores

Los combinadores expresan relaciones entre elementos: descendiente, hijo directo, hermano adyacente y hermano general.

```css
/* Descendiente: cualquier <a> dentro de <nav> */
nav a {
  text-decoration: none;
  padding: 0.5rem 1rem;
}

/* Hijo directo: solo <li> directos de <ul class="menu"> */
ul.menu > li {
  display: inline-block;
}

/* Hermano adyacente: el primer <p> inmediatamente después de <h2> */
h2 + p {
  margin-top: 0.25rem;
  font-style: italic;
}
```

**Descomenta el bloque `/* PASO 3 */`** en `styles.css`.

---

## Paso 4: Pseudo-clases de estado

Las pseudo-clases aplican estilos según el estado interactivo del elemento.

```css
/* Hover sobre botones */
.btn:hover {
  opacity: 0.85;
  transform: translateY(-2px);
}

/* Focus visible para accesibilidad */
.btn:focus-visible {
  outline: 3px solid #58a6ff;
  outline-offset: 2px;
}

/* Enlace ya visitado */
a:visited {
  color: #8b949e;
}
```

**Descomenta el bloque `/* PASO 4 */`** en `styles.css`.

---

## ✅ Verificación

- [ ] Los párrafos tienen color `#c9d1d9` y line-height 1.6
- [ ] El elemento con `.highlight` tiene fondo azul
- [ ] El `#main-title` es de color azul claro y tamaño 2rem
- [ ] Los links externos (`https://`) se muestran en verde
- [ ] Los items del menú se muestran en línea horizontal
- [ ] El botón cambia al hacer hover
