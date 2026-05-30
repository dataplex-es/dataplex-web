## Why

El relanzamiento dejó la web demasiado plana: todo claro, sin contraste ni gravedad. La referencia (Harvey.ai) no es "todo claro" — alterna secciones claras y oscuras serias para dar ritmo y peso, y abre con una foto editorial y una declaración de posicionamiento potente. Además, un bug de CSS deja los enlaces del footer clavados en la cabecera. Esta iteración da gravedad a la estética, corrige el bug y refuerza el mensaje de marca.

## What Changes

- **Ritmo claro/oscuro**: hero, credibilidad y contacto+footer pasan a **oscuro**; enfoque, productos, declaración, sobre nosotros y FAQ siguen en **claro**.
- **Hero con foto a sangre completa**: imagen editorial de un momento de negocio real, desaturada y con velo oscuro, texto blanco legible encima. Foto de licencia libre (Unsplash/Pexels), descargada al repo en `/assets`. Sin clichés de IA (robots, cerebros, circuitos).
- **Lockup de logo en el hero**: icono de puntos + wordmark "Dataplex" (ahora falta en el hero).
- **Nueva "sección 2" de posicionamiento** (estilo Harvey), declaración potente: *"Dataplex es IA diseñada para la dirección y la gestión de la PYME. Lleva a tu empresa las capacidades que antes solo tenían las grandes corporaciones y libera a tu equipo para centrarse en lo que realmente aporta valor."*
- **Quitar LinkedIn de todo el sitio** (contacto y footer); se mantiene el email. Decisión provisional ("de momento").
- **Corregir el bug del nav**: la regla `nav { position:fixed }` afecta también al `<nav>` del footer y lo clava arriba; el posicionamiento fijo debe aplicar solo a la cabecera.
- Mantener: single-page, estático, tagline del hero, los 4 productos, estructura general y despliegue GitHub Pages.

## Capabilities

### New Capabilities
<!-- No se introducen capacidades nuevas; se modifican las existentes. -->

### Modified Capabilities
- `brand-identity`: la estética pasa de "todo claro" a editorial con **ritmo claro/oscuro**; se añade el tratamiento de **foto editorial en el hero**.
- `homepage-narrative`: se inserta la **sección de declaración de posicionamiento** tras el hero; el hero incorpora el **lockup de logo** y tratamiento oscuro; se retira **LinkedIn** de contacto y footer (solo email); se corrige el solapamiento del footer con la cabecera.

## Impact

- `index.html`: tokens/estilos para secciones oscuras, hero con foto + overlay, nueva sección de declaración, fix del selector `nav`, retirada de enlaces LinkedIn.
- Nuevo directorio `/assets` con la foto del hero (binario, licencia libre).
- Sin nuevas dependencias ni build step. No afecta a `CNAME` ni al despliegue.
- Modifica las specs base `brand-identity` y `homepage-narrative`.
