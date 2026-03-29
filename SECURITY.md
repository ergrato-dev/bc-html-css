# 🔒 Política de Seguridad

## Versiones Soportadas

| Versión | Soportada |
| ------- | --------- |
| main    | ✅        |

---

## Reportar una Vulnerabilidad

La seguridad de este proyecto es importante para nosotros. Si encuentras un problema de seguridad (por ejemplo, contenido malicioso en el material educativo, scripts dañinos en código de ejemplo, o vulnerabilidades en las instrucciones de código HTML/CSS), te pedimos que lo reportes de manera responsable.

### ⚠️ NO hacer público el reporte

Por favor, **NO** abras un issue público para reportar vulnerabilidades de seguridad.

### 📧 Cómo Reportar

1. **Abre un Security Advisory privado** en GitHub:
   - Ve a la pestaña **"Security"** del repositorio
   - Haz clic en **"Report a vulnerability"**
   - Completa el formulario con los detalles

2. **Incluye en tu reporte**:
   - Descripción detallada del problema
   - Archivo(s) afectado(s) y número de línea si aplica
   - Impacto potencial para los estudiantes o el proyecto
   - Sugerencias de solución (si las tienes)

### ⏱️ Tiempo de Respuesta

- **Confirmación inicial**: 48 horas
- **Evaluación**: 7 días
- **Resolución**: Dependiendo de la severidad

### 🎁 Reconocimiento

Agradecemos a todos los que reportan vulnerabilidades de manera responsable. Tu nombre será incluido en nuestros agradecimientos (si lo deseas).

---

## Mejores Prácticas en el Material Educativo

Este bootcamp enseña las siguientes prácticas de seguridad web:

### Validación de Formularios HTML

```html
<!-- ✅ Usar atributos de validación nativos -->
<input
  type="email"
  name="email"
  required
  maxlength="254"
  pattern="[^@]+@[^@]+\.[^@]+"
  autocomplete="email"
/>

<!-- ❌ Jamás confiar solo en validación del lado del cliente -->
<!-- Siempre validar en el servidor también -->
```

### Prevención de XSS en Contenido HTML

```html
<!-- ✅ Usar textContent en lugar de innerHTML cuando el contenido viene de usuarios -->
<!-- Este concepto se enseña como introducción al pensamiento de seguridad -->

<!-- ✅ Escapar caracteres especiales en atributos -->
<img src="foto.jpg" alt="Descripción segura sin &lt;script&gt;" />
```

### Atributos de Seguridad en Links

```html
<!-- ✅ Usar rel="noopener noreferrer" en links externos con target="_blank" -->
<a href="https://example.com" target="_blank" rel="noopener noreferrer">
  Recurso externo
</a>
```

### Recursos de Imágenes

```html
<!-- ✅ Siempre usar atributo alt para evitar exponer rutas internas -->
<img src="assets/images/photo.jpg" alt="Descripción de la imagen" />

<!-- ✅ Usar loading="lazy" solo para imágenes fuera del viewport inicial -->
<img src="assets/images/gallery-1.jpg" alt="Galería item 1" loading="lazy" />
```

### Privacidad en Formularios

```html
<!-- ✅ Usar autocomplete correctamente para no exponer datos sensibles -->
<input type="password" name="password" autocomplete="current-password" />

<!-- ✅ No usar autocomplete="off" indiscriminadamente (mala práctica de UX) -->
```

---

## Dependencias

Este bootcamp no tiene dependencias de paquetes npm ni sistemas de build. El material educativo usa únicamente:

- **HTML5** estático — sin dependencias de servidor
- **CSS3** puro — sin preprocesadores
- **VS Code + Live Server** — herramienta de desarrollo local

El mantenimiento de seguridad se realiza mediante:

- Revisión manual del código de ejemplo
- Validación periódica en [W3C Validator](https://validator.w3.org/)
- Auditorías del contenido educativo

---

Gracias por ayudar a mantener este proyecto seguro. 🛡️
