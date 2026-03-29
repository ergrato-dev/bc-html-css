# Ejercicio 01 — Hover Transitions

Practica transiciones suaves usando `transition` y tokens CSS para efectos de hover en tarjetas y botones.

---

## 🎯 Objetivos

- Declarar tokens de duración y easing en `:root`
- Aplicar `transition` a propiedades específicas (no `all`)
- Crear el efecto "card lift" con `translateY` y `box-shadow`
- Animar botones con cambio de color y escala

---

## PASO 1 — Tokens de transición en `:root`

Declara las variables de tiempo y función de easing que usarás en toda la página:

```css
/* Tokens de transición */
:root {
  --duration-fast:       150ms;
  --duration-base:       200ms;
  --ease-out:            ease-out;
  --transition-base:     var(--duration-base) var(--ease-out);
  --transition-elevation:
    transform  var(--duration-base) var(--ease-out),
    box-shadow var(--duration-base) var(--ease-out);
}
```

**Abre `starter/css/styles.css`** y descomenta la sección PASO 1.

---

## PASO 2 — Card lift effect

Aplica la transición de elevación a `.feature-card` y define el estado hover:

```css
/* Base: sin transformación */
.feature-card {
  transition: var(--transition-elevation);
}

/* Hover: sube 4px y proyecta sombra mayor */
.feature-card:hover {
  transform:  translateY(-4px);
  box-shadow: var(--shadow-lg);
}
```

**Descomenta** la sección PASO 2 en `styles.css`.

---

## PASO 3 — Botón con color y escala

Transiciona el color de fondo y aplica `scale` al hacer hover/press:

```css
.btn-primary {
  transition:
    background var(--transition-base),
    transform  var(--duration-fast) var(--ease-out);
}
.btn-primary:hover  { background: var(--blue-700); }
.btn-primary:active { transform: scale(0.96); }
```

**Descomenta** la sección PASO 3 en `styles.css`.

---

## PASO 4 — Estado focus accesible

Agrega un estado `:focus-visible` que no interfiera con el hover:

```css
.btn-primary:focus-visible {
  outline:        2px solid var(--color-primary);
  outline-offset: 3px;
}
```

**Descomenta** la sección PASO 4 en `styles.css`. Verifica con Tab que el foco es visible.
