Normalmente, el usuario llega con las ideas muy claras. {++A los diez minutos se da cuenta de que no es así.++} 
Es normal, las ideas abstractas siempre tienden a funcionar en nuestros pensamientos, luego, cuando queremos 
materializarlos, surgen los problemas. A continuación presentamos una lista de actividades que apoyaran 
al especialista a desarrollar un correcto análisis de los requerimientos del usuario. 

## ¿Quién es quién?
**Antes de empezar a trabajar**, lo primero que hay que hacer es identificar **quién es quien**. Es decir, 
{++¿Quién es el cliente?, ¿Cuál es el área beneficiada?, ¿Quién es el desarrollador?++} dependiendo del 
producto en el que estamos trabajando y de lo que haya que hacer, estas preguntas pueden tener 
respuestas muy diferentes.

!!! Tip
    hay que identificar a la persona con la que vamos a tener que realizar esa comunicación y comprometerla desde
    el inicio del proyecto. **Esa persona tiene que tener el suficiente conocimiento sobre la aplicación que 
    se pretende desarrollar**

## Identificar Características
Lo primero que hay que hacer es **una lista simple** con las características a implementar. {++El lenguaje a 
utilizar debe ser llano.++} Los usuarios deben de entender esta lista ya que deben validarla. Esta lista define el 
de lo que se va a desarrollar. Es la primera transformación de la idea abstracta.

!!! Quote
    Para encontrar las respuestas, antes hay que dar con la pregunta adecuada.

### Identificar los Roles
Un rol define el conjunto de privilegios asignado a un miembro. Los privilegios se asignan a los miembros 
mediante un rol predeterminado o un rol personalizado. A los miembros se les asigna un rol cuando se les 
agrega a la organización.

### Identificar Requerimientos Funcionales
Los requerimientos funcionales de un sistema, {++son aquellos que describen cualquier actividad que este deba 
realizar,++} en otras palabras, el **comportamiento** o función particular de un sistema o software cuando se 
cumplen ciertas condiciones. {==Siempre están relacionadas con un ROL.==} Ejemplos:

* El sistema permitirá a los {++usuarios autorizados++} el ingresar planes y cronogramas de proyecto.
* El sistema permitirá aprobar, cambiar o actualizar planes y cronogramas de proyecto a los {++products owners.++}
* El sistema permitirá el envío automatizado de reportes por medio de correo a {++los planners de cada pais.++}

### Identificar Requerimientos No Funcionales
Representan características generales y restricciones de la aplicación o sistema que se esté desarrollando. Suelen
presentar dificultades en su definición dado que su conformidad o no conformidad podría ser sujeto 
de libre interpretación, por lo cual es {++recomendable acompañar su definición con criterios de aceptación 
que se puedan medir.++} Ejemplos:

* El sistema debe ser capaz de procesar N transacciones por segundo. ¿Cómo lo medimos?
* El reporte debe ser cargar en menos de 20 segundos. ¿Cómo lo medimos?
* El sistema debe proporcionar mensajes de error que sean informativos y orientados a usuario final. ¿Cómo lo verificamos?

## Crear Casos de Uso
Un caso de uso es la descripción de una acción o actividad. Toma como base los **requerimientos funcionales** y
comenzaras a **describirlos** detallando {==TODOS los posibles escenarios==}, sé meticuloso ten en cuenta que 
los escenarios o situaciones que no consideres pueden traer problemas para ti o al equipo. Recuerda, Los CU son 
una respuesta, no preguntas. Ejemplo:

!!! summary "Requerimiento Funcional"
    Cuando un Usuario Planner, agregue o elimine una oferta o producto en Planit, el cambio 
    debera de reflejarse en Tableau.

* Nombre: Actualizar Oferta o Producto (Verbo)
* Identifica los roles involucrados en esta actividad:
    - Usuario Planner
    - Usuario Tableau
* Identifica Precondiciones:
    - Comunicación Planit - Tableau Activa (NRT) 
* Secuencia:
    - Usuario ingresa a Planit
    - procede con la creación o eliminación del producto u oferta y confirma
    - El sistema toma los cambios mediante un proceso programado llamado NRT
    - NRT escribe el cambio en HANA BI en la tabla Stage STAGE_BI.MAE_CORP.XYZ
    - NRT Ejecuta el SP CROSS_20D_XYZ que envía la información a la Tabla BI_CORP.XYZ
    - Tableau se sincroniza con la tabla
    - El usuario accede al reporte y ve los cambios.
* Errores:
    - Cuando NRT no funcione:
        - Solicitar Inyección de datos manual a Planit por BDI 
        - Ejecución de interfaces manuales
* Postcondición:
    - El usuario ve los cambios reflejados en el reporte
    
## Modelo de Datos
Un modelo de datos es entonces una serie de conceptos que puede utilizarse para describir un conjunto de datos 
y las operaciones para manipularlos. Hay dos tipos de modelos de datos: 

* Los modelos conceptuales y los modelos lógicos. Los modelos conceptuales se utilizan para representar la 
  realidad a un alto nivel de abstracción.
* Los modelos lógicos, las descripciones de los datos tienen una correspondencia sencilla con 
  la estructura física de la base de datos.

![model_example](http://www.plantuml.com/plantuml/svg/POwn3eCm34JtV8N5qgcm8tK15PMb8FW0v8P0QHD0YUbIyUyD0Y6WjzdlVEVJawWtlkVr4biQb7HvfxpkyHASpcM3jKR5M8_yZRM0r9eQWYy3gza4ILK9RRQRL7VbmCailadBwevAm0KSGxffQ-U8m-5pf2CRr_ORjXZ4-_QSB2d-VmZY8aooj4YYw9hbDeJD7d3T_Stwx16mxJJHVIJu4AAKaAS_){ loading=lazy }

