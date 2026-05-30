## MODIFIED Requirements

### Requirement: Estructura de página única
El sitio SHALL ser una única página con secciones en este orden: navegación, hero, declaración de posicionamiento, enfoque, productos, credibilidad, sobre nosotros, FAQ, contacto y footer. La declaración de posicionamiento SHALL aparecer justo después del hero, y el enfoque antes que los productos. Cada sección de contenido SHALL tener un `id` referenciable por la navegación.

#### Scenario: Orden de secciones
- **WHEN** se hace scroll desde arriba hasta abajo
- **THEN** las secciones aparecen en el orden: hero → declaración → enfoque → productos → credibilidad → sobre nosotros → FAQ → contacto → footer

### Requirement: Hero con propuesta de valor
El hero SHALL comunicar el posicionamiento con el tagline "Decisiones más inteligentes. Procesos más eficientes.", un mensaje de apoyo breve orientado a la PYME y un CTA dominante de conversión, sin jerga técnica. El hero SHALL mostrar el lockup de marca (icono de puntos + wordmark "Dataplex") y presentarse con tratamiento oscuro sobre la fotografía editorial.

#### Scenario: Tagline visible
- **WHEN** se carga la página
- **THEN** el hero muestra el tagline "Decisiones más inteligentes. Procesos más eficientes." de forma prominente

#### Scenario: Lockup de marca en el hero
- **WHEN** se muestra el hero
- **THEN** aparece el icono de puntos concéntricos junto al wordmark "Dataplex"

#### Scenario: CTA dominante
- **WHEN** se muestra el hero
- **THEN** existe un único CTA primario de conversión con la acción "Agenda un diagnóstico" claramente destacado

### Requirement: Sección de contacto y conversión
La página SHALL incluir una sección de contacto con la acción de conversión "Agenda un diagnóstico" y los datos de contacto. El formulario SHALL presentarse con la nueva estética; su backend funcional se define en el cambio `corporate-compliance`.

#### Scenario: Acción de conversión presente
- **WHEN** se llega a la sección de contacto
- **THEN** se ofrece una vía clara para agendar un diagnóstico/contacto y se muestra el email de contacto

## ADDED Requirements

### Requirement: Sección de declaración de posicionamiento
La página SHALL incluir, justo después del hero, una sección de declaración de posicionamiento destacada (estilo editorial, tipografía grande) con el texto: "Dataplex es IA diseñada para la dirección y la gestión de la PYME. Lleva a tu empresa las capacidades que antes solo tenían las grandes corporaciones y libera a tu equipo para centrarse en lo que realmente aporta valor."

#### Scenario: Declaración presente tras el hero
- **WHEN** se pasa del hero a la siguiente sección
- **THEN** se muestra la declaración de posicionamiento con ese texto, de forma prominente

### Requirement: Sitio sin enlaces a redes sociales
El sitio MUST NOT incluir enlaces a redes sociales (incluido LinkedIn) en ninguna sección, ni en contacto ni en el footer. El email SHALL mantenerse como vía de contacto. (Decisión provisional.)

#### Scenario: Sin LinkedIn en el sitio
- **WHEN** se recorre la página completa, incluido contacto y footer
- **THEN** no aparece ningún enlace a LinkedIn ni a otras redes sociales, y sí el email de contacto

### Requirement: La cabecera fija no solapa otros enlaces
Solo la barra de navegación principal (cabecera) SHALL tener posicionamiento fijo. Cualquier elemento de navegación o enlaces del footer SHALL renderizarse dentro del footer y MUST NOT solaparse con la cabecera ni quedar clavados en la parte superior.

#### Scenario: Enlaces del footer en su sitio
- **WHEN** se carga la página en la parte superior
- **THEN** la cabecera muestra el logo, los enlaces de navegación y el CTA, y ningún enlace del footer aparece solapado arriba
