# Ejercicio 03 — Inspeccionar con DevTools

## Objetivo

Aprender a usar el panel **Elements** y el panel **Styles** de las DevTools del navegador
para explorar el DOM, inspeccionar estilos aplicados y editar en vivo sin tocar el código.

## Lo que practicarás

- Seleccionar un elemento con el inspector de DevTools
- Explorar el árbol DOM en el panel Elements
- Leer reglas CSS en el panel Styles (propiedades activas y tachadas)
- Modificar estilos temporalmente en el navegador
- Agregar nuevas reglas CSS desde DevTools

---

## Paso 1: Abrir DevTools e inspeccionar un elemento

Con Live Server activo y `starter/index.html` abierto en el navegador:

```
F12                        →  abre DevTools (panel completo)
Ctrl+Shift+I               →  mismo resultado
Ctrl+Shift+C               →  activa el inspector de selección directa
Clic derecho → Inspeccionar →  abre DevTools apuntando al elemento
```

Activa el inspector (`Ctrl+Shift+C`) y haz clic sobre el título `<h1>`.
DevTools seleccionará ese nodo en el árbol DOM.

**Descomenta la sección PASO 1** en `starter/index.html`.

---

## Paso 2: Explorar el árbol DOM

En el panel **Elements** verás el árbol HTML de la página. Las flechas `▶ / ▼`
expanden y colapsan nodos.

Puedes:

- **Editar texto**: doble clic sobre el texto dentro de una etiqueta
- **Cambiar atributos**: doble clic sobre el valor de un atributo (`class`, `id`, `href`)
- **Agregar atributos**: doble clic al final de la etiqueta de apertura
- **Eliminar un nodo**: seleccionarlo y presionar `Supr`
- **Duplicar un nodo**: clic derecho → Duplicate element

> ⚠️ Los cambios en DevTools son **temporales**: al recargar la página vuelven al estado original del archivo HTML.

**Descomenta la sección PASO 2** en `starter/index.html`.

---

## Paso 3: Leer el panel Styles

Al seleccionar un elemento en el panel Elements, el panel **Styles** (a la derecha o abajo)
muestra todas las reglas CSS que se aplican a ese elemento, de mayor a menor especificidad.

Cómo leer el panel Styles:

| Lo que ves | Qué significa |
| ---------- | ------------- |
| Propiedad con valor normal | Regla activa |
| Propiedad ~~tachada~~ | Sobreescrita por otra regla de mayor especificidad |
| `element.style { }` | Estilos inline aplicados directamente |
| Nombre de archivo + número de línea (ej: `styles.css:12`) | Origen de la regla |
| `user agent stylesheet` | Estilos por defecto del navegador |

**Descomenta la sección PASO 3** en `starter/index.html`.

---

## Paso 4: Modificar y agregar estilos en DevTools

Editar estilos directamente desde DevTools es útil para experimentar antes de escribir en el archivo.

```
Hacer clic sobre el valor de una propiedad   →  editar el valor
Presionar Tab dentro del panel Styles         →  avanzar al siguiente campo
Hacer clic en el espacio vacío del bloque     →  agregar nueva propiedad
Hacer clic en el "+" del panel Styles        →  agregar una nueva regla CSS
```

Practica:
1. Cambia el `font-size` del `h1` a `3rem`
2. Cambia el `color` por un color diferente (prueba: `#7ee787`)
3. Añade `text-transform: uppercase`
4. Recarga la página (`F5`) → verifica que vuelve al estado original

**Descomenta la sección PASO 4** en `starter/index.html`.

---

## Verificación final

- [ ] Puedes seleccionar cualquier elemento de la página con el inspector
- [ ] Identifies propiedades activas y tachadas en el panel Styles
- [ ] Encuentras el origen de una regla CSS (archivo + línea)
- [ ] Modificas estilos en DevTools y ves el resultado en tiempo real
- [ ] Sabes que los cambios en DevTools son temporales

> ⬇️ Sigue con [Ejercicio 04 — Debug de layout con DevTools](../04-ejercicio-debug-layout/README.md)
