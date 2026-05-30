## Why

La web no cumple aún los mínimos legales de un sitio corporativo en España (LSSI-CE y RGPD/LOPDGDD): falta aviso legal, política de privacidad y política de cookies, el formulario no recoge consentimiento ni tiene backend, y no hay aviso de cookies. Es lo "obligatorio" pendiente antes de promocionar el sitio.

## What Changes

- **Aviso legal** (`aviso-legal.html`): titular **Omniplex, S.L.** (nombre comercial Dataplex), CIF, domicilio, dominio, contacto, propiedad intelectual, responsabilidad y legislación aplicable.
- **Política de privacidad** (`privacidad.html`): responsable, datos del formulario, finalidad, base legal (consentimiento), conservación, destinatarios (Formspree y transferencia internacional), derechos RGPD y cómo ejercerlos.
- **Política de cookies** (`cookies.html`): tipos de cookies, estado actual (sin cookies de seguimiento), terceros (Google Fonts, Formspree) y gestión.
- **Enlaces legales en el footer** de todas las páginas (Aviso legal · Privacidad · Cookies).
- **Banner de cookies** informativo en `index.html` (aceptar/cerrar + enlace a la política), recordando la elección en `localStorage`.
- **Formulario**: casilla de **consentimiento** obligatoria con enlace a la privacidad; backend listo (Formspree) pendiente de ID real o, alternativamente, fallback `mailto`.
- Plantilla simple y coherente (tokens de marca) para las páginas legales.

## Capabilities

### New Capabilities
- `legal-compliance`: páginas legales (aviso legal, privacidad, cookies), banner de cookies y consentimiento del formulario conforme a LSSI-CE y RGPD.

### Modified Capabilities
- `homepage-narrative`: el footer incorpora enlaces legales; el formulario de contacto añade consentimiento y queda operativo.

## Impact

- Nuevos archivos: `aviso-legal.html`, `privacidad.html`, `cookies.html`.
- `index.html`: enlaces legales en footer, banner de cookies + JS, casilla de consentimiento en el formulario.
- Datos de Omniplex, S.L. pendientes de confirmación del usuario (CIF, domicilio, datos registrales) antes de publicar.
- Backend del formulario requiere ID de Formspree del usuario (o fallback mailto).
- Recomendación (fuera de alcance inmediato): self-hostear las fuentes para evitar la transferencia de IP a Google (Google Fonts).
