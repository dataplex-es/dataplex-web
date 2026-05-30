## MODIFIED Requirements

### Requirement: Sección de contacto y conversión
La página SHALL incluir una sección de contacto con la acción de conversión "Agenda un diagnóstico" y los datos de contacto. El formulario SHALL incluir una casilla de **consentimiento obligatoria** con enlace a la política de privacidad antes de poder enviarse, y SHALL tener un destino de envío operativo (Formspree con ID real o, en su defecto, un fallback `mailto`).

#### Scenario: Acción de conversión presente
- **WHEN** se llega a la sección de contacto
- **THEN** se ofrece una vía clara para agendar un diagnóstico/contacto y se muestra el email de contacto

#### Scenario: Consentimiento obligatorio
- **WHEN** el usuario intenta enviar el formulario sin marcar el consentimiento
- **THEN** el formulario no se envía y se solicita marcar la casilla, que enlaza a la política de privacidad

#### Scenario: Envío operativo
- **WHEN** el usuario completa el formulario y marca el consentimiento
- **THEN** el envío se dirige a un destino operativo (Formspree o mailto)
