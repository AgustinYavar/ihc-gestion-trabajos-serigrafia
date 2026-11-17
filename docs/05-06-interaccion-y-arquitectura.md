# 5. Tipos de interacción y 6. Arquitectura de información y flujo

## 5. Tipos de interacción

| Tipo | Acciones concretas de la usuaria |
|---|---|
| Instruir | Crear un trabajo con "+ Nuevo trabajo", registrar un pago, elegir una plantilla y presionar "WhatsApp" o "Correo" |
| Manipular | Arrastrar una tarjeta entre columnas (en celular, botón "Mover a…"); tocar una tarjeta para abrir su ficha |
| Explorar | Revisar el panel Hoy, navegar la ficha de un cliente, mirar quién debe cuánto |
| Responder | Indicador de plazo en la tarjeta, avisos en el panel y confirmaciones tras cada acción. La usuaria decide si actúa |
| Conversar | No incluido: ya conversa con sus clientes por WhatsApp y correo; un chatbot no resolvería ningún hallazgo |

Las notificaciones externas quedan fuera del alcance porque requerirían integraciones.

## 6. Arquitectura de información y flujo

### Sistema de organización

| Eje | Pregunta | Pantalla |
|---|---|---|
| Tiempo | ¿Qué tengo que hacer hoy y esta semana? | Hoy |
| Etapa | ¿En qué va cada trabajo? | Tablero |
| Persona | ¿Quién me debe y qué me ha pedido? | Clientes y Cobros |

### Mapa de contenidos

```
Hoy
├── Vencen hoy y esta semana
├── Plazo largo
├── Hecho esta semana
└── Me deben (resumen)

Tablero
├── Cotizado / En diseño / Aprobado / En producción / Entregado
└── Ficha del trabajo
    ├── Datos
    ├── Pagos y saldo
    └── Enviar mensaje (WhatsApp / correo)

Clientes
├── Lista
└── Ficha del cliente (contacto, trabajos, saldo)

Cobros
├── Pendientes por cliente
└── Enviar recordatorio
```

### Etiquetas

| Etiqueta | En lugar de | Motivo |
|---|---|---|
| Trabajo | Orden, ticket, pedido | Es la palabra que ella usa |
| Cotización | Presupuesto, propuesta | Coincide con su vocabulario |
| Entrega | Fecha límite | Más natural |
| Me deben | Cuentas por cobrar | Lenguaje cotidiano |
| Hoy | Dashboard | Dice lo que muestra |

### Navegación

- Celular: barra inferior con Hoy, Tablero, Clientes y Cobros, y botón flotante "+ Nuevo trabajo".
- Notebook: el mismo menú en barra lateral.
- Mismos nombres y orden en ambos dispositivos.

### Flujo principal

Tarea: registrar un trabajo nuevo y enviar la cotización.

1. Hoy: toca "+ Nuevo trabajo".
2. Cliente: elige uno existente o escribe uno nuevo.
3. Datos del trabajo: descripción, cantidad, precio y fecha de entrega.
4. Cotización lista: la app arma el mensaje con la plantilla.
5. Enviar: elige WhatsApp o correo; se abre su aplicación con el texto prellenado y ella lo envía.
6. Confirmación: el trabajo queda en "Cotizado" y aparece en el tablero.

Son 6 pasos agrupados en 3 pantallas en el prototipo (cliente, datos, cotización
lista). Objetivo medible: registrar un trabajo con cliente existente en menos de
1 minuto.

### Flujos secundarios

- Actualizar estado: Tablero, arrastrar la tarjeta (2 pasos).
- Cobrar: Cobros, elegir trabajo, "Enviar recordatorio", WhatsApp o correo.
- Registrar pago: ficha del trabajo, "Registrar pago", monto.

Diagrama: ver `../evidencias/diagrama-flujo.png`.
