## Why

La web actual posiciona a Dataplex como una consultoría de datos genérica y técnica (ticker de tecnologías, "100% Open Source", "Cloud Native", estética oscura neón) dirigida a un perfil de ingeniería de datos. El negocio real es otro: **consultoría de IA para la dirección y gestión de la PYME**, dirigida a CEO, CFO, COO, gerentes y despachos contables. El sitio le habla al público equivocado con el tono equivocado, y no presenta los productos vendibles que ya existen. Hay que relanzarlo para que respire seriedad y negocio (referencia: Harvey.ai).

## What Changes

- **BREAKING** Reposicionamiento completo del mensaje: de "consultoría de datos/IA técnica" a "IA para decisiones y procesos de la PYME". Nuevo tagline: *"Decisiones más inteligentes. Procesos más eficientes."*
- **BREAKING** Cambio total de estética: de oscuro/neón/techie a **claro y editorial** estilo Harvey (fondo claro, mucho aire, tipografía elegante, azul Dataplex `#00aaff` solo como acento puntual).
- Nuevo logo: icono de **puntos concéntricos** (gradiente de densidad) en lugar del cuadrado de píxeles 8×8 actual; wordmark "DATAPLEX".
- Nuevo **orden de página**: hero → enfoque (tesis + cómo trabajamos) → productos → credibilidad → sobre nosotros → FAQ → contacto → footer. El enfoque va **antes** que los productos: la consultora vende primero su tesis, luego su catálogo.
- Sección de **enfoque** con la tesis de **democratización** (capacidades de gran empresa, ahora al alcance de la PYME gracias a la IA) y un bloque **"Cómo trabajamos"** con el proceso en 4 pasos: Diagnóstico → Diseño → Implantación → Acompañamiento (recoge el modelo implantación + mantenimiento).
- Sustituir los 4 servicios abstractos (Analítica, IA, Ing. Datos, Estrategia) por los **4 productos concretos y vendibles**, en este orden y con nombres aspiracionales pero concretos: **Formación en IA para directivos** · **Asesor de negocio con IA** · **Control de gestión con IA** · **Propuestas comerciales con IA**. Cada uno con qué hace, para quién y qué resultado busca. (El trabajo fino de copy/fichas de producto se aborda en una fase posterior.)
- Nueva sección de **credibilidad** basada en estudios de terceros de prestigio + escenarios ilustrativos claramente etiquetados + objetivos de servicio + encuadre de fase temprana como exclusividad. **Sin inventar clientes, testimonios ni métricas.**
- Nueva sección **"Sobre nosotros"**: profesionales con trayectoria en consultoría de gran empresa que ponen ese conocimiento al servicio de la PYME (sin personalizar en nadie aún). Refuerza la tesis: el equipo es la prueba de la democratización.
- Nueva sección **FAQ** con las dudas típicas de un directivo antes de contratar (datos, seguridad, duración, tamaño de empresa, facturación, impacto en el equipo).
- **CTA dominante** consultivo, orientado a la venta de implantación: **"Agenda un diagnóstico"**.
- **Eliminar** elementos técnicos: ticker de tecnologías, stats "100% Open Source / Cloud Native / Data-led", rejilla de fondo y glows neón.
- Mantener: single-page, despliegue GitHub Pages, idioma español.

Fuera de alcance (cambio posterior `corporate-compliance`): aviso legal, política de privacidad, política y banner de cookies (RGPD), formulario de contacto funcional (Formspree real), SEO. Aquí el formulario se rediseña visualmente pero su backend real se aborda en ese cambio.

## Capabilities

### New Capabilities
- `brand-identity`: lenguaje visual del sitio — estética clara editorial, logo de puntos concéntricos, tipografía, tokens de diseño y retirada de los elementos técnicos/neón.
- `homepage-narrative`: estructura y flujo de la página única — navegación, hero (tagline + CTA), sección de método/democratización, sección de contacto/conversión, orden de secciones y comportamientos de scroll.
- `product-showcase`: presentación de los 4 productos de IA, cada uno con propuesta (qué hace · para quién · qué resultado).
- `credibility`: contenido de confianza sin fabricación — estudios de terceros, escenarios ilustrativos etiquetados, objetivos de servicio y encuadre de fase temprana.

### Modified Capabilities
<!-- No hay specs previas en openspec/specs/. Es el primer conjunto de capacidades. -->

## Impact

- `index.html`: reescritura prácticamente total (estructura HTML de secciones, CSS inline / tokens, copy, SVGs de logo e iconos, script de scroll). Es el único archivo de la web.
- Assets de marca: se toma como referencia `/Users/josep.salom/Documents/Business/Empreneduria/Dataplex/Logos` (icono de puntos concéntricos, versiones clara/oscura).
- Metadatos: `<title>`, `meta description`, Open Graph y favicon SVG se actualizan al nuevo posicionamiento y logo.
- Sin nuevas dependencias ni build step (sigue siendo HTML estático servible directamente).
- No afecta a `CNAME` ni al flujo de despliegue.
