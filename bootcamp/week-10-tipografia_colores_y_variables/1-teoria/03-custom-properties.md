# CSS Custom Properties, calc() y Sistemas de Diseño

## 🎯 Objetivos

- Declarar y consumir CSS Custom Properties (variables CSS)
- Entender el scope, herencia y fallbacks de las variables
- Usar `calc()` para valores dinámicos
- Construir un sistema de design tokens coherente

---

## 1. CSS Custom Properties — ¿Qué son?

Las CSS Custom Properties son propiedades que tú defines y que pueden almacenar cualquier valor CSS. Se acceden con `var()`.

```css
/* Declaración: empieza con -- */
:root {
  --color-primary: hsl(225, 73%, 52%);
  --font-size-base: 1rem;
  --spacing-md: 1.5rem;
}

/* Uso: var(--nombre-variable) */
.btn {
  background: var(--color-primary);
  font-size: var(--font-size-base);
  padding: var(--spacing-md);
}
```

---

## 2. Scope y Herencia

Las variables CSS siguen el cascado normal: se heredan de padres a hijos.

```css
/* Global: disponible en todo el documento */
:root {
  --color-text: hsl(215, 25%, 10%);
}

/* Local: solo disponible en .card y sus descendientes */
.card {
  --card-bg: hsl(220, 14%, 97%);
  background: var(--card-bg);
}

/* ✅ Funciona — es descendiente de .card */
.card .card-title {
  color: var(--card-bg); /* hereda de .card */
}

/* ❌ No funciona — no es descendiente de .card */
.nav {
  background: var(--card-bg); /* undefined */
}
```

---

## 3. Fallbacks

`var()` acepta un segundo argumento: el valor de respaldo si la variable no existe.

```css
:root {
  /* Sin declarar --color-accent */
}

.badge {
  /* Si --color-accent no existe, usa el fallback */
  background: var(--color-accent, hsl(38, 92%, 50%));

  /* Fallbacks encadenados */
  color: var(--color-badge-text, var(--color-text, hsl(0, 0%, 0%)));
}
```

---

## 4. Override por contexto — Tema oscuro

La forma canónica de implementar modo oscuro con CSS Custom Properties:

```css
/* Modo claro (por defecto) */
:root {
  --color-bg: hsl(0, 0%, 100%);
  --color-surface: hsl(220, 14%, 97%);
  --color-text: hsl(215, 25%, 10%);
  --color-text-muted: hsl(215, 15%, 45%);
  --color-border: hsl(215, 20%, 88%);
}

/* Modo oscuro: redefine las mismas variables */
@media (prefers-color-scheme: dark) {
  :root {
    --color-bg: hsl(215, 28%, 8%);
    --color-surface: hsl(215, 25%, 12%);
    --color-text: hsl(215, 20%, 95%);
    --color-text-muted: hsl(215, 15%, 55%);
    --color-border: hsl(215, 20%, 22%);
  }
}

/* Toda la UI usa var() → el tema cambia automáticamente */
body {
  background: var(--color-bg);
  color: var(--color-text);
}
```

---

## 5. Escala tipográfica modular

Una **escala modular** multiplica cada nivel por una razón constante. La razón `1.25` (Major Third) da una progresión elegante:

| Nivel | Factor | Fórmula | Valor |
|---|---|---|---|
| xs | base ÷ 1.25² | 1 / 1.5625 | ≈ 0.64rem |
| sm | base ÷ 1.25 | 1 / 1.25 | 0.8rem |
| base | 1× | 1rem | 1rem |
| md | 1.25× | ×1.25 | 1.25rem |
| lg | 1.563× | ×1.25² | 1.563rem |
| xl | 1.953× | ×1.25³ | 1.953rem |
| 2xl | 2.441× | ×1.25⁴ | 2.441rem |
| 3xl | 3.052× | ×1.25⁵ | 3.052rem |

```css
:root {
  --text-xs:   0.64rem;
  --text-sm:   0.8rem;
  --text-base: 1rem;
  --text-md:   1.25rem;
  --text-lg:   1.563rem;
  --text-xl:   1.953rem;
  --text-2xl:  2.441rem;
  --text-3xl:  3.052rem;
}
```

