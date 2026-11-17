# 3. Modelo conceptual y 4. Metáfora de interfaz

## 3. Modelo conceptual

### Qué hace el sistema

Centraliza la gestión de los **trabajos** del negocio: los registra desde que
el cliente los solicita hasta su entrega y pago, muestra qué viene y qué se
debe cobrar, y prepara mensajes listos para enviar por WhatsApp o correo. Es
una herramienta de uso interno para una única usuaria. El envío siempre lo
hace ella desde sus propias cuentas.

### Conceptos principales

| Concepto | Qué es para la usuaria |
|---|---|
| Cliente | Persona o empresa que le encarga trabajos, con contacto e historial |
| Trabajo | Concepto central: un encargo con descripción, cantidad, precio y fecha de entrega |
| Estado | Etapa del trabajo: cotizado, en diseño, aprobado, en producción, entregado |
| Cotización | Propuesta de precio asociada a un trabajo |
| Pago | Abono o pago total recibido por un trabajo |
| Saldo | Lo que falta por cobrar (precio menos pagos) |
| Plantilla de mensaje | Texto base (cotización, confirmación, aviso de entrega, recordatorio de cobro) |
| Mensaje preparado | Plantilla más datos del trabajo, listo para abrir en WhatsApp o correo |

### Relaciones

- Un cliente tiene muchos trabajos; cada trabajo pertenece a un solo cliente.
- Un trabajo tiene un estado actual y puede cambiar de estado varias veces.
- Un trabajo puede tener una o más cotizaciones.
- Un trabajo puede tener cero o más pagos; el saldo se calcula a partir de ellos.
- Una plantilla más los datos de un trabajo y su cliente generan un mensaje preparado.

### Organización de la experiencia

Gira en torno a tres preguntas diarias de la usuaria:

1. ¿Qué tengo que hacer hoy y esta semana?
2. ¿En qué etapa va cada trabajo?
3. ¿Quién me debe y cuánto?

## 4. Metáfora de interfaz

**El tablero de trabajos:** una pizarra con tarjetas, una por trabajo, en
columnas según su etapa. Se complementa con la **ficha del cliente**, como una
carpeta con sus trabajos y pagos.

| Elemento de la metáfora | En la aplicación |
|---|---|
| Pizarra | Pantalla Tablero |
| Columnas | Estados del trabajo |
| Tarjeta | Un trabajo, con cliente, entrega y saldo visibles |
| Mover la tarjeta | Arrastrar (notebook) o botón "Mover a…" (celular) |
| Carpeta del cliente | Ficha con historial y saldo total |

### Justificación

1. Calza con su modelo mental: ya usa una pizarra física (ver `../evidencias/feedback-usuaria.md`).
2. Resuelve el dolor principal: lo repartido en muchos chats se ve en una pantalla.
3. Es familiar sin ser técnica, lo que cumple RNF2.

### Límites de la metáfora

Un tablero por etapas no muestra bien plazos ni cobros. Por eso cada tarjeta
incluye indicador de plazo y saldo pendiente, y existe el panel "Hoy" como vista
complementaria ordenada por fecha. Además, la pizarra de la usuaria se organiza
por cliente, mientras el tablero lo hace por etapa; esa vista por cliente se
cubre con la pantalla Clientes.
