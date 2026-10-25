# Guion de apoyo para la sustentación

## 1. Presentación del proyecto

Mi proyecto se llama Plataforma de Gestión Logística de Última Milla y está orientado a una empresa de retail digital.

El objetivo es mejorar la gestión de los pedidos, inventarios, rutas, repartidores e incidencias mediante una solución que permita centralizar la información.

## 2. Necesidad del negocio

En el diagnóstico de la Actividad 1 identifiqué que la información logística se encuentra distribuida entre diferentes actores y procesos.

Esta situación puede generar duplicación de información, inconsistencias en el inventario, retrasos en las entregas y dificultades para conocer el estado real de los pedidos.

## 3. Requisitos priorizados

Priorizé el registro y la consulta de pedidos, la consulta de estados, la validación del inventario, la preparación de pedidos, la asignación de rutas, la actualización de entregas y la gestión de incidencias.

También consideré importantes los atributos de seguridad, rendimiento, disponibilidad, consistencia y trazabilidad.

## 4. Escenarios de calidad

Definí escenarios para establecer cómo se espera que responda el sistema y cómo se verificará su comportamiento.

Por ejemplo, se propone que las consultas de pedidos respondan en menos de dos segundos en las condiciones de prueba acordadas. También se busca controlar los accesos por roles y conservar los cambios relevantes de los pedidos.

Estos valores son objetivos iniciales que deben confirmarse y comprobarse mediante pruebas.

## 5. Comparación de alternativas

Comparé dos alternativas estructurales: el monolito modular con límites claros y la arquitectura distribuida por dominios y servicios.

El monolito modular reduce la complejidad operativa inicial y permite organizar las responsabilidades dentro de una aplicación. La arquitectura distribuida facilita el despliegue y el escalado independiente de los servicios, pero requiere más coordinación e infraestructura.

## 6. Decisión arquitectónica

Propuse inicialmente un monolito modular con límites claros por dominio.

Esta decisión responde a la necesidad actual de centralizar la información logística y organizar los procesos de pedidos, inventario, entregas, rutas e incidencias sin introducir una complejidad innecesaria desde el comienzo.

## 7. Riesgos y trade-offs

La decisión tiene ventajas y desventajas. Se reduce la complejidad operativa inicial, pero la aplicación se despliega como una unidad y los módulos deben mantenerse separados correctamente.

Si en el futuro las mediciones muestran que es necesario escalar o desplegar un módulo de manera independiente, se podrá revisar la decisión.

## 8. Conclusión

La arquitectura propuesta busca responder al problema del negocio con una estructura organizada y coherente con la información disponible.

Los requisitos priorizados, los escenarios de calidad y la comparación de alternativas sirven como base para justificar la decisión y evaluar su conveniencia en las siguientes etapas del proyecto.