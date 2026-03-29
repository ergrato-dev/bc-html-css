# Ejercicio 03 — Keyframe Animations

Crea tres animaciones de entrada clásicas y un spinner infinito usando `@keyframes` y la propiedad `animation`.

---

## 🎯 Objetivos

- Definir `@keyframes` con `from / to` y con porcentajes
- Usar `animation-fill-mode: forwards` para mantener el estado final
- Crear un spinner con `animation: spin infinite linear`
- Ver animaciones escalonadas con `animation-delay`

---

## PASO 1 — @keyframes fade-in

Define la animación de opacidad de 0 a 1:

```css
@keyframes fade-in {
  from { opacity: 0; }
  to   { opacity: 1; }
}

.fade-card {
  opacity: 0; /* estado inicial antes de que empiece la animación */
  animation: fade-in 500ms ease-out forwards;
}
```

**Abre `starter/css/styles.css`** y descomenta la sección PASO 1.

---

## PASO 2 — @keyframes slide-up

Combina opacidad con movimiento vertical:

```css
@keyframes slide-up {
  from {
    opacity:   0;
    transform: translateY(20px);
  }
  to {
    opacity:   1;
    transform: translateY(0);
  }
}

.slide-card {
  opacity: 0;
  animation: slide-up 500ms ease-out forwards;
}
```

**Descomenta** PASO 2. Observa la diferencia vs fade-in.

---

## PASO 3 — Spinner infinito

Un loader que gira sin parar:

```css
@keyframes spin {
  from { transform: rotate(0deg); }
  to   { transform: rotate(360deg); }
}

.spinner {
  animation: spin 800ms linear infinite;
}
```

**Descomenta** PASO 3.

---

## PASO 4 — Entrada escalonada con animation-delay

Cada tarjeta entra con un retraso progresivo:

```css
.stagger-card:nth-child(1) { animation-delay: 0ms; }
.stagger-card:nth-child(2) { animation-delay: 150ms; }
.stagger-card:nth-child(3) { animation-delay: 300ms; }
```

**Descomenta** PASO 4. Recarga la página para ver la secuencia de entradas.
