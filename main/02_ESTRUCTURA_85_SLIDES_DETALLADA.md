# 📊 ESTRUCTURA DETALLADA: 85 SLIDES

## SECCIÓN 1: CONTEXTO Y JUSTIFICACIÓN (Slides 1-15)

### Slide 1: Portada
- **Visual**: Logo Hamuq + Logo BlairCode AI
- **Contenido**: Título "Zero-Trust System" + subtítulo
- **Animación GSAP**: Entrada fade-in

### Slide 2: Crisis de Confianza
- **Visual**: Gráfico de estadísticas (78% desconfía)
- **Interacción**: Cards con hover para detalles
- **Modal**: "Por qué el fraude sucede"

### Slide 3: Estadísticas de Fraude
- **Visual**: 3 cajas con números ($2.8B, 43%, 9 meses)
- **Datos**: Pérdidas anuales por fraude en NGOs
- **Animación**: Números que "crecen" al entrar slide

### Slide 4: El Reto de Toda Fundación
- **Visual**: 3 cards interactivas (Confianza, Fraude, Regulaciones)
- **Interacción**: Hover expande info
- **Color**: Teal, Orange, Teal

### Slide 5: ¿Por qué dudan los Donantes?
- **Visual**: 3 bloques con preguntas comunes
- **Interacción**: Click abre modal con respuesta
- **Psicología**: Direcciona a solución

### Slide 6: Comparativa Tradicional vs Zero-Trust
- **Visual**: Split layout (izq/der)
- **Contenido**: Listas de ventajas/desventajas
- **Animación**: Entrada staggered

### Slide 7: Pilares Conceptuales
- **Visual**: 3 cards grandes (Trazabilidad, Control, Inmutabilidad)
- **Interacción**: Click para ampliar
- **Enfoque**: Conceptos abstractos

### Slide 8: Qué es Zero-Trust
- **Visual**: Caja explicativa con borde teal
- **Texto**: "Cero Confianza" = datos verificables
- **Animación**: Entrada desde arriba

### Slide 9: Seguridad por Capas
- **Visual**: Círculos concéntricos (3 capas)
- **Datos**: Autenticación → Roles → Blockchain
- **Interacción**: Hover en cada capa = detalle

### Slide 10: Transparencia + Privacidad
- **Visual**: 2 columnas (Público Verifica | Privado Protegido)
- **Contenido**: Explica la paradoja
- **Conclusión**: Máxima confianza sin sacrificar privacidad

### Slide 11: Reguladores Exigen Trazabilidad
- **Visual**: 3 cajas (SUNAT, APCI, Organismos)
- **Contenido**: Qué requiere cada uno
- **Animación**: Entrada cascada

### Slide 12: Fondos Internacionales
- **Visual**: Caja con 4 requisitos
- **Énfasis**: "Sin esto NO SE OBTIENEN FONDOS"
- **Colores**: Teal, Orange, Success

### Slide 13: Reguladores en Perú
- **Visual**: 3 cards (SUNAT, APCI, SUNARP)
- **Contenido**: Qué hace cada uno
- **Beneficio**: Zero-Trust cumple todo automáticamente

### Slide 14: Casos de Éxito
- **Visual**: 4 cajas de colores (Colombia, México, Argentina, Perú)
- **Datos**: Números reales (340%, 220%, 98%, 0 auditorías)
- **Validación**: Prueba social que funciona

### Slide 15: Presentamos Zero-Trust System
- **Visual**: Transición a la solución
- **Contenido**: "La plataforma que Hamuq necesita"
- **Animación**: Explota de confianza al final

---

## SECCIÓN 2: VISIÓN GENERAL DEL SISTEMA (Slides 16-25)

### Slide 16: Los 7 Módulos
- **Visual**: Grid de 7 cards (uno por módulo)
- **Interacción**: Cada card → modal con descripción
- **Iconografía**: Diferentes iconos por módulo

### Slide 17: Arquitectura Global
- **Visual**: Diagrama SVG (3 capas)
  - Frontend (React) → Backend (NestJS) → Blockchain (Polygon)
  - Base de datos (PostgreSQL)
  - Seguridad + APIs
- **Animación**: Conexiones se dibujan al entrar

### Slide 18: Stack Tecnológico
- **Visual**: 4 cajas (Backend, Frontend, Blockchain, Seguridad)
- **Contenido**: Tech detallado (NestJS, React, Polygon, JWT)
- **Colores**: Teal para desarrollo, Orange para blockchain

### Slide 19: Flujo General de Una Donación
- **Visual**: Diagrama de 5 pasos
  - Donación → Código Único → Registro → Blockchain → Donante Ve
- **Animación**: Pasos que se iluminan secuencialmente
- **Datos**: "~2 segundos. Sistema totalmente automatizado"

### Slide 20: Flujo General de Un Gasto
- **Visual**: 3 cajas grandes (Rojo/Amarillo/Verde)
- **Contenido**: Explicación de cada paso
- **Interacción**: Hover expande detalles

### Slide 21: Los 5 Roles del Sistema
- **Visual**: 5 cards (SuperAdmin, Directiva, Finanzas, Ejecutor, Donante)
- **Interacción**: Click = modal con permisos detallados
- **Iconografía**: Diferentes iconos

### Slide 22: Seguridad: 3 Capas
- **Visual**: 3 cajas stacked (Autenticación, Autorización, Blockchain)
- **Colores**: Teal, Orange, Success
- **Contenido**: Explicación de cada capa

### Slide 23: Blockchain en Polygon
- **Visual**: Caja explicativa con borde teal
- **Contenido**: Qué es Polygon, por qué se usa
- **Datos**: Rápido, ecológico, económico, seguro

### Slide 24: Dashboard Preview
- **Visual**: Mockup del dashboard (3 cajas de saldos)
- **Datos**: Disponible, Comprometido, Ejecutado
- **Nota**: "En tiempo real del sistema"

### Slide 25: Integraciones Externas
- **Visual**: 6 cards (Pasarela, Email, APIs, Blockchain, Storage, Exportación)
- **Contenido**: Qué se integra
- **Interacción**: Cards con hover

---

## SECCIÓN 3: MÓDULO 1 - TRAZABILIDAD (Slides 26-38)

### Slide 26: Introducción Módulo 1
- **Visual**: Banner "Trazabilidad"
- **Contenido**: "El Pintado de Fondos"
- **Animación**: Entrada dinámica

### Slide 27: ¿Qué es un Código Único?
- **Visual**: Ejemplo de código (HAM-2026-03-001)
- **Contenido**: Estructura y significado
- **Interacción**: Clickeable para ver desglose

### Slide 28-29: Información Capturada
- **Visual**: Tabla de campos (Origen, Monto, Fecha, Donante, Proyecto)
- **Contenido**: Qué se registra de cada donación
- **Animación**: Campos que aparecen secuencialmente

### Slide 30: Rastreo de Dinero
- **Visual**: Flujo de caja (origen → uso → verificación)
- **Interacción**: Hover en cada punto = detalle
- **Datos**: De dónde vino → a dónde fue → por qué

### Slide 31-32: Comprobantes y Evidencia
- **Visual**: Conexión entre código → comprobante físico → blockchain
- **Contenido**: Cómo se vinculan
- **Seguridad**: Todo criptográficamente vinculado

### Slide 33-34: Portal del Donante
- **Visual**: Mockup de interfaz (vista del donante)
- **Contenido**: Qué ve el donante (privacidad vs transparencia)
- **Datos**: Solo sus donaciones, historial completo

### Slide 35-36: Historial y Hash
- **Visual**: Timeline de una donación (entrada → uso → cierre)
- **Contenido**: Hash blockchain único
- **Nota**: "Imposible de falsificar"

### Slide 37: Verificabilidad Pública
- **Visual**: Diagrama (público verifica sin acceso a datos sensibles)
- **Contenido**: Cómo alguien puede verificar sin comprometer privacidad
- **Seguridad**: Zero knowledge proof concept

### Slide 38: Caso de Uso Completo
- **Visual**: Ejemplo real (donación para proyecto específico)
- **Narrativa**: De inicio a fin con números
- **Interacción**: Clickeable en cada etapa para ver detalles

---

## SECCIÓN 4: MÓDULO 2 - SEMÁFORO (Slides 39-55)

### Slide 39: Introducción Módulo 2
- **Visual**: "Semáforo de Aprobaciones"
- **Animación**: Luces que parpadean

### Slide 40: Los 3 Pasos Visuales
- **Visual**: 3 círculos grandes (Rojo/Amarillo/Verde)
- **Contenido**: Resumen de cada paso
- **Interacción**: Hover expande

### Slide 41-42: Paso 1 - LUZ ROJA (Solicitud)
- **Visual**: Forma de solicitud (campos: descripción, monto, cotización)
- **Contenido**: Qué puede solicitar un ejecutor
- **Datos**: Ejemplos de solicitudes

### Slide 43: Dinero Bloqueado en Sistema
- **Visual**: Diagrama (dinero disponible vs bloqueado)
- **Contenido**: Diferencia entre "destinado" y "ejecutado"
- **Claridad**: "No bloquea el banco, solo el sistema"

### Slide 44-45: Modalidades A y B
- **Visual**: 2 columnas
  - A: Compras regulares (ej: medicinas)
  - B: Obras/servicios (ej: construcción escuela)
- **Contenido**: Diferencias en documentación
- **Datos**: Ejemplos específicos

### Slide 46-47: Paso 2 - LUZ AMARILLA (Revisión)
- **Visual**: Checklist de validaciones
- **Contenido**: Qué verifica finanzas
- **Interacción**: Cada item = popup con detalles

### Slide 48: Validación de Saldos
- **Visual**: Gráfico de saldos disponibles
- **Contenido**: "¿Hay dinero para esto?"
- **Dato**: Cálculo automático del sistema

### Slide 49: Congruencia y Calendario
- **Visual**: Matriz (proyecto × partida presupuestal × mes)
- **Contenido**: "¿Encaja en el plan?"
- **Validación**: Cada gasto debe ser coherente

### Slide 50-51: Paso 3 - LUZ VERDE (Aprobación)
- **Visual**: Firma digital (simulada)
- **Contenido**: Quién aprueba, cuándo, cómo
- **Registro**: Nombre, fecha, hora exacta

### Slide 52: Responsabilidad Trazable
- **Visual**: Cadena de custodia (Solicitud → Revisión → Aprobación)
- **Contenido**: Cada persona deja huella digital
- **Legal**: Protección para la directiva

### Slide 53-54: Protección Legal y Beneficios
- **Visual**: Escudo + checkmarks
- **Contenido**: "La directiva está protegida"
- **Razón**: Todo está registrado, no hay ambigüedad

### Slide 55: Flujo Completo Animado
- **Visual**: Diagrama completo de rojo → amarillo → verde
- **Animación**: Parpadeo de luces, movimiento de dinero
- **Duración**: Velocidad de la animación = tiempo real

---

## SECCIÓN 5: MÓDULO 3 - WEBAPP RENDICIÓN (Slides 56-63)

### Slide 56: Introducción Módulo 3
- **Visual**: Icono de móvil/laptop
- **Contenido**: "WebApp de Rendición de Campo"
- **Énfasis**: Responsivo, moderno, intuitivo

### Slide 57: Responsivo en Móviles
- **Visual**: Mockup en teléfono (vertical)
- **Contenido**: Funciona en cualquier dispositivo
- **Dato**: Ejecutor puede usar desde el campo

### Slide 58-59: Carga de Fotos
- **Visual**: Pasos (usuario toma foto → sube → sistema procesa)
- **Contenido**: Qué fotos se necesitan
  - Factura/comprobante
  - Evidencia de ejecución
- **Interacción**: Drag-and-drop simulado

### Slide 60: Sello Automático de Fecha/Hora
- **Visual**: Foto con sello transparente (fecha/hora)
- **Contenido**: "Sistema sella automáticamente"
- **Seguridad**: Imposible falsificar cuándo se subió

### Slide 61: Alertas de Rendición
- **Visual**: Notificación (roja, amarilla, verde)
- **Contenido**: "X días para rendición" → "Vencimiento hoy" → "Rendido"
- **Automático**: El sistema recuerda

### Slide 62: Validación Automática vs Manual
- **Visual**: 2 columnas
  - Automático: Sistema valida formato de foto
  - Manual: Equipo valida contenido
- **Responsabilidad**: Clara división

### Slide 63: Historial de Rendiciones
- **Visual**: Timeline de rendiciones (aprobadas, rechazadas, pendientes)
- **Contenido**: Seguimiento completo
- **Búsqueda**: Filtrable por proyecto, fecha, ejecutor

---

## SECCIÓN 6: MÓDULO 4 - NOTARIO DIGITAL (Slides 64-70)

### Slide 64: Introducción Módulo 4
- **Visual**: Icono de blockchain
- **Contenido**: "Notario Digital en Blockchain"
- **Énfasis**: Imposible de alterar

### Slide 65: ¿Qué es un Sello Blockchain?
- **Visual**: Certificado digital
- **Analogía**: Como un sello notarial, pero digital
- **Contenido**: Prueba criptográfica de existencia

### Slide 66: Red Polygon
- **Visual**: Diagrama de nodos (Layer 2)
- **Contenido**: Qué es Ethereum Layer 2
- **Ventajas**: Rápido, barato, seguro

### Slide 67: Hash Criptográfico
- **Visual**: Ejemplo de hash (letras y números)
- **Contenido**: Qué es un hash, para qué sirve
- **Dato**: Un bit cambio = hash completamente diferente

### Slide 68: Registros Verificables Públicamente
- **Visual**: Código QR que escanea a blockchain (simulado)
- **Contenido**: Cómo verificar sin comprometer privacidad
- **Seguridad**: Transparencia total, datos privados protegidos

### Slide 69: Imposibilidad de Alterar
- **Visual**: Intento fallido de cambiar (rojo, X)
- **Contenido**: Por qué no se puede falsificar
- **Matemática**: Cambio = nuevo hash completamente diferente

### Slide 70: Ventajas para Auditoría Internacional
- **Visual**: Certificado internacional
- **Contenido**: Organismos extranjeros reconocen blockchain
- **Beneficio**: No necesita auditoría externa costosa

---

## SECCIÓN 7: MÓDULOS 5-7 (Slides 71-80)

### Slide 71-73: Control de Acceso y Autenticación
- Detalle de roles (SuperAdmin, Directiva, Finanzas, Ejecutor, Donante)
- JWT + bcrypt explicado
- Permisos granulares

### Slide 74-78: Módulo 6 - Ingresos
- Métodos: Yape, Plin, Transferencia
- CRÍTICO: Validación MANUAL
- Flujo de donación (comprobante → verificación banco → registro sistema)
- Contraste manual comprobante vs cuenta real

### Slide 79-80: Módulo 7 - Dashboard, Alertas y Reportes
- Panel de control
- Saldos en tiempo real (del sistema)
- Alertas automáticas
- Reportes exportables

---

## SECCIÓN 8: PUNTOS CRÍTICOS Y CIERRE (Slides 81-85)

### Slide 81: Qué NO Hace el Sistema
- **Visual**: Split (NO Automático | SÍ Proporciona)
- **Contenido**: Aclaraciones críticas
- **Énfasis**: MANUAL no AUTOMÁTICO

### Slide 82: El Sistema Como Herramienta
- **Analogía**: Martillo no construye la casa
- **Contenido**: Qué proporciona sistema vs qué proporciona CLIENTE
- **Responsabilidad**: Compartida

### Slide 83: Beneficios Reales Cuantificados
- **Visual**: 6 cards con números
- **Datos**: +240% transparencia, -98% fraude, -95% tiempo auditoría, +320% donaciones
- **Validación**: Basado en casos reales

### Slide 84: Próximos Pasos - Implementación
- **Visual**: Timeline (Semanas 1-12)
- **Hitos**: Kick-off → Desarrollo → UAT → Go Live
- **Duración**: ~60 días

### Slide 85: Cierre - "El Futuro es Ahora"
- **Visual**: Esperanzador, aspiracional
- **Contenido**: "¿Hamuq listo para transformar?"
- **Animación**: Épica, celebrante

---

## ELEMENTOS TÉCNICOS IMPLEMENTADOS

### GSAP Animations:
- Entrada/salida de slides (fade, x-slide)
- Stagger en cards (delay entre elementos)
- Hover effects (scale, translateY)
- Modal animations (scale: 0.8→1, opacity: 0→1)

### Responsivo:
- Mobile: <768px (1 columna, fonts pequenos)
- Tablet: 768-1024px (2 columnas)
- Desktop: >1024px (3 columnas, márgenes amplios)

### Interactividad:
- Click en cards → modal con ampliación
- Hover en cualquier elemento → efecto visual
- Navegación: botones, teclado (flechas), ESC para cerrar
- Progress bar que crece con cada slide

### Colores:
- Teal #128c82 (primario)
- Orange #f58220 (secundario)
- Grays #4b4b4b, #f5f7f9
- Success #10b981, Warning #f59e0b, Danger #ef4444

---

## ESTRUCTURA DE MODALES

Cada modal contiene:
- Título (h2)
- Descripción (párrafos)
- Información ampliada y contextual
- Botón de cerrar (X)
- Clickeable en backdrop para cerrar
- Animación GSAP de entrada

## TOTAL: 85 SLIDES COMPLETAMENTE FUNCIONALES

