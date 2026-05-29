## ADDED Requirements

### Requirement: Catálogo de los cuatro productos
La página SHALL presentar los cuatro productos actuales de Dataplex como oferta principal, en este orden, sustituyendo a los servicios abstractos anteriores: 1) Formación en IA para directivos, 2) Asesor de negocio con IA, 3) Control de gestión con IA, 4) Propuestas comerciales con IA. Los nombres son aspiracionales pero concretos; el copy detallado de cada ficha se afina en una fase posterior.

#### Scenario: Los cuatro productos presentes y ordenados
- **WHEN** se muestra la sección de productos
- **THEN** aparecen los cuatro productos en el orden indicado (Formación → Asesor de negocio → Control de gestión → Propuestas comerciales), y no los servicios genéricos anteriores (Analítica, IA, Ingeniería de Datos, Estrategia)

### Requirement: Ficha de producto orientada a negocio
Cada producto SHALL presentarse con: nombre, qué hace (en lenguaje de negocio), para quién es (perfil/rol destinatario) y qué resultado busca aportar. La redacción MUST evitar jerga técnica y centrarse en el resultado de negocio.

#### Scenario: Contenido de cada ficha
- **WHEN** se examina la ficha de cualquiera de los cuatro productos
- **THEN** incluye nombre, descripción de qué hace, destinatario y resultado de negocio esperado

#### Scenario: Tono de negocio
- **WHEN** se lee la descripción de un producto
- **THEN** no contiene jerga técnica (nombres de frameworks, infraestructura) y habla en términos de valor para el negocio

### Requirement: Productos presentados como vendibles ahora
Los productos SHALL presentarse como ofertas actuales y disponibles (no como "próximamente"), coherentes con que ya se implantan en clientes.

#### Scenario: Disponibilidad actual
- **WHEN** se muestra la sección de productos
- **THEN** el encuadre y las llamadas a la acción los tratan como servicios disponibles para contratar/implantar hoy
