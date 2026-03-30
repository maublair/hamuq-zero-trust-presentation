# GUIA DE ESTILOS CSS COMPLETA
# Sistema de Diseño Zero-Trust Presentation

## PALETA DE COLORES

### Colores Principales
```css
:root {
  /* Hamuq - Tonos Tierra/Naturaleza */
  --hamuq-primary: #2D5016;      /* Verde oscuro */
  --hamuq-secondary: #6B8E23;    /* Verde oliva */
  --hamuq-accent: #8FBC8F;       /* Verde suave */
  
  /* BlairCode - Tecnología/Innovación */
  --blair-primary: #1A237E;      /* Azul oscuro */
  --blair-secondary: #3F51B5;    /* Azul índigo */
  --blair-accent: #7986CB;       /* Azul claro */
  
  /* Sistema Zero-Trust - Seguridad */
  --trust-primary: #263238;      /* Gris oscuro */
  --trust-secondary: #37474F;    /* Gris medio */
  --trust-accent: #546E7A;       /* Gris azulado */
  
  /* Estados y Alertas */
  --success: #4CAF50;
  --warning: #FF9800;
  --error: #F44336;
  --info: #2196F3;
  
  /* Neutros */
  --white: #FFFFFF;
  --black: #000000;
  --gray-100: #F5F5F5;
  --gray-200: #EEEEEE;
  --gray-300: #E0E0E0;
  --gray-400: #BDBDBD;
  --gray-500: #9E9E9E;
  --gray-600: #757575;
  --gray-700: #616161;
  --gray-800: #424242;
  --gray-900: #212121;
  
  /* Gradientes */
  --gradient-hamuq: linear-gradient(135deg, #2D5016 0%, #6B8E23 100%);
  --gradient-blair: linear-gradient(135deg, #1A237E 0%, #3F51B5 100%);
  --gradient-overlay: linear-gradient(180deg, rgba(0,0,0,0.7) 0%, rgba(0,0,0,0.3) 100%);
}
```

## TIPOGRAFIA

### Fuentes
```css
/* Importar desde Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800;900&family=Open+Sans:wght@400;600;700&display=swap');

:root {
  --font-heading: 'Montserrat', sans-serif;
  --font-body: 'Open Sans', sans-serif;
}
```

### Escalas Tipográficas
```css
:root {
  /* Tamaños Base */
  --text-xs: clamp(0.75rem, 0.7rem + 0.25vw, 0.875rem);      /* 12-14px */
  --text-sm: clamp(0.875rem, 0.8rem + 0.375vw, 1rem);        /* 14-16px */
  --text-base: clamp(1rem, 0.95rem + 0.25vw, 1.125rem);      /* 16-18px */
  --text-lg: clamp(1.125rem, 1.05rem + 0.375vw, 1.25rem);    /* 18-20px */
  --text-xl: clamp(1.25rem, 1.15rem + 0.5vw, 1.5rem);        /* 20-24px */
  --text-2xl: clamp(1.5rem, 1.35rem + 0.75vw, 1.875rem);     /* 24-30px */
  --text-3xl: clamp(1.875rem, 1.7rem + 0.875vw, 2.25rem);    /* 30-36px */
  --text-4xl: clamp(2.25rem, 2rem + 1.25vw, 3rem);           /* 36-48px */
  --text-5xl: clamp(3rem, 2.5rem + 2.5vw, 4rem);             /* 48-64px */
  
  /* Peso */
  --weight-normal: 400;
  --weight-medium: 500;
  --weight-semibold: 600;
  --weight-bold: 700;
  --weight-extrabold: 800;
  --weight-black: 900;
  
  /* Altura de línea */
  --leading-tight: 1.25;
  --leading-normal: 1.5;
  --leading-relaxed: 1.75;
  
  /* Espaciado de letras */
  --tracking-tight: -0.05em;
  --tracking-normal: 0;
  --tracking-wide: 0.05em;
}
```

## ESPACIADO Y LAYOUT

### Sistema de Espaciado (8pt grid)
```css
:root {
  --space-1: 0.5rem;   /* 8px */
  --space-2: 1rem;     /* 16px */
  --space-3: 1.5rem;   /* 24px */
  --space-4: 2rem;     /* 32px */
  --space-5: 2.5rem;   /* 40px */
  --space-6: 3rem;     /* 48px */
  --space-8: 4rem;     /* 64px */
  --space-10: 5rem;    /* 80px */
  --space-12: 6rem;    /* 96px */
  --space-16: 8rem;    /* 128px */
  --space-20: 10rem;   /* 160px */
}
```

### Contenedores
```css
.container {
  width: 100%;
  max-width: min(1440px, 95vw);
  margin-inline: auto;
  padding-inline: var(--space-4);
}

.slide-container {
  width: 100vw;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  overflow: hidden;
  position: relative;
}

.slide-inner {
  width: min(960px, 90vw);
  max-height: 85vh;
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: var(--space-4);
  padding: var(--space-6);
}
```

