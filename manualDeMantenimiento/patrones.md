
# patrones de diseño

Una vez que se identifican los requerimientos en el mantenimiento, será el momento de identificar y definir los patrones de diseño que apliquen en el desarrollo; en este sentido, es importante tener en cuenta si bien en las etapas anteriores del ciclo de vida del software se realizó un proceso detallado de análisis y definición de patrones de diseño; en las labores de mantenimiento también puede ser necesario aplicar nuevos patrones, adicionales a los que el software ya presenta.

Los patrones de diseño son de suma importancia en el software, ya que un alto porcentaje de los incidentes de mantenimiento correctivo pueden ser rastreados hacia una causa raíz que tiene que ver con un diseño ineficiente o degradado; así mismo, un software con antipatrones tiende a sufrir más fallos y a una mayor entropía, consecuentemente a ser menos mantenible en el tiempo. Los patrones de diseño varían según su complejidad, nivel de detalle y aplicabilidad. Todos los patrones pueden clasificarse según su propósito, así:

- **Los patrones creacionales:** proporcionan mecanismos de creación de objetos que incrementan la flexibilidad y la reutilización de código existente.

- **Los patrones estructurales:** explican cómo ensamblar objetos y clases en estructuras más grandes a la vez que se mantiene la flexibilidad y eficiencia de la estructura.

- **Los patrones de comportamiento:** se encargan de una comunicación efectiva y la asignación de responsabilidades entre objetos.

| Nombre del patrón        | Descripción                                                                                                   | Tipo de patrón |
|---------------------------|---------------------------------------------------------------------------------------------------------------|----------------|
| Factory method (fábrica) | Proporcionar una interfaz para crear objetos en una superclase, mientras permite a las subclases alterar el tipo de objetos que se crearán. | Creacional    |
| Abstract factory (fábrica abstracta) | Producir familias de objetos relacionados sin especificar sus clases concretas. | Creacional    |
| Builder (constructor) | Construir objetos complejos paso a paso. El patrón permite producir distintos tipos y representaciones de un objeto empleando el mismo código de construcción. | Creacional    |
| Prototype/clone (prototipo, clon) | Copiar objetos existentes sin que el código dependa de sus clases. | Creacional    |
| Singleton (única instancia) | Asegurar que una clase tenga una única instancia, a la vez que proporciona un punto de acceso global a dicha instancia. | Creacional    |
| Adapter/Wrapper (adaptador, envoltorio) | Permitir la colaboración entre objetos con interfaces incompatibles. | Estructural   |
| Bridge (puente) | Dividir una clase grande, o un grupo de clases estrechamente relacionadas, en dos jerarquías separadas (abstracción e implementación) que pueden desarrollarse independientemente la una de la otra. | Estructural   |
| Composite/ object tree (objeto compuesto, árbol de objetos) | Componer objetos en estructuras de árbol y trabajar con esas estructuras como si fueran objetos individuales. | Estructural   |
| Decorator (decorador) | Añadir funcionalidades a objetos colocando estos objetos dentro de objetos encapsuladores especiales que contienen estas funcionalidades. | Estructural   |
| Facade (fachada) | Proporcionar una interfaz simplificada a una biblioteca, un framework o cualquier otro grupo complejo de clases. | Estructural   |
| Flyweight (peso mosca, caché) | Mantener más objetos dentro de la cantidad disponible de RAM compartiendo las partes comunes del estado entre varios objetos en lugar de mantener toda la información en cada objeto. | Estructural   |
| Proxy | Proporcionar un sustituto o marcador de posición para otro objeto. Un proxy controla el acceso al objeto original, permitiéndote hacer algo antes o después de que la solicitud llegue al objeto original. | Estructural   |
| Chain of responsibility (cadena de responsabilidad) | Pasar solicitudes a lo largo de una cadena de manejadores. Al recibir una solicitud, cada manejador decide si la procesa o si la pasa al siguiente manejador de la cadena. | Comportamental |
| Command/ transaction (comando/ transacción) | Convertir una solicitud en un objeto independiente que contiene toda la información sobre la solicitud. Esta transformación permite parametrizar los métodos con diferentes solicitudes, retrasar o poner en cola la ejecución de una solicitud y soportar operaciones que no se pueden realizar. | Comportamental |
| Iterator (iterador) | Recorrer elementos de una colección sin exponer su representación subyacente (lista, pila, árbol, etc.). | Comportamental |
| Mediator/ controller (mediador, controlador) | Reducir las dependencias caóticas entre objetos. El patrón restringe las comunicaciones directas entre los objetos, forzándolos a colaborar únicamente a través de un objeto mediador. | Comportamental |
| Memento (recuerdo) | Guardar y restaurar el estado previo de un objeto sin revelar los detalles de su implementación. | Comportamental |
| Observer (observador) | Definir un mecanismo de suscripción para notificar a varios objetos sobre cualquier evento que le suceda al objeto que están observando. | Comportamental |
| State (estado) | Permitir a un objeto alterar su comportamiento cuando su estado interno cambia. Parece como si el objeto cambiara su clase. | Comportamental |
| Strategy (estrategia) | Definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables. | Comportamental |
| Template method (plantilla de métodos) | Definir el esqueleto de un algoritmo en la superclase pero permite que las subclases sobrescriban pasos del algoritmo sin cambiar su estructura. | Comportamental |
| Visitor (visitante) | Separar algoritmos de los objetos sobre los que operan. | Comportamental |

