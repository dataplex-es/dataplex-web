## Context

Ajustes de pulido sobre el sitio en producción (single-file `index.html`). Sin cambios estructurales.

## Goals / Non-Goals

**Goals:** lockup del hero más grande; "Decisiones más inteligentes." en una línea; FAQ menos separada; envío de formulario sin redirección.

**Non-Goals:** cambiar contenido, páginas legales o el endpoint de Formspree.

## Decisions

- **Envío AJAX**: interceptar el `submit`, enviar con `fetch` a Formspree con cabecera `Accept: application/json` y mostrar confirmación in situ. La validación nativa (incluido el consentimiento `required`) se ejecuta antes del envío. Alternativa descartada: `mailto` (peor UX) y dejar la redirección de Formspree (lo que el usuario quería evitar).
- **Hero**: ampliar `hero-content` a 960px y bajar el máximo del titular a 56px para que la primera línea quepa; lockup a ~84px de icono y 40px de wordmark.
- **FAQ**: `padding` por pregunta de 34px a 26px.

## Risks / Trade-offs

- [El titular en una línea depende del ancho] → en móvil envuelve de forma natural; verificado en preview.
- [Formspree puede requerir confirmación de email la primera vez] → ya gestionado por el usuario.

## Open Questions

- Ninguna.
