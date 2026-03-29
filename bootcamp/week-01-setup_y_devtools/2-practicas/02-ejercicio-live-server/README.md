# Ejercicio 02 — Tu primera página con Live Server

## Objetivo

Crear un proyecto HTML desde cero, abrirlo con Live Server y verificar que los cambios
en el editor se reflejan al instante en el navegador.

## Lo que practicarás

- Crear la estructura de carpetas de un proyecto web real
- Vincular un archivo CSS externo con `<link>`
- Activar Live Server y verificar la URL `localhost:5500`
- Editar HTML y CSS y observar la recarga automática

---

## Paso 1: Estructura del proyecto

Un proyecto web bien organizado separa el HTML, el CSS y los recursos visuales:

```
mi-primera-pagina/
├── index.html          ← página principal
├── css/
│   └── styles.css      ← estilos globales
└── assets/
    └── images/         ← imágenes optimizadas
```

La carpeta `starter/` de este ejercicio ya tiene esa estructura.

**Abre VS Code** apuntando a la carpeta `starter/` como raíz del proyecto.

**Descomenta la sección PASO 1** en `starter/index.html`.

---

## Paso 2: Vincular el CSS con `<link>`

Para conectar un archivo CSS externo, usamos la etiqueta `<link>` dentro de `<head>`:

```html
<link rel="stylesheet" href="css/styles.css" />
```

Atributos obligatorios:
- `rel="stylesheet"` → indica que es una hoja de estilos
- `href="ruta/al/archivo.css"` → ruta relativa desde el HTML

**Descomenta la sección PASO 2** en `starter/index.html`.

---

## Paso 3: Activar Live Server

Tres formas de iniciar Live Server:

1. **Botón en la barra de estado**: haz clic en `⚡ Go Live` (esquina inferior derecha)
2. **Clic derecho** sobre `index.html` en el Explorer → _Open with Live Server_
3. **Command Palette**: `Ctrl+Shift+P` → escribe `Live Server: Open with Live Server`

Verifica que el navegador abre `http://localhost:5500/`.

**Descomenta la sección PASO 3** en `starter/index.html` y observa el resultado.

---

## Paso 4: Editar en vivo

La magia de Live Server es que cada cambio guardado (`Ctrl+S`) se refleja de inmediato.

Prueba:

1. Cambia el texto del `<h1>` en `index.html` y guarda → el navegador se actualiza
2. Cambia el `color` del `h1` en `css/styles.css` y guarda → el color cambia en vivo
3. Añade una nueva regla en `styles.css` → efecto inmediato sin recargar manualmente

**Descomenta la sección PASO 4** en `starter/index.html`.

---

## Verificación final

- [ ] El proyecto abre en `http://localhost:5500/` (no en `file://`)
- [ ] Los estilos CSS se aplican correctamente
- [ ] Al modificar y guardar, el navegador se actualiza automáticamente
- [ ] Sin errores en la consola de DevTools (`F12` → pestaña Console)

> ⬇️ Sigue con [Ejercicio 03 — Inspeccionar con DevTools](../03-ejercicio-devtools-inspect/README.md)
