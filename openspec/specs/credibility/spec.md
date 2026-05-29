# credibility Specification

## Purpose
TBD - created by archiving change relaunch-ai-for-business. Update Purpose after archive.
## Requirements
### Requirement: Credibilidad sin fabricación
El contenido de credibilidad MUST NOT inventar clientes, testimonios, logos ni métricas de resultados que no hayan ocurrido. Cualquier dato presentado como propio de Dataplex SHALL ser veraz.

#### Scenario: Sin clientes ni resultados ficticios
- **WHEN** se revisa la sección de credibilidad
- **THEN** no aparecen nombres de clientes reales, ni testimonios atribuidos, ni cifras de resultados presentadas como logros pasados de Dataplex que no sean ciertas

### Requirement: Respaldo en estudios de terceros
La página SHALL sustentar la oportunidad de mercado y la tesis de democratización en estudios de terceros de prestigio (p. ej. McKinsey, BCG, Banco de España, INE, Comisión Europea), citados como fuente externa y atribuidos correctamente.

#### Scenario: Cita atribuida a fuente externa
- **WHEN** se presenta un dato de mercado o de impacto de la IA
- **THEN** se atribuye explícitamente a su fuente de tercero y no se presenta como dato propio de Dataplex

### Requirement: Escenarios ilustrativos etiquetados
La página MAY usar escenarios o casos de uso ilustrativos para mostrar el valor, pero SHALL etiquetarlos claramente como ejemplos genéricos (p. ej. "Ejemplo:") y MUST NOT presentarlos como clientes reales.

#### Scenario: Ejemplo claramente marcado
- **WHEN** se muestra un caso de uso ilustrativo
- **THEN** queda visualmente identificado como ejemplo genérico y no como un cliente o caso real concreto

### Requirement: Objetivos de servicio, no logros pasados
Cuando se comuniquen resultados esperables, SHALL formularse como objetivos o promesas de servicio (lo que Dataplex busca conseguir), no como resultados ya alcanzados.

#### Scenario: Formulación como objetivo
- **WHEN** se menciona una mejora o ahorro esperable
- **THEN** se expresa como objetivo/propósito del servicio y no como un resultado histórico verificado

### Requirement: Encuadre de fase temprana como exclusividad
La página SHALL evitar exhibir escala o volumen de clientes que no se tiene y, cuando aluda a la tracción, MUST encuadrar la fase temprana como acceso selectivo/exclusivo (p. ej. "trabajamos con un grupo selecto de primeras empresas").

#### Scenario: Exclusividad en lugar de escala fingida
- **WHEN** se alude al volumen de clientes o tracción
- **THEN** se comunica como selectividad/acompañamiento cercano, sin afirmar cifras de escala inexistentes

### Requirement: Credibilidad por experiencia del equipo
La página SHALL sustentar la confianza en la trayectoria del equipo —profesionales con experiencia en consultoría para la gran empresa al servicio de la PYME—, sin nombrar a personas concretas por ahora y sin atribuir credenciales falsas.

#### Scenario: Experiencia de equipo veraz y sin personalizar
- **WHEN** se presenta la credibilidad del equipo
- **THEN** se describe la experiencia en gran empresa puesta al servicio de la PYME, sin nombres propios y sin inventar titulaciones, premios ni clientes

