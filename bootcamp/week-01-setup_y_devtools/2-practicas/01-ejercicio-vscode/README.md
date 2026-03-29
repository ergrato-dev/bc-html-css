# Ejercicio 01 — Configura tu entorno de desarrollo

## Objetivo

Dejar VS Code completamente listo para trabajar: extensiones instaladas, configuración optimizada y un proyecto HTML de prueba funcionando.

## Lo que practicarás

- Instalar extensiones esenciales en VS Code
- Configurar `settings.json` con las opciones recomendadas
- Crear un archivo `.prettierrc` para formateo automático
- Verificar que Emmet funciona con el atajo `!` + `Tab`

---

## Paso 1: Instalar las extensiones esenciales

Abre VS Code. Presiona `Ctrl+Shift+X` para abrir el panel de extensiones.

Busca e instala cada extensión por su **ID exacto** (cópialo en la caja de búsqueda):

```
ritwickdey.LiveServer
esbenp.prettier-vscode
ecmel.vscode-html-css
formulahendry.auto-rename-tag
usernamehw.errorlens
```

> Para verificar que quedaron instaladas: `Ctrl+Shift+X` → pestaña **Installed**.

**Abre `starter/index.html`** y descomenta la sección marcada como PASO 1.

---

## Paso 2: Configurar settings.json

VS Code guarda sus ajustes en un archivo JSON. Lo abrimos con el Command Palette.

```
Presiona: Ctrl+Shift+P
Escribe: Open User Settings (JSON)
Selecciona la opción que aparece
```

El bloque de configuración que debes pegar es:

```json
{
  "editor.formatOnSave": true,
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  "editor.tabSize": 2,
  "editor.wordWrap": "on",
  "editor.fontSize": 14,
  "files.autoSave": "onFocusChange",
  "liveServer.settings.donotShowInfoMsg": true,
  "emmet.includeLanguages": {
    "html": "html"
  }
}
```

**Descomenta la sección PASO 2** en `starter/index.html`.

---

## Paso 3: Crear el archivo .prettierrc

`.prettierrc` define las reglas de formateo del proyecto. Lo creamos en la raíz.

```json
{
  "printWidth": 120,
  "tabWidth": 2,
  "singleQuote": false,
  "trailingComma": "es5"
}
```

Crea el archivo en la misma carpeta donde está `index.html` y pega el contenido.

> Guarda cualquier archivo HTML para comprobar que Prettier lo formatea automáticamente.

**Descomenta la sección PASO 3** en `starter/index.html`.

---

## Paso 4: Generar la plantilla HTML con Emmet

Emmet es el sistema de autocompletado de código integrado en VS Code. El atajo más poderoso:

```
! → Tab    →    genera la plantilla HTML5 completa
```

Otros atajos útiles:

```
h1          → Tab  →  <h1></h1>
p.intro     → Tab  →  <p class="intro"></p>
ul>li*3     → Tab  →  <ul> con 3 <li>
a[href="#"] → Tab  →  <a href="#"></a>
```

**Descomenta la sección PASO 4** en `starter/index.html` para ver la plantilla generada.

---

## Verificación final

Cuando termines, tu `starter/index.html` debe:

- [ ] Mostrar el contenido de los 4 pasos descomentado correctamente
- [ ] Validar sin errores en [https://validator.w3.org/](https://validator.w3.org/) (opción "Validate by Direct Input")
- [ ] VS Code tiene las 5 extensiones instaladas y visibles en la pestaña Installed

> ⬇️ Sigue con [Ejercicio 02 — Primera página con Live Server](../02-ejercicio-live-server/README.md)
