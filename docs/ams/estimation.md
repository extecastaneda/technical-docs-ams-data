Una de las tareas más **complejas**, pero de vital importancia, en la gestión de todo proyecto de desarrollo de 
software es la estimación de esfuerzo y costo, **es causa frecuente de errores** {==y puede significar el éxito 
o el fracaso de los proyectos o mejoras continuas.==} Este proceso involucra varios componentes y genera normalmente
más de un artefacto.

![Placeholder](http://www.plantuml.com/plantuml/svg/SoWkIImgAKygvj9IS2t8JERIqb9mIqqiAIrALJ04ShHi54ABKuiKF3ABI_ABAY5YMWeXYSNPA6mZ9BOnY8sgpGX56x8bHfHOOeFF5Wn76ECn5kuUB8udpZbS3gbvAS201000){ loading=lazy }


[:material-link: Product Backlog Items (PBI)](https://jiracorp.belcorp.biz/browse/ISD-150746?jql=project%20%3D%20ISD%20AND%20issuetype%20%3D%20%22Mejora%20Continua%22%20AND%20status%20in%20(Cerrado%2C%20Cancelado%2C%20%22En%20planeaci%C3%B3n%22%2C%20Reabierto%2C%20%22En%20Revision%22%2C%20%22En%20Pruebas%20de%20Usuario%22%2C%20%22En%20Aprobaci%C3%B3n.%22%2C%20%22Validar%20Beneficio%22%2C%20Solicitante%2C%20Validado%2C%20%22Validaci%C3%B3n%2FEstimaci%C3%B3n%22%2C%20%22En%20Revisi%C3%B3n%20Estimaci%C3%B3n%22%2C%20%22En%20Fabrica%22)%20AND%20%22L%C3%ADder%20T%C3%A9cnico%20Inetum%22%20in%20(currentUser())%20AND%20cf%5B12710%5D%20!%3D%20%22Producto%20Testing%22%20AND%20status%20%3D%20%22Validaci%C3%B3n%2FEstimaci%C3%B3n%22%20ORDER%20BY%20updated%20DESC) 

## Historia de Usuario (HU)
Una historia de usuario es una **representación de un requisito escrito** en una o dos frases 
utilizando el lenguaje común del usuario. Las historias de usuario son transversales a **cualquier frameworks ágil** 
(scrum, extreme programming (XP) o incluso kanban). Características:

* Las HU serán siempre en lenguaje común
* Las HU deberán ser independientes entre ellas
* Una HU no tiene en cuenta el estado actual o futuro del producto
* Expresa una necesidad del usuario durante el uso del producto
* Se pueden agrupar en Épicas

!!! example "Sintaxis" 
    Como **[ROL]**  quiero **[ALGO]** para poder **[BENEFICIO]**.

A continuación mostramos ejemplos válidos:

- **COMO** Analista de BI Planeamiento **QUIERO** la data de MTO en el Universo Real Estimado Producto **PARA**
  que todos los usuarios de planeamiento cuenten con la data necesaria.

- **COMO** Analista Comercial **QUIERO** poder encontrar las variables 
  del programa de socias asociadas a la nueva tabla de ganancia **PARA** armar las estrategias 
  correspondientes en todos los países de la corporación.

Una frase no es suficiente para describir una funcionalidad! Cierto, pero las historias de usuario 
{++no son solo una frase!.++}

{==Las historias de usuario nos deben generar conversaciones profundas acerca de la funcionalidad.==} 
La conversación **nos llevará a unos criterios de aceptación**, en los que el equipo se alineará para acordar 
en qué consiste aquella funcionalidad y **como se realizará.**

### Conversaciones 
Tienen como objetivo principal {++la consecución (logro) de acuerdos sobre los distintos 
puntos hablados.++} Estos acuerdos, que **quedarán reflejados en los criterios de aceptación**, nos permitirán validar 
que una historia de usuario está **terminada.**

**Cuantos más puntos de vista participen mayor será el entendimiento de la necesidad.** A mayor entendimiento mayor 
facilidad en acordar qué significa realmente una historia de usuario. Las historias de usuario son una herramienta 
para **mejorar la comunicación** entre las personas involucradas. 
{==Si no generas conversaciones sobre las historias de usuario tienes un grave problema.==}

!!! quote
    Ante una historia de usuario **levántate**, junta a los **involucrados**, empieza una conversación 
    y **genera acuerdos.**

### Criterios de Calidad
Dentro de la elaboración de una historia de usuario {==se deben tener en cuenta una serie de
criterios que permitan evaluar la calidad de ésta==}; para ello, se debe tener en cuenta el método **INVEST**, 
descrito por Bill Wake que consiste en cumplir las siguientes características:

* **I - Independent (Independiente):** Cada HU debe poder ser planificada e implementada en
cualquier orden, {++no debe depender una de otra, si esto ocurre, se deben dividir o combinar.++}
* **N - Negotiable (Negociable):** Las HU deben ser negociables, ya que sus detalles serán acordados por el
usuario y el equipo durante la fase de conversación.  
* **V – Valuable (Valiosa):** Una HU tiene que ser importante para el usuario, por esto es conveniente
que ellos las describan y definan el valor objetivo para el negocio.
* **E – Estimable (Estimable):** Una buena HU {++debe poder ser estimada por el equipo de desarrollo++}
con la **precisión** suficiente para ayudar al usuario a priorizar y planificar su implementación.
* **S – Small (Pequeña):** Las historias {==deben poder construirse en poco tiempo==}, generalmente alrededor de 2 o 3
semanas. Una descripción corta ayuda a disminuir el tamaño de una historia de usuario facilitando así su
estimación.
* **T – Testable (Comprobable):** La HU debe **poderse probar** tanto por el usuario como por el equipo
de desarrollo; de tal forma, que sea posible **verificar** que el producto implementado funciona acorde a lo solicitado
en la HU (finalizada).  

## Criterios de Aceptación
El resultado que debes obtener de la conversación son {==unos criterios de aceptación claros y específicos 
que todo el equipo comprenda exactamente de la misma forma.==}

De algún modo podemos afirmar que lo que hacemos es detallar la historia de usuario para:

- Entender mejor el trabajo a realizar
- Definir aquellos puntos indispensables
- Los eventos del sistema o las interacciones del usuario

!!! resume
    los criterios de aceptación facilitan la identificación de que una historia de usuario está realmente terminada.

!!! example "Sintaxis" 
    Escenario **[número]** - **[Título del escenario (opcional)]**: **[DADO]**, **[CUANDO]**, **[ENTONCES]**.

Los estándares marcan que los criterios de validación también tienen su sintaxis definida.

- **DADO:** Estado del software antes de la ejecución de la historia del usuario, situación inicial. Puede 
  ser el camino feliz o un camino de excepción o una regla de negocio
- **CUANDO:** Un evento que desencadena un proceso
- **ENTONCES:** Estado del software después de la ejecución (puede ser uno deseado y válido o uno inesperado 
  y no permitido), situación final. Es lo que se verifica y que permite establecer si la prueba pasó o falló

Ejemplos:

- **DADO** un usuario sin iniciarse sesión en la página de inicio, 
  **CUANDO** haga clic en el botón «Conectar» **ENTONCES** navega a la página de inicio del sitio

- **DADO** un analista comercial, 
  **CUANDO** ingrese a la pantalla de variables en tableau y se ubique en la variable
  ‘Pedidos de Alto valor 2’ **ENTONCES** verá el nuevo nombre ‘Pedidos de Alto Valor Plus (programa)’

{==Un error frecuente cuando empiezas a trabajar con historias de usuario es construir 
historias demasiado largas.==} La conversación y consecución de los criterios de validación 
nos ayudarán a detectar los casos en los que necesitamos **dividir una historia de usuario.**

En general, los criterios de aceptación deben cumplir las características siguientes:

* **Atomicidad:** Deben tener 2 resultados únicos: ÉXITO o ERROR no hay “éxito parcial”.
* **No Ambiguos:** Deben ser interpretados de única manera por N personas.
* **Verificables:** Deben estar escritos de forma que el usuario los pueda verificar rápidamente.
* **Completos:** El grupo de criterios de aceptación debe incluir todos los requerimientos funcionales.

!!! tip 
    Los criterios de aceptación nos evitan la aparición de discrepancias futuras sobre la necesidad 
    descrita en la historia de usuario.

## Ejemplos
**ISD-150746:** Incorporación de variables de Demanda en Universo Profit Real Estimado Negocio

    
    Código:         ISD-150746
    Informador:     Marcela Rodriguez Mantilla (Planning & Merchandising Analyst)
    Area:           ?
    Resumen:        Incorporación de variables de Demanda en 
                    Universo Profit Real Estimado Negocio
    -------------------------------------------------------------------------
    Dependencias:   No sé exactamente de qué equipos dependen, pero Leonardo Palomino 
                    ve el tema de la demanda y ya se le informó que se está 
                    realizando este jira.  
    -------------------------------------------------------------------------
    HU:             Buenos días,
                    Nos gustaría que se habilitaran las variables de Demanda en el universo 
                    Profit Real Estimado Negocio (Variables adjuntadas en el excel). 
                    Estas variables se encuentran en el universo Real Estimado Producto. 
                    Sin embargo, se necesita en el universo mencionado hasta nivel 
                    de negocio para poder hacer las comparaciones vs objetivos como 
                    Profit Must Have y M04, etc.

                    La demanda es un proyecto que aún se está afinado. Si bien en el Profit 
                    Real Estimado Negocio existe una demanda, esa no es la correcta con 
                    la cual se está trabajando el proyecto de SAP demanda vs Tableau. 
                    Por lo cual, solicitamos que se pueda incorporar.
                    Muchas gracias!
    -------------------------------------------------------------------------
    Criterios:      Tener la demanda correcta en el universo Profit Real Estimado 
                    Negocio nos va a permitir compararnos vs objetivos y no será 
                    necesario hacer el cruce con otro universo, 
                    lo cual podría hacer demoras en el dashboard.
                    El dashboard que se está construyendo son resultados para 
                    M&A para gerencia, jefaturas y analistas. Es ideal tener la demanda 
                    en el universo para ver tendencias reales, pues el faltante nos ha 
                    impactado fuertemente en los resultados y 
                    no se logra visualizar en data a nivel solo real.

**ISD-153618:** Agregaciones y eliminaciones de registros NRT Planit vs Tableau
    
    Código:         ISD-153618
    Informador:     Cesar Alonso Herrera Rose (?)
    Area:           ?
    Resumen:        Agregaciones y eliminaciones de registros 
                    NRT Planit vs Tableau
    -------------------------------------------------------------------------
    Dependencias:   NR 
    -------------------------------------------------------------------------
    HU:             Se requiere que en caso se agregue o elimine un producto u 
                    oferta en Planit, se vea el cambio en NRT en Tabelau.
                    Actualmente en NRT se visualizan variaciones en los valores de 
                    los registros, pero no se visualiza si es que se ingresan 
                    nuevos registros. Es decir, si se cambia la información de 
                    un producto u oferta existente, sí se visualiza el cambio 
                    en Tableau, pero no se visualiza si es que se agrega 
                    o elimina un producto u oferta.
    -------------------------------------------------------------------------
    Criterios:      NR

**ISD-152758:** LivingData - HANA - Recepción campos de Planit
    
    Código:         ISD-152758
    Informador:     Sebastian Alejandro Andre Villamar (Product Owner)
    Area:           ?
    Resumen:        LivingData - HANA - Recepción campos de Planit
    -------------------------------------------------------------------------
    Dependencias:   Modificación en planit ya que los campos 
                    vienen desde ahí. También en BDI 
    -------------------------------------------------------------------------
    HU:             Es necesario enviar desde Planit 2 nuevas variables ya creadas 
                    'ncampaign' y 'ciclodevida' a fin de mostrarlas tanto en Hana 
                    (Universo Real Estimado Producto) como en el 
                    Datalake (fnc_analitico.dwh_fvtaprocammes).
    -------------------------------------------------------------------------
    Criterios:      Se recibiría a través de la interfaz BIA.TácticaEstimada

## Tareas o Actividades
### Definition Of Ready (DoR)
{==Si las tareas que hay en el backlog no cumplen con los requisitos definidos en el DoR, 
no deben incluirse dentro del Sprint Backlog.==}

* La tarea debe tener una estimación de complejidad.
* {++El detalle funcional, detalle técnico y los casos de prueba de cada tarea deben ser claros 
  para que sean entendibles por cualquier miembro del equipo.++}
* La tarea no debe tener bloqueos que impidan su ejecución.
* Las dependencias deben estar resueltas.
* {++La tarea debe poder validarse y verificarse dentro del Sprint++}

### Definition Of Done (DoD) 
Es un conjunto de reglas que determinan {==cuándo un elemento está terminado.==} 
**Terminado** significa **listo para poner en producción o a disposición del usuario.**

* El trabajo de todos los miembros del equipo de desarrollo tiene que estar totalmente 
  integrado en cada iteración.
* El trabajo de cada miembro del equipo ha sido revisado por al menos otro miembro del equipo.
* {++Todo el equipo considera que para cada objetivo/requisito se cumplen sus 
  Criterios de Aceptación.++}
* El trabajo en cada iteración tiene que cumplir con los requisitos de calidad.
* {++Tiene que estar aprobado por el Team Lead.++}

## Refinamiento
El objetivo del proceso de refinamiento del product backlog es {++conseguir que los elementos estén listos para 
la planificación del sprint++}, de modo que los elementos de la cartera de productos sean:

* **Lo suficientemente claro y comprensible para todos en el equipo**
* Lo suficientemente pequeño como para ser incluido en un sprint (2 Semanas)

!!! quote 
    las ideas abstractas siempre tienden a funcionar en nuestros pensamientos, luego, cuando queremos 
    materializarlos, surgen los problemas.

Normalmente, los usuarios llega con las ideas muy claras. Sin embargo pueden darse distintas situaciones:

- El usuario tiene poco conocimiento de lo que solicita, y se le complica explicar la necesidad
- El usuario sea un experto y tenga un nivel técnico medio-avanzado y comunicará su necesidad usando un lenguaje 
  más técnico. 

{++Para todos los casos nuestro objetivo es refinar el requerimiento del usuario a 
tal punto de que la solicitud sea medible, clara, objetiva y testeable desde el primer momento y cualquier persona
dentro del equipo lo pueda desarrollar. ++}

### Participantes
- Especialista(s) de Nivel 3 (1 ó 2 personas)
- Analista Funcional (1) - Optional
- Team Lead (1) - Optional

### Planeamiento
El mecanismo adecuado es aquella que **involucre activamente a ambas partes**, para ello {==programaremos con anticipación
, de 1 o 2 dias, reuniones (según su disponibilidad de entre 40 minutos a 1 hora) con el usuario==} 
con el objetivo de:

- Detallar a mayor nivel como se realizará la solución
- Clarificar los aspectos de valor, funcionamiento y técnicos
- Resolver las dudas que aparezcan

### Plantilla Invitación al Refinamiento

    - De: responsable@inetum.world
    - Para: usuario@belcorp.biz
    - Asunto: Coordinación - Refinamiento de HU ISD-123456 1
    
    Estimado(a) [nombre_usuario] un gusto saludarte, mi nombre es [nombre_especialista] 
    Especialista del equipo Data Analytics & BI (AMS Inetum). El motivo 
    de la presente es solicitarle un espacio de 40 minutos a 1 con la finalidad de clarificar 
    los aspectos funcionales y técnicos relacionados al ticket ISD-123456 [titulo_resumen] 

    Sin otro en particular, me despido.

!!! note
    El usuario puede invitar a otros a la reunion de refinamiento, incluyendo otros desarrolladores o PO, jefes,
    supervisores, etc. Es necesario mostrar una actitud profesional y evitar frases como: 
    "me entiende?", "como te repito...", "creo que no me ha entendido", etc. 

## Cálculo del Esfuerzo
### Por Juicio Experto
Los métodos de estimación de software por juicio de experto, consisten entregar la información de 
levantamiento de requisitos de software (por ejemplo las minutas de reunión o documento de especificación de 
requisitos de software) y entregárselo a uno o varios conocedores del desarrollo de software y del área de 
negocio que se dispone representar en el nuevo sistema.

!!! note
    Una vez que el experto o grupo de expertos ha dividido el problema en actividades, pueden proceder a asignar un 
    estimado a cada una, por medio de las siguientes técnicas.

!!! tip
    Involucra a todo el mundo (desarrolladores, diseñadores, testers, deployers... todos) en el equipo es clave. 
    Cada miembro del equipo aporta una perspectiva diferente sobre el producto y el trabajo necesario para entregar una historia de usuario.

La fase de análisis y planificación consta de dos partes bien diferenciadas. 
La primera se realiza **antes de empezar el desarrollo**, es donde se intenta hacer {==la primera traducción de la 
idea que se tiene a algo más estructurado.==} Esta fase a su vez consta de pasos que van consiguiendo aportar más 
detalle a los requerimientos y, de esta forma, conseguir unas estimaciones **más aproximadas.**

## Artefactos
[:material-link: Plantilla Requerimientos](https://gfi1.sharepoint.com/sites/AMSDataAnalyticsBigData/_layouts/15/Doc.aspx?OR=teams&action=edit&sourcedoc={2CD126EB-2BE5-4B64-B80C-933088881DAE}) • 
[:material-link: Plantilla Calculadora](https://gfi1.sharepoint.com/sites/AMSDataAnalyticsBigData/_layouts/15/Doc.aspx?OR=teams&action=edit&sourcedoc={D84E3500-1BE2-4782-928B-6BA29D83CF4F})
