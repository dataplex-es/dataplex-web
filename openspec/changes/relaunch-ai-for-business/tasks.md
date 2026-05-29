## 1. Identidad visual y tokens (brand-identity)

- [x] 1.1 Redefinir las CSS custom properties de `:root` para tema claro/editorial (fondo claro/crema, texto oscuro, superficies claras) con `#00aaff` reservado a acentos
- [x] 1.2 Portar el icono de puntos concéntricos de `Logos/icon_circles_dots_v1.1.html` a SVG inline reutilizable
- [x] 1.3 Reemplazar el logo de nav y footer por el icono de puntos + wordmark "DATAPLEX"
- [x] 1.4 Sustituir el favicon SVG (`data:image/svg+xml`) por la versión de puntos concéntricos
- [x] 1.5 Integrar la tipografía de negocio (serif elegante para titulares + sans legible para cuerpo, vía Google Fonts) con jerarquía titular/subtítulo/cuerpo
- [x] 1.6 Eliminar ticker de tecnologías, stats "Open Source/Cloud Native/Data-led", rejilla de fondo y glows neón
- [x] 1.7 Verificar contraste WCAG AA del cuerpo de texto sobre el nuevo fondo claro

## 2. Estructura y narrativa (homepage-narrative)

- [x] 2.1 Establecer el orden de secciones con `id`: hero → enfoque → productos → credibilidad → sobre nosotros → FAQ → contacto → footer
- [x] 2.2 Reescribir la navegación en lenguaje de negocio (Enfoque, Productos, Contacto…) + CTA "Agenda un diagnóstico" destacado
- [x] 2.3 Reescribir el hero con el tagline "Decisiones más inteligentes. Procesos más eficientes.", mensaje de apoyo y CTA dominante "Agenda un diagnóstico"
- [x] 2.4 Redactar la sección de enfoque con la tesis de democratización (capacidades de gran empresa al alcance de la PYME), situada antes de productos
- [x] 2.5 Añadir el bloque "Cómo trabajamos" (Diagnóstico → Diseño → Implantación → Acompañamiento)
- [x] 2.6 Redactar la sección "Sobre nosotros" (equipo veterano de gran consultora al servicio de la PYME, sin nombres propios)
- [x] 2.7 Redactar la sección FAQ con las 6 preguntas clave (requisitos para empezar, seguridad/confidencialidad, duración, idoneidad PYME, facturación, impacto en el equipo)
- [x] 2.8 Rediseñar la sección de contacto con la nueva estética (formulario visual; backend real queda para `corporate-compliance`) y datos de contacto
- [x] 2.9 Ajustar el IntersectionObserver de nav activo y los fade-in a realces discretos acordes a la estética seria

## 3. Productos (product-showcase)

- [x] 3.1 Sustituir los 4 servicios abstractos por los 4 productos en orden: Formación en IA para directivos → Asesor de negocio con IA → Control de gestión con IA → Propuestas comerciales con IA
- [x] 3.2 Redactar cada ficha con: qué hace · para quién · qué resultado, en tono de negocio sin jerga técnica (copy fino se afina en fase posterior)
- [x] 3.3 Encuadrar los productos como disponibles/contratables hoy (no "próximamente")

## 4. Credibilidad (credibility)

- [x] 4.1 Seleccionar y citar 2-3 estudios de terceros de prestigio (McKinsey + Banco de España/Comisión Europea), atribuidos como fuente externa
- [x] 4.2 Crear 1-2 escenarios ilustrativos claramente etiquetados como "Ejemplo:" (no clientes reales)
- [x] 4.3 Redactar los resultados esperables como objetivos de servicio, no como logros pasados
- [x] 4.4 Añadir el encuadre de fase temprana como acceso selectivo/exclusivo; sin clientes, testimonios ni métricas inventadas
- [x] 4.5 Asegurar que "Sobre nosotros" sostiene la credibilidad por experiencia del equipo, sin nombres ni credenciales falsas

## 5. Metadatos y verificación final

- [x] 5.1 Actualizar `<title>`, `meta description` y Open Graph al nuevo posicionamiento
- [x] 5.2 Verificar en vista previa: estética, contraste, responsive (900px/600px) y que no quedan restos del diseño técnico anterior
- [x] 5.3 Revisar que credibilidad y "sobre nosotros" no contienen clientes, testimonios, métricas ni credenciales fabricadas
- [x] 5.4 Validar el cambio (`openspec validate relaunch-ai-for-business`) y dejarlo listo para archivar
