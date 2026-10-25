# Escenarios de calidad

## 1. Introducción

Este documento define escenarios de calidad para la Plataforma de Gestión Logística de Última Milla. Los escenarios permiten establecer cómo se espera que responda el sistema ante determinadas condiciones y cómo se verificará su comportamiento.

Las medidas propuestas son objetivos iniciales de análisis que deberán confirmarse con el negocio y comprobarse mediante pruebas cuando exista una implementación.

## 2. Escenarios de calidad

| ID | Atributo | Condición o estímulo | Respuesta esperada | Medida verificable |
|---|---|---|---|---|
| EC-01 | Rendimiento | Un usuario autorizado consulta un pedido. | El sistema muestra la información principal y el estado del pedido. | La consulta responde en menos de 2 segundos en al menos el 95 % de las pruebas acordadas. |
| EC-02 | Seguridad | Un usuario intenta acceder a información que no corresponde a su rol. | El sistema rechaza el acceso y protege la información restringida. | Todas las pruebas de acceso no autorizado deben ser rechazadas. |
| EC-03 | Consistencia | Un usuario autorizado confirma una actualización del inventario. | Las consultas posteriores muestran la información actualizada. | No deben aparecer diferencias entre la actualización confirmada y la información consultada en las pruebas. |
| EC-04 | Disponibilidad | Un usuario intenta consultar un pedido durante el periodo de operación. | El sistema permite realizar la consulta, excepto durante mantenimientos acordados. | Se propone evaluar un objetivo inicial de disponibilidad mensual del 99,5 %, sujeto a confirmación del negocio. |
| EC-05 | Trazabilidad | Se modifica el estado de un pedido o se registra una incidencia. | El sistema conserva el cambio para permitir su consulta posterior. | Todos los cambios realizados durante la prueba deben aparecer en el historial con la información definida para su seguimiento. |
| EC-06 | Mantenibilidad | Se modifica una regla del módulo de incidencias. | El cambio se realiza sin alterar innecesariamente las responsabilidades de otros módulos. | La revisión del cambio debe comprobar que no se modificaron módulos ajenos sin justificación. |
| EC-07 | Escalabilidad | Aumenta el volumen de pedidos respecto a la carga inicial acordada. | Se puede medir el comportamiento y determinar si se requieren ajustes. | Se ejecuta una prueba de carga y se documentan los tiempos de respuesta, los errores y el uso de recursos. |

## 3. Criterios de validación

Para validar los escenarios se deben seguir estos pasos:

1. Confirmar con el negocio las condiciones y los objetivos de calidad.
2. Definir los datos y las condiciones de las pruebas.
3. Ejecutar las pruebas cuando exista una implementación.
4. Registrar los resultados obtenidos.
5. Comparar los resultados con las medidas propuestas.
6. Documentar los incumplimientos y las acciones de mejora.

## 4. Conclusión

Los escenarios de calidad convierten las expectativas del negocio en condiciones que pueden comprobarse. Estos criterios orientarán la evaluación de la arquitectura y permitirán identificar si la solución responde a las necesidades de rendimiento, seguridad, consistencia, disponibilidad, trazabilidad y evolución.

Las métricas aquí propuestas no representan resultados de pruebas realizadas; deberán verificarse cuando exista una implementación.