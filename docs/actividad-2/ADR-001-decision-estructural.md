# ADR-001: Decisión de estructura inicial

## Estado

Propuesta.

## 1. Contexto

La Plataforma de Gestión Logística de Última Milla busca centralizar la información de pedidos, inventarios, rutas, repartidores e incidencias de una empresa de retail digital.

En la Actividad 1 se identificó que la dispersión de la información puede generar duplicaciones, inconsistencias de inventario, retrasos en las entregas y pérdida de trazabilidad.

Todavía es necesario confirmar el volumen máximo de pedidos, la cantidad de almacenes, los sistemas actuales y las necesidades definitivas de disponibilidad.

## 2. Decisión arquitectónica

Se propone utilizar inicialmente un monolito modular con límites claros por dominio.

Los módulos principales serán:

- Pedidos.
- Inventario.
- Entregas y rutas.
- Incidencias.
- Usuarios y permisos.

Cada módulo tendrá responsabilidades definidas para facilitar el mantenimiento y reducir las dependencias innecesarias entre las diferentes partes del sistema.

Esta decisión no selecciona todavía lenguajes de programación, frameworks, bases de datos ni proveedores de infraestructura.

## 3. Alternativas consideradas

### Alternativa A: Monolito modular

Ventajas:

- Reduce la complejidad operativa inicial.
- Permite organizar las responsabilidades por módulos.
- Facilita centralizar la información logística.
- Permite construir una primera versión integrada.

Desventajas:

- Los módulos pueden quedar acoplados si no se definen límites claros.
- La aplicación se despliega inicialmente como una unidad.
- El crecimiento futuro puede requerir optimizaciones o cambios estructurales.

### Alternativa B: Arquitectura distribuida por dominios y servicios

Ventajas:

- Permite desplegar servicios de manera independiente.
- Facilita escalar determinados servicios por separado.
- Puede favorecer la evolución autónoma de los dominios.

Desventajas:

- Aumenta la complejidad operativa.
- Requiere gestionar la comunicación y la consistencia entre servicios.
- Puede necesitar más infraestructura y coordinación técnica.

## 4. Justificación

Se selecciona inicialmente el monolito modular porque el problema principal identificado es la falta de centralización y trazabilidad de la información.

Esta alternativa permite organizar los procesos de pedidos, inventario, entregas e incidencias sin introducir desde el comienzo la complejidad adicional de una arquitectura distribuida.

La decisión se ajusta a la información disponible y podrá revisarse cuando existan datos reales sobre el crecimiento, el rendimiento y las necesidades operativas.

### 4.1 Resultado de la evaluación

La comparación de alternativas obtuvo los siguientes resultados mediante una evaluación ponderada de criterios:

- Monolito modular: 4,35 sobre 5.
- Arquitectura distribuida: 2,85 sobre 5.

Estos resultados respaldan la selección del monolito modular, teniendo en cuenta que el costo, la complejidad operativa y la rapidez de implementación tienen mayor importancia en la etapa inicial del proyecto.

La evaluación corresponde a una valoración arquitectónica preliminar y no a mediciones realizadas sobre un sistema implementado.

## 5. Consecuencias y trade-offs

- Se prioriza la simplicidad operativa inicial.
- Se acepta que la aplicación se despliegue como una unidad.
- Se requiere mantener límites claros entre los módulos.
- No se dispone inicialmente de escalado independiente por dominio.
- Podría ser necesario optimizar o separar módulos si las necesidades futuras lo justifican.

## 6. Riesgos y medidas de mitigación

| Riesgo | Medida de mitigación |
|---|---|
| Acoplamiento entre módulos | Definir responsabilidades y límites claros. |
| Aumento del volumen de pedidos | Medir el rendimiento y evaluar optimizaciones. |
| Inconsistencias de inventario | Definir reglas de actualización y comprobarlas mediante pruebas. |
| Accesos no autorizados | Establecer permisos por rol y verificar su funcionamiento. |

## 7. Criterios para revisar la decisión

La decisión deberá revisarse si:

1. El rendimiento no cumple los objetivos acordados después de realizar optimizaciones.
2. Un dominio necesita escalar de manera independiente.
3. Los fallos de un módulo afectan repetidamente a otros.
4. Se requiere desplegar diferentes dominios de forma independiente.
5. El crecimiento de la operación justifica la complejidad adicional de una arquitectura distribuida.
6. Se identifican necesidades de integración o crecimiento que no puedan atenderse adecuadamente mediante la estructura modular actual.

Cualquier cambio hacia una arquitectura distribuida deberá justificarse mediante mediciones, necesidades operativas y una nueva decisión arquitectónica documentada.
## 8. Conclusión

El monolito modular con límites claros se propone como estructura inicial para la Plataforma de Gestión Logística de Última Milla. La decisión busca responder a las necesidades actuales del negocio y reducir los riesgos de complejidad prematura.

La arquitectura podrá evolucionar si las mediciones y las necesidades reales del negocio justifican una estructura diferente.