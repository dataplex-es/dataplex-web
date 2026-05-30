## 1. Bug y limpieza

- [x] 1.1 Acotar el posicionamiento fijo a la cabecera (`#nav`) para que el `<nav>` del footer no quede clavado arriba
- [x] 1.2 Quitar el enlace de LinkedIn de la sección de contacto (mantener email y ubicación)
- [x] 1.3 Quitar el enlace de LinkedIn del footer (mantener email/marca)
- [x] 1.4 Verificar que ningún enlace del footer aparece solapado en la cabecera

## 2. Ritmo claro/oscuro (brand-identity)

- [x] 2.1 Definir estilos de "sección oscura" (clase modificadora) que invierten fondo/texto/bordes manteniendo contraste AA
- [x] 2.2 Aplicar oscuro a hero, credibilidad y contacto+footer; dejar claro el resto
- [x] 2.3 Ajustar componentes dentro de secciones oscuras (tarjetas de stats, inputs del formulario, enlaces, logo) para contraste y coherencia
- [x] 2.4 Verificar contraste WCAG AA en secciones claras y oscuras

## 3. Hero con foto editorial (brand-identity)

- [x] 3.1 Curar 2-3 fotos editoriales de negocio de licencia libre (Unsplash/Pexels), montarlas en el hero y elegir con vista previa
- [x] 3.2 Descargar la foto elegida al repo en `/assets` (comprimida/redimensionada para web)
- [x] 3.3 Montar el hero a sangre completa con la foto + velo oscuro (navy) y texto blanco legible
- [x] 3.4 Añadir el lockup de marca (icono de puntos + "Dataplex") en el hero
- [x] 3.5 Verificar legibilidad del texto del hero (AA) en desktop y móvil

## 4. Declaración de posicionamiento (homepage-narrative)

- [x] 4.1 Insertar, tras el hero, la sección de declaración (clara, tipografía grande) con el texto acordado
- [x] 4.2 Acortar el mensaje de apoyo del hero para no duplicar la declaración

## 5. Verificación final

- [x] 5.1 Revisar la página completa en vista previa (desktop y móvil): ritmo claro/oscuro, foto, declaración, sin LinkedIn, sin solape del footer
- [x] 5.2 Confirmar que el peso de la imagen es razonable para web
- [x] 5.3 Validar el cambio (`openspec validate add-editorial-dark-theme`) y dejarlo listo para archivar
