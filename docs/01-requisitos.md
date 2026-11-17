# 1. Descubrimiento de requisitos

Fuente de los hallazgos: ver `../evidencias/entrevista-usuaria.md`.

## Problema de interacción

La dueña de un negocio de serigrafía e impresión gestiona pedidos,
cotizaciones, aprobaciones y cobros a través de múltiples chats de WhatsApp y
correos, sin un registro centralizado. Esto genera olvidos de trabajos, falta
de visibilidad de plazos y deudas, y esfuerzo constante de revisión manual.

## Usuaria

Publicista y dueña del negocio, que trabaja sola y atiende principalmente a
clientes recurrentes que le escriben por WhatsApp. Maneja varios trabajos en
paralelo y prioriza los urgentes. Usa notebook y celular. No usa herramientas
de gestión.

Los clientes quedan fuera del alcance: ya se comunican por WhatsApp y correo,
no necesitan adoptar nada, y el problema está en la gestión interna.

## Contexto de uso

Uso diario, alternando entre el celular (recibir pedidos, responder rápido) y
el notebook (cotizar, diseñar, revisar). Interrupciones frecuentes y tiempo
limitado, por lo que las acciones deben ser rápidas.

## Tarea principal

Registrar un trabajo y darle seguimiento desde la solicitud hasta la entrega y
el pago.

## Situación observada y requisito

| Situación observada | Requisito |
|---|---|
| Pedidos, cotizaciones y aprobaciones repartidos en muchos chats | RF1, RF2, RF3: centralizar trabajos, estados y clientes |
| Se olvidan trabajos pequeños o de plazo largo | RF6: mostrar entregas próximas, incluidos los de plazo largo |
| No hay control de quién debe | RF5, RF9: pagos, saldos y recordatorios de cobro |
| Cotiza y aprueba por WhatsApp y Gmail | RF4: preparar mensajes para ambos canales |
| Quiere saber cuánto se hizo en la semana | RF8: resumen semanal (surgió del feedback) |

## Requisitos funcionales

- RF1. Registrar un trabajo con cliente, descripción, cantidad, fecha de entrega y precio.
- RF2. Asignar y cambiar el estado del trabajo (cotizado, en diseño, aprobado, en producción, entregado).
- RF3. Mantener una ficha por cliente con su historial de trabajos.
- RF4. Preparar cotizaciones y mensajes para enviar por WhatsApp o correo.
- RF5. Registrar pagos y mostrar saldos pendientes por cliente.
- RF6. Mostrar los trabajos próximos a vencer, incluyendo los de plazo largo.
- RF7. Buscar y filtrar por cliente, estado o fecha.
- RF8. Mostrar un resumen de lo realizado en la semana.
- RF9. Enviar un recordatorio de cobro con un clic.

## Requisitos no funcionales

- RNF1. Usable desde celular y notebook (diseño adaptable).
- RNF2. Aprendizaje rápido, sin capacitación.
- RNF3. Registrar un trabajo en pocos pasos (objetivo: menos de 1 minuto con cliente existente).
- RNF4. Lenguaje cercano a su vocabulario: "trabajo", "cotización", "entrega", "me deben".
- RNF5. No requiere que los clientes cambien su forma de comunicarse.
