# Procesos de mantenimiento

Todos los sistemas se degradan con el tiempo, en el ambito del software, esto se conoce con diversos nombres, como decadencia, degradación o desgaste del sistema o del software. así mismo los sistemas de software incrementan su complejidad en el tiempo, algunos autores llaman a esta función entropía del software. la entropia contribuye al desgaste del software, dado que en un sistema con alta entropía, se hace mas dificil predecir el comportamiento de las variables, entradas y salidas; en otras palabras, los sistemas de software mas complejos se desgastan mas rápido, son mas propensos a errores y consecuentemente, son mas dificiles y costosos de mantener.  

## tipos de mantenimiento

la IEEE propone en el estandar 1219, que el mantenimiento de software puede ser de cuatro tipos:
  
- correctivo
- preventivo
- perfectivo
- adaptativo

generalmente son separados segun su tipo y su proposito
| | corrección | mejora |
| ---|---|--- |
|| | |
|**proactivo**| preventivo | perfectivo|
|**reactivo**| correctivo | adaptativo|
  
este estandar es ampliamente aceptado dentro de la industria del software y provee una base para diversos [modelos](#modelos-de-mantenimiento) que pueden adaptarse a diversas situaciones y gran variedad de proyectos.

un ejemplo es el concepto de mantenimiento planeado y no planeado; de esta forma, las labores de mantenimiento se agrupan según su urgencia y prioridad

**Mantenimiento planeado (planeable)**: se refiere a todas las labores de mantenimiento que pueden ser previstas y priorizadas según las necesidades de la organización a cargo del software. Dependerá de cada organización como se aborda la gestión del ciclo de vida de mantenimiento.
en esta instancia, se abordan los siguientes tipos de mantenimiento:

- correctivo no urgente: en este caso, si bien los resultados o condiciones del sistema pueden diferir de lo especificado en el requerimiento, no interfieren de manera directa en su funcionamiento, existe algún tipo de plan te contingencia para el escenario o bien no tiene un impacto significativo en la experiencia del usuario, algunos ejemplos son:
  - el sistema no muestra los componentes visuales en la paleta de colores requerida
  - el modulo de facturación, no toma en cuenta los decimales; con lo cual los empleados de la caja deben realizar un ajuste en caso de ser necesario.
  - hay un modulo que se encuentra obsoleto, sin embargo aún hay un cliente que lo utiliza una vez al año
- preventivo: incluye todas las actividades de [refactoring](#refactoring), la idea es hacer que el software mantenga o incremente su calidad para mitigar los efectos del desgaste del software, así mismo intentar reducir la entropía del software que es introducida a medida que se mantienen las funcionalidades existentes y se agregan nuevas funcionalidades.
- perfectivo: incluye labores que buscan mejorar las funcionalidades del software, adionalmente puede implicar agregar nuevas funcionalidades, por ejemplo:
  - un cliente va a expandir sus operaciones a otro país, por lo que el software de facturación debe soportar la moneda de este país.
  - un modulo que genera reportes, ahora debe generar también gráficos de barras con la información de ventas en función del tiempo.
- adaptativo: incluye todas las actividades de [reingeniería](#reingeniería), la idea es modificar el software para poder asimilar los cambios del entorno que se ejecuta, algunos ejemplos son:
  - migración de proveedores de hosting
  - actualizaciones del sistema operativo del servidor o el cliente
  - librerias deprecadas

**Mantenimiento no planeado**: son todas las actividades de mantenimiento que no pueden ser previstas, pueden ocurrir por diversas causas y no necesariamente implican que el software tenga baja calidad o un diseño defectuoso; sin embargo, el diseño del software, juega un papel vital en evitar que este tipo de incidentes ocurran. las tareas de mantenimiento no planeado, tienen  prioridad maxima, ya que constituyen mantenimiento correctivo urgente, puede incluir las siguientes afectaciones:

- que afecta a una gran cantidad o todos los usuarios
- causan inoperabilidad en el sistema
- no existe un plan de contingencia
  
en este ambito son vitales las herramientas de monitoreo, permitiendo a los ingenieros observar datos y reportes del comportamiento del software de forma integral.

 existen diversas herramientas que permiten analizar y monitorear el software, tanto para detectar bloques de codigo propensos a errores, o que tengan un diseño deficiente como para mantener registros de las transacciones del sistema, el comportamiento de diversos módulos, entre otros indicadores.

- [Google Cloud Operations](https://cloud.google.com/products/operations?hl=en)
- [IBM Instana](https://www.ibm.com/products/instana)
- [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/)
- [New relic](https://newrelic.com/)
- [Grafana](https://grafana.com/)
- [Prometeus](https://prometheus.io/)
- [Datadog](https://www.datadoghq.com/)
- [Splunk](https://www.splunk.com/)

---

para que el mantenimiento agregue la mayor antidad de valor posible, es necesario entender el sistema, de la forma mas integral posible; para poder designarle un alcance y prioridad optimo a las labores de mantenimiento.
esto dependerá de cada caso, sin embargo algunas consideraciones generales son:

### 1. Objetivos

¿Qué se pretende lograr con el mantenimiento ? ¿Reducir errores, mejorar el rendimiento, aumentar la seguridad o una combinación de estos?
¿Qué tan crítico es el software para la organización? ¿Un fallo podría tener un impacto significativo en las operaciones o los ingresos?
¿Cuáles son las expectativas de las partes interesadas, como usuarios, gerentes y equipo de desarrollo?

### 2. Características del software

¿Qué tipo de software es? ¿Aplicación web, aplicación móvil, sistema embebido o un tipo diferente?
¿Qué tecnologías se utilizan en el desarrollo del software? ¿Lenguajes de programación, frameworks, bases de datos, etc.?
¿Cuál es la complejidad del software? ¿Cuántas líneas de código tiene, cuántos módulos y componentes?
¿Cuál es el historial de mantenimiento del software? ¿Ha habido problemas recurrentes o errores conocidos?

### 3. Recursos disponibles

¿Cuánto tiempo y personal se puede dedicar al mantenimiento?
¿Qué presupuesto se ha asignado para las actividades de mantenimiento ?
¿Se dispone de las herramientas y tecnologías necesarias para realizar el mantenimiento ?
¿Se cuenta con la experiencia y el conocimiento técnico necesarios en el equipo?

### 4. Riesgos potenciales

¿Cuáles son los principales riesgos asociados al software? ¿Vulnerabilidades de seguridad, errores conocidos, problemas de rendimiento?
¿Qué impacto podrían tener estos riesgos en la organización si no se abordan?
¿Cuáles son los costos potenciales de no realizar el mantenimiento?

### 5. Priorización de actividades

¿Qué actividades de mantenimiento son más importantes y urgentes?
¿En qué orden se deben realizar las actividades de mantenimiento ?
¿Es posible agrupar las actividades de mantenimiento por tipo o tecnología?

### 6. Comunicación y coordinación

¿Cómo se comunicará el alcance del mantenimiento  a las partes interesadas?
¿Cómo se coordinará el mantenimiento con otras actividades, como desarrollo de nuevas funcionalidades o soporte técnico?
¿Cómo se gestionarán los cambios en el alcance del mantenimiento  durante el proceso?

### 7. Evaluación y revisión

¿Cómo se evaluará el éxito del mantenimiento ?
¿Con qué frecuencia se revisará el alcance del mantenimiento ?
¿Cómo se adaptará el alcance del mantenimiento a los cambios en el software, las tecnologías y las necesidades de la organización?


# Refactoring

El refactoring es un proceso de mejora continua del código fuente sin modificar su comportamiento externo. Se centra en organizar y simplificar el código sin agregar nuevas funcionalidades ni cambiar la lógica del software.

los objetivos del refactoring son:

- Mejorar la legibilidad: El código debe ser fácil de entender y leer para otros desarrolladores.
- Aumentar la mantenibilidad: El código debe ser fácil de modificar y adaptar a nuevos requisitos.
- Reducir la complejidad: El código debe ser lo más simple y directo posible.
- Evitar errores: Un código bien estructurado y organizado es menos propenso a errores.

Existen numerosas técnicas de refactoring, algunas de las más comunes incluyen:

- Renombrar variables y métodos: Se utilizan nombres más descriptivos y significativos para mejorar la comprensión del código.
- Extraer métodos: Se extraen fragmentos de código repetitivos en métodos independientes para mejorar la modularidad.
- Generalizar código: Se modifica el código para que sea más flexible y reutilizable en diferentes contextos.
- Simplificar expresiones: Se simplifican expresiones complejas para mejorar la legibilidad y reducir el riesgo de errores.

Al momento de realizar un refactor tenga en cuenta la siguiente lista de checkeo:

- [X] el código debe estar más limpio, despue del refactor.
- [X] no se deben agregar nuevas funcionalidades durante el refactor
- [X] el codigo debe cumplir con todas las pruebas existentes, despues del refactor.

---

**código limpio**
: el concepto de codigo limpio se refiere a codigo que cumple con un estandar de calidad establecido dentro de los equipos de desarrollo, la idea es mantener la calidad del producto de software y evitar la deuda técnica, además de incrementar la mantenibilidad del software.
algunos de los principios del codigo limpio son:

- obviedad: el código debe ser legible y obvio para otros ingenieros y programadores, independiete si estos tienen contexto sobre este o no.
- unico: las funcionalidades, algoritmos y demás implementaciones deben construirse una única vez, de lo contrario se incrementa la carga cognitiva y la entropía del sistema, reduciendo la mantenibilidad y haciendo lentos los avances.
- cantidad minima de partes moviles: el código debe ser lo mas simple posible, en terminos generales, menos codigo significa menos errores, menos mantenimiento, complejidad, entropía y menos carga cognitiva
- facil de probar y cumple el plan de pruebas: aunque puede variar dependiendo del equipo a cargo, generalmente se busca que el código cumpla con un porcentaje de cobertura, así como superar un umbral de porcentaje de exito en las pruebas; estas pruebas a su vez, deben ser faciles de implementar.

**Code smells**
: también llamado código apestoso, se refiere basicamente al codigo que tiene una mala calidad. esto no implica que el código no funcione correctamente o que no cumpla con los requerimientos del sistema, sino mas bien a que el código no está completamente limpio y que potencialmente puede generar inconvenientes en el largo plazo.

<mark> nota: cuando se detectan code smells es muy importante atacarlos lo antes posible.

los principales code smell son:

- Bloater: un bloque del codigo que ha crecido demasiado, tanto que resulta complejo de entender y manejar, algunos ejemplos son:
  - métodos demasiado largos: la mayoría de los métodos, deben tener menos de diez lineas.
  - clases muy complejas: las clases deben ser sencillas y concretas, una clase con demasiados métodos.
  - mal uso de primitivos: los tipos primitivos no deben usarse para representar objetos de dominio.
  - listas de parametros demasiado largas: los metodos, no deben tener mas de tres o cuatro parametros.  
  - agrupación de datos: si dos o más bloques de codigo tienen las mismas variables, entonces estos datos deben estar en su propia clase.
- abuso de la orientación a objetos: una aplicación incorrecta o incompleta de los principios de la orientación a objetos, algunos ejemplos son:
  - condicionales complejos
  - atributos condicionales o temporales
  - herencia incompleta o condicionada
  - clases iguales con interfaces diferentes
- inconveniente de cambios: al realizar una modificación a un bloque de codigo, es necesario también realizar modificaciones en una gran cantidad de bloques diferentes, algunos ejemplos son:
  - cambios divergentes: una vez realizado un cambio, es necesario hacer ajustes en otros bloques que no están relacionados con la funcionalidad modificada
  - operaciones dispersas: un cambio cualquiera, implica realizar una gran cantidad de pequeños ajustes en otros bloques del codigo
  - herencias paralelas: cuando se crea una subclase, es necesario crear otras subclases para otras clases no relacionadas.
- desechables: es cualquier cosa que puede ser eliminada del código sin afectar su funcionamiento, algunos ejemplos son:
  - comentarios
  - codigo duplicado
  - clases innecesarias
  - codigo muerto
- acopladores: cuando el codigo favorece el acoplamiento o genera una delegación excesiva, algunos ejemplos son:
  - envidia de funcionalidad: los metodos no deben acceder datos de otros objetos
  - poca intimidad: las clases no deben acceder a los atributos de otras clases
  - cadenas de mensajes: el código no debería seguir una estructura  `a()-> b() -> c() -> d()`

existen diversas herramientas para detectar code smells:

- [sonarqube](https://www.sonarsource.com/products/sonarqube/)
- [jDeodorant](https://github.com/tsantalis/JDeodorant)
- [infusion](https://www.intooitus.com/products/infusion/)
- [Codebeat](https://codebeat.co/)
- [Jetbrains Upsource](https://www.jetbrains.com/upsource/)
- [PMD](https://pmd.github.io/)
- [Codeclimate](https://codeclimate.com/)  

---

<mark>nota: cuando se cambia el comportamiento del código fuente, ya no se está realizando refactoring, se está realizando reingeniería</mark>


### reingeniería

La reingeniería es un proceso de transformación profunda del software para mejorar su arquitectura, diseño y código. Se centra en modificar la estructura fundamental del software para hacerlo más moderno, adaptable y mantenible; en ultima instancia, la reingeniería puede desencadenar una migración completa del software hacia una arquitectura, motor de base de datos, lenguaje de programación o patrones de diseño más adecuados a los nuevos requerimientos. Dependiendo de la madurez, tamaño y complejidad del software(comprendiendo aquí también, a las personas detrás de este software, así como sus procesos empresariales y logisticos.) los procesos de reingeniería pueden ser más o menos comunes, complejos y profundos;

los objetivos de la reingeniería son:

- Modernizar el software: Adaptar el software a las tecnologías y frameworks modernos.
- Mejorar la arquitectura: Simplificar la arquitectura del software para hacerlo más modular y flexible.
- Reestructurar el código: Reorganizar el código para hacerlo más legible, mantenible y reutilizable.
- Eliminar código obsoleto: Eliminar código innecesario o no utilizado que dificulta la comprensión y el mantenimiento del software.

en cuanto a las técnicas, podemos destacar:  

- Análisis estático: Analizar el código fuente para identificar problemas de diseño, errores y código obsoleto.
- Reestructuración de la arquitectura: Modificar la arquitectura del software para mejorar su modularidad, separación de preocupaciones y patrones de diseño.
- Reescritura del código: Reescribir el código desde cero utilizando tecnologías y frameworks modernos.

---

### Migración

---
En ocasiones, los productos de software requieren una reestructuración completa en su ambiente de ejecución,por ejemplo, mover el software de una nube publica a una privada o viceversa, este proceso es conocido como migración, algunos ejemplos son:

- Migración de arquitectura
- Migración de sistema operativo
- Migración a la nube
- Migración a SAP

existen diversos patrones para ejecutar migraciones, conocidos como Rs:

- Reubicar/ realojar (rehost): esta estrategia suele ser más rapida en comparación por lo que reduce costos, la idea es mover la aplicación de un servidor fisico local( on premise ) a una maquina virtual alojada en la nube sin realizar cambios mayores al software.
- Reingeiería: implica realizar cambios a la aplicación para adaptarse a nuevas funcionalidades, mejorar su rendimiento y escalar de manera mas eficiente, un caso común es separa una aplicación monolitica en un grupo de servicios o microservicios.
- cambio de plataforma( replatform ): es una combinación de la reingeniería y la reubicación, la idea es hacer cambios menores a la aplicación para que esta se adapte mejor a las nuevas condiciones, por ejemplo, convertir la aplicación en contenedores o modificarla para que soporte bases de datos en la nube.
- retirar/ reemplazar: en ocasiones tiene sentido simplemente retirar la aplicación, las razones pueden variar e incluyen poco valor, capacidades duplicadas o limitadas o altos costos de operación.

por la manera en como se contruyen las aplicaciones de software, estas están diseñadas para ser ejecutadas en sistemas operativos especificos, con arquitecturas de red, datos y nube particulares. Por lo tanto determinar una estrategia de migración implica conocer y entender cada componente de la aplicación de forma individual; algunos de los factores a considerar cuando se evaluan componentes del sistema candidatos a migración son:

- complejidad
- importancia
- implicaciones de cumplimiento
- disponibilidad
- aplicación de pruebas

Realizar una migración conlleva una serie de riesgos, los cuales deben ser considerados antes de tomar la decisión de migrar un sistema:

- retos tecnicos: la aplicación puede tener dependencias criticas, o una gran cantidad de las dependencias, que agregan complejidad a la migración
- costos inesperados: si la planeación no se realiza correctamente, la organización puede incurrir en costos que no se encontraban en el presupuesto planeado, como pueden ser costos de licencias o entrenamientos relacionados con las nuevas herramientas o plataformas.
- inoperabilidad: es posible que al realizar cambios en la aplicación, esta falle o presente errores que causen tiempos de inoperabilidad inesperados.
- diferencias culturales o de administración: dado que cada organización es diferente, cada una utiliza los productos de software de maneras diferentes, esto puede causar fricción y relentizar los procesos de migración.

---

### requerimientos

---
Así como el software tiene un ciclo de vida, el mantenimiento tiene internamente su propio ciclo de vida, este es similar al ciclo de vida del software, dependiendo de las metodologías de cada equipo puede variar, sin embargo, cuenta basicamente con las fases de planeación, diseño, implementación, pruebas y despliegue. Así, homologamente al ciclo de vida del desarrollo de software, en el mantenimiento se deben recolectar y analizar los requerimientos de las actualizaciones del software.

- La IEEE presentó en 1980 el estandar *IEEE830* que propone especificaciones de requerimientos de software deben cumplir y estos pueden ser funcionales o no funcionales.
Los principales objetivos que se identifican en la especificación de requisitos del software son los siguientes:

  - Ayudar a los clientes a describir claramente lo que quieren de un programa de software.
  
  - Ayudar a los desarrolladores a entender lo que quiere el cliente, incluso si ellos mismos no saben exactamente lo que quieren.
  - Servir de base para el desarrollo de normas ERS (especificación de requisitos de software) específicas para cada organización. Esto ayudará a los desarrolladores a entender exactamente lo que quiere el cliente.
  
- ### requerimientos funcionales

  Los requerimientos funcionales se refieren a que debe hacer el software, es de suma importancia que estos requerimientos así como su contexto y alcance, se definan con alto nivel de detalle y claridad; de lo contrario, se corre el riesgo de que el equipo de desarrollo realice interpretaciones subjetivas, que pueden generar reprocesos, introducir regresiones, reducir la calidad y la mantenibilidad del software.

  en general, los requerimientos funcionales describen los requerimientos que puede tener el usuario y el sistema, los tipos mas comunes de requerimientos funcionales son:
  - Regulaciones comerciales
  - Requisitos de Certificación
  - Los requisitos de información
  - Funciones administrativas
  - Niveles de autorización
  - Seguimiento de auditoría
  - Interfaces externas
  - Administración de datos
  - Requisitos legales y reglamentarios

  Algunos ejemplos de requerimientos funcionales son:
  - Descripciones de los datos a ser ingresados en el sistema.
    - "El campo país consistirá en una lista de preselección. El país asociado a una dirección debe ser previamente registrado en el sistema."
  - Descripciones de las operaciones a ser realizadas por cada pantalla.
    - "Un usuario podrá iniciar sesión en el sistema utilizando su nombre de usuario y contraseña, en la pantalla de *acceder* "
  - Descripción de los flujos de trabajo realizados por el sistema.
    - "El proceso de compras en el sistema abarcará los siguientes pasos y transacciones: Ingreso de la requisición, emisión de la solicitud de cotización y emisión de la orden de compra."
  - Descripción de los reportes del sistema y otras salidas.
    - "El sistema enviará un correo electrónico cuando se registre alguna de las siguientes transacciones: pedido de venta de cliente, despacho de mercancía al cliente, emisión de factura a cliente y registro de pago de cliente."
  - Definición de seguridad.
    - "El sistema enviará una alerta al administrador del sistema cuando ocurra alguno de los siguientes eventos: Registro de nueva cuenta, ingreso al sistema por parte del cliente, 2 o más intentos fallidos en el ingreso de la contraseña de usuario y cambio de contraseña de usuario."
  - Como el sistema cumplirá los reglamentos y regulaciones de sector o generales que le sean      aplicables.
    - "El sistema permitirá elaborar y emitir el reporte regulatorio XX, según los requerimientos establecidos en el reglamento y ley aplicable."

- ### requerimientos no funcionales

   Los requerimientos no funcionales se refieren a los requisitos especificos que se pueden usar para juzgar la operación del software y sus caracteristicas de funcionamiento; por esto también son llamados requerimientos de calidad. Son vitales para determinar si el software cumple con las necesidades establecidas por el usuario.
   en general, los requerimientos no funcionales se pueden agrupar en requerimientos de producto, organizacionales y externos. Cada uno de estos agrupa diversos tipos de requerimientos no funcoonales.
   algunos ejemplos son:

- ### Producto

  - Eficiencia: "El sistema debe ser capaz de operar adecuadamente con hasta 100.000 usuarios con sesiones concurrentes".
  - Seguridad: "Todos los sistemas deben respaldarse cada 24 horas. Los respaldos deben ser almacenados en una localidad segura ubicada en un edificio distinto al que reside el sistema".
  - Seguridad del hardware: "El sistema no continuará operando si la temperatura externa es menor a 4 grados Celsius".
  - Usabilidad: "El sistema debe contar con un módulo de ayuda en línea".
  - Disponibilidad: "El tiempo para iniciar o reiniciar el sistema no podrá ser mayor a 5 minutos".

- ### Organizacionales

  - "Debe especificarse un plan de recuperación ante desastres para el sistema a ser desarrollado".
  - "Cada dos semanas deberán producirse reportes gerenciales en los cuales se muestre el esfuerzo invertido en cada uno de los componentes del nuevo sistema".
  - "Las pruebas de software se ejecutarán utilizando Selenium y Ruby como herramienta y lenguaje Scripting para automatización de software testing".

- ### Externos

  - El nuevo sistema se acogerá a las reglas de las licencias generales públicas (GNU), es decir será gratuito, código abierto en el que cualquiera podrá cambiar el software, sin patentes y sin garantías.
  - Las páginas web a ser desarrolladas deben cumplir con la ley de tratamiento en condiciones de igualdad para personas con discapacidad.
  - El sistema no revelara a sus operadores otros datos personales de los clientes distintos a nombres y números de referencia.
  
## Modelos de mantenimiento

- **quick fix** : este metodo consiste en priorizar las soliciones mas rapidas por encima de las de mayor calidad. por lo general implica realizar un cambio rapido y localizado, esto con el fin de brindar una solición inmediata a los problemas que pueda presentar el software; además, es común que bajo este modelo se salten algunas reglas del proceso de diseño y deasarrollo, por ejemplo no implementar pruebas unitarias.

Cabe anotar que, esta estrategia genera un rapido deterioro del software, además de agregar entropía, deuda técnica y reducir la calidad general del sistema y solamente debería ser adoptada en casos de emergencia; en conjunto con un proceso de analisis *post mortem* para identificar la causa raiz del problema e implementar una solución de mayor calidad y que aporte al mejoramiento del sistema.

- **Modelo de Bohem**: en 1983 el cientifico de la computación Barry Bohem propuso este modelo, basandose en modelos y principios de economía, la tesis de Bohem propone que como la economía es el eje central de muchos procesos, incluido el desarrollo de software, sus modelos y principios podrían ayudar a entender y mejorar el desarrollo de software.
  
  El modelo de Bohem consiste en un ciclo circular, partiendo de las decisiones administrativas, el equipo administrativo es clave en este modelo pues es quien tiene la responsabilidad de alinear los objetivos de la compañia con las labores de mantenimiento de software y a la vez balancear estos objetivos con las diferentes limitaciones del proyecto( presupuesto, talento, herramientas, tiempo)

- **Modelo de Osborne**:En este modelo se lidia con el proceso de mantenimiento desde una perspectiva más realista; dado que la mayoría de los modelos parten del supuesto de condiciones ideales, como puede ser la existencia de documentación.
  
  El proceso de mantenimiento es tratado como una serie de reiteraciones continuas del ciclo de vida del software y en cada una de las etapas, se toman acciones para mejorar la mantenibilidad del software. Osborne planteó la hipotesis de que un alto porcentaje de los problemas técnicos que se presentan al realizar mantenimiento al software, se deben a una administracion inadecuada, falta de comunicación o una combinación de ambas; además propone estrategias para mitigar estos problemas:
  - incluir requerimientos de mantenimiento en las propuestas o solicitudes de cambio( historias de usuario )
  - adoptar un software de control de calidad en el proyecto
  - implementar estrategias para verificar que los objetivos de mantenimiento fueron alcanzados
  - evaluaciones de desempeño, para retroalimentar a los equipos y sus lideres.
- **Modelo de Taute**: fue propuesto en 1983 por B.J. Taute y popone el mantenimiento de software como un ciclo cerrado de 8 fases:
  - solicitud de cambio: un cliente o usuario realiza una solicitud de cambio
  - estimación: el equipo de mantenimiento se encarga de determinar la cantidad de esfuerzo y tiempo requerido para ejecutar la silicitud
  - planeación: se determina cuando serán desplegados los cambios solicitados al sistema
  - desarrollo: el codigo fuente de la aplicación es modificado para cumplir con el requermiento
  - pruebas: según la organización, el plan de pruebas y los requerimientos, el equipo se asegura de la calidad del nuevo codigo implementado en el sistema
  - documentación: el equipo debe encargarse de documentar el proceso de desarrollo, diseño y pruebas del nuevo requerimiento.
  - despliegue: la modificación o nueva funcionalidad son entregados al cliente
  - operación: el software permanecerá en este estado hasta que se desplieguen nuevas funcionalidades o modificaciones.
- **modelo iterativo**: parte de la premisa de que la implementación del software es un proceso iterativo que implica mejorar el sistema con el tiempo, consta de tres etapas principales:
  - Analisis del sistema
  - proposisción de soliciones candidato
  - implementación de la solución
  En este modelo es de suma importancia una documentación rigurosa del sistema, así como de su ciclo de vida( requerimientos, diseño, plan de pruebas ) puesto que dicha documentación es el punto de partida pra la fase de analisis. Asi mismo la fase de proposición e implementación pueden implicar un rediseño del componentes del sistema, el cual debe ser debidamente documentado, para ser usado en futuras iteraciones.
- **modelos reuso**: se basa en la idea de que el mantenimiento puede ser entendido como un proceso que implica reusar partes existentes del sistema, además de construir componentes que posteriormente podrán reutilizados; generalmente cuenta con cuatro etapas:
  - Identidicación de candidatos a reuso
  - analisis de los componentes del sistema
  - adaptar los componentes a reusar, para cumplir los nuevos requerimientos
  - integrar el nuevo componente al sistema
- **modelo reactivo**: en este modelo se aplica la estrategia de esperar a que los componentes del software fallen para repararlos, suele ser una estrategia de bajo costo y aplicarse solamente a componentes no escenciales o con poco impacto en la oprabilidad del sistema, esto debido a que en el modelo reactivo no se suelen contemplar fases de planeación, algunas topologías de este modelo son:
  - Mantenimiento de avería: puede ser planeado o no planeado, la idea es que una vez que un componente del software falle total o parcialmente, regresarlo a un estado en el cual sea nuevamente funcional. Existe una variación conocida como "run to failure" que consiste en permitir que el componente falle totalmente para reconstruirlo o restaurarlo a un estado operable.
  - Mantenimiento correctivo: la idea es que cuando un componente falle, se identifique la causa raiz del comportamiento inesperado y se rectifique el mismo, con el fin de evitar que uno o varios incidentes generen un fallo mayor
  - Mantenimiento de emergencia: es el tipo de mantenimiento que se ejecuta cuando el software presenta inoperabilidad en cualquier nivel, el objetivo es regresar el sistema a un estado operable lo antes posible, durante o despues de ejecutar el mantenimiento, se debe identificar y solucionar la causa raiz del incidente.
- **open source**: el software libre, no suele contar con un equipo establecido de mantenimiento, sino que sus comunidades se encargan de administrar y realizar dicha labor. En estos casos el ciclo de vida puede estar a cargo de diversas personas de la comunidad.
  |tarea| descripción | encargado|
  |:---:|:---:|:---:|
  |Analisis inicial| puede ser el reporte de un incidente, su verificación y documenteación o la solicitud de una nueva funconalidad  | cualquier persona(usuario, desarrollador, autor) |
  |asignación| uno o varios desarrolladores se encargarán de implementar el requerimiento| cualquier desarrollador( es común que un desarrollador se asigne tareas a si mismo)|
  |implementación | uno o varios desarrolladores implementan y documentan el requerimiento | desarrollador(es) asignado(s) |
  |enviar la modificación | la implementación es enviada para su revisión y validación, estos cambios se almacenan y administran usando diversas herramientas por ejemplo GitHub | desarrollador(es) asignado(s) |
  |revisión | implica la discusión y posterior aceptación o rechazo de la solución propuesta | comunidad|
  |pruebas|  se ejecuta un plan de pruebas sobre la implementación, que puede variar según el proyecto | moderadores/testers / autores |
  |despliegue| dependiendo del proyecto, puede existir una serie de ambientes previos a producción(stage, QA, lab) | moderadores /autores |
  |Anuncio | implica comunicar las nuevas funcionalidades del proyecto, además de información relevante, como fechas de despliegue. | moderadores/autores|
  |publicación | consiste en desplegar la nueva versión del software, para que esté disponible a los usuarios; dependiendo del proyecto, desplegar una nueva versión puede ser más o menos complejo,  | moderadores/autores|
