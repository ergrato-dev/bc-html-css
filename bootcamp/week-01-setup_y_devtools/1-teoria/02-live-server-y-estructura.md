# Live Server y Estructura de Proyecto

## 🎯 Objetivos

- Entender por qué usar Live Server en lugar de abrir el HTML directamente
- Activar y usar Live Server correctamente desde VS Code
- Organizar los archivos de un proyecto HTML/CSS con la estructura estándar
- Conocer las convenciones de nombrado de archivos y carpetas

---

## 1. ¿Por Qué No Abrir el HTML con Doble Clic?

Cuando abres un archivo HTML haciendo doble clic, el navegador lo lee con el protocolo `file://`. Esto provoca problemas:

| `file://` ❌ | `http://localhost` ✅ |
| ------------ | --------------------- |
| Rutas relativas a veces fallan | Rutas relativas funcionan igual que en producción |
| Fuentes externas pueden bloquearse | Todos los recursos cargan correctamente |
| Sin recarga automática | Se recarga solo al guardar (`Ctrl+S`) |
| No simula un servidor real | Simula el comportamiento real de la web |

> 🔑 **Regla de oro**: siempre abre tus proyectos con Live Server, nunca con doble clic.

---

## 2. Cómo Usar Live Server

**Activar** (elige cualquiera de las tres formas):

```
1. Clic en "Go Live" en la barra de estado inferior derecha
2. Clic derecho en index.html → "Open with Live Server"
3. Ctrl+Shift+P → "Live Server: Open with Live Server"
```

El navegador se abrirá en `http://localhost:5500` y se recargará automáticamente cada vez que guardes cualquier archivo del proyecto.

**Detener**: clic en "Port: 5500" en la barra de estado inferior.

---

## 3. Estructura Estándar de Proyecto

Esta es la estructura que usaremos en todos los proyectos del bootcamp:

```
mi-proyecto/
├── index.html           ← Página principal (siempre index.html)
├── css/
│   ├── reset.css        ← Reset de estilos del navegador
│   ├── variables.css    ← CSS Custom Properties globales
│   └── styles.css       ← Estilos principales
└── assets/
    └── images/          ← Imágenes del proyecto
```

| Decisión | Razón |
| -------- | ----- |
| `index.html` en raíz | Los servidores buscan `index.html` automáticamente |
| CSS en `css/` | Separa los estilos del HTML para facilitar el mantenimiento |
| Assets en `assets/` | Agrupa todos los recursos: imágenes, fuentes, iconos |

---

## 4. Vincular CSS al HTML

El CSS externo se vincula en el `<head>` con la etiqueta `<link>`:

```html
<!DOCTYPE html>
<html lang="es">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mi Proyecto</title>
    <!-- El atributo href usa una ruta relativa desde index.html -->
    <link rel="stylesheet" href="css/styles.css" />
  </head>
  <body>
    <!-- contenido -->
  </body>
</html>
```

**Rutas relativas frecuentes:**

```
href="css/styles.css"      ✅  CSS está dentro de css/ junto a index.html
href="../css/styles.css"   ✅  CSS está un nivel arriba del HTML actual
href="/css/styles.css"     ⚠️  solo válido con un servidor con raíz definida
```

---

## 5. Convenciones de Nombrado

Usa siempre `kebab-case` (minúsculas y guiones) para archivos y carpetas:

| ✅ Correcto | ❌ Evitar |
| ----------- | --------- |
| `index.html` | `Index.HTML` |
| `styles.css` | `Styles.CSS`, `myStyles.css` |
| `hero-banner.jpg` | `HeroBanner.jpg`, `foto final.jpg` |
| `about.html` | `About.html`, `aboutMe.html` |

> 💡 Los servidores Linux distinguen mayúsculas de minúsculas. `styles.css` y `Styles.css` son archivos distintos. Minúsculas siempre evita errores al subir a producción.

---

## 6. Errores Comunes al Vincular CSS

| Síntoma | Causa probable | Solución |
| ------- | -------------- | -------- |
| Los estilos no aparecen | Ruta en `href` incorrecta | Verifica mayúsculas y separadores (`/`) |
| CSS solo aplica en una página | `<link>` falta en otras páginas | Añade `<link>` en el `<head>` de cada `.html` |
| Cambios en CSS no se reflejan | Caché del navegador | `Ctrl+Shift+R` (recarga forzada) |
| Live Server no recarga | Guardaste con otro método | Usa siempre `Ctrl+S` en VS Code |

---

## 7. Git Mínimo para el Bootcamp

Solo necesitas tres comandos desde la terminal integrada de VS Code (`Ctrl+\``):

```bash
# Inicializar repositorio en tu proyecto
git init

# Guardar un punto de control con todos los cambios
git add .
git commit -m "feat: descripción breve de lo que hiciste"

# Clonar el repositorio del bootcamp
git clone https://github.com/ergrato-dev/bc-html-css.git
```

---

## 📚 Recursos Adicionales

- [Live Server en Marketplace](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)
- [MDN — Organizar archivos de un sitio web](https://developer.mozilla.org/es/docs/Learn/Getting_started_with_the_web/Dealing_with_files)

---

## ✅ Checklist de Verificación

- [ ] Live Server instalado y funcionando
- [ ] Abriste tu proyecto con Live Server (no con doble clic)
- [ ] La página se recarga sola al guardar con `Ctrl+S`
- [ ] Creaste la estructura `index.html + css/styles.css + assets/images/`
- [ ] El CSS se aplica correctamente al HTML vía `<link>`
- [ ] Archivos y carpetas nombrados en `kebab-case`
