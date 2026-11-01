# Catálogo de requisitos

## 1. Introducción

Este documento identifica los requisitos funcionales y los atributos de calidad de la Plataforma de Gestión Logística de Última Milla, teniendo en cuenta las necesidades y los riesgos identificados en la Actividad 1.

## 2. Requisitos funcionales

Los requisitos funcionales describen las acciones que debe realizar el sistema para apoyar los procesos de gestión logística. Se identifican los actores responsables de utilizar cada funcionalidad.

| ID | Requisito | Descripción | Actor responsable |
|---|---|---|---|
| RF-01 | Registrar pedidos | El sistema debe permitir registrar pedidos recibidos desde los diferentes canales de venta. | Operador de comercio o tienda |
| RF-02 | Consultar pedidos | El sistema debe permitir consultar la información de los pedidos registrados. | Cliente, operador y soporte |
| RF-03 | Consultar estado | El sistema debe mostrar el estado actualizado de cada pedido a los usuarios autorizados. | Cliente y soporte |
| RF-04 | Validar inventario | El sistema debe permitir consultar la disponibilidad de los productos antes de preparar los pedidos. | Administrador de almacén |
| RF-05 | Gestionar preparación | El administrador de almacén debe poder consultar los pedidos pendientes y actualizar su estado de preparación. | Administrador de almacén |
| RF-06 | Asignar rutas | El sistema debe permitir asignar pedidos a rutas y repartidores. | Personal encargado de logística |
| RF-07 | Actualizar entregas | El repartidor debe poder actualizar el estado de las entregas y reportar novedades. | Repartidor |
| RF-08 | Gestionar incidencias | El sistema debe permitir registrar y consultar incidencias relacionadas con los pedidos. | Repartidor y soporte |
| RF-09 | Enviar notificaciones | El sistema debe facilitar el envío de notificaciones sobre cambios importantes en los pedidos. | Sistema de notificaciones |
| RF-10 | Integrar sistemas externos | El sistema debe permitir intercambiar información con servicios externos de pagos, geolocalización, notificaciones y ERP o CRM. | Sistemas externos |
| RF-11 | Consultar información logística por roles | El sistema debe permitir que los usuarios autorizados consulten la información correspondiente a sus funciones. | Cliente, operador, almacén, repartidor y soporte |

## 3. Requisitos no funcionales

Los requisitos no funcionales describen las condiciones de calidad que debe cumplir el sistema.

| ID | Atributo de calidad | Descripción |
|---|---|---|
| RNF-01 | Rendimiento | Las consultas de pedidos deben responder en un tiempo adecuado para la operación. |
| RNF-02 | Seguridad | El acceso a la información debe controlarse según los permisos de cada usuario. |
| RNF-03 | Disponibilidad | El sistema debe estar disponible durante los periodos de operación acordados con el negocio. |
| RNF-04 | Consistencia | La información de pedidos e inventarios debe mantenerse coherente después de cada actualización confirmada. |
| RNF-05 | Mantenibilidad | La estructura debe permitir realizar cambios sin afectar innecesariamente otras funcionalidades. |
| RNF-06 | Escalabilidad | La solución debe permitir evaluar ajustes cuando aumente el volumen de pedidos. |
| RNF-07 | Trazabilidad | El sistema debe permitir consultar los cambios relevantes realizados en los pedidos. |
| RNF-08 | Facilidad de evolución | Los módulos deben tener responsabilidades claras para facilitar futuras modificaciones. |

## 4. Restricciones y supuestos

- La empresa recibe pedidos desde diferentes canales de venta.
- El inventario se encuentra distribuido entre distintos puntos.
- Los procesos involucran clientes, operadores, administradores de almacén, repartidores y personal de soporte.
- La plataforma necesita intercambiar información con sistemas externos.
- El volumen máximo de pedidos y las necesidades definitivas de disponibilidad todavía deben confirmarse con el negocio.
- En esta actividad no se seleccionan tecnologías definitivas ni se implementa la plataforma completa.

## 5. Conclusión

El catálogo identifica las principales funcionalidades y condiciones de calidad que deben orientar la arquitectura de la plataforma. Estos requisitos servirán como base para la priorización, la definición de escenarios de calidad y la comparación de alternativas estructurales.