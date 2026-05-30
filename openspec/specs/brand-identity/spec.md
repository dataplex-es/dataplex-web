# brand-identity Specification

## Purpose
TBD - created by archiving change relaunch-ai-for-business. Update Purpose after archive.
## Requirements
### Requirement: Estética clara y editorial
El sitio SHALL usar un lenguaje visual editorial y serio, en la línea de Harvey.ai. La base SHALL ser clara (fondo claro/crema, texto oscuro de alto contraste, abundante espacio en blanco y tipografía de tamaño generoso), pero secciones concretas SHALL emplear un tratamiento oscuro para dar ritmo (ver requisito de ritmo de secciones). Tanto las secciones claras como las oscuras SHALL mantener contraste suficiente (mínimo WCAG AA en texto de cuerpo).

#### Scenario: Sección clara
- **WHEN** se carga una sección de base clara
- **THEN** el fondo es claro y el texto principal es oscuro, con contraste mínimo WCAG AA

#### Scenario: Sección oscura
- **WHEN** se carga una sección con tratamiento oscuro
- **THEN** el fondo es oscuro y el texto principal es claro, con contraste mínimo WCAG AA

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
El sitio SHALL definir una tipografía coherente y elegante adecuada a un tono de negocio/consultoría, con jerarquía clara entre titulares, subtítulos y cuerpo. El wordmark "Dataplex" SHALL usar una grotesca geométrica (Space Grotesk), distinta de la serif de los titulares, para una identidad de marca diferenciada.

#### Scenario: Jerarquía tipográfica
- **WHEN** se muestran titular, subtítulo y cuerpo en una sección
- **THEN** se distinguen por tamaño, peso y/o familia de forma consistente en toda la web

#### Scenario: Wordmark diferenciado
- **WHEN** se muestra el wordmark "Dataplex" (nav, hero, footer)
- **THEN** se renderiza en Space Grotesk, distinta de la tipografía de los titulares de sección

### Requirement: Retirada de elementos técnicos
El sitio SHALL eliminar los elementos de estética técnica del diseño anterior: ticker de tecnologías, indicadores "100% Open Source / Cloud Native First / Data-led", rejilla de fondo y efectos de glow neón.

#### Scenario: Sin ticker ni rejilla
- **WHEN** se recorre la página completa
- **THEN** no aparece el ticker de tecnologías, ni la rejilla de fondo, ni textos de "Open Source / Cloud Native", ni glows neón

### Requirement: Ritmo de secciones claro/oscuro
La página SHALL alternar secciones claras y oscuras para dar ritmo y gravedad. El hero, la credibilidad y el bloque de contacto+footer SHALL ser oscuros; la declaración de posicionamiento, el enfoque, los productos, el sobre nosotros y la FAQ SHALL ser claros.

#### Scenario: Momentos oscuros
- **WHEN** se recorre la página completa
- **THEN** el hero, la sección de credibilidad y el cierre de contacto+footer se presentan en oscuro, y el resto en claro

### Requirement: Foto editorial en el hero
El hero SHALL usar una fotografía editorial a sangre completa de un momento de negocio real, tratada (desaturada/sobria) y con un velo oscuro encima de forma que el texto blanco superpuesto mantenga contraste mínimo WCAG AA. La imagen MUST ser de licencia libre con uso comercial (p. ej. Unsplash/Pexels), MUST almacenarse en el repositorio y MUST NOT recurrir a clichés de IA (robots, cerebros, circuitos).

#### Scenario: Foto presente y legible
- **WHEN** se carga el hero
- **THEN** se muestra una fotografía editorial a sangre completa con velo oscuro y el texto blanco se lee con contraste suficiente

#### Scenario: Licencia y almacenamiento
- **WHEN** se revisa el origen de la imagen del hero
- **THEN** es de licencia libre para uso comercial y está servida desde el propio repositorio, no de un enlace externo

#### Scenario: Sin clichés de IA
- **WHEN** se observa el contenido de la fotografía
- **THEN** representa un momento de negocio real y no robots, cerebros ni circuitos

