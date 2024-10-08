# Actividad 03: Requerimientos del Sistema

Para esta actividad es necesario que se identifiquen los requerimientos del sistema **por módulo**. Cada alumno debe especificar lo correspondiente al módulo elegido considerando las 3 categorías de requerimientos vistas en clase: Requerimientos funcionales, requerimientos de atributos de calidad y restricciones.

Para ilustrar la especificación de estos requerimientos se utilizará el ejemplo de una empresa fintech (CrediMype).

## Requerimientos Funcionales

Lo ideal es que el grupo utilice una aplicación como MarvelApp o Figma para realizar el diseño. Deben complementar esta especificación con la especificación de casos de uso o historias de usuario que contengan además una descripción textual detallada de las funcionalidades del sistema.

Para esta entrega, lo mínimo indispensable es que provean una descripción textual de los principales requerimientos por módulo:

### Ejemplo (Especificación Mínima)
El sistema debe permitir a los usuarios (mypes) registrar solicitudes de préstamos a través de la plataforma en línea, ingresando información relevante de manera segura y eficiente. Este módulo debe integrar la verificación automática de la información proporcionada por el usuario, calcular las condiciones del préstamo (tasas de interés, plazos, montos máximos) y enviar la solicitud al módulo de Evaluación de Riesgo para su procesamiento.

## Requerimientos de Atributos de Calidad
Utilice el formato de escenarios para realizar la especificación. No olvide que la especificación debe ser por módulo y considerar varios escenarios por cada atributo de calidad.

| **Atributo de Calidad** | **Estímulo**                          | **Fuente del Estímulo**         | **Artefacto**                       | **Entorno**                      | **Respuesta**                                     | **Medida de Respuesta**                            |
|-------------------------|---------------------------------------|---------------------------------|-------------------------------------|-----------------------------------|--------------------------------------------------|---------------------------------------------------|
| **Disponibilidad**       | Fallo en el servidor de base de datos | Servidor de la nube             | Módulo de Procesamiento de Pagos    | Operación en horario laboral      | El sistema pasa automáticamente a un servidor de respaldo | El sistema está disponible el 99.9% del tiempo al año |
| **Disponibilidad**       | Actualización del sistema             | Equipo de desarrollo            | Servicio de Notificaciones          | Fuera del horario laboral         | El sistema entra en modo de mantenimiento programado | El tiempo de inactividad es menor de 15 minutos |
| **Rendimiento**          | Solicitud de préstamo simultánea de 500 usuarios | Clientes (mypes)           | Módulo de Solicitud de Préstamos    | Alta demanda durante días festivos | El sistema debe procesar las solicitudes sin retraso significativo | El tiempo de respuesta no supera los 2 segundos |
| **Rendimiento**          | Consulta masiva de datos históricos   | Administradores del sistema     | Servicio de Búsqueda de Transacciones   | Operación normal                  | El sistema debe devolver los resultados en un tiempo razonable | El tiempo de respuesta no excede los 5 segundos para un millón de registros |


## Restricciones
En este caso la especificación puede darse por el sistema en su totalidad o para un módulo específico. Por ejemplo, es posible que el grupo tenga una restricción a nivel de motor de BD pero solamente 

### Ejemplo
- El módulo de Evaluación de Riesgo deberá hacer uso del lenguaje Python, que es el que domina el equipo de Data, que será el encargado del desarrollo de los modelos necesarios.
- Todo el sistema deberá ser construido utilizando Typescript y Postgresql, que es el estándar corporativo utilizado.