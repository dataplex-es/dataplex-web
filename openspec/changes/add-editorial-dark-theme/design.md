## Context

Segunda iteración estética sobre el sitio relanzado (single-file `index.html`, estático, GitHub Pages). El usuario lo ve demasiado plano; quiere el ritmo claro/oscuro de Harvey.ai, una foto editorial en el hero y una declaración de posicionamiento potente. Además hay un bug en vivo: la regla CSS `nav { position:fixed }` aplica al `<nav>` del footer y clava sus enlaces (email, LinkedIn) en la cabecera. Posicionamiento, audiencia y restricciones en la memoria de proyecto y en las specs base.

## Goals / Non-Goals

**Goals:**
- Introducir ritmo claro/oscuro: hero, credibilidad y contacto+footer en oscuro; resto en claro.
- Hero con foto editorial a sangre completa, tratada + velo oscuro, texto blanco legible (AA), con lockup de logo.
- Nueva sección de declaración de posicionamiento tras el hero.
- Quitar LinkedIn de todo el sitio (email se mantiene).
- Corregir el bug del nav fijo.

**Non-Goals:**
- Formulario funcional, legal, cookies, SEO → cambio `corporate-compliance`.
- Cambiar el tagline, los 4 productos o la estructura de contenido (más allá de insertar la declaración).
- Múltiples fotos: solo una, en el hero. Las demás secciones oscuras van en oscuro sólido.
- Introducir build tools o dependencias.

## Decisions

- **Tokens duales sin framework.** Mantener tokens claros como base y definir un conjunto de estilos para "secciones oscuras" (clase modificadora por sección, p. ej. `.block--dark`) que invierte fondo/texto/bordes. Alternativa descartada: variables de tema conmutadas globalmente (no aplica: el ritmo es por sección, no un dark-mode global).
- **Hero a sangre con overlay.** Foto como `background-image` de la sección hero, con un `linear-gradient` oscuro (navy translúcido) encima para legibilidad; texto blanco. La foto se **desatura** (filtro o elección de imagen sobria). Alternativa descartada: hero dividido (el usuario eligió a sangre completa).
- **Foto descargada al repo en `/assets`.** Licencia libre (Unsplash/Pexels, uso comercial, sin atribución obligatoria). Se descarga al repo para no depender de un enlace externo (fiabilidad, velocidad, sin tracking). Alternativa descartada: hotlink externo.
- **Selección de foto con aprobación.** Como no se pueden ver miniaturas a ciegas, en implementación se curan 2-3 candidatas concretas, se montan en el hero y se eligen con vista previa antes de fijar. Es una decisión abierta (ver Open Questions).
- **Fix del nav.** Acotar el posicionamiento fijo a la cabecera (`nav#nav` / `#nav`) en lugar del selector de elemento `nav`, para que el `<nav>` del footer no quede fijo. Alternativa: cambiar el `<nav>` del footer por otro elemento; se prefiere acotar el selector por ser el origen del bug.
- **Lockup en hero.** Reutilizar el SVG de puntos (variante que se solapa) + wordmark "Dataplex", en versión clara sobre el hero oscuro.
- **Declaración de posicionamiento** como sección propia (clara, tipografía grande) tras el hero, replicando la "sección 2" de Harvey. El mensaje de apoyo del hero se acorta para no duplicarla.

## Risks / Trade-offs

- [Foto a sangre → riesgo de legibilidad del texto] → Velo oscuro generoso + elegir imagen con zona tranquila; verificar contraste AA en preview en desktop y móvil.
- [Foto de stock genérica abarata la marca] → Imagen editorial sobria, desaturada; descartar clichés; curar candidatas y aprobar visualmente.
- [Inversión a oscuro rompe contrastes en componentes claros heredados (tarjetas, bordes, inputs)] → Definir explícitamente los estilos de los componentes dentro de secciones oscuras; revisar cada sección oscura en preview.
- [El peso de la imagen penaliza la carga] → Comprimir/redimensionar la foto a un tamaño razonable para web.

## Migration Plan

- Rama dedicada; implementar por secciones con vista previa local.
- Curar y aprobar la foto antes de fijarla.
- Verificar contraste AA en secciones claras y oscuras, desktop y móvil; confirmar que el footer ya no se solapa arriba.
- Despliegue por push a `main` → GitHub Pages. Rollback = revertir el PR.

## Open Questions

- Foto concreta del hero: se decide entre 2-3 candidatas curadas, con vista previa y aprobación del usuario.
- ¿Color exacto del oscuro corporativo? (navy muy oscuro vs. casi negro) — se afina en preview.
