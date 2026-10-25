# Comparación de alternativas estructurales

## 1. Introducción

Este documento compara dos alternativas estructurales para la Plataforma de Gestión Logística de Última Milla, considerando las necesidades del negocio, los requisitos priorizados y los riesgos identificados en la Actividad 1.

Las alternativas evaluadas son:

- Alternativa A: monolito modular con límites claros.
- Alternativa B: arquitectura distribuida por dominios y servicios.

## 2. Comparación de alternativas

| Criterio | Alternativa A: Monolito modular | Alternativa B: Arquitectura distribuida por servicios |
|---|---|---|
| Complejidad | Menor complejidad operativa inicial. | Mayor complejidad por la comunicación y coordinación entre servicios. |
| Costo | Generalmente requiere menos infraestructura operativa al inicio. | Puede requerir más infraestructura, monitoreo y recursos de operación. |
| Rapidez de implementación | Permite construir una primera versión integrada. | Puede requerir más tiempo para configurar y coordinar los servicios. |
| Facilidad de evolución | Facilita los cambios si se mantienen límites claros entre módulos. | Permite evolucionar servicios por separado, pero requiere gestionar sus contratos e integraciones. |
| Riesgo operativo | Un fallo general de la aplicación puede afectar varios módulos. | Puede aislar algunos fallos, pero añade riesgos de comunicación y consistencia distribuida. |
| Integración | Permite integrar sistemas externos mediante interfaces definidas. | Permite separar integraciones, pero aumenta los puntos de comunicación. |
| Escalabilidad | La aplicación se escala inicialmente como una unidad. | Permite escalar servicios de manera independiente. |
| Alineación con el negocio | Adecuada para comenzar centralizando la información logística. | Puede ser adecuada si el crecimiento y las necesidades operativas justifican la separación de servicios. |

## 3. Alternativa A: Monolito modular con límites claros

### Ventajas

- Reduce la complejidad operativa inicial.
- Permite organizar las responsabilidades en módulos.
- Facilita construir una primera versión integrada.
- Ayuda a centralizar la información de pedidos, inventario, entregas e incidencias.

### Desventajas

- Los módulos pueden quedar acoplados si no se respetan sus límites.
- La aplicación se despliega inicialmente como una unidad.
- El crecimiento futuro puede exigir optimizaciones o una reorganización de la estructura.

## 4. Alternativa B: Arquitectura distribuida por dominios y servicios

### Ventajas

- Permite separar los servicios por dominio.
- Facilita el despliegue y escalado independiente de los servicios.
- Puede facilitar la evolución autónoma de diferentes partes del sistema.

### Desventajas

- Aumenta la complejidad operativa.
- Requiere gestionar la comunicación entre servicios.
- Puede necesitar más infraestructura y coordinación técnica.
- Puede resultar excesiva si el negocio todavía no necesita esa separación.

## 5. Alternativa seleccionada

Se selecciona inicialmente el monolito modular con límites claros por dominio.

Esta alternativa permite abordar el problema principal de la empresa, que es la falta de centralización y trazabilidad de la información, sin introducir desde el comienzo la complejidad de una arquitectura distribuida.

## 6. Justificación de la decisión

La decisión se fundamenta en la necesidad de centralizar los pedidos, validar el inventario, coordinar las entregas y gestionar las incidencias.

La estructura modular permite separar las responsabilidades y mantener una base para futuras modificaciones. La arquitectura distribuida se podrá reconsiderar si las necesidades de crecimiento, rendimiento o despliegue independiente lo justifican.

## 7. Trade-offs: beneficios y desventajas aceptadas

- Se acepta desplegar inicialmente la aplicación como una unidad para reducir la complejidad operativa.
- Se requiere mantener límites claros entre los módulos para evitar el acoplamiento.
- Se acepta que no habrá escalado independiente por dominio en la primera etapa.
- Se considera la posibilidad de optimizar o separar módulos en el futuro si existen evidencias que lo justifiquen.

## 8. Conclusión

La comparación muestra que ambas alternativas tienen beneficios y desventajas. Con la información disponible, el monolito modular es la opción inicial más coherente con las necesidades del negocio, ya que permite centralizar los procesos y mantener una estructura organizada con menor complejidad operativa.

La decisión deberá revisarse si las condiciones reales de operación demuestran que se necesita una arquitectura distribuida.