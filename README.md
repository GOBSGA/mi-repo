# Rentia — Tu arriendo, garantizado

Prototipo funcional (solo frontend) de una webapp para dueños pequeños de
inmuebles en Colombia que arriendan sin inmobiliaria.

**Propuesta de valor:** garantizamos y adelantamos el arriendo cada mes;
nosotros nos encargamos de cobrarle al inquilino, incluso en efectivo
(Efecty / Baloto).

## Cómo verlo

Abre `index.html` en cualquier navegador. No requiere instalación ni build:
React, Babel y Tailwind se cargan por CDN (necesitas conexión a internet).

## Qué incluye

- **Onboarding del dueño (3 pasos):** inmueble → inquilino (transferencia o
  efectivo) → plan (*Arriendo Garantizado*, tarifa fija ~8%, o *Solo Gestión
  de Cobro*, ~4%).
- **Dashboard:** tarjetas por inmueble con estado del mes (Adelantado ✓ /
  Cobrando al inquilino / En mora), próximo desembolso e historial de pagos.
- **Vista de cobranza:** link de pago y generación de código de pago en
  efectivo con recibo tipo Efecty/Baloto; el flujo del dinero deja claro que
  el efectivo entra a Rentia, nunca al dueño.
- **Simulador ("avanzar un mes"):** el día 1 se adelanta el arriendo al dueño
  y luego cada inquilino paga a su manera (a tiempo, tarde, en efectivo o cae
  en mora). El dueño nunca se ve afectado.

## Notas técnicas

- Un solo archivo (`index.html`): React 18 + Tailwind, componentes
  funcionales con `useState`/`useReducer`.
- Todo el estado vive en memoria (sin backend, sin `localStorage`); al
  recargar, vuelve a los datos de ejemplo (3 inmuebles en distintos estados).
- Es un prototipo de demostración: los pagos, códigos y gestiones son
  simulados.
