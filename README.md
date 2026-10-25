# Actividad 2. Requisitos y decisión estructural

## Proyecto

**Nombre:** Plataforma de Gestión Logística de Última Milla

**Caso:** Sistema de Gestión Logística para Retail Digital.

## 1. Problema del negocio

La empresa de retail digital recibe pedidos desde diferentes canales y administra inventarios distribuidos en distintos puntos. Actualmente, la información relacionada con pedidos, inventarios, rutas, repartidores e incidencias no se encuentra completamente centralizada.

Esta situación puede generar duplicación de información, errores en la gestión de inventarios, retrasos en las entregas, dificultades para coordinar las rutas y poca trazabilidad durante el proceso logístico.

## 2. Objetivo de la actividad

Transformar las necesidades del negocio en requisitos funcionales y atributos de calidad, priorizar los requisitos, establecer escenarios verificables, comparar alternativas estructurales y justificar una decisión arquitectónica inicial.

## 3. Requisitos prioritarios

Los requisitos funcionales prioritarios de la plataforma son:

1. Registrar los pedidos recibidos desde los diferentes canales de venta.
2. Consultar los pedidos y conocer su estado.
3. Validar la disponibilidad de los productos en el inventario.
4. Gestionar la preparación de los pedidos en los almacenes.
5. Asignar rutas y repartidores para realizar las entregas.
6. Actualizar el estado de las entregas.
7. Registrar y consultar las incidencias relacionadas con los pedidos.
8. Controlar el acceso a la información según el rol de cada usuario.

También se consideran prioritarios los siguientes atributos de calidad:

- **Rendimiento:** permitir consultar la información de los pedidos en un tiempo adecuado.
- **Seguridad:** proteger la información y controlar los permisos de acceso.
- **Disponibilidad:** permitir el acceso al sistema durante los periodos de operación acordados.
- **Consistencia:** mantener coherentes los datos de pedidos e inventarios.
- **Mantenibilidad:** organizar las responsabilidades para facilitar los cambios.
- **Trazabilidad:** conservar información sobre los cambios de estado de los pedidos.

## 4. Decisión arquitectónica inicial

Se propone utilizar un **monolito modular con límites claros por dominio**. Esta estructura permitirá organizar las responsabilidades de pedidos, inventario, entregas y rutas, incidencias y usuarios dentro de una misma aplicación.

## 5. Justificación de la decisión

Se elige esta alternativa porque el problema principal del negocio es la falta de centralización de la información logística.

Un monolito modular permite comenzar con una estructura organizada, separar las responsabilidades y reducir la complejidad operativa inicial.

También se considera una arquitectura distribuida por dominios y servicios. Sin embargo, esta alternativa puede aumentar los costos, la infraestructura necesaria y la complejidad de operación. Por esta razón, se evaluará nuevamente si el crecimiento del negocio demuestra que es necesario separar y desplegar determinados módulos de manera independiente.

## 6. Alcance de la actividad

Esta actividad comprende:

- Elaboración del catálogo de requisitos.
- Priorización de los requisitos funcionales y no funcionales.
- Definición de escenarios de calidad con medidas verificables.
- Comparación de al menos dos alternativas estructurales.
- Justificación de la decisión arquitectónica.
- Elaboración del registro de decisión arquitectónica (ADR).
- Organización de los documentos en un repositorio de GitHub.
- Preparación de la sustentación en video.

Esta actividad no incluye la implementación completa de la plataforma ni la selección definitiva de lenguajes de programación, frameworks, bases de datos o proveedores de infraestructura.

## 7. Documentación de la actividad

Los documentos de análisis se organizarán en la carpeta `docs/actividad-2` del repositorio.

Allí se incluirán el catálogo de requisitos, la matriz de priorización, los escenarios de calidad, la comparación de alternativas, el registro de decisión arquitectónica y los criterios de verificación.

## 8. Criterios para verificar la decisión

La decisión arquitectónica se revisará considerando los siguientes criterios:

1. Los requisitos prioritarios están identificados y documentados.
2. La matriz explica la importancia de los requisitos para el negocio y su impacto arquitectónico.
3. Los escenarios de calidad contienen condiciones, respuestas esperadas y medidas verificables.
4. Se comparan al menos dos alternativas estructurales.
5. La decisión está justificada de acuerdo con las necesidades del negocio.
6. El registro ADR incluye las alternativas consideradas, los beneficios, los riesgos y las desventajas aceptadas.
7. Los documentos están organizados en GitHub y cuentan con historial de commits.
8. La sustentación explica los requisitos priorizados, las alternativas y la decisión tomada.

Las métricas propuestas deberán validarse con las necesidades del negocio y con pruebas cuando exista una implementación.

## 9. Conclusión

La decisión arquitectónica inicial busca responder al problema de dispersión de información de la empresa mediante una estructura modular y organizada.

La comparación de alternativas permite justificar la elección con base en la complejidad, el costo, la evolución y los riesgos operativos. La arquitectura propuesta podrá revisarse cuando se disponga de información real sobre el volumen de pedidos, el rendimiento y las necesidades de crecimiento de la plataforma.