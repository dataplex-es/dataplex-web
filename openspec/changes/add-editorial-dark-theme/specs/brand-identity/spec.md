## MODIFIED Requirements

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

## ADDED Requirements

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
