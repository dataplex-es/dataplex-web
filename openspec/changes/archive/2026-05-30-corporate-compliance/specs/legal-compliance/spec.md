## ADDED Requirements

### Requirement: Aviso legal
El sitio SHALL ofrecer una página de aviso legal que identifique al titular (Omniplex, S.L., nombre comercial Dataplex) con sus datos identificativos (CIF, domicilio, dominio y contacto) e incluya propiedad intelectual, exención de responsabilidad y legislación aplicable, conforme a la LSSI-CE.

#### Scenario: Aviso legal accesible
- **WHEN** el usuario abre la página de aviso legal desde el footer
- **THEN** ve al titular Omniplex, S.L., sus datos identificativos y las cláusulas legales

### Requirement: Política de privacidad
El sitio SHALL ofrecer una política de privacidad conforme al RGPD/LOPDGDD que indique responsable, datos tratados (los del formulario), finalidad, base jurídica (consentimiento), plazo de conservación, destinatarios (incluida transferencia internacional si aplica) y los derechos del interesado con la vía para ejercerlos.

#### Scenario: Privacidad accesible
- **WHEN** el usuario abre la política de privacidad desde el footer o el formulario
- **THEN** ve responsable, finalidad, base legal, conservación, destinatarios y derechos RGPD

### Requirement: Política de cookies
El sitio SHALL ofrecer una política de cookies que describa qué cookies se usan (o que no se usan cookies de seguimiento), los terceros implicados (p. ej. Google Fonts, Formspree) y cómo gestionarlas.

#### Scenario: Cookies accesible
- **WHEN** el usuario abre la política de cookies desde el footer o el banner
- **THEN** ve la descripción de cookies, terceros y gestión

### Requirement: Aviso de cookies
El sitio SHALL mostrar un aviso de cookies en la primera visita con un enlace a la política y una acción para aceptarlo/cerrarlo, y SHALL recordar la elección para no volver a mostrarlo.

#### Scenario: Primera visita
- **WHEN** el usuario entra por primera vez
- **THEN** se muestra el aviso de cookies con enlace a la política y opción de aceptar

#### Scenario: Visitas posteriores
- **WHEN** el usuario ya aceptó/cerró el aviso
- **THEN** el aviso no vuelve a mostrarse

### Requirement: Enlaces legales en el footer
El footer de todas las páginas SHALL incluir enlaces a aviso legal, política de privacidad y política de cookies.

#### Scenario: Enlaces presentes
- **WHEN** se muestra el footer en cualquier página
- **THEN** contiene enlaces a aviso legal, privacidad y cookies
