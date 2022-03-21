El ciclo de vida dependerá del tipo de petición de servicio. Se trabajan 2 tipos de peticiones de servicio: 

## Requerimientos
Inician desde el lado del cliente hasta dejarlo en un estado {++Ejecución.++} 
El requerimiento ingresa al **backlog de Inetum** para iniciar su atención por parte del Team AMS (fábrica). 
La solicitud tiene los siguientes atributos: 

`Duración`
:   {==Según calculadora.==} El inicio empieza a contar desde su activación, es decir desde cuando pasa al estado {++En Progreso.++}  

`Prioridad`
:   El valor será definido por reglas internas de nuestro cliente en la fase de {++Priorización.++}

### Estados de Peticiones del Cliente (ISD)
El ciclo de vida de las peticiones de servicio sigue el siguiente diagrama de estados 
(actualmente Belcorp tiene implementado los estados de flujo de su lado): 

![Placeholder](http://www.plantuml.com/plantuml/svg/dLL1JiCm4Bpx5PPwG-e7E22L9fMGE4H1S44SjiwM6hbsjKahqM_n13w67SUkqoG5SRDdPxqxiuwpbHLotEsRJrvXBKZk6saqOwytRtm-l-EvNkp9h45ObD_o9I4Gwu6ULU9Hrfu3RSon8ZXoKeL7euv87RqobySgt3GsxSaeAMG3ka6R5NR47_J6qCvolxyqIqaZjR9OI_6L4Q0kUti19QkMdTUDt8Myi74bHYa3xSDAatd_4ZRHQ5hsqKwK_j9kxuI2f25vwigEabps4hH0PQVbxe9VqpJRDq7tg578ZJGzdM52PtCJufLEezPqEh-qC32iHB654z1VHrmeq1YI5uCBVfsVwwEqfO07r7USS7pI2jOa1Knd149NWmwuXZh3v_e0rBfRG6rSbe-m4KuxH2JgHkXMDCNpVhJ4Ra1Jp19XBP4QqrhhkYHsnWRgFb0SlAO-QU9s3HwRrAZqj8dk2aCPrdk5xq15cPqdwFn2vrUPiKlIk04jbR6w0Vj1nl1CoHrsO32tXqLT7ktWdh9PdkSHZo_AA9hSjYIUFXK9FFYqUaSE_6gZB2fpBjXV0GkguZug2iWF){ loading=lazy }

### Estados de Peticiones Inetum (DM)
A continuación, se detallan los estados del lado de Inetum: 

![Placeholder](http://www.plantuml.com/plantuml/svg/bLAxRiCm3Dpv5GIw1V0FT2ZG91sw6Hco11qOcr28AfP3AqF_lf9bsR6Jekrsl3i-fPFKZ7nk_HVMt5KghHVN01nM7rYec9ClNd1DrQTr1fzneqmAEIw2jg6cOakrYsh2SyDRKwepobrql3TI2Ibc2cxKPFRA9bKRiC94HikEwIYiFbeYLb6OkFzrp0i-N68nsjgwovMJPy1XqP7yI-FRDVPafKxL4bGOgVwkh3eC5D7o2h_8fTCjTwsDzojtss1xRTKTmpWzBMokZ8H1WgNryN3tUNc27vyDeFFaUIhsPENC0vcpPzpu2ecT7oJyo5dFFXupClCD){ loading=lazy }

`Backlog`
:   Estado en el que se mostrará en el tablero Kanban para los miembros del **Team AMS**, que está integrado 
    por los **Facilitadores y Líderes Técnicos**, quienes en coordinación {==asignan los tickets del backlog al equipo.==} 

`En progreso`
:   Indica que ha sido asignado a un desarrollador(es) y está en curso. 

`Bloqueada`
:   {==El desarrollo ha sido detenido hasta que se resuelva el impedimento.==} Solo se puede **bloquear** un desarrollo 
    en curso por alguno de los siguientes motivos: información pendiente, accesos, el ambiente no está disponible, 
    dependencia de algún desarrollo por parte del cliente. 

`Entregada`
:   **Según el tipo de petición de servicio**, {==si es Requerimiento entonces el desarrollo involucrado ha sido 
    puesto en ambiente de calidad (QAs)==} para su posterior **validación** por parte del Focal Point / Product Owner, 
    si es **Incidente** entonces {==el fix ha sido puesto en ambiente productivo==}. Alternativamente puede 
    pasar a un estado **Reabierta** ya sea por algunos de estos motivos: Se encontró un error en el desarrollo, 
    no cumple con algún criterio de aceptación, el desarrollo impactó en otra funcionalidad, entre otros. 

`Validada`
:   El desarrollo ha sido validado satisfactoriamente por el Focal Point / Product Owner y {==está puesto en 
    ambiente de producción.==} 

`Cerrada`
:   Este estado da por cerrado finalmente el ticket.

`Reabierta`
:   El desarrollo ha sido observado y requiere ser pasado a progreso. 

!!! info
    Cuando el requerimiento finaliza, aún se puede regresar a un estado anterior.
    El cambio a este estado se dará según sea: 
    
     * Si el tipo de solicitud es **Requerimiento (Mejora Continua)** entonces es realizado por el **Focal Point o Producto Owner**.
     * Si el tipo de solicitud es **Incidente** entonces es realizado por el **especialista de Soporte Nivel 2.**
     * {++Si ha transcurrido un # de días (será una configuración acordada con el cliente) desde que pasó al estado **Validada** entonces pasa a estado **Cerrada** de forma automática.++}
     * Alternativamente puede volver al estado **Entregada** en caso se identifique **alguna disconformidad con el requerimiento.**

## Incidentes 
**Es creado por un operador de Soporte Nivel 2 (SOP N2)** e ingresa al backlog de Inetum para iniciar su atención por 
parte del Team AMS (nosotros), {==con la máxima prioridad==} por tratarse de un problema que impacta a muchos usuarios en 
ambiente productivo. Es atendido por un especialista y puesto directamente en ambiente de producción con la debida 
coordinación con el SRE encargado. La solicitud tiene los siguientes atributos: 

`Clasificación`
:   Bloqueante, alta, media, baja.

`Duración`
:   La duración es estándar según atributo clasificación. **El inicio empieza a contar desde su activación**, 
    es decir desde cuando pasa al estado {++En Progreso.++}

`Prioridad`
:   {==Si es de clasificación Bloqueante o Alta entonces su prioridad es La más alta (Highest).==} Si es de clasificación 
    Media o Baja entonces su prioridad es **Alta (High).**

`Garantía`
:   {==Si NO tiene garantía entonces computa horas de fábrica AMS y aplican SLAs.==} Si tiene garantía entonces se 
    verifica si la garantía es del proveedor (y se deriva al proveedor) o es de fábrica AMS (no computa horas 
    de fábrica AMS y aplica SLAs). 
