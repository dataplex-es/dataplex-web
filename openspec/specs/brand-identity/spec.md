# brand-identity Specification

## Purpose
TBD - created by archiving change relaunch-ai-for-business. Update Purpose after archive.
## Requirements
### Requirement: Estética clara y editorial
El sitio SHALL usar un lenguaje visual claro y editorial (fondo claro/crema, texto oscuro de alto contraste, abundante espacio en blanco y tipografía de tamaño generoso), transmitiendo seriedad y orientación a negocio en la línea de Harvey.ai.

#### Scenario: Fondo y contraste base
- **WHEN** se carga cualquier sección de la página
- **THEN** el fondo es claro y el texto principal es oscuro, con contraste suficiente para lectura cómoda (mínimo WCAG AA en texto de cuerpo)

#### Scenario: Espacio en blanco
- **WHEN** se renderiza una sección de contenido
- **THEN** existe padding vertical amplio entre secciones y márgenes generosos, sin densidad visual recargada

### Requirement: Azul Dataplex como acento puntual
El color azul de marca (`#00aaff`) SHALL emplearse únicamente como acento puntual (enlaces, CTA, icono, detalles), nunca como color dominante ni como fondo de página.

#### Scenario: Uso contenido del acento
- **WHEN** se inspecciona la proporción de color azul en una vista
- **THEN** el azul aparece solo en elementos de énfasis (botones, logo, microdetalles) y no domina la composición

### Requirement: Logo de puntos concéntricos
El sitio SHALL usar como identidad el icono de puntos concéntricos (gradiente de densidad de datos) y el wordmark "DATAPLEX", reemplazando el icono de cuadrado de píxeles 8×8 anterior. El logo SHALL renderizarse como SVG nítido en nav, favicon, hero (si aplica) y footer.

#### Scenario: Logo en navegación
- **WHEN** se muestra la barra de navegación
- **THEN** aparece el icono de puntos concéntricos junto al wordmark "DATAPLEX" en SVG

#### Scenario: Favicon coherente
- **WHEN** el navegador solicita el favicon
- **THEN** se sirve un favicon SVG con el icono de puntos concéntricos, no el cuadrado de píxeles anterior

### Requirement: Sistema tipográfico de negocio
El sitio SHALL definir una tipografía coherente y elegante adecuada a un tono de negocio/consultoría, con jerarquía clara entre titulares, subtítulos y cuerpo.

#### Scenario: Jerarquía tipográfica
- **WHEN** se muestran titular, subtítulo y cuerpo en una sección
- **THEN** se distinguen por tamaño, peso y/o familia de forma consistente en toda la web

### Requirement: Retirada de elementos técnicos
El sitio SHALL eliminar los elementos de estética técnica del diseño anterior: ticker de tecnologías, indicadores "100% Open Source / Cloud Native First / Data-led", rejilla de fondo y efectos de glow neón.

#### Scenario: Sin ticker ni rejilla
- **WHEN** se recorre la página completa
- **THEN** no aparece el ticker de tecnologías, ni la rejilla de fondo, ni textos de "Open Source / Cloud Native", ni glows neón

