# Criterios de verificación de la decisión arquitectónica

## 1. Objetivo

Definir criterios que permitan comprobar si la estructura arquitectónica propuesta responde a las necesidades de la Plataforma de Gestión Logística de Última Milla.

## 2. Criterios verificables

| ID | Criterio | Evidencia para verificarlo |
|---|---|---|
| CV-01 | Los requisitos funcionales están identificados y tienen un código único. | Catálogo de requisitos. |
| CV-02 | Los requisitos tienen prioridad e impacto en el negocio y en la arquitectura. | Matriz de priorización. |
| CV-03 | Los escenarios de calidad describen condiciones, respuestas esperadas y medidas verificables. | Documento de escenarios de calidad. |
| CV-04 | Se comparan al menos dos alternativas estructurales utilizando criterios comunes. | Comparación de alternativas. |
| CV-05 | La decisión arquitectónica está relacionada con el problema identificado en la Actividad 1. | Registro ADR-001. |
| CV-06 | La decisión incluye ventajas, desventajas, riesgos y trade-offs. | Registro ADR-001. |
| CV-07 | Los módulos propuestos tienen responsabilidades diferenciadas. | Registro ADR-001 y diseño posterior. |
| CV-08 | Se identifican las condiciones que justificarían revisar la decisión. | Criterios de revisión del ADR-001. |
| CV-09 | Los documentos están organizados en el repositorio de GitHub y tienen historial de cambios. | Repositorio y registro de commits. |
| CV-10 | La sustentación explica los requisitos prioritarios, las alternativas comparadas y la decisión tomada. | Enlace al video publicado. |
| CV-11 | Todos los requisitos funcionales del catálogo aparecen en la matriz de priorización. | Catálogo de requisitos y matriz de priorización. |
| CV-12 | Los documentos mantienen coherencia entre los requisitos, la comparación y la decisión arquitectónica. | Revisión conjunta de los documentos de la actividad. |

## 3. Validación de los escenarios de calidad

Cuando exista una implementación, se deberán realizar pruebas para verificar los objetivos de rendimiento, seguridad, disponibilidad, consistencia y trazabilidad.

Los resultados obtenidos deberán compararse con las medidas definidas en el documento de escenarios de calidad.

Las métricas propuestas son objetivos iniciales de análisis y no resultados de pruebas ya realizadas.

## 4. Revisión de la decisión arquitectónica

La decisión deberá revisarse si las mediciones muestran problemas de rendimiento, crecimiento de la operación, necesidad de escalar módulos de forma independiente o dificultades operativas que justifiquen otra estructura.

## 5. Conclusión

Estos criterios permiten comprobar que los entregables de la actividad están documentados y establecer cómo se evaluará posteriormente la decisión arquitectónica. La verificación técnica definitiva requerirá pruebas sobre una implementación del sistema.