<Mark> Nota: Los patrones de diseño más básicos suelen llamarse *idioms* y suelen aplicarse únicamente a un lenguaje de programación; por otra parte, cuando un patrón aplica a un nivel más alto y se vuelve más universal, se considera un patrón de arquitectura. </Mark>

## Antipatrones de diseño

Análogamente a los patrones de diseño, existen prácticas en el desarrollo de software que deben evitarse. En general, son patrones de diseño que, en lugar de mejorar la calidad del software y ayudar a resolver algún problema, terminan teniendo el efecto opuesto. Por ejemplo:

- **Parálisis por análisis**: Este antipatrón ocurre cuando las tareas de un proyecto se retrasan por demasiada planificación, análisis o discusiones.
- **Arquitectura implícita**: Se presenta comúnmente cuando las decisiones de diseño son ejecutadas de manera implícita en lugar de explícita, lo cual puede causar entropía en el sistema.
- **Programación basada en asunciones**: De manera simplificada, este antipatrón consiste en asumir que los usuarios piensan como el programador.
- **Bola de lodo**: Se refiere a una arquitectura que no tiene un diseño modular, convirtiéndose en una especie de masa de código desorganizado sin estructura.
- **Grandes diseños primero**: Consiste en crear un diseño sumamente detallado del sistema antes de iniciar su implementación, haciendo que el desarrollo sea inflexible y difícil de adaptar al cambio.
- **Ventanas rotas**: Se refiere a problemas pequeños que no son corregidos, lo cual indica poco mantenimiento en el software y tiende a reducir la mantenibilidad y estabilidad del software.
- **Versionamiento por copias de carpetas**: Cuando en un proyecto se realizan las actualizaciones de código mediante copias de la carpeta que contiene el archivo implicado.
- **Programación tipo copiar pegar**: Cuando un bloque de código que puede ser utilizado en otro módulo del sistema, pero en lugar de modularizarse, es copiado al siguiente componente.
- **Muerte por planificación**: Este patrón surge cuando un proyecto no tiene un balance entre la planificación y la ejecución del mismo; generalmente se realizan planes a muy largos plazos en el futuro.
- **Marcha de la muerte**: Se refiere a un proyecto que tiene una posibilidad de éxito tan mínima que, en términos prácticos, no valdría la pena invertir recursos en él.
- **Programación de cinta adhesiva**: Se refiere a un estilo de programación donde los ingenieros son capaces de hacer que cualquier funcionalidad, librería o herramienta se integre y haga parte del software, pero sin prestar atención al diseño, la calidad o mantenibilidad del software.
- **Exposición de propiedades de colección**: Esta práctica se considera un antipatrón pues rompe la encapsulación y puede desembocar en un modelo de dominio anémico.
- **Rápido mejor que correcto**: Cuando se prefiere la velocidad sobre la calidad en un proyecto.
- **Creep de la funcionalidad**: Se refiere a agregar pequeñas funcionalidades extra de manera constante, causando retrasos en los entregables y pérdida del enfoque en el proyecto.
- **Banderas sobre objetos**: Ocurre cuando los comportamientos son escritos por fuera de los objetos mediante banderas (ej: códigos de estado), resultando en una responsabilidad poco clara y una distribución de comportamientos problemática.
- **Código Frankenstein**: Consiste en que bloques de código o módulos completos, que no fueron diseñados para trabajar juntos, son forzados dentro de una funcionalidad o aplicación y unidos con una especie de "cinta adhesiva" como algún patrón de adaptador o una interfaz.
- **Cavernícola**: Este antipatrón de desarrollo se caracteriza por la inhabilidad o negación por parte del equipo o la organización para adoptar nuevas tecnologías, metodologías o prácticas.
- **Martillo dorado**: Se refiere a un lenguaje, herramienta, marco de trabajo o plataforma con la cual un ingeniero o equipo se siente cómodo y productivo, por lo que intenta usarla para resolver todos los problemas que se puedan presentar.
- **Clases iceberg**: Ocurre cuando una gran una clase tiene una gran cantidad de métodos privados, lo cual puede indicar que hay comportamientos más allá del alcance de responsabilidad de dicha clase.
- **La trampa del 10%**: Ocurre cuando las fases finales del proyecto son subestimadas en complejidad y esfuerzo.
- **Strings mágicos**: Se refiere a datos de tipo string que son especificados dentro de la aplicación e impactan el funcionamiento de la aplicación.
- **Reinventar la rueda**: Ocurre cuando los ingenieros, equipos u organizaciones prefieren construir herramientas para un proyecto dado por su propia cuenta, en lugar de buscar una herramienta que se encuentre disponible y permita suplir el requerimiento.
- **Juguete brillante**: Es la práctica de creer que los problemas modernos pueden ser resueltos mediante las herramientas, técnicas o librerías más modernas.
- **Código espagueti**: Se refiere a código que está enredado, especialmente respecto al orden en el que el programa fluye.
- **Adhesión estática**: Describe un acoplamiento indeseado causado por el acceso a una funcionalidad de manera global, ya sea en forma de variables o métodos.
- **Campo minado**: Ocurre cuando se despliega una funcionalidad o una versión que no es lo suficientemente estable y los usuarios pueden incurrir en una gran cantidad de errores.
- **Caldero de bruja**: Este antipatrón se caracteriza por una base de código caótica y poco estructurada, donde se combinan múltiples tecnologías, patrones de diseño, principios de programación, entre otros, de forma inconsistente y aleatoria.

