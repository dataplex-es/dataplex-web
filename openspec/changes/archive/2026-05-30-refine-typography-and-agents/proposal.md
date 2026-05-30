## Why

Tras revisar el sitio en vivo, el usuario pide una ronda de pulido y una incorporación de contenido: ajustar el wordmark y la declaración tipográficamente, mejorar legibilidad/copys puntuales, hacer la FAQ más invitadora, y añadir el concepto de **agentes de IA** (procesos autónomos 24/7), que refuerza el posicionamiento (IA que ejecuta, no solo informa).

## What Changes

- **Wordmark "Dataplex" en Space Grotesk** (grotesca geométrica) en lugar de Fraunces, en nav, hero y footer. Los titulares de sección siguen en Fraunces.
- **Declaración de posicionamiento sin serif**: pasa de Fraunces a la sans del cuerpo, manteniendo tamaño y el contraste de color entre las dos frases.
- **Reducir el espacio entre el icono y "Dataplex"** en el lockup (nav, hero, footer).
- **Nueva sección "Agentes que trabajan por ti"** (en oscuro, entre enfoque y productos): agentes de IA que ejecutan procesos de forma autónoma 24/7/365, según las reglas del cliente. Con 3 micro-ideas.
- **Copy del producto 02 (Asesor de negocio con IA)**: eliminar la redundancia entre "para quién" y "resultado".
- **Errata del producto 03 (Control de gestión con IA)**: "qué te lo cuesta" → "qué te cuesta".
- **FAQ más visual**: más espacio entre preguntas y marcador (bullet) en el azul de marca, para invitar a clicar.

## Capabilities

### New Capabilities
<!-- Ninguna nueva; se modifican las existentes. -->

### Modified Capabilities
- `brand-identity`: se fija la tipografía del wordmark (Space Grotesk), distinta de la de titulares.
- `homepage-narrative`: la declaración pasa a sans-serif; se añade la sección de agentes de IA.

## Impact

- `index.html`: enlace de Google Fonts (añadir Space Grotesk), variables/estilos del wordmark, declaración, lockup (gap), FAQ (espaciado + marcador), copys de producto 02 y 03, y nueva sección de agentes.
- Sin nuevas dependencias ni assets. No afecta a despliegue ni a `CNAME`.
- Modifica las specs base `brand-identity` y `homepage-narrative`.
