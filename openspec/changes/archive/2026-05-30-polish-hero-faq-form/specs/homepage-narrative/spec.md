## MODIFIED Requirements

### Requirement: Sección de contacto y conversión
La página SHALL incluir una sección de contacto con la acción de conversión "Agenda un diagnóstico" y los datos de contacto. El formulario SHALL incluir una casilla de consentimiento obligatoria con enlace a la política de privacidad antes de poder enviarse, y SHALL enviarse de forma asíncrona (AJAX) a un destino operativo (Formspree), mostrando una confirmación en la propia página sin redirigir al usuario fuera del sitio. Si el envío falla, SHALL mostrarse un mensaje de error en la página.

#### Scenario: Acción de conversión presente
- **WHEN** se llega a la sección de contacto
- **THEN** se ofrece una vía clara para agendar un diagnóstico/contacto y se muestra el email de contacto

#### Scenario: Consentimiento obligatorio
- **WHEN** el usuario intenta enviar el formulario sin marcar el consentimiento
- **THEN** el formulario no se envía y se solicita marcar la casilla, que enlaza a la política de privacidad

#### Scenario: Envío sin redirección
- **WHEN** el usuario envía el formulario correctamente
- **THEN** el envío se realiza de forma asíncrona y se muestra un mensaje de agradecimiento en la página, sin navegar a una página externa

#### Scenario: Error de envío
- **WHEN** el envío falla
- **THEN** se muestra un mensaje de error en la página y el usuario puede reintentar
