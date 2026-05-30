## Context

Sitio estático single-file (`index.html`) en GitHub Pages. Faltan los mínimos legales (LSSI-CE, RGPD). Titular: Omniplex, S.L. (nombre comercial Dataplex). Datos registrales pendientes de confirmación del usuario. El formulario apunta a un Formspree placeholder.

## Goals / Non-Goals

**Goals:**
- Páginas legales (aviso legal, privacidad, cookies) accesibles desde el footer.
- Banner de cookies con memoria de elección.
- Formulario con consentimiento obligatorio y destino operativo.

**Non-Goals:**
- Cambiar diseño o contenido del resto del sitio.
- Analítica o cookies de seguimiento (no se añaden).
- Self-hosting de fuentes (se recomienda, no se implementa aquí).

## Decisions

- **Páginas legales como HTML estáticos separados** (`aviso-legal.html`, `privacidad.html`, `cookies.html`), enlazadas desde el footer. Coherente con sitio estático sin build. Cada una con una plantilla mínima y los tokens de marca (claro, Inter/Fraunces/Space Grotesk, columna de lectura).
- **Banner de cookies propio** (sin librería): div fijo + JS que guarda la aceptación en `localStorage`. Dado que no hay cookies de seguimiento, el banner es informativo (no bloqueante).
- **Formulario**: añadir `<input type="checkbox" required>` de consentimiento con enlace a privacidad. Para el envío, dos opciones según decida el usuario: (a) ID real de Formspree, o (b) fallback `mailto:hola@dataplex.es`. Por defecto se deja Formspree con marcador y se documenta.
- **Datos de Omniplex, S.L.**: se rellenan con los datos públicos encontrados (CIF B44816619; Ronda General Mitre 172, 08006 Barcelona), pendientes de confirmación del usuario antes de publicar.

## Risks / Trade-offs

- [Datos legales incorrectos (otra "Omniplex SL")] → No publicar hasta que el usuario confirme CIF/domicilio/datos registrales; la revisión del PR es el punto de verificación.
- [Google Fonts transfiere IP a Google (RGPD)] → Documentarlo en la política de cookies; recomendar self-hosting como mejora posterior.
- [Formulario sin ID de Formspree no envía] → Pedir el ID o usar fallback mailto; no dar por "funcional" hasta resolverlo.
- [Textos legales como plantilla genérica] → Son base estándar; el usuario debería validarlos (idealmente con asesoría) antes de publicar.

## Open Questions

- Confirmar datos de Omniplex, S.L. (CIF, domicilio, tomo/folio/hoja registral).
- Formulario: ¿ID de Formspree (cuál) o fallback mailto?
