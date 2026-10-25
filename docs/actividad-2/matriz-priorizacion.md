# Matriz de priorización de requisitos

## 1. Introducción

Esta matriz permite priorizar los requisitos de la Plataforma de Gestión Logística de Última Milla según su importancia para el negocio, su impacto arquitectónico y su complejidad inicial.

## 2. Matriz de priorización

| ID | Requisito | Prioridad | Impacto en el negocio | Impacto arquitectónico | Complejidad |
|---|---|---|---|---|---|
| RF-01 | Registrar pedidos | Alta | Evita la pérdida y duplicación de pedidos. | Define las reglas principales del módulo de pedidos. | Media |
| RF-02 | Consultar pedidos | Alta | Facilita la operación y la atención al cliente. | Requiere consultas y acceso controlado a la información. | Media |
| RF-03 | Consultar estado | Alta | Mejora el seguimiento de los pedidos. | Requiere mantener estados actualizados y coherentes. | Media |
| RF-04 | Validar inventario | Alta | Reduce pedidos incompletos y cancelaciones. | Requiere reglas de disponibilidad y consistencia. | Alta |
| RF-05 | Gestionar preparación | Alta | Facilita la coordinación de los almacenes. | Relaciona los procesos de pedidos e inventario. | Media |
| RF-06 | Asignar rutas | Alta | Ayuda a organizar las entregas. | Define responsabilidades para rutas y repartidores. | Media |
| RF-07 | Actualizar entregas | Alta | Permite conocer el resultado de cada entrega. | Requiere registrar cambios de estado. | Media |
| RF-08 | Gestionar incidencias | Alta | Facilita la atención de problemas y reclamos. | Requiere relacionar incidencias con pedidos. | Media |
| RF-09 | Enviar notificaciones | Media | Mantiene informados a los usuarios. | Requiere integración con un servicio de notificaciones. | Media |
| RF-10 | Integrar sistemas externos | Media | Facilita el intercambio de información. | Requiere definir interfaces e integración entre sistemas. | Alta |
| RNF-01 | Rendimiento | Alta | Reduce las demoras en las consultas. | Influye en las consultas y en la medición de tiempos. | Media |
| RNF-02 | Seguridad | Alta | Protege la información de la empresa y los clientes. | Requiere controlar los permisos de acceso. | Alta |
| RNF-03 | Disponibilidad | Alta | Facilita la continuidad de la operación. | Influye en la gestión de fallos y recuperación. | Media |
| RNF-04 | Consistencia | Alta | Reduce diferencias entre pedidos e inventarios. | Requiere reglas claras para actualizar información. | Alta |
| RNF-05 | Mantenibilidad | Alta | Facilita corregir errores y realizar cambios. | Requiere separar las responsabilidades de los módulos. | Media |
| RNF-06 | Escalabilidad | Media | Permite prepararse para el crecimiento. | Puede requerir optimizaciones futuras. | Alta |
| RNF-07 | Trazabilidad | Alta | Facilita investigar retrasos e incidencias. | Requiere conservar el historial de cambios. | Media |
| RNF-08 | Facilidad de evolución | Media | Facilita incorporar nuevas necesidades. | Requiere límites claros entre responsabilidades. | Media |

## 3. Criterios de priorización

- **Prioridad alta:** requisitos indispensables para resolver el problema principal de centralización, seguimiento, inventario, seguridad y coordinación logística.
- **Prioridad media:** requisitos importantes que pueden desarrollarse progresivamente según las necesidades y los recursos disponibles.
- **Complejidad baja:** requiere pocos cambios o reglas sencillas.
- **Complejidad media:** requiere coordinación entre varias funciones.
- **Complejidad alta:** implica reglas importantes de consistencia o integración entre diferentes componentes.

## 4. Justificación

Los requisitos relacionados con pedidos, inventario, entregas e incidencias tienen prioridad alta porque responden directamente a los problemas identificados en la Actividad 1.

Los atributos de seguridad, consistencia, disponibilidad y trazabilidad también son prioritarios porque afectan el funcionamiento confiable de la plataforma.

La priorización podrá ajustarse cuando se confirmen con el negocio el volumen de pedidos, las necesidades operativas y las restricciones técnicas.

## 5. Conclusión

La matriz permite identificar los requisitos que deben orientar las primeras decisiones arquitectónicas. Esta priorización servirá como base para definir los escenarios de calidad y comparar las alternativas estructurales.