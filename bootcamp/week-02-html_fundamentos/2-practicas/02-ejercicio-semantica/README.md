# Ejercicio 02 — HTML Semántico vs Divitis

## Objetivo

Transformar código con "divitis" (uso excesivo de `<div>`) en HTML semántico correcto,
descomentando la versión mejorada bloque por bloque.

## Paso 1: Identifica el problema — divitis

```html
<!-- ❌ Divitis: sin semántica -->
<div class="header">
  <div class="nav">
    <div class="nav-item"><a href="#inicio">Inicio</a></div>
  </div>
</div>
<div class="main-content">
  <div class="section">
    <div class="title">Mi Blog</div>
    <div class="post">Texto del post...</div>
  </div>
</div>
```

**Descomenta la sección PASO 1** para ver el problema visualmente.

---

## Paso 2: La solución semántica

```html
<!-- ✅ Semántico -->
<header>
  <nav>
    <ul>
      <li><a href="#inicio">Inicio</a></li>
    </ul>
  </nav>
</header>
<main>
  <section>
    <h1>Mi Blog</h1>
    <article>Texto del post...</article>
  </section>
</main>
```

**Descomenta la sección PASO 2** para comparar las dos versiones.

---

## Paso 3: Semántica en el footer

**Descomenta la sección PASO 3**.

---

## Verificación

- [ ] Identificas qué etiqueta semántica reemplaza a cada `<div>`
- [ ] Sabes cuándo sí corresponde usar `<div>` (cuando no hay etiqueta semántica adecuada)
