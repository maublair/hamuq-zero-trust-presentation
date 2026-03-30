# PROMPT MAESTRO: Generación Presentación Zero-Trust Fundación Hamuq

> Usa este prompt completo con Claude CLI, GPT-4, Gemini u otra IA para generar el archivo `index.html` final.

---

## INSTRUCCION DIRECTA PARA LA IA

Eres un experto en desarrollo web frontend. Tu tarea es generar UN SOLO ARCHIVO `index.html` autosuficiente que sea una presentacion ejecutiva interactiva para el Sistema Zero-Trust de Fundacion Hamuq Peru. El archivo debe funcionar directamente en el navegador sin dependencias locales.

Lee TODA la documentacion de este repositorio antes de generar el codigo:
- `CONTRACT_INFO.md` - Informacion del contrato
- `SLIDES_CONTENT.md` - Contenido de los 16 slides
- `STYLE_GUIDE.md` - Estilos y diseno
- `TECHNICAL_SPECS.md` - Especificaciones tecnicas

---

## STACK TECNOLOGICO

```html
<!-- GSAP 3.12.2 -->
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js"></script>

<!-- Google Fonts -->
<link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&family=Open+Sans:wght@400;600&display=swap" rel="stylesheet">

<!-- Font Awesome (iconos) -->
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
```

Logos (usar como img src):
- Hamuq: https://drive.google.com/uc?export=view&id=1Zk3mueJ2WM9LUj2R0C7D7qka0tHhDQEE
- BlairCode AI: https://drive.google.com/uc?export=view&id=1BVWl7CpBOecgb6SX1YlXDuO_V2gWJKPy

---

## ARQUITECTURA HTML

```
body
  #presentation-wrapper
    #progress-bar
    #presentation-container
      .slide.active (solo uno visible a la vez)
        .slide-inner
          .slide-content (centrado H+V)
    #nav-buttons
      #btn-prev
      #slide-counter
      #btn-next
  .modal-overlay (oculto por defecto)
    .modal-box
      .modal-close
      .modal-body
```

---

## REQUISITOS DE DISENO

### Centrado
```css
.slide {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
}
.slide-inner {
  width: min(960px, 90vw);
  max-height: 85vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  text-align: center;
}
```

### Overflow
- Si el contenido de un slide no cabe, dividirlo en slide-A y slide-B
- Nunca usar scroll interno en un slide
- Usar font-size clamp() para adaptar texto

### Cards con hover
```css
.card {
  transition: transform 0.3s, box-shadow 0.3s;
  cursor: pointer;
}
.card:hover {
  transform: translateY(-6px) scale(1.03);
  box-shadow: 0 20px 40px rgba(0,0,0,0.2);
}
```

### Modales
- Al hacer click en una card, abrir modal con info ampliada
- Backdrop blur
- Animacion GSAP de entrada (scale 0.8 -> 1, opacity 0 -> 1)
- Cerrar con X o click en backdrop

### Diagramas
- Usar SVG inline o divs con CSS
- Tooltips en hover sobre cada nodo
- Flechas animadas con CSS o GSAP

---

## ANIMACIONES GSAP

```javascript
// Transicion entre slides
gsap.to(currentSlide, {opacity:0, x:-50, duration:0.4, onComplete: () => {
  currentSlide.classList.remove('active');
  nextSlide.classList.add('active');
  gsap.fromTo(nextSlide, {opacity:0, x:50}, {opacity:1, x:0, duration:0.4});
}});

// Entrada de elementos en slide
gsap.from('.slide-title', {y:-30, opacity:0, duration:0.6});
gsap.from('.card', {y:30, opacity:0, duration:0.5, stagger:0.1, delay:0.3});
gsap.from('.diagram-node', {scale:0, opacity:0, duration:0.4, stagger:0.15, delay:0.5});

// Modal
gsap.fromTo('.modal-box', {scale:0.8, opacity:0}, {scale:1, opacity:1, duration:0.3, ease:'back.out(1.7)'});
```

---

## NAVEGACION

```javascript
// Botones
document.getElementById('btn-next').addEventListener('click', nextSlide);
document.getElementById('btn-prev').addEventListener('click', prevSlide);

// Teclado
document.addEventListener('keydown', (e) => {
  if (e.key === 'ArrowRight' || e.key === 'ArrowDown') nextSlide();
  if (e.key === 'ArrowLeft' || e.key === 'ArrowUp') prevSlide();
  if (e.key === 'Escape') closeModal();
});

// Progress bar
function updateProgress() {
  const pct = ((currentIndex+1) / totalSlides) * 100;
  gsap.to('#progress-bar', {width: pct+'%', duration:0.3});
}
```

---

## RESPONSIVE

```css
/* Mobile */
@media (max-width: 768px) {
  .slide-title { font-size: clamp(1.4rem, 5vw, 2rem); }
  .cards-grid { grid-template-columns: 1fr; }
  .slide-inner { width: 95vw; }
}

/* Tablet */
@media (min-width: 769px) and (max-width: 1024px) {
  .cards-grid { grid-template-columns: repeat(2, 1fr); }
}

/* Desktop */
@media (min-width: 1025px) {
  .cards-grid { grid-template-columns: repeat(3, 1fr); }
}
```

---

## CHECKLIST FINAL PARA LA IA

Antes de entregar el codigo, verifica:
- [ ] Los 16 slides estan completos con todo el contenido de `SLIDES_CONTENT.md`
- [ ] Montos exactos del contrato en el slide de inversiones
- [ ] Logos de Hamuq y BlairCode en portada
- [ ] Navegacion con botones y teclado
- [ ] Progress bar funcional
- [ ] Todas las cards tienen hover effects
- [ ] Todos los modales funcionan
- [ ] Todos los diagramas tienen tooltips
- [ ] Responsive en mobile/tablet/desktop
- [ ] Sin errores de consola
- [ ] Sin overflow en ningun slide
- [ ] Animaciones GSAP en entrada y salida
- [ ] Colores segun `STYLE_GUIDE.md`

---

## COMO USAR CON CLAUDE CLI

```bash
# Instalar Claude CLI
npm install -g @anthropic-ai/claude-code

# En tu directorio de trabajo
claude-code

# Pegar este prompt o ejecutar:
# "Lee todos los .md de este directorio y genera index.html"
```

## COMO USAR CON CURSOR

1. Clona el repositorio
2. Abrelo en Cursor
3. Cmd+L -> "Lee todos los archivos .md y genera index.html siguiendo exactamente las especificaciones"

## COMO USAR CON COPILOT CLI

```bash
gh copilot suggest "Lee los .md de este repo y genera index.html"
```
