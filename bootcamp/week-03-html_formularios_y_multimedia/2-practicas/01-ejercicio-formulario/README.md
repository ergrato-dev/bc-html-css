# Ejercicio 01 — Formulario de Contacto

## 🎯 Objetivo

Crear un formulario de contacto accesible con todos los elementos esenciales: `<form>`, `<fieldset>`, `<legend>`, `<label>`, `<input>`, `<textarea>`, `<button>` y validación HTML5.

## 📋 Instrucciones

Abre `starter/index.html` en VS Code con Live Server y descomenta cada sección en orden.

---

### Paso 1: Estructura del formulario

Un formulario accesible necesita `action` y `method`. Aunque para este ejercicio no tenemos servidor, usar `method="post"` es la práctica correcta para datos sensibles:

```html
<form action="/enviar-mensaje" method="post" novalidate>
  <!-- novalidate aquí solo para poder testear los campos sin servidor -->
</form>
```

**Descomenta** el `PASO 1`.

---

### Paso 2: Fieldset con datos personales

```html
<fieldset>
  <legend>Información personal</legend>

  <label for="nombre">Nombre completo *</label>
  <input type="text" id="nombre" name="nombre" required
         minlength="3" maxlength="80"
         placeholder="Ej: Ana García" autocomplete="name" />
</fieldset>
```

El `*` indica campo obligatorio; también se indica con `required` en el input.

**Descomenta** el `PASO 2`.

---

### Paso 3: Fieldset con datos de contacto

```html
<label for="email">Correo electrónico *</label>
<input type="email" id="email" name="email"
       required placeholder="tu@correo.com" autocomplete="email" />

<label for="telefono">Teléfono (opcional)</label>
<input type="tel" id="telefono" name="telefono"
       placeholder="+52 123 456 7890" autocomplete="tel" />
```

**Descomenta** el `PASO 3`.

---

### Paso 4: Fieldset con el mensaje y botón

```html
<label for="asunto">Asunto *</label>
<select id="asunto" name="asunto" required>
  <option value="">— Selecciona el asunto —</option>
  <option value="consulta">Consulta general</option>
  <option value="soporte">Soporte técnico</option>
</select>

<label for="mensaje">Mensaje *</label>
<textarea id="mensaje" name="mensaje" rows="5"
          required minlength="10" maxlength="500"
          placeholder="Escribe tu mensaje aquí..."></textarea>

<button type="submit">Enviar mensaje</button>
```

**Descomenta** el `PASO 4`.

---

## ✅ Verificación

- [ ] El formulario tiene `action` y `method`
- [ ] Cada campo tiene `<label>` con `for` = `id` del input
- [ ] Los campos obligatorios tienen `required`
- [ ] El tipo de input es correcto (email, tel, text)
- [ ] El botón usa `<button type="submit">`, no `<input type="submit">`
- [ ] El formulario agrupa campos en `<fieldset>` con `<legend>`