## COMPONENTES

### Cards
```css
.card {
  background: var(--white);
  border-radius: var(--radius-lg);
  padding: var(--space-6);
  box-shadow: var(--shadow-md);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  cursor: pointer;
  position: relative;
  overflow: hidden;
}

.card::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: var(--gradient-hamuq);
  transform: scaleX(0);
  transform-origin: left;
  transition: transform 0.3s ease;
}

.card:hover {
  transform: translateY(-8px) scale(1.02);
  box-shadow: var(--shadow-2xl);
}

.card:hover::before {
  transform: scaleX(1);
}

.card-title {
  font-family: var(--font-heading);
  font-size: var(--text-xl);
  font-weight: var(--weight-bold);
  color: var(--trust-primary);
  margin-bottom: var(--space-2);
}

.card-content {
  font-family: var(--font-body);
  font-size: var(--text-base);
  color: var(--gray-700);
  line-height: var(--leading-relaxed);
}

.card-icon {
  width: 64px;
  height: 64px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: var(--gradient-blair);
  border-radius: 50%;
  color: var(--white);
  font-size: var(--text-3xl);
  margin-bottom: var(--space-3);
}
```

### Botones
```css
.btn {
  display: inline-flex;
  align-items: center;
  gap: var(--space-2);
  padding: var(--space-3) var(--space-6);
  font-family: var(--font-heading);
  font-size: var(--text-base);
  font-weight: var(--weight-semibold);
  border-radius: var(--radius-full);
  border: none;
  cursor: pointer;
  transition: all 0.3s ease;
  text-decoration: none;
  position: relative;
  overflow: hidden;
}

.btn-primary {
  background: var(--gradient-hamuq);
  color: var(--white);
  box-shadow: 0 4px 14px rgba(45, 80, 22, 0.4);
}

.btn-primary:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(45, 80, 22, 0.5);
}

.btn-secondary {
  background: var(--gradient-blair);
  color: var(--white);
  box-shadow: 0 4px 14px rgba(26, 35, 126, 0.4);
}

.btn-outline {
  background: transparent;
  color: var(--trust-primary);
  border: 2px solid var(--trust-primary);
}

.btn-ghost {
  background: transparent;
  color: var(--gray-700);
}

.btn:hover::before {
  content: '';
  position: absolute;
  inset: 0;
  background: rgba(255, 255, 255, 0.2);
  animation: shimmer 0.6s;
}

@keyframes shimmer {
  from { transform: translateX(-100%); }
  to { transform: translateX(100%); }
}
```

### Modales
```css
.modal-overlay {
  position: fixed;
  inset: 0;
  background: rgba(0, 0, 0, 0.85);
  backdrop-filter: blur(8px);
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 9999;
  opacity: 0;
  pointer-events: none;
  transition: opacity 0.3s ease;
}

.modal-overlay.active {
  opacity: 1;
  pointer-events: all;
}

.modal-box {
  background: var(--white);
  border-radius: var(--radius-2xl);
  padding: var(--space-8);
  max-width: min(900px, 90vw);
  max-height: 85vh;
  overflow-y: auto;
  position: relative;
  box-shadow: var(--shadow-2xl);
  transform: scale(0.9);
  transition: transform 0.3s cubic-bezier(0.68, -0.55, 0.265, 1.55);
}

.modal-overlay.active .modal-box {
  transform: scale(1);
}

.modal-close {
  position: absolute;
  top: var(--space-4);
  right: var(--space-4);
  width: 40px;
  height: 40px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: var(--gray-200);
  color: var(--gray-700);
  cursor: pointer;
  transition: all 0.2s ease;
  border: none;
  font-size: var(--text-xl);
}

.modal-close:hover {
  background: var(--error);
  color: var(--white);
  transform: rotate(90deg);
}
```

## ANIMACIONES Y EFECTOS

### Transiciones Estándar
```css
:root {
  --transition-fast: 150ms;
  --transition-base: 300ms;
  --transition-slow: 500ms;
  
  --ease-in: cubic-bezier(0.4, 0, 1, 1);
  --ease-out: cubic-bezier(0, 0, 0.2, 1);
  --ease-in-out: cubic-bezier(0.4, 0, 0.2, 1);
  --ease-bounce: cubic-bezier(0.68, -0.55, 0.265, 1.55);
}
```

### Sombras (Neumorphism + Material)
```css
:root {
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 
               0 2px 4px -1px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 
               0 4px 6px -2px rgba(0, 0, 0, 0.05);
  --shadow-xl: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 
               0 10px 10px -5px rgba(0, 0, 0, 0.04);
  --shadow-2xl: 0 25px 50px -12px rgba(0, 0, 0, 0.25);
  
  --shadow-inner: inset
