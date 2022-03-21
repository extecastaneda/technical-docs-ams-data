# Acuerdos de nivel de servicio (SLA)
Los SLA se crean para documentar los compromisos que piensa cumplir para los clientes. Los SLA especifican 
compromisos que son niveles de servicio acordados entre el proveedor de servicios y el 
cliente. {==Los compromisos de SLA se pueden medir de forma cualitativa o cuantitativa==}. 
Los compromisos de SLA pueden estar asociados con una o varias escalabilidades, que especifican 
las acciones que son necesarias si no se cumple el compromiso.

!!! abstract
    Un SLA o ANS, Es un **contrato** escrito entre un proveedor de servicio y su cliente con objeto 
    de fijar el nivel acordado mediante indicadores y métricas asociadas para la calidad de dicho 
    servicio.

## Objetivos
Nuestra propuesta de gestión del acuerdo de nivel de servicio debería cumplir principalmente con dos objetivos:

* Ser **ágil y simple**.  
* Transmitir la información de manera **sencilla** haciéndola {++entendible por todas las personas implicadas++}.

Inetum propone un método de mejora continua que, partiendo de un compromiso inicial, busque 
reducir los tiempos de respuesta tanto a incidencias como a cambios y evolución de las 
aplicaciones. Para ello el **Responsable de Servicio de Inetum** y el **Responsable de Servicio de 
nuestro cliente** irán *analizando la información obtenida* y podrán **adaptar** los parámetros del ANS a 
{==objetivos más ambiciosos==}.

## Severidad
A continuación, se proponen unas definiciones para la severidad de las incidencias reportadas al equipo de soporte. 
La criticidad propuesta se fundamenta en el impacto en la operativa del negocio de nuestro cliente:

!!! bug "Bloquante"
    Toda aquella interrupción o disfunción en los servicios y/o procesos **que dé lugar a una completa inoperatividad 
    del sistema o de un módulo o funcionalidad principal del mismo.** También se incluyen aquellas que sin llegar a la 
    inoperatividad descrita **tengan un impacto en la producción o impidan dar adecuadamente el servicio**, cuando se 
    vean afectados un volumen elevado de los usuarios que utilizan dicha operativa.

!!! danger "Alta"
    Son aquellas disfunciones que afectan a una parte de la funcionalidad, sin que suponga la caída total del sistema 
    o un proceso crítico, pero sí deben ser resueltos en un periodo corto de tiempo pues no hay una alternativa 
    para seguir con su operativa.

!!! caution "Media"
    Toda aquella disfunción en los servicios y/o procesos del sistema que, sin entrar en la categoría de crítica o alta, no 
    suponga una interrupción de estos pues se tiene procedimientos alternativos manuales o automáticos 
    para seguir con la operativa.

!!! Success "Baja"
    Cualquier disfunción en los servicios y/o procesos del sistema, no contemplada en las anteriores definiciones.

## Compromisos de Resolución
A continuación mostramos una tabla de compromisos de resolución, el cual, indica el tiempo maximo invertido en cada 
tipo de requerimiento. 

| Tipo                          | Estado           | Bloqueadora | Alta  | Media   | Baja    |
| ----------------------------  | ---------------- | :---------: | :---: | :-----: | :-----: |
| Mejora Continua Correctiva    | `En Fabrica`     | **2h**      | 8h    | 24h     | 32h     |
| Mejora Continua               | `En Estimación`  | -           | 80h   | 80h     | 80h     |
| Mejora Continua               | `En Planeación`  | -           | 16h   | 16h     | 16h     |

!!! tip "Importante"
    **Nosotros**, como equipo {==no debemos de superar estos compromisos==} porque de hacerlo estaríamos incumpliendo parte del 
    contrato que se derivaran en penalizaciones para la empresa
