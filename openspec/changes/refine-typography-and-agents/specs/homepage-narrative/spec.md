## MODIFIED Requirements

### Requirement: Estructura de página única
El sitio SHALL ser una única página con secciones en este orden: navegación, hero, declaración de posicionamiento, enfoque, agentes, productos, credibilidad, sobre nosotros, FAQ, contacto y footer. La declaración SHALL ir justo después del hero; el enfoque antes de los agentes; y los agentes antes de los productos. Cada sección de contenido SHALL tener un `id` referenciable.

#### Scenario: Orden de secciones
- **WHEN** se hace scroll desde arriba hasta abajo
- **THEN** las secciones aparecen en el orden: hero → declaración → enfoque → agentes → productos → credibilidad → sobre nosotros → FAQ → contacto → footer

### Requirement: Sección de declaración de posicionamiento
La página SHALL incluir, justo después del hero, una sección de declaración de posicionamiento destacada (tipografía grande, sin serif) con el texto: "Dataplex es IA diseñada para la dirección y la gestión de la PYME. Lleva a tu empresa las capacidades que antes solo tenían las grandes corporaciones y libera a tu equipo para centrarse en lo que realmente aporta valor." La segunda frase SHALL distinguirse de la primera por color (más atenuada).

#### Scenario: Declaración presente tras el hero
- **WHEN** se pasa del hero a la siguiente sección
- **THEN** se muestra la declaración con ese texto, en tipografía sans-serif grande y con la segunda frase en color más atenuado

## ADDED Requirements

### Requirement: Sección de agentes de IA
La página SHALL incluir una sección "Agentes" (entre enfoque y productos) que presente el concepto de agentes de IA que ejecutan procesos de forma autónoma y continua (24/7/365) según las reglas del cliente, comunicando que el negocio sigue funcionando aunque el usuario no esté.

#### Scenario: Concepto de agentes presente
- **WHEN** se lee la sección de agentes
- **THEN** comunica que son procesos autónomos que trabajan de forma continua (24/7/365) según las reglas del cliente, liberando al equipo de lo repetitivo
