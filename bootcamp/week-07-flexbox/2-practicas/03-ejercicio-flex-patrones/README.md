# Ejercicio 03 — Flex Patrones

Aplica Flexbox a los patrones de layout más comunes en el desarrollo web real: navbar, centrado, sidebar+main, cards responsive y sticky footer.

---

## 🎯 Objetivos

- Construir una barra de navegación con `space-between`
- Centrar contenido horizontalmente y verticalmente
- Crear un layout sidebar + contenido principal
- Hacer cards adaptables con `flex-wrap`
- Implementar un sticky footer con `min-height: 100vh`

---

## Paso 1: Navbar con justify-content: space-between

El patrón más frecuente: logo a la izquierda, navegación a la derecha.

```css
.navbar {
  display: flex;
  justify-content: space-between; /* logo ←——————→ nav */
  align-items: center;
  padding: 0 1.5rem;
  height: 60px;
}
```

**Abre `starter/css/styles.css`** y descomenta la sección **PASO 1**.

---

## Paso 2: Centrado perfecto

Centrar un elemento en toda la pantalla, tanto horizontal como verticalmente.

```css
.hero-section {
  display: flex;
  justify-content: center;
  align-items: center;
  min-height: 50vh; /* al menos 50% de la ventana */
  text-align: center;
}
```

**Descomenta** la sección **PASO 2**.

---

## Paso 3: Sidebar + Main Content

Layout de dos columnas: sidebar de ancho fijo y contenido principal que ocupa el resto.

```css
.layout {
  display: flex;
  gap: 1.5rem;
}

.sidebar  { flex: 0 0 220px; } /* tamaño fijo, no crece ni encoge */
.main     { flex: 1; }          /* ocupa todo el espacio restante */
```

**Descomenta** la sección **PASO 3**.

---

## Paso 4: Cards responsivas + Sticky Footer

Cards que se adaptan con `flex-wrap` y footer fijo al fondo de la página.

```css
/* Cards responsivas */
.card-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
}
.card { flex: 1 1 200px; } /* mínimo 200px, crece para llenar */

/* Sticky footer */
body {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}
main  { flex: 1; }   /* empuja el footer al fondo */
```

**Descomenta** la sección **PASO 4**.

---

## ✅ Verificación

- [ ] Navbar: logo fijo a la izquierda, links a la derecha
- [ ] Hero: El bloque de texto está centrado vertical y horizontalmente
- [ ] Sidebar de 220px fijo; el main ocupa el resto
- [ ] Cards saltan de línea cuando no caben y mantienen `gap` consistente
- [ ] Footer siempre visible al fondo aunque haya poco contenido