## Patrones de arquitectura

  Si bien en las labores de mantenimiento del software, muchas decisiones de arquitectura y patrones ya se tomaron, a medida que el software evoluciona, también lo debe hacer su arquitectura. En este orden de ideas, podemos destacar la importancia de tomar decisiones respecto a los patrones de arquitectura del software.

  Los patrones de arquitectura aplicables a un producto de software dependen de los requerimientos funcionales y no funcionales. Asimismo, los requerimientos pueden ser satisfechos con diferentes arquitecturas y un producto de software puede estar construido usando más de un patrón de arquitectura. Por lo tanto, es imperativo conocer los patrones arquitectónicos, sus ventajas y desventajas. Algunos patrones son:

  *"La arquitectura son las cosas importantes, independiente de lo que sean" - Ralph Jonhson.*

- **Arquitectura monolítica**: Este es considerado el punto de entrada del diseño del sistema; en muchos casos, las primeras versiones de productos de software siguen este patrón, el cual consiste en construir toda la aplicación en un contenedor único y unificado, es decir, todos los componentes, módulos y funcionalidades están integradas en un solo ejecutable. El patrón no especifica cómo se deben organizar estos componentes, por lo general se complementa con un patrón de capas para separar los componentes funcionales; aunque también se utilizan otros métodos como la separación por módulos o subdominios. En cualquier caso, siempre se debe apuntar a tener alta cohesión y bajo acoplamiento en este patrón, con el fin de hacerlo más durable y eficiente.

  Adicionalmente, en la arquitectura monolítica son cruciales los [patrones de diseño](#patrones-de-diseño) de software, ya que en este patrón, mientras aumenta la complejidad del sistema, se hace cada vez más difícil de mantener, lo que lleva a un desgaste más acelerado.

  <p align="center">
    <img src="./Arquitectura/Monolito.png" />
  </p>

    Las aplicaciones monolíticas pueden tener un buen rendimiento y suelen ser fáciles de gestionar en las fases iniciales de los proyectos de software. A medida que el software evoluciona, suelen ser escalables hasta cierta medida dependiendo de la naturaleza del software, pero eventualmente pueden hacerse casi imposibles de escalar. Este patrón tiene una desventaja notable frente a otros: los despliegues e integraciones suelen hacerse más lentos y complejos. Además, las aplicaciones monolíticas suelen ser difíciles de probar y mantener a medida que se hacen más complejas. El acoplamiento entre los componentes, la deuda técnica y la dificultad para separar las responsabilidades pueden ser factores de riesgo para este patrón.

- **Arquitectura de capas (N layers)**: Este patrón suele ser complementario a aplicaciones monolíticas; consiste en organizar los componentes de la aplicación en capas horizontales, donde cada capa tiene una responsabilidad específica (por ejemplo, lógica de negocio, lógica de presentación). El patrón no especifica la cantidad ni el tipo de capas; esta decisión depende del equipo de desarrolladores. Aun así, la mayoría de las arquitecturas de capas cuentan con 4 capas principales: presentación, negocio, persistencia y datos. En algunos casos, las capas de persistencia y negocio se combinan en una sola capa.

  En la arquitectura de capas, las capas deben estar separadas e independientes. Es decir, por ejemplo, la capa de negocio no debería tener información de cómo se muestra la información al usuario en la capa de presentación, ni debería necesitarla. Lo mismo aplica para las demás capas, ya que cada capa debe proveer una abstracción de sus funcionalidades que permita la interacción con el resto de los componentes de la aplicación.

  <p align="center">
    <img src="./Arquitectura/Ncapas.png" />
  </p>

      En general, este patrón permite un prototipado y desarrollo rápidos, además de adaptarse a una gran variedad de necesidades de negocio. Sin embargo, tiene una desventaja de escalabilidad, ya que a medida que el software se hace más complejo, puede ser difícil organizar las capas y separar sus responsabilidades. Además, es fácil caer en el antipatrón de sumidero, es decir, una solicitud a un servicio de arquitectura en capas debe pasar por todas las capas sin aplicar ninguna lógica empresarial.

- **Arquitectura orientada a servicios (service-oriented)**: Este patrón consiste en separar los componentes del software en servicios desacoplados e independientes que se encargan de una fracción de la lógica de negocio y se comunican entre ellos mediante peticiones de red (tradicionalmente HTTP). Esta arquitectura le permite a los desarrolladores aprovechar código heredado, así como reutilizar componentes ya construidos e integrar nuevos fácilmente.
Este patrón consta de cuatro componentes principales:

  - Servicios: este es el componente básico de la arquitectura, pueden ser privados dentro de equipos y organizaciones o ser expuestos para el uso del público en general. Internamente, los servicios se componen de tres partes principales:
    - Implementación: contiene toda la lógica necesaria para que el servicio realice sus funciones.
    - Contrato: define la naturaleza del servicio y sus condiciones, por ejemplo, requisitos para su funcionamiento, tipo de datos, entre otros.
    - Interfaz: esta es la cara visible del servicio para los demás servicios, en ella se define cómo se accede a los métodos del servicio.
  - Proveedor de servicios: este crea, mantiene y provee los servicios para ser usados.
  - Consumidor de servicios: es quien sea que utilice los servicios, puede ser una aplicación o otro servicio. Entre el proveedor y consumidor debe haber un contrato que indique cómo interactúan ambas partes.
  - Registry (registro/repositorio): en este componente se almacenan los servicios, consiste en un directorio que puede ser accedido por los consumidores para acceder a los servicios que necesiten.

  En este patrón se requiere implementar un contrato de comunicación, como puede ser: protocolo de acceso simple a objetos (SOAP), RESTful HTTP, colas de mensajes, entre otros. En general, se suele usar una combinación de varios patrones y es común el uso de un patrón complementario: *bus de servicios empresariales (ESB por sus siglas en inglés)*.

  Un ESB es, en esencia, un componente encargado de la comunicación entre otros componentes del software. En el caso de la arquitectura orientada a servicios, se encarga de gestionar modelos, conexiones, mensajería, patrones de comunicación, entre otras, haciendo que los servicios puedan integrarse entre ellos y a otras aplicaciones de forma rápida y sencilla. Si no se implementa un ESB o cualquier otro patrón de integración y comunicación, este patrón pierde su propósito, pues los servicios estarían aislados.

<Mark>Nota: los servicios en este patrón deben ser desacoplados e independientes, sin embargo, cuando se implementa un ESB, este suele ser centralizado.</Mark>

<p align="center">
  <img src="./Arquitectura/SOA.png" />
</p>

      En términos generales, este patrón provee una alta adaptabilidad, rendimiento y mantenibilidad, gracias a que sus componentes son independientes y están desacoplados. Sin embargo, el ESB puede ser un factor de riesgo en esta arquitectura, al ser un componente centralizado; si este falla, la aplicación no funcionará.
      Mientras el software evoluciona y se hace más complejo, también se hacen más complejas las comunicaciones entre los servicios. Asimismo, un diseño ineficiente del ESB afecta el rendimiento y la escalabilidad del producto en su conjunto.
      La escalabilidad es limitada en este patrón de arquitectura, ya que varios servicios pueden necesitar uno o varios recursos simultáneamente y necesitan ser orquestados. Sumado a esto, el acoplamiento en los servicios y el antipatrón de sumidero pueden generar inconvenientes. A medida que la red de servicios crece, pueden darse casos de servicios repetidos y relaciones circulares.

- **Arquitectura de eventos (event-driven)**: Esta arquitectura se compone de diversos servicios altamente desacoplados y con responsabilidad única, los cuales reciben y procesan eventos de manera asincrónica. En este patrón, hay dos formas principales de organizar los componentes dependiendo de las necesidades: mediador y agente o corredor.

  - **Mediador**: esta topología consiste en delegar la orquestación de diversos pasos a un servicio. Por ejemplo, al realizar una orden de compra en una aplicación de e-commerce, podría ser necesario verificar si el producto solicitado está en el inventario, luego verificar la información bancaria del usuario, la cobertura del envío y la confirmación de pago, para posteriormente generar un recibo de pago, enviar un correo electrónico de confirmación de orden y mostrar información sobre el envío del producto.

  Todos estos pasos necesitan ser orquestados para determinar el orden de los pasos y cuáles se pueden ejecutar en paralelo o son dependientes de otros.
  
<p align="center">
  <img src="./Arquitectura/Mediador.png" />
</p>

El patrón de mediador consta de cuatro partes principales:

- La cola de eventos: este componente actúa como punto de entrada, recibe los eventos y los transporta al mediador. El patrón no especifica qué tipo de cola implementar; esta puede ser una cola de mensajes, el endpoint de un servicio web o una combinación de ambos.

- El mediador: es el responsable de recibir el evento inicial y orquestar los pasos que este contenga. Al ejecutar cada uno de estos pasos, el mediador emite un mensaje de procesamiento al canal de eventos que luego será procesado. Es importante señalar que el mediador no ejecuta ni tiene conocimiento de ninguna lógica de negocio, sino que conoce los pasos y el flujo entre ellos.

- El canal de eventos: este componente es usado por el mediador para enviar mensajes a los procesadores. Los canales pueden ser implementados en forma de colas de mensajes o temas de mensajes; generalmente se implementan temas, ya que permiten un procesamiento paralelo por parte de varios ejecutores.

- El ejecutor o procesador: contiene toda la lógica de negocio necesaria para procesar un evento. Este componente debería ser autocontenido, independiente y altamente desacoplado. Según los requerimientos, los procesadores pueden ser más o menos granulares; sin embargo, el objetivo es que tengan responsabilidades únicas y no dependan de otros procesadores para realizar su trabajo.

- **Agente**: esta topología retira la orquestación de los eventos. En este caso, los eventos fluyen a través de los ejecutores en forma de cadena. En este caso, hay solamente dos componentes:

  - El corredor: es equivalente al canal de eventos y contiene todos los canales pertinentes al flujo de eventos de la aplicación. Este puede ser centralizado o distribuido. Al igual que en la topología de mediador, se pueden implementar en forma de temas o colas de mensajes.
  
  - El ejecutor o procesador: cumple la misma función que en la topología de mediador.
  
    <p align="center">
      <img src="./Arquitectura/Broker.png" />
    </p>

        En este patrón, la escalabilidad y el rendimiento de la aplicación son destacables, así como la mantenibilidad de los componentes de lógica de negocio. Sin embargo, el desarrollo puede ser más complejo, especialmente considerando que debido a su naturaleza asíncrona y distribuida, se deben abordar requerimientos de disponibilidad y tolerancia a fallas. Además, la mantenibilidad y el gobierno de los componentes de mensajería pueden hacerse difíciles a medida que el software se hace más complejo.

- **Microkernel (plug-in)**: Esta arquitectura se compone tradicionalmente de 2 componentes básicos: un sistema principal o núcleo y una serie de módulos intercambiables.

  - Core: Tradicionalmente, este componente debería contener la lógica mínima para que el sistema funcione. Además, debe tener conocimiento de los módulos adicionales conectados y cómo acceder a estos. Existen diversas formas de implementar este requerimiento; una de las más comunes es almacenar el registro de los módulos adicionales junto con datos o metadatos (nombre, protocolo de comunicación, protocolo de datos, datos de entrada y salida, etc.), según sea el caso en algún formato conveniente.

  - Los módulos: Este componente debe ser independiente y autocontenido, permitiendo funcionalidades adicionales al sistema principal o apalancando las funcionalidades existentes del mismo. Si bien los módulos deben ser independientes entre sí, es posible diseñar módulos que se apoyen en uno o varios módulos más. Siempre teniendo en cuenta que la interacción entre los módulos debe ser mínima, para evitar problemas de dependencias y alto acoplamiento.

    <p align="center">
      <img src="./Arquitectura/MicroKernel.png" />
    </p>

        En este patrón, es importante considerar que puede aplicarse fácilmente junto con otros patrones, destacando su versatilidad y rendimiento. La mantenibilidad del software con esta arquitectura es alta, ya que es relativamente simple agregar nuevas funcionalidades así como mejorar las existentes, gracias a la separación marcada de responsabilidades. Sin embargo, a medida que el sistema se hace más complejo, puede tener menos escalabilidad. Además, es necesario determinar protocolos y contratos para la conexión de los módulos, junto con protocolos marcados de gobierno de aplicación, lo que puede hacer el desarrollo más complejo.

- **Microservicios**: La idea básica detrás de este patrón es tener un conjunto de unidades desplegadas independientemente. Estas unidades contienen servicios o componentes del software, y pueden variar en granularidad y complejidad (similar a las clases en los lenguajes orientados a objetos).

  La arquitectura de microservicios es distribuida, por ende es importante tener en cuenta los protocolos de comunicación entre los servicios que la componen (JMS, AMQP, REST, SOAP, RMI, etc.).

  Existen muchas topologías en una arquitectura de microservicios y estas varían según los requerimientos del software; algunas de las más populares son:

  - API-Rest: En esta topología se organizan varios componentes que tienen responsabilidades simples y específicas de forma independiente entre sí. Estos servicios son accedidos a través de una API desplegada de forma separada.
  
  - Aplicaciones Rest: En estos casos los componentes son accedidos a través de un cliente (una aplicación web o móvil, un servicio en nube, etc.) que de forma remota se comunica con servicios desplegados independientemente a través de protocolos tipo rest. En esta topología los componentes tienden a ser más complejos.
  
  - Mensajes centralizados/cola de mensajes: En esta topología un agente de mensajería se encarga de gestionar la interacción entre los servicios. Esta topología ayuda a gestionar aplicaciones con requerimientos más complejos y es más escalable que las aproximaciones más simples basadas en REST. En este caso es importante destacar que se requiere implementar un agente de mensajería, así como gestores de errores, monitoreo, operaciones asíncronas, balanceo de cargas, entre otros.
  
  La arquitectura de microservicios se creó originalmente para abordar problemas típicos de la arquitectura monolítica y de la arquitectura basada en servicios (SOA). Gracias a esto presenta grandes ventajas con respecto a estas últimas arquitecturas. Entre las principales se destaca la integración y despliegue continuos, brindando un mejor control sobre la interacción de los componentes distribuidos, permitiendo hacer más y mejores pruebas al software, además de evitar eventos de tipo "big bang" como puede ocurrir en las arquitecturas monolíticas.

  <p align="center">
    <img src="./Arquitectura/Microservicios.png" />
  </p>

      En este patrón, la mantenibilidad, escalabilidad y versatilidad son altas, además de permitir un proceso de desarrollo y pruebas muy óptimo, gracias a la separación marcada de responsabilidades. Aun así, estas separaciones pueden ser un arma de doble filo, ya que en un diseño ineficiente, las responsabilidades pueden estar demasiado separadas, o no estarlo lo suficiente. Sumado a esto, mantener el rendimiento de la aplicación puede hacerse complicado en el tiempo, ya que cuanto más complejo es el software, más microservicios podrían ser agregados. Esto representa carga sobre el agente de mensajería, integración de más componentes entre sí y en general más partes móviles en el software, lo que se traduce en más entropía en el sistema.

- **Arquitectura basada en espacio**: La idea de este patrón es abordar los problemas de escalabilidad que podría tener una aplicación, apuntando a que tengan el menor impacto posible. Esto se logra a través de un espacio en tuplas o memoria distribuida, en otras palabras, usar una red de datos replicados, en lugar de una base de datos centralizada. Los datos de la aplicación son replicados en las unidades de procesamiento activas, estas mismas pueden encenderse o apagarse dinámicamente, según las necesidades de la aplicación.

  En esta arquitectura hay dos componentes básicos:
  - Unidades de procesamiento: En este se despliegan los componentes del software (en algunos casos parcialmente) que hagan falta. Según el caso pueden ser componentes web, lógica de negocio o una combinación de ambos. Todo dependerá del tipo de software. Así mismo, dependiendo de la complejidad del sistema, puede haber una o varias unidades de procesamiento. Adicionalmente, en las unidades de procesamiento se despliega una red de almacenamiento de datos y según el caso, un mecanismo para replicar los cambios en el resto de las unidades de procesamiento.
  
  - Intermediario o middleware: Este componente es el encargado de gestionar las unidades de procesamiento y las comunicaciones. Está conformado por cuatro componentes:
    - Red de mensajes: Es el encargado de gestionar los datos de entrada y la información de sesión. En este componente se determina qué unidades de procesamiento se encuentran disponibles para atender las peticiones y las redirige a la unidad correspondiente.
    - Red de datos: Este componente es uno de los ejes centrales de la arquitectura, es el responsable de interactuar con el gestor de replicación de datos y cada una de las unidades de procesamiento para gestionar la replicación de datos cuando hay una actualización en alguna unidad de procesamiento. Dado que la red de mensajes puede asignar una tarea a cualquier unidad de procesamiento, es crucial que todas tengan exactamente los mismos datos.
    - Red de procesamiento: Este componente es opcional y se encarga de gestionar peticiones distribuidas cuando las unidades de procesamiento tienen la lógica de negocio distribuida en varias unidades de procesamiento (ej: Unidad1: inventario, Unidad2: información de pago).
    - Gestor de despliegue: Está a cargo de gestionar dinámicamente (encender o apagar) unidades de procesamiento, según sea el caso, basándose en la carga que esté soportando el sistema. Este componente es muy importante para lograr una escalabilidad variable y óptima en el sistema.

  <p align="center">
    <img src="./Arquitectura/SpaceBased.png" />
  </p>
  
   Existen variaciones de este patrón, que incluyen una base de datos centralizada, donde se almacenan datos poco volátiles o para inicializar los datos de las bases de datos distribuidas. Esta práctica puede ayudar a reducir el estrés en las unidades de procesamiento causado por la red de datos en memoria.

  <mark>Este patrón también es conocido como arquitectura basada en la nube, sin embargo, no necesariamente debe tener sus componentes alojados en un servicio basado en la nube o en PaaS (plataforma como servicio).</mark>

      Este patrón destaca por la escalabilidad y el rendimiento, además de ser muy versátil y poderse aplicar a diversos requerimientos. Sin embargo, en cuanto a la mantenibilidad, desarrollo y aplicación, puede hacerse complicado. Si bien la separación de responsabilidades puede ser relativamente fácil de ejecutar, estos factores deben ser atendidos con especial cuidado; de lo contrario, puede verse afectado el rendimiento del software o su escalabilidad.

| Patrón            | Mantenibilidad | Testeabilidad | Rendimiento | Escalabilidad | Complejidad en desarrollo |
|-------------------|----------------|---------------|-------------|---------------|----------------------------|
| Monolítica        | Media          | Baja          | Alto        | Bajo          | Media                      |
| N-capas           | Baja           | Media         | Bajo        | Bajo          | Media                      |
| Orientada a servicios | Alta        | Alta          | Bajo        | Media         | Media                      |
| Orientada a eventos   | Alta        | Baja          | Alto        | Alto          | Alta                       |
| Microkernel       | Alta           | Alta          | Alta        | Baja          | Alta                       |
| Microservicios    | Alta           | Alta          | Bajo        | Alta          | Baja                       |
| Basado en espacio | Baja           | Baja          | Alta        | Alta          | Alta                       |