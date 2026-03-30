# INFORMACION COMPLETA DEL CONTRATO
# Contrato Marco de Desarrollo - Plataforma Zero-Trust - Modulo Basico

---

## PARTES DEL CONTRATO

### CLIENTE
- **Nombre**: Fundacion Hamuq Peru
- **RUC**: [COMPLETAR AL FIRMAR]
- **Domicilio**: [COMPLETAR AL FIRMAR - Arequipa]
- **Representante**: [COMPLETAR AL FIRMAR]
- **DNI/CE**: [COMPLETAR AL FIRMAR]
- **Alias en contrato**: "CLIENTE" o "FUNDACION"

### PROVEEDOR
- **Nombre**: BlairCode AI | B & D Co S.A.C.
- **RUC**: 20614096561
- **Domicilio**: Yanahuara, Arequipa, Peru
- **Representante**: Juan Mauricio Blair Farah
- **CE**: 000925350
- **Cargo**: Subgerente Administrativo
- **Alias en contrato**: "PROVEEDOR" o "BLAIRCODE"

---

## MONTOS Y PAGOS

| Concepto | Monto |
|---|---|
| Precio Base (sin IGV) | S/ 7,450.00 |
| IGV 18% | S/ 1,341.00 |
| **TOTAL (con IGV)** | **S/ 8,791.00** |

### Esquema de Pago

| Cuota | Porcentaje | Sin IGV | IGV | **Total** |
|---|---|---|---|---|
| Anticipo (Pago 1) | 70% | S/ 5,215.00 | S/ 938.70 | **S/ 6,153.70** |
| Saldo (Pago 2) | 30% | S/ 2,235.00 | S/ 402.30 | **S/ 2,637.30** |

### Condiciones de Pago
- **Pago 1 (Anticipo 70%)**: S/ 6,153.70 - Pagadero al momento de la firma. El PROVEEDOR no inicia labores hasta recibir el anticipo.
- **Pago 2 (Saldo 30%)**: S/ 2,637.30 - Pagadero al funcionamiento (firma del Acta de Conformidad).
- **Modalidad**: Transferencia bancaria o deposito a cuenta indicada por el PROVEEDOR.

### Soporte Tecnico Opcional (Separado del Contrato)
- Mantenimiento mensual: S/ 2,800.00 + IGV
- Hora adicional de soporte: S/ 250.00 + IGV

---

## PLAZO DE EJECUCION

- **Duracion total**: Aproximadamente 60 dias calendario
- **Inicio**: Fecha de recepcion del Anticipo (70%)
- **El cronograma es REFERENCIAL y puede modificarse**

---

## MODULOS FUNCIONALES - ALCANCE MODULO BASICO

### MODULO 1: TRAZABILIDAD DE FONDOS ("PINTADO" DE DONACIONES)
- Codigo unico alfanumerico por donacion al momento del ingreso
- Registro de: origen, monto, fecha, donante asociado
- Rastreo del uso por: proyecto, partida presupuestal, comprobante fisico
- Portal privado del donante: cada donante ve solo sus propias donaciones

### MODULO 2: SEMAFORO DE APROBACIONES (FLUJO DE 3 PASOS)
- **Paso 1 - Solicitud (Luz Roja)**: Ejecutor de campo ingresa solicitud de gasto/adelanto con descripcion, monto y cotizacion preliminar. Dinero permanece bloqueado en sistema.
- **Paso 2 - Revision (Luz Amarilla)**: Area de Finanzas verifica saldos, congruencia de cotizacion y validez de partidas segun calendario valorizado.
- **Paso 3 - Aprobacion (Luz Verde)**: Directiva aprueba el desembolso con firma digital interna. Sistema registra nombre, fecha y hora exacta.

### MODULO 3: WEBAPP DE RENDICION DE CAMPO
- Aplicacion web responsiva accesible desde moviles
- Ejecutor adjunta foto de factura fisica y foto de evidencia de ejecucion
- Sistema imprime automaticamente fecha y hora oficial sobre la evidencia cargada
- Alertas automaticas cuando plazo de rendicion vence sin respuesta

### MODULO 4: NOTARIO DIGITAL (BLOCKCHAIN)
- Sello criptografico diario en red Polygon (Layer 2 de Ethereum)
- Registros sellados: gastos rendidos y aprobados
- Hash unico e inmutable por transaccion
- Registros verificables publicamente, no alterables ni por desarrolladores

### MODULO 5: CONTROL DE ACCESO Y ROLES (5 ROLES)
- **Super Admin (BlairCode)**: Configuracion global del sistema
- **Directiva**: Aprobacion de gastos y firma digital interna
- **Finanzas**: Revision de saldos, validacion de cotizaciones y calendarios
- **Ejecutor de Campo**: Rendicion de cuentas via WebApp, acceso solo a sus proyectos
- **Donante**: Portal privado de trazabilidad exclusivo de sus propias donaciones
- Autenticacion: JWT + contrasenas hasheadas con bcrypt

### MODULO 6: CAPTACION OMNICANAL - INGRESOS (DONACIONES)
- **Metodos de pago iniciales**: Transferencia bancaria, Yape, Plin
- **PSP (pasarela de pago)**: Se integrara durante el desarrollo, aun no definida
- **Flujo de donacion**:
  1. Donante realiza transferencia/Yape/Plin
  2. Donante sube comprobante (captura o voucher) en el sistema
  3. Encargado recibe notificacion
  4. Encargado contrasta comprobante con cuenta bancaria real MANUALMENTE
  5. Encargado aprueba o rechaza la donacion
  6. Solo si aprobada, el ingreso queda registrado en el sistema
- Sistema NO tiene acceso automatizado a cuentas bancarias
- Toda validacion de ingresos es MANUAL, responsabilidad de la FUNDACION

### MODULO 7: DASHBOARD EJECUTIVO, ALERTAS Y REPORTES
- Panel de control con saldos por proyecto (disponibles, comprometidos, ejecutados)
- Saldos se actualizan SOLO cuando encargados registran informacion en el sistema
- Bandeja unificada de solicitudes pendientes de aprobacion
- **Alertas automaticas del sistema** (no de cuentas reales): rendiciones vencidas, solicitudes sin respuesta, movimientos fuera de calendario
- Generacion de reportes internos por proyecto (ingresos, gastos, evidencia, hash blockchain)
- Exportacion CSV compatible con herramientas contables externas
- Historial completo con sellos criptograficos para consulta interna
- **Los reportes son en formato interno del sistema. La adaptacion a formatos de SUNAT, organismos internacionales u otros es responsabilidad del CLIENTE**

---

## CRONOGRAMA REFERENCIAL (60 dias)

| Semana | Dias | Fase | Hitos Principales |
|---|---|---|---|
| 1-2 | 1-14 | Configuracion e Inicio | Kick-off, VPS/Docker/SSL, PostgreSQL, Autenticacion JWT/Roles |
| 3-4 | 15-28 | Modulos Core Parte I | Trazabilidad de Fondos, Semaforo de Aprobaciones, Portal Donante |
| 5-6 | 29-42 | Modulos Core Parte II | WebApp Rendicion, Captacion Omnicanal, Calendario Valorizado |
| 7-8 | 43-56 | Integracion + Blockchain | Notario Digital (Polygon), Dashboard Ejecutivo, Modulo Reportes |
| 9 | 57-63 | Pruebas y Entrega | UAT, Correccion bugs, Capacitacion, Deploy produccion, Acta Conformidad |

**Notas del Cronograma**:
- Fechas exactas se confirman en el Kick-off
- Retrasos atribuibles al CLIENTE no computan en el plazo del PROVEEDOR
- Cronograma puede alterarse por acuerdo mutuo, cambios de alcance o causas justificadas

---

## LO QUE INCLUYE EL MODULO BASICO

- Desarrollo e implementacion de los 7 modulos descritos
- Sesion de capacitacion al equipo administrador del CLIENTE
- Despliegue en entorno de produccion
- 30 dias de garantia correctiva post-entrega
- Documentacion tecnica basica
- Soporte para correccion de errores dentro del alcance durante garantia

## LO QUE NO INCLUYE

- Pasarela de pago (PSP) lista: se define e integra durante el desarrollo
- APIs bancarias automatizadas o acceso a cuentas reales
- Generacion de documentos con formatos de SUNAT u entidades externas
- Bloqueo de cuentas bancarias reales (el sistema controla el sistema, no la cuenta)
- Auditoria legal, financiera o tributaria
- Integraciones no descritas en Anexo 1
- Modulos adicionales fuera del Modulo Basico

---

## PUNTOS CRITICOS DEL SISTEMA (Para la Presentacion)

### El Sistema es una Herramienta de CONTROL, NO de Ejecucion

1. **El sistema NO controla cuentas bancarias reales**
   - Si un empleado con acceso a la cuenta hace un retiro no autorizado, el sistema no puede impedirlo fisicamente
   - PERO: al registrar los movimientos, el sistema cruza la informacion con el codigo blockchain y detecta la irregularidad
   - El sistema entonces bloquea al usuario infractor y emite alerta de fraude

2. **Fondos bloqueados en el sistema != cuenta bancaria bloqueada**
   - Cuando se bloquea un desembolso en el sistema, la cuenta bancaria fisica sigue operando
   - El control es dentro del sistema: si el dinero sale sin autorizacion del sistema, al registrarse se detecta el fraude

3. **Nada es tiempo real automatico**
   - Los datos del sistema reflejan lo que los encargados han cargado
   - Si no se registran los movimientos, el sistema no ayudara a detectar fraude
   - La responsabilidad del registro es del equipo de la FUNDACION

4. **Los roles se definen durante el desarrollo**
   - El contrato establece 5 roles base, pero pueden ajustarse
   - Las definiciones exactas de permisos se refinan con el CLIENTE

5. **Reportes son internos**
   - El sistema genera reportes en su propio formato
   - NO se adaptan automaticamente a formatos de SUNAT, APCI, cooperacion internacional, etc.
   - El CLIENTE es responsable de convertir esos datos a los formatos que necesite para terceros

6. **Las alertas automaticas son del sistema**
   - Rendiciones vencidas, solicitudes sin respuesta, movimientos fuera de calendario
   - NO son alertas de movimientos bancarios en tiempo real
   - Se basan en los datos registrados en el sistema

---

## ASSETS PARA LA PRESENTACION

### Logos (URLs directas para usar en img src)
```
Logo Hamuq:
https://drive.google.com/uc?export=view&id=1Zk3mueJ2WM9LUj2R0C7D7qka0tHhDQEE

Logo BlairCode AI:
https://drive.google.com/uc?export=view&id=1BVWl7CpBOecgb6SX1YlXDuO_V2gWJKPy
```

### CDNs
```
GSAP: https://cdnjs.cloudflare.com/ajax/libs/gsap/3.12.2/gsap.min.js
Fonts: https://fonts.googleapis.com/css2?family=Montserrat:wght@400;500;600;700;800&family=Open+Sans:wght@400;600&display=swap
Font Awesome: https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css
```
