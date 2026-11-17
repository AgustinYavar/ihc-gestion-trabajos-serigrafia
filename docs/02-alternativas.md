# 2. Diseño de alternativas

## Alternativas consideradas

**A. Planilla compartida o tablero tipo Trello.** Registro manual de pedidos en
una hoja de cálculo o tarjetas. Gratuita y de aprendizaje inmediato, pero no
genera alertas de plazos, no calcula saldos y no prepara mensajes.

**B. Uso avanzado de WhatsApp Business.** Etiquetas, respuestas rápidas y
catálogo. Es la más cercana al hábito actual, pero mantiene la información
dentro de los chats, no sigue plazos ni cobros y no cubre el correo.

**C. Aplicación web de gestión con canal dual.** Aplicación adaptable a celular
y notebook que centraliza trabajos, clientes, cobros y plazos, y prepara
mensajes listos para enviar por WhatsApp (enlace `wa.me`) o correo (`mailto:`).
El envío siempre lo hace la usuaria. Exige más desarrollo, pero responde
directamente a los hallazgos de la entrevista.

## Criterios (derivados de la entrevista)

| Criterio | Origen |
|---|---|
| Centralización de la información | Dolor principal: revisar muchos chats |
| Visibilidad de plazos | Olvido de trabajos pequeños o de plazo largo |
| Control de cobros | Deudas que hoy "solo se recuerdan" |
| Compatibilidad con su flujo actual | Clientes que ya usan WhatsApp y Gmail |
| Esfuerzo de adopción | Usuaria sin experiencia en herramientas de gestión |
| Costo | Negocio pequeño |

## Comparación

Escala de 1 (responde mal) a 3 (responde bien). Valoración cualitativa basada
en la entrevista.

| Criterio | A. Planilla / Trello | B. WhatsApp Business | C. App con canal dual |
|---|---|---|---|
| Centralización de la información | 2 | 1 | 3 |
| Visibilidad de plazos | 2 | 1 | 3 |
| Control de cobros | 2 | 1 | 3 |
| Compatibilidad con su flujo actual | 1 | 3 | 3 |
| Esfuerzo de adopción | 2 | 3 | 2 |
| Costo | 3 | 3 | 2 |
| **Total** | **12** | **12** | **16** |

## Alternativa seleccionada: C

1. **Responde a la causa del problema:** solo C reúne pedidos, plazos y cobros en un lugar.
2. **Respeta su forma de trabajar:** no obliga a abandonar WhatsApp ni Gmail.
3. **Es factible:** al usar enlaces en vez de APIs, el desarrollo se mantiene acotado.

Contrapartida: más esfuerzo de desarrollo y adopción. Se mitiga con un diseño
simple, vocabulario de la usuaria y funciones acotadas.

## Fuera de alcance y trabajo futuro

Integración con API de WhatsApp Business y Gmail, portal para clientes,
reportes avanzados y facturación.
