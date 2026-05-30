## Why

Ajustes finos tras revisar el sitio en producción: el lockup del hero se ve pequeño, el titular parte "inteligentes" en otra línea, la FAQ quedó demasiado separada, y el envío del formulario redirige a la página de Formspree (experiencia poco cuidada).

## What Changes

- **Hero**: el lockup (icono + "Dataplex") se agranda (~el doble) y el titular se ajusta para que "Decisiones más inteligentes." quepa en una sola línea (columna más ancha y tamaño de titular afinado).
- **FAQ**: se reduce el espacio vertical entre preguntas (de 34px a 26px).
- **Formulario**: el envío pasa a ser **asíncrono (AJAX)**; el usuario permanece en dataplex.es y ve un mensaje de agradecimiento en lugar de ser redirigido a Formspree. Se mantiene el consentimiento y el endpoint de Formspree.

## Capabilities

### New Capabilities
<!-- Ninguna nueva. -->

### Modified Capabilities
- `homepage-narrative`: el formulario de contacto se envía sin redirección (AJAX) mostrando confirmación en la página.

## Impact

- `index.html`: tamaños del lockup y del titular del hero, anchura de la columna del hero, espaciado de la FAQ, y handler JS de envío AJAX del formulario + estilos del mensaje de confirmación/error.
- Sin nuevas dependencias. No afecta a páginas legales ni a despliegue.
