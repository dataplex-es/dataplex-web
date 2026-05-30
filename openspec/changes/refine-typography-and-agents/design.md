## Context

Ronda de pulido sobre el sitio en vivo más una incorporación de contenido (agentes). Single-file `index.html`, estático. Decisiones tomadas con el usuario: wordmark en Space Grotesk; declaración sin serif; sección de agentes en oscuro entre enfoque y productos.

## Goals / Non-Goals

**Goals:**
- Wordmark en Space Grotesk (nav, hero, footer); titulares siguen en Fraunces.
- Declaración en sans-serif manteniendo tamaño y contraste de color.
- Reducir el gap icono–wordmark en el lockup.
- Añadir sección de agentes de IA (oscuro) con 3 micro-ideas.
- Pulir copy del producto 02 (redundancia) y corregir errata del 03.
- FAQ con más espacio y marcador azul.

**Non-Goals:**
- Cambiar la tipografía de los titulares de sección (Fraunces se mantiene).
- Tocar el resto de copys, la foto del hero o la estructura más allá de insertar agentes.
- Formulario funcional, legal y cookies (cambio `corporate-compliance`).

## Decisions

- **Space Grotesk solo para el wordmark.** Nueva variable `--wordmark` aplicada a `.nav-brand`, `.hero-lockup span` y `.ft-brand`. Mantener Fraunces en titulares crea un contraste intencional marca/contenido. Se añade la familia al `<link>` de Google Fonts.
- **Declaración con la sans del cuerpo** (Inter) a tamaño grande, peso medio-alto, con la segunda frase atenuada por color. Alternativa descartada: Space Grotesk (menos legible en párrafo largo).
- **Agentes en oscuro entre enfoque y productos** para sumar al ritmo claro/oscuro (enfoque claro → agentes oscuro → productos claro → credibilidad oscuro). Reutiliza estilos `.dark` y una rejilla de 3 columnas para las micro-ideas.
- **FAQ**: marcador propio (triángulo azul a la izquierda que rota al abrir) eliminando el marcador por defecto de forma robusta (`list-style:none` + `::-webkit-details-marker`), y más padding vertical por pregunta.

## Risks / Trade-offs

- [Mezclar dos familias display (Space Grotesk wordmark + Fraunces titulares) puede chocar] → Son roles distintos (marca vs. contenido); validar coherencia en preview.
- [Dos secciones oscuras cercanas (agentes y credibilidad) separadas solo por productos] → Aceptable: productos (claro) las separa y mantiene la alternancia.
- [El marcador por defecto de `<summary>` reaparece en algún navegador] → Verificar en preview que solo se ve el triángulo azul propio.

## Open Questions

- Ninguna; decisiones cerradas con el usuario (wordmark = Space Grotesk; mensaje y ubicación de agentes aprobados).