---

## 6. `calc()` — Cálculos dinámicos

`calc()` permite combinar unidades diferentes y expresar relaciones matemáticas:

```css
/* Mezclar unidades */
.sidebar {
  width: calc(100% - var(--sidebar-width));
}

/* Offset de header fijo */
.hero {
  min-height: calc(100vh - var(--header-height));
}

/* Padding proporcional */
.container {
  padding: 0 calc(var(--spacing-md) * 1.5);
}

/* Columnas con gap incluido */
.col {
  width: calc(50% - var(--gap) / 2);
}

/* Con variables matemáticas */
:root {
  --type-ratio: 1.25;
  --text-base: 1rem;
  --text-md:   calc(var(--text-base) * var(--type-ratio));        /* 1.25rem */
  --text-lg:   calc(var(--text-md)   * var(--type-ratio));        /* 1.5625rem */
}
```

---

## 7. Sistema de Design Tokens

Un **design token** es una variable CSS con nombre semántico que representa una decisión de diseño.

```css
:root {
  /* ── PRIMITIVOS ────────────────────────────── */
  /* Colores — valores brutos */
  --primitive-blue-500: hsl(225, 73%, 52%);
  --primitive-blue-700: hsl(225, 73%, 35%);
  --primitive-gray-100: hsl(215, 20%, 95%);
  --primitive-gray-900: hsl(215, 25%, 10%);

  /* ── SEMÁNTICOS ────────────────────────────── */
  /* Colores de mark */
  --color-primary:       var(--primitive-blue-500);
  --color-primary-hover: var(--primitive-blue-700);
  --color-text:          var(--primitive-gray-900);
  --color-bg:            var(--primitive-gray-100);

  /* Tipografía */
  --font-family-body: 'Inter', system-ui, sans-serif;
  --font-size-base: 1rem;
  --font-weight-regular: 400;
  --font-weight-bold: 700;
  --line-height-normal: 1.6;

  /* Espaciados — t-shirt sizes */
  --space-1: 0.25rem;
  --space-2: 0.5rem;
  --space-3: 0.75rem;
  --space-4: 1rem;
  --space-6: 1.5rem;
  --space-8: 2rem;
  --space-12: 3rem;
  --space-16: 4rem;

  /* Borders */
  --border-radius-sm:  4px;
  --border-radius-md:  8px;
  --border-radius-lg:  12px;
  --border-radius-full: 9999px;

  --border-width:  1px;
  --border-color:  hsl(215, 20%, 88%);

  /* Sombras */
  --shadow-sm: 0 1px 3px hsl(0 0% 0% / 0.08);
  --shadow-md: 0 4px 12px hsl(0 0% 0% / 0.12);
}
```

### Beneficios

- **Consistencia:** toda la UI usa los mismos valores
- **Mantenibilidad:** cambiar un token actualiza toda la interfaz
- **Tema:** redefinir en `@media (prefers-color-scheme: dark)` cambia todo a la vez
- **Documentación:** el código se auto-documenta con nombres semánticos

---

## ✅ Checklist de Verificación

- [ ] Variables con nombres semánticos (`--color-primary`, no `--azul`)
- [ ] Primitivos separados de semánticos en `:root`
- [ ] `var()` en todas las propiedades reutilizables
- [ ] Fallbacks en variables críticas
- [ ] `calc()` para relaciones matemáticas, no valores hard-coded
- [ ] Escala tipográfica modular declarada como variables
- [ ] Override en `@media (prefers-color-scheme: dark)`

## 📚 Recursos Adicionales

- MDN — Using CSS custom properties: https://developer.mozilla.org/es/docs/Web/CSS/Using_CSS_custom_properties
- MDN — calc(): https://developer.mozilla.org/es/docs/Web/CSS/calc
- Style Dictionary (tokens en JSON): https://styledictionary.com/
- Open Props (sistema de tokens open source): https://open-props.style/
