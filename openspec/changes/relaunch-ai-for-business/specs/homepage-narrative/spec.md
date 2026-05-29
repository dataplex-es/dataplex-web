## ADDED Requirements

### Requirement: Estructura de página única
El sitio SHALL ser una única página con secciones en este orden: navegación, hero, enfoque, productos, credibilidad, sobre nosotros, FAQ, contacto y footer. El enfoque SHALL aparecer antes que los productos. Cada sección de contenido SHALL tener un `id` referenciable por la navegación.

#### Scenario: Orden de secciones
- **WHEN** se hace scroll desde arriba hasta abajo
- **THEN** las secciones aparecen en el orden: hero → enfoque → productos → credibilidad → sobre nosotros → FAQ → contacto → footer

### Requirement: Navegación de negocio
La navegación SHALL ofrecer enlaces a las secciones clave en lenguaje de negocio (p. ej. Productos, Enfoque, Contacto) más un CTA destacado de conversión, sin terminología técnica.

#### Scenario: Enlaces de navegación
- **WHEN** se muestra la barra de navegación
- **THEN** contiene enlaces a las secciones principales y un CTA de conversión visualmente diferenciado

#### Scenario: Navegación a sección
- **WHEN** el usuario pulsa un enlace de la navegación
- **THEN** la página se desplaza suavemente hasta la sección correspondiente

### Requirement: Hero con propuesta de valor
El hero SHALL comunicar el posicionamiento con el tagline "Decisiones más inteligentes. Procesos más eficientes.", un mensaje de apoyo orientado a la PYME y un CTA dominante de conversión, sin jerga técnica.

#### Scenario: Tagline visible
- **WHEN** se carga la página
- **THEN** el hero muestra el tagline "Decisiones más inteligentes. Procesos más eficientes." de forma prominente

#### Scenario: CTA dominante
- **WHEN** se muestra el hero
- **THEN** existe un único CTA primario de conversión con la acción "Agenda un diagnóstico" claramente destacado

### Requirement: Sección de enfoque y democratización
La página SHALL incluir una sección de enfoque, situada antes de los productos, que explique el método de Dataplex y la tesis de democratización: capacidades antes reservadas a la gran empresa, ahora accesibles a la PYME gracias a la IA.

#### Scenario: Mensaje de democratización
- **WHEN** se lee la sección de enfoque
- **THEN** comunica explícitamente que Dataplex acerca a la PYME capacidades antes solo disponibles para grandes empresas

#### Scenario: Enfoque precede a productos
- **WHEN** se recorre la página
- **THEN** la sección de enfoque aparece antes que la de productos

### Requirement: Bloque "Cómo trabajamos"
La sección de enfoque SHALL incluir un bloque "Cómo trabajamos" que describa el proceso de servicio en cuatro pasos: Diagnóstico, Diseño, Implantación y Acompañamiento, reflejando el modelo de implantación más mantenimiento.

#### Scenario: Proceso de cuatro pasos
- **WHEN** se lee el bloque "Cómo trabajamos"
- **THEN** se presentan los cuatro pasos (Diagnóstico → Diseño → Implantación → Acompañamiento) de forma ordenada

### Requirement: Sección "Sobre nosotros"
La página SHALL incluir una sección "Sobre nosotros" que presente al equipo como profesionales con trayectoria en consultoría para la gran empresa que ponen ese conocimiento al servicio de la PYME, sin nombrar a personas concretas por ahora.

#### Scenario: Credibilidad de equipo sin personalizar
- **WHEN** se lee la sección "Sobre nosotros"
- **THEN** comunica la experiencia del equipo en gran empresa al servicio de la PYME y no incluye nombres propios de personas

### Requirement: Sección FAQ
La página SHALL incluir una sección de preguntas frecuentes que resuelva las dudas típicas de un directivo antes de contratar (al menos: requisitos para empezar, confidencialidad/seguridad de datos, duración del proceso, idoneidad para PYME, facturación e impacto en el equipo).

#### Scenario: Dudas clave cubiertas
- **WHEN** se lee la sección FAQ
- **THEN** incluye preguntas y respuestas que cubren, como mínimo, datos/requisitos, seguridad/confidencialidad, duración, tamaño de empresa, facturación e impacto en el equipo

### Requirement: Sección de contacto y conversión
La página SHALL incluir una sección de contacto con la acción de conversión "Agenda un diagnóstico" y los datos de contacto. El formulario SHALL presentarse con la nueva estética; su backend funcional se define en el cambio `corporate-compliance`.

#### Scenario: Acción de conversión presente
- **WHEN** se llega a la sección de contacto
- **THEN** se ofrece una vía clara para agendar un diagnóstico/contacto y se muestran los datos de contacto

### Requirement: Comportamientos de scroll discretos
El sitio SHALL mantener realces de scroll discretos y acordes a la estética seria: resaltado del enlace de navegación de la sección activa y aparición progresiva (fade-in) de los bloques al entrar en viewport.

#### Scenario: Enlace activo según scroll
- **WHEN** una sección entra en el viewport durante el scroll
- **THEN** su enlace correspondiente en la navegación se marca como activo

#### Scenario: Aparición progresiva
- **WHEN** un bloque con animación entra en el viewport
- **THEN** aparece con una transición suave de opacidad/desplazamiento una sola vez
