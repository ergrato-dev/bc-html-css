# Ejercicio 02 — Flex Items

Aprende a controlar el comportamiento individual de cada flex item con `flex-grow`, `flex-shrink`, `flex-basis` y el shorthand `flex`.

![Propiedades Flexbox](../../0-assets/02-flex-propiedades.svg)

---

## 🎯 Objetivos

- Distribuir espacio sobrante con `flex-grow`
- Evitar el encogimiento con `flex-shrink: 0`
- Definir tamaño inicial con `flex-basis`
- Usar el shorthand `flex` correctamente
- Alinear un solo item con `align-self`
- Reordenar visualmente con `order`

---

## Paso 1: flex-grow — crecer para llenar el espacio

`flex-grow` define la proporción en que un item absorbe el espacio libre del contenedor.

```css
/* Un item con flex-grow:1 ocupa todo el espacio libre */
.main-content {
  flex-grow: 1;
}

/* flex-grow:2 ocupa el doble que flex-grow:1 */
.featured {
  flex-grow: 2;
}
```

**Abre `starter/css/styles.css`** y descomenta la sección **PASO 1**.

---

## Paso 2: flex-shrink — no encogerse nunca

`flex-shrink: 0` evita que el item se encoja cuando no hay espacio suficiente.  
Ideal para logos, avatares e iconos con tamaño fijo.

```css
.logo {
  flex-shrink: 0; /* nunca reduce su tamaño */
  width: 40px;
  height: 40px;
}

.nav-links {
  flex-grow: 1;   /* ocupa el resto */
}
```

**Descomenta** la sección **PASO 2**.

---

## Paso 3: flex-basis y shorthand flex

`flex-basis` define el tamaño inicial antes de que se distribuya el espacio libre.

```css
/* flex: grow shrink basis */
.sidebar  { flex: 0 0 240px; }  /* tamaño fijo 240px, no crece ni encoge */
.main     { flex: 1; }          /* equivale a flex: 1 1 0%  → crece */
.card     { flex: 1 1 220px; }  /* mínimo 220px + crece proporcionalmente */
```

**Descomenta** la sección **PASO 3**.

---

## Paso 4: align-self y order

`align-self` sobreescribe `align-items` para un solo item.  
`order` cambia el orden visual sin alterar el DOM (usar con precaución por accesibilidad).

```css
.highlighted {
  align-self: flex-end; /* alineado al final del eje cruzado */
}

.first-visual {
  order: -1; /* aparece antes visualmente aunque esté último en HTML */
}
```

**Descomenta** la sección **PASO 4**.

---

## ✅ Verificación

- [ ] El item con `flex-grow: 1` expande para llenar el espacio sobrante
- [ ] El logo con `flex-shrink: 0` mantiene su tamaño aunque la ventana sea pequeña
- [ ] El shorthand `flex: 1 1 220px` produce cards de tamaño adaptable
- [ ] `align-self: flex-end` mueve solo ese item al extremo
- [ ] `order: -1` lo desplaza al principio visualmente
