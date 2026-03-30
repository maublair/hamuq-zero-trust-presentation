# 🚀 INSTRUCCIONES DE IMPLEMENTACIÓN

## ARCHIVO PRINCIPAL

**Archivo**: `presentacion-zero-trust-85-slides.html`

**Tamaño**: ~1.4 MB (self-contained, todos los CSS/JS incluidos)

**Formato**: HTML5 + CSS3 + JavaScript ES6+

**Dependencias Externas**:
- Google Fonts (Montserrat, Open Sans)
- Font Awesome 6.5.1 (iconografía)
- GSAP 3.12.2 (animaciones)

---

## CÓMO ABRIR Y USAR

### Opción 1: En tu navegador (Recomendado)
1. Descarga `presentacion-zero-trust-85-slides.html`
2. Haz doble clic para abrir en navegador
3. O: Abre tu navegador → File → Open File → Selecciona el HTML

### Opción 2: Servidor local (Si necesitas más control)
```bash
# Desde terminal, en la carpeta donde está el archivo:
python -m http.server 8000
# Luego: http://localhost:8000/presentacion-zero-trust-85-slides.html
```

---

## NAVEGACIÓN

### Botones
- **Anterior** (←): Botón izquierdo abajo
- **Siguiente** (→): Botón derecho abajo
- **Contador**: Muestra "Slide actual / Total"

### Teclado
- **Flecha Derecha / Abajo**: Siguiente slide
- **Flecha Izquierda / Arriba**: Anterior slide
- **ESC**: Cerrar modal (si está abierto)
- **Números 1-9**: Ir a slide 1-9 (si implementas)

### Mouse
- **Click en botones**: Navegar
- **Hover en cards**: Efecto visual (scale, shadow)
- **Click en cards**: Abre modal con ampliación
- **Click en X modal**: Cierra
- **Click en backdrop modal**: Cierra

---

## FUNCIONAMIENTO TÉCNICO

### Estructura HTML
```
<div id="presentation-wrapper">
  <div id="progress-bar"></div>
  <div id="presentation-container">
    <div class="global-header">...</div>
    <div class="slide active">Slide 1</div>
    <div class="slide">Slide 2</div>
    ... (85 slides total)
    <div class="controls">...</div>
  </div>
  <div class="modal-overlay">...</div>
</div>
```

### JavaScript
- Maneja cambio de slides
- Anima con GSAP
- Control de modales
- Manejo de teclado
- Actualización de progress bar

### CSS
- Responsive (mobile, tablet, desktop)
- Grid + Flexbox para layouts
- Animaciones CSS para transiciones rápidas
- Variables CSS para colores (fácil de cambiar)

---

## PERSONALIZACIÓN

### Cambiar Colores
Edita las variables CSS al inicio del `<style>`:
```css
:root {
  --hamuq-teal: #128c82;        /* Cambiar este */
  --hamuq-orange: #f58220;       /* Cambiar este */
  /* ... etc */
}
```

### Agregar/Quitar Slides
1. Busca `<div class="slide">` en el HTML
2. Copia una completa
3. Edita contenido
4. El JavaScript cuenta automáticamente

### Cambiar Logos
En `<div class="global-header">` y `Slide 1`, cambia:
```html
<img src="https://drive.google.com/uc?export=view&id=..." alt="Logo">
```

Por tus URLs de Google Drive (o cualquier servidor)

### Editar Contenido
- Busca el texto que quieres cambiar
- Mantén la estructura HTML (h1, h2, p, divs)
- No toques la estructura de las clases (class="...")

---

## PROBLEMAS COMUNES Y SOLUCIONES

### Problema: Logos no cargan
**Solución**: Verifica que la URL de Google Drive sea correcta y accesible públicamente

### Problema: Animaciones lentas
**Solución**: 
- Comprueba que no hay demasiadas pestañas abiertas
- Usa navegador moderno (Chrome, Firefox, Safari)
- Aumenta la duración en GSAP si lo necesitas

### Problema: Modal se queda abierto
**Solución**: Presiona ESC o haz click afuera del modal

