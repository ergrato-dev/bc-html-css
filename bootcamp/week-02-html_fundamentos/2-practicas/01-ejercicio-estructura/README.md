# Ejercicio 01 — Estructura HTML5

## Objetivo

Crear un documento HTML5 completo con estructura semántica, descomentando bloque por bloque
para entender el rol de cada zona.

## Paso 1: DOCTYPE y `<html>`

El DOCTYPE le dice al navegador que use el estándar HTML5. Sin él, el navegador entra en "quirks mode".

```html
<!DOCTYPE html>
<html lang="es">
</html>
```

**Descomenta la sección PASO 1** en `starter/index.html`.

---

## Paso 2: El `<head>` y sus etiquetas obligatorias

```html
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Página de ejemplo</title>
</head>
```

**Descomenta la sección PASO 2**.

---

## Paso 3: Etiquetas semánticas del `<body>`

```html
<body>
  <header>…</header>
  <nav>…</nav>
  <main>
    <section>…</section>
  </main>
  <footer>…</footer>
</body>
```

**Descomenta la sección PASO 3**.

---

## Paso 4: Validación W3C

Copia el HTML completo y pégalo en [https://validator.w3.org/](https://validator.w3.org/) usando la opción "Validate by Direct Input". Verifica que no aparecen errores en rojo.

**Descomenta la sección PASO 4**.

---

## Verificación final

- [ ] El documento tiene DOCTYPE, html, head, body
- [ ] `<html lang="es">` presente
- [ ] `<meta charset>` y `<meta viewport>` en head
- [ ] Estructura semántica: header, nav, main, footer
- [ ] Sin errores en W3C Validator
