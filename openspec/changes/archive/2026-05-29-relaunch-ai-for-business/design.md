## Context

La web vive en un único `index.html` (~990 líneas) con CSS y JS inline, sin build ni dependencias, desplegado en GitHub Pages (`dataplex.es`). El relanzamiento es casi una reescritura del contenido y del lenguaje visual, manteniendo las restricciones del proyecto: single-file, estático, sin framework ni paso de build. Los assets de marca (icono de puntos concéntricos en SVG, versiones clara/oscura) están en `/Users/.../Dataplex/Logos`. La referencia de tono y estética es Harvey.ai (claro, editorial, serio). El posicionamiento y la estrategia de credibilidad están fijados (ver `proposal.md` y memoria de proyecto).

## Goals / Non-Goals

**Goals:**
- Reescribir `index.html` con la estructura, narrativa y estética nuevas cumpliendo las specs de `brand-identity`, `homepage-narrative`, `product-showcase` y `credibility`.
- Mantener el sitio como un único HTML estático servible sin build.
- Estética clara/editorial con el azul `#00aaff` como acento puntual.
- Sustituir el logo de píxeles por el icono de puntos concéntricos (SVG), incluido favicon.
- Presentar los 4 productos con tono de negocio y la sección de método/credibilidad.

**Non-Goals:**
- Formulario de contacto funcional con backend real (Formspree), aviso legal, privacidad, banner de cookies y SEO avanzado → cambio `corporate-compliance`.
- Multipágina, blog, CMS o i18n.
- Introducir build tools, frameworks o dependencias.
- Crear nuevos assets de marca desde cero (se reutilizan los existentes).

## Decisions

- **Seguir en single-file `index.html` con CSS/JS inline.** Coherente con el proyecto y GitHub Pages; evita complejidad innecesaria. Alternativa descartada: separar CSS/JS o introducir un generador estático — sobredimensionado para una landing.
- **Rediseño de tokens hacia tema claro.** Redefinir las CSS custom properties de `:root`: fondo claro/crema, texto oscuro, superficies claras, y `#00aaff` reservado a acentos. Alternativa descartada: mantener tema oscuro (rechazada por el usuario; Harvey es claro y es la fuente de su seriedad).
- **Logo como SVG inline reutilizable.** Portar el icono de puntos concéntricos del experimento `Logos/icon_circles_dots_v1.1.html` a SVG inline en nav/footer y como favicon `data:image/svg+xml`. Alternativa descartada: PNG (no escala nítido; el SVG ya existe).
- **Tipografía orientada a negocio.** Sustituir el trío techie (Syne/Space Mono/Barlow Condensed) por una combinación más editorial y sobria (p. ej. una serif/grotesque elegante para titulares + sans legible para cuerpo), vía Google Fonts. La elección concreta se valida en implementación con vista previa.
- **Estructura de secciones explícita** hero → productos → método → credibilidad → contacto, con `id` para navegación e IntersectionObserver, reutilizando el patrón de scroll existente pero con realces discretos.
- **Credibilidad por composición de contenido**, no por widgets: bloques de cita a estudios externos (atribuidos), escenarios "Ejemplo:" claramente marcados y objetivos de servicio. Sin testimonios ni logos de clientes.

## Risks / Trade-offs

- [El cambio de datos de color a tema claro puede romper contrastes/legibilidad en componentes heredados] → Verificar contraste (WCAG AA) en vista previa antes de cerrar; revisar cada sección.
- [El logo de puntos en fondo claro puede perder fuerza visual frente al fondo oscuro original] → Usar la variante adecuada y ajustar opacidades/tamaño del icono sobre claro.
- [Sin resultados reales, la sección de credibilidad puede quedar vacía o poco convincente] → Apoyarse en estudios de terceros reales y escenarios ilustrativos etiquetados; encuadre de exclusividad. Recopilar 2-3 fuentes de prestigio durante la implementación.
- [Tentación de reaprovechar copy técnico antiguo] → El copy se reescribe desde el posicionamiento de negocio; no portar textos del sitio anterior.
- [Reescritura grande en un solo archivo dificulta la revisión] → Implementar por secciones y verificar con vista previa incrementalmente; PR único pero revisable por bloques.

## Migration Plan

- Trabajar en rama dedicada; implementar por secciones con vista previa local.
- Reemplazar `index.html` de forma incremental verificando estética y contraste.
- Conservar `CNAME`; el despliegue sigue siendo push a `main` → GitHub Pages.
- Rollback trivial: revertir el commit/PR (el sitio anterior queda en el historial).

## Open Questions

- Elección tipográfica final (familias concretas) — dirección acordada: serif elegante para titulares + sans legible para cuerpo; se concreta en implementación con vista previa.
- Estudios de terceros a citar — dirección acordada: McKinsey (potencial de la IA generativa) + fuente española/europea (Banco de España / Comisión Europea); seleccionar las referencias exactas en implementación.

Resuelto: CTA = "Agenda un diagnóstico" (consultivo). Orden de página = hero → enfoque → productos → credibilidad → sobre nosotros → FAQ → contacto → footer. Nombres de producto reencuadrados (ver `proposal.md` y spec `product-showcase`); el copy fino de cada producto se aborda en una fase posterior.