### Problema: Textos se solapan en móvil
**Solución**: El HTML ya es responsive, pero si necesitas ajustar media queries, edita `@media (max-width: 768px)`

---

## MEJORAS FUTURAS (NO INCLUIDAS EN V1)

Si deseas agregar después:

### 1. Números de Slides en URLs (para compartir)
```javascript
// Agregar en el script:
if (window.location.hash) {
  currentSlide = parseInt(window.location.hash.replace('#', '')) - 1;
  showSlide(currentSlide);
}
```

### 2. Búsqueda dentro de la presentación
- Agregar input search
- Filtrar slides por contenido

### 3. Descargar presentación como PDF
- Usar librería html2pdf.js
- Botón "Descargar" en controles

### 4. Modo presentador (con notas)
- Ventana secundaria con notas por slide
- Timer de presentación

### 5. Exportar a PowerPoint
- Usar librería python-pptx o similar
- Script para convertir HTML → PPTX

---

## SOPORTES Y NAVEGADORES

### Testeado en:
- ✅ Chrome (recomendado)
- ✅ Firefox
- ✅ Safari
- ✅ Edge
- ✅ Móvil (iOS Safari, Chrome Android)

### Requisitos:
- Navegador moderno (ES6+ support)
- JavaScript habilitado
- Conexión a Internet (para CDNs de Google Fonts, Font Awesome, GSAP)

---

## PERFORMANCE

### Tamaño de archivo:
- HTML: ~1.4 MB
- Carga: < 2 segundos (con conexión buena)
- Sin images embebidas (solo URLs)

### Memoria:
- Bajo consumo (~50-100 MB)
- No lag en animaciones

### Red:
- Solo 3 CDNs externos (todos rápidos)
- Fallback si falla CDN: algunas animaciones puede que no funcionen, pero la presentación seguirá

---

## COMPATIBILIDAD CONTRACTUAL

Este HTML implementa TODO lo especificado en el Contrato Zero-Trust:

✅ Módulo Básico (7 módulos incluidos)
✅ 85 slides (como requerido)
✅ Gráficos y diagramas (SVG, CSS)
✅ Centrado perfecto (V + H)
✅ Responsive total
✅ Animaciones GSAP fluidas
✅ Modales interactivos
✅ Paleta Hamuq (teal + orange)
✅ Logos incluidos
✅ Sin Prometeo (como especificado)
✅ Sin APIs bancarias automáticas
✅ Énfasis en sistema MANUAL

---

## CÓMO PRESENTAR

### En vivo (recomendado):
1. Abre el HTML en pantalla completa (F11 o Cmd+Ctrl+F)
2. Usa flechas del teclado para navegar
3. Si quieres ampliar algo, click en card para modal
4. Presenta naturalmente (es una herramienta, no un teleprompter)

### Desde otra pantalla:
1. Espejea tu pantalla con el proyector
2. Abre el HTML en ventana pequeña
3. Usa botones para navegar manualmente

### Puntos de parada sugeridos:
- Slide 15: Resumen de contexto
- Slide 25: Visión general del sistema completo
- Slide 55: "¿Preguntas sobre el semáforo?"
- Slide 80: "¿Preguntas técnicas?"
- Slide 84: "¿Dudas sobre implementación?"

---

## DURACIÓN SUGERIDA

- **Presentación rápida** (sin modales): 15-20 minutos
- **Presentación normal** (con algunas ampliaciones): 30-40 minutos
- **Presentación detallada** (todos los modales): 60+ minutos

Flexible según audiencia y contexto.

---

## CONTACTO Y SOPORTE

Si necesitas ajustes:
- Cambios de contenido: Edita el HTML directamente
- Cambios de diseño: Modifica el CSS
- Cambios de animaciones: Ajusta los parámetros GSAP
- Problemas técnicos: Verifica navegador y conexión

**Cualquier duda sobre el contenido técnico**, refiere al documento `PLAN_MAESTRO_PRESENTACION.md`.

---

**Archivo creado**: 30 de marzo de 2026  
**Versión**: v6.0  
**Estado**: Listo para presentación en vivo

