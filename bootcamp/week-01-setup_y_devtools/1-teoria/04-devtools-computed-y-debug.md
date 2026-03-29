# DevTools: Computed, Console y Debug de Layout

## 🎯 Objetivos

- Entender la diferencia entre el panel Styles y el panel Computed
- Leer valores finales de CSS después de la cascada y herencia
- Usar la consola para detectar errores del navegador
- Depurar problemas comunes de layout con DevTools

---

## 1. Panel Computed: El CSS Final Real

Mientras el panel **Styles** muestra todas las reglas que *intentan* aplicarse al elemento, el panel **Computed** muestra los **valores finales calculados** que el navegador realmente usa para renderizar el elemento.

### Diferencia clave

```
Panel Styles                        Panel Computed
─────────────────────────────────── ────────────────────────────────────
Muestra TODAS las reglas CSS        Muestra UN SOLO valor por propiedad
Puede haber conflictos y tachados   Es el resultado final calculado
Muestra de dónde viene cada regla   Sin duplicados ni conflictos
Los valores pueden ser relativos    Los valores siempre son absolutos (px)
```

### Cuándo usar Computed

- Conocer el tamaño real en píxeles de un elemento (aunque uses `rem` o `%`)
- Ver qué valor de `font-size` heredó un elemento de su padre
- Confirmar el color final cuando la cascada tiene múltiples reglas en conflicto
- Verificar `margin`, `padding` y `border` con valores absolutos

### Cómo abrirlo

```
Panel Elements seleccionado → Pestaña "Computed" (junto a "Styles")
```

Haz clic en cualquier propiedad del panel Computed para ver **de qué regla CSS proviene** ese valor.

---

## 2. Panel Console: Errores y Mensajes

La **consola** es la ventana directa al motor del navegador. Muestra:

| Tipo de mensaje | Icono | Significado |
| --------------- | ----- | ----------- |
| **Error** | 🔴 | Algo falló (archivo no encontrado, sintaxis rota) |
| **Warning** | 🟡 | Algo funciona pero puede causar problemas |
| **Info** | 🔵 | Mensaje informativo del navegador |

### Errores más comunes en HTML/CSS

```
❌ Failed to load resource: net::ERR_FILE_NOT_FOUND
   → Un archivo referenciado (CSS, imagen) no existe o la ruta es incorrecta

❌ Failed to load resource: 404 (Not Found)
   → El archivo existe pero la URL es incorrecta (mayúsculas, typo)

⚠️ Quirks Mode
   → Falta el DOCTYPE. Agrega <!DOCTYPE html> al inicio del HTML

⚠️ <link rel="stylesheet"> not applied — MIME type mismatch
   → El archivo CSS tiene extensión incorrecta o la ruta apunta a otro tipo
```

> 💡 **Hábito clave**: abre siempre la consola antes de reportar un bug. El 80% de los problemas tienen un mensaje de error claro esperándote ahí.

---

## 3. Depurar Problemas de Layout

Estos son los problemas más frecuentes al empezar a trabajar con CSS y cómo identificarlos con DevTools:

### El elemento no ocupa el espacio esperado

```
1. Selecciona el elemento con el inspector
2. En el panel Computed, revisa width y height
3. Compara con el resalte visual del Box Model en la página
→ Si el padding está comiendo espacio: box-sizing puede ser la causa
```

### El CSS no se aplica

```
1. Abre la consola → ¿hay error 404 en el archivo CSS?
2. Revisa el <link> en el <head> del HTML
3. En el panel Styles → ¿la regla aparece tachada?
   → Si está tachada, otra regla con mayor especificidad la anula
4. ¿La regla no aparece en absoluto?
   → El selector no coincide con el elemento seleccionado
```

### Un elemento se "escapa" del contenedor

```
1. Selecciona el contenedor
2. En Styles, busca overflow: visible (valor por defecto)
3. Cambia temporalmente a overflow: hidden para confirmar
   → Si el elemento desaparece, estaba desbordando el contenedor
```

---

## 4. Modo Responsive en DevTools

DevTools incluye un **emulador de dispositivos** para ver la página en distintos tamaños:

```
Cómo activarlo:
  Icono de dispositivos 📱 (en la barra superior de DevTools)
  o  Ctrl+Shift+M

Qué permite:
  - Seleccionar dispositivos predefinidos (iPhone, iPad, etc.)
  - Escribir dimensiones personalizadas de ancho × alto
  - Ver la página como la vería un usuario móvil
```

> 💡 El modo responsive se usará intensivamente en la Semana 9 (Media Queries). Por ahora, úsalo para ver cómo cambia tu layout al reducir el ancho de la ventana.

---

## 5. Truco: Forzar Estado CSS (:hover, :focus)

DevTools puede forzar pseudo-clases sin mover el cursor:

```
1. Selecciona el elemento
2. En el panel Styles → clic en ":hov" (barra de herramientas superior del panel)
3. Marca :hover, :focus, :active o :visited
→ El elemento mantiene ese estado aunque el cursor no esté encima
```

Esto es útil para inspeccionar los estilos de un menú desplegable o un botón al pasar el cursor.

---

## 📚 Recursos Adicionales

- [Chrome DevTools — Console overview](https://developer.chrome.com/docs/devtools/console/)
- [MDN — Examinar valores Computed](https://developer.mozilla.org/es/docs/Tools/Page_Inspector/How_to/Examine_and_edit_CSS#examining_computed_css)
- [Chrome DevTools — Depurar CSS](https://developer.chrome.com/docs/devtools/css/)

---

## ✅ Checklist de Verificación

- [ ] Sabes abrir el panel Computed y entiendes que muestra el valor final
- [ ] Puedes leer el tamaño real en px de un elemento usando Computed
- [ ] Abres la consola y sabes distinguir errores (rojo) de warnings (amarillo)
- [ ] Puedes identificar en el panel Styles cuando una regla está tachada (sobreescrita)
- [ ] Sabes activar el modo responsive con `Ctrl+Shift+M`
- [ ] Puedes forzar el estado `:hover` en un elemento desde el panel Styles
