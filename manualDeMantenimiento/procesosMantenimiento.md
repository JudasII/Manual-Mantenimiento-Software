# Procesos de mantenimiento

Todos los sistemas se degradan con el tiempo; en el ámbito del software, esto se conoce con diversos nombres, como decadencia, degradación o desgaste del sistema o del software. Asimismo, los sistemas de software incrementan su complejidad con el tiempo; algunos autores llaman a esta función entropía del software. La entropía contribuye al desgaste del software, dado que en un sistema con alta entropía, se hace más difícil predecir el comportamiento de las variables, entradas y salidas; en otras palabras, los sistemas de software más complejos se desgastan más rápido, son más propensos a errores y, consecuentemente, son más difíciles y costosos de mantener.

## Tipos de mantenimiento

La IEEE propone en el estándar 1219 que el mantenimiento de software puede ser de cuatro tipos:

- Correctivo
- Preventivo
- Perfectivo
- Adaptativo

Generalmente son separados según su tipo y su proposito:

| | Corrección | Mejora |
| ---|---|--- |
|| | |
|**Proactivo**| Preventivo | Perfectivo|
|**Reactivo**| Correctivo | Adaptativo|
  
Este estándar es ampliamente aceptado dentro de la industria del software y provee una base para diversos [modelos](#modelos-de-mantenimiento) que pueden adaptarse a diversas situaciones y una gran variedad de proyectos.

Un ejemplo es el concepto de mantenimiento planeado y no planeado; de esta forma, las labores de mantenimiento se agrupan según su urgencia y prioridad.

**Mantenimiento planeado (planeable)**: se refiere a todas las labores de mantenimiento que pueden ser previstas y priorizadas según las necesidades de la organización a cargo del software. Dependerá de cada organización cómo se aborda la gestión del ciclo de vida de mantenimiento.
En esta instancia, se abordan los siguientes tipos de mantenimiento:

- Correctivo no urgente: en este caso, si bien los resultados o condiciones del sistema pueden diferir de lo especificado en el requerimiento, no interfieren de manera directa en su funcionamiento. Existe algún tipo de plan de contingencia para el escenario o bien no tiene un impacto significativo en la experiencia del usuario. Algunos ejemplos son:
  - El sistema no muestra los componentes visuales en la paleta de colores requerida.
  - El módulo de facturación no toma en cuenta los decimales, con lo cual los empleados de la caja deben realizar un ajuste en caso de ser necesario.
  - Hay un módulo que se encuentra obsoleto; sin embargo, aún hay un cliente que lo utiliza una vez al año.
- Preventivo: incluye todas las actividades de [refactoring](#refactoring). La idea es hacer que el software mantenga o incremente su calidad para mitigar los efectos del desgaste del software. Asimismo, intentar reducir la entropía del software que se introduce a medida que se mantienen las funcionalidades existentes y se agregan nuevas funcionalidades.
- Perfectivo: incluye labores que buscan mejorar las funcionalidades del software. Además, puede implicar agregar nuevas funcionalidades. Por ejemplo:
  - Un cliente va a expandir sus operaciones a otro país, por lo que el software de facturación debe soportar la moneda de este país.
  - Un módulo que genera reportes ahora debe generar también gráficos de barras con la información de ventas en función del tiempo.
- Adaptativo: incluye todas las actividades de [reingeniería](#reingeniería). La idea es modificar el software para poder asimilar los cambios del entorno en el que se ejecuta. Algunos ejemplos son:
  - Migración de proveedores de hosting.
  - Actualizaciones del sistema operativo del servidor o el cliente.
  - Bibliotecas deprecadas.

**Mantenimiento no planeado**: son todas las actividades de mantenimiento que no pueden ser previstas. Pueden ocurrir por diversas causas y no necesariamente implican que el software tenga baja calidad o un diseño defectuoso. Sin embargo, el diseño del software juega un papel vital en evitar que este tipo de incidentes ocurran. Las tareas de mantenimiento no planeado tienen prioridad máxima, ya que constituyen mantenimiento correctivo urgente. Puede incluir las siguientes afectaciones:

- Que afecta a una gran cantidad o todos los usuarios.
- Causan inoperabilidad en el sistema.
- No existe un plan de contingencia.

En este ámbito son vitales las herramientas de monitoreo, permitiendo a los ingenieros observar datos y reportes del comportamiento del software de forma integral.

Existen diversas herramientas que permiten analizar y monitorear el software, tanto para detectar bloques de código propensos a errores o que tengan un diseño deficiente, como para mantener registros de las transacciones del sistema, el comportamiento de diversos módulos, entre otros indicadores.

- [Google Cloud Operations](https://cloud.google.com/products/operations?hl=en)
- [IBM Instana](https://www.ibm.com/products/instana)
- [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/)
- [New Relic](https://newrelic.com/)
- [Grafana](https://grafana.com/)
- [Prometheus](https://prometheus.io/)
- [Datadog](https://www.datadoghq.com/)
- [Splunk](https://www.splunk.com/)

---

Para que el mantenimiento agregue la mayor cantidad de valor posible, es necesario entender el sistema de la forma más integral posible, para poder designarle un alcance y prioridad óptimo a las labores de mantenimiento.
Esto dependerá de cada caso; sin embargo, algunas consideraciones generales son:

### 1. Objetivos

¿Qué se pretende lograr con el mantenimiento? ¿Reducir errores, mejorar el rendimiento, aumentar la seguridad o una combinación de estos?
¿Qué tan crítico es el software para la organización? ¿Un fallo podría tener un impacto significativo en las operaciones o los ingresos?
¿Cuáles son las expectativas de las partes interesadas, como usuarios, gerentes y equipo de desarrollo?

### 2. Características del software

¿Qué tipo de software es? ¿Aplicación web, aplicación móvil, sistema embebido u otro tipo?
¿Qué tecnologías se utilizan en el desarrollo del software? ¿Lenguajes de programación, frameworks, bases de datos, etc.?
¿Cuál es la complejidad del software? ¿Cuántas líneas de código tiene, cuántos módulos y componentes?
¿Cuál es el historial de mantenimiento del software? ¿Ha habido problemas recurrentes o errores conocidos?

### 3. Recursos disponibles

¿Cuánto tiempo y personal se puede dedicar al mantenimiento?
¿Qué presupuesto se ha asignado para las actividades de mantenimiento?
¿Se dispone de las herramientas y tecnologías necesarias para realizar el mantenimiento?
¿Se cuenta con la experiencia y el conocimiento técnico necesarios en el equipo?

### 4. Riesgos potenciales

¿Cuáles son los principales riesgos asociados al software? ¿Vulnerabilidades de seguridad, errores conocidos, problemas de rendimiento?
¿Qué impacto podrían tener estos riesgos en la organización si no se abordan?
¿Cuáles son los costos potenciales de no realizar el mantenimiento?

### 5. Priorización de actividades

¿Qué actividades de mantenimiento son más importantes y urgentes?
¿En qué orden se deben realizar las actividades de mantenimiento?
¿Es posible agrupar las actividades de mantenimiento por tipo o tecnología?

### 6. Comunicación y coordinación

¿Cómo se comunicará el alcance del mantenimiento a las partes interesadas?
¿Cómo se coordinará el mantenimiento con otras actividades, como el desarrollo de nuevas funcionalidades o el soporte técnico?
¿Cómo se gestionarán los cambios en el alcance del mantenimiento durante el proceso?

### 7. Evaluación y revisión

¿Cómo se evaluará el éxito del mantenimiento?
¿Con qué frecuencia se revisará el alcance del mantenimiento?
¿Cómo se adaptará el alcance del mantenimiento a los cambios en el software, las tecnologías y las necesidades de la organización?

## Refactoring

El refactoring es un proceso de mejora continua del código fuente sin modificar su comportamiento externo. Se centra en organizar y simplificar el código sin agregar nuevas funcionalidades ni cambiar la lógica del software.

Los objetivos del refactoring son:

- Mejorar la legibilidad: El código debe ser fácil de entender y leer para otros desarrolladores.
- Aumentar la mantenibilidad: El código debe ser fácil de modificar y adaptar a nuevos requisitos.
- Reducir la complejidad: El código debe ser lo más simple y directo posible.
- Evitar errores: Un código bien estructurado y organizado es menos propenso a errores.

Existen numerosas técnicas de refactoring, algunas de las más comunes incluyen:

- Renombrar variables y métodos: Se utilizan nombres más descriptivos y significativos para mejorar la comprensión del código.
- Extraer métodos: Se extraen fragmentos de código repetitivos en métodos independientes para mejorar la modularidad.
- Generalizar código: Se modifica el código para que sea más flexible y reutilizable en diferentes contextos.
- Simplificar expresiones: Se simplifican expresiones complejas para mejorar la legibilidad y reducir el riesgo de errores.

Al momento de realizar un refactor tenga en cuenta la siguiente lista de chequeo:

- [X] el código debe estar más limpio después del refactor.
- [X] no se deben agregar nuevas funcionalidades durante el refactor.
- [X] el código debe cumplir con todas las pruebas existentes después del refactor.

---

### Código limpio

El concepto de código limpio se refiere a código que cumple con un estándar de calidad establecido dentro de los equipos de desarrollo. La idea es mantener la calidad del producto de software y evitar la deuda técnica, además de incrementar la mantenibilidad del software. Algunos de los principios del código limpio son:

- Obviedad: El código debe ser legible y obvio para otros ingenieros y programadores, independientemente de si estos tienen contexto sobre este o no.
- Único: Las funcionalidades, algoritmos y demás implementaciones deben construirse una única vez; de lo contrario, se incrementa la carga cognitiva y la entropía del sistema, reduciendo la mantenibilidad y haciendo lentos los avances.
- Cantidad mínima de partes móviles: El código debe ser lo más simple posible; en términos generales, menos código significa menos errores, menos mantenimiento, complejidad, entropía y menos carga cognitiva.
- Fácil de probar y cumple el plan de pruebas: Aunque puede variar dependiendo del equipo a cargo, generalmente se busca que el código cumpla con un porcentaje de cobertura, así como superar un umbral de porcentaje de éxito en las pruebas; estas pruebas a su vez, deben ser fáciles de implementar.

### Code smells

También llamado código apestoso, se refiere básicamente al código que tiene una mala calidad. Esto no implica que el código no funcione correctamente o que no cumpla con los requerimientos del sistema, sino más bien a que el código no está completamente limpio y que potencialmente puede generar inconvenientes a largo plazo.

<mark>Nota: Cuando se detectan code smells es muy importante atacarlos lo antes posible.</mark>

Los principales code smells son:

- Bloater: Un bloque del código que ha crecido demasiado, tanto que resulta complejo de entender y manejar. Algunos ejemplos son:
- Métodos demasiado largos: La mayoría de los métodos deben tener menos de diez líneas.
- Clases muy complejas: Las clases deben ser sencillas y concretas, una clase con demasiados métodos.
- Mal uso de primitivos: Los tipos primitivos no deben usarse para representar objetos de dominio.
- Listas de parámetros demasiado largas: Los métodos no deben tener más de tres o cuatro parámetros.
- Agrupación de datos: Si dos o más bloques de código tienen las mismas variables, entonces estos datos deben estar en su propia clase.
- Abuso de la orientación a objetos: Una aplicación incorrecta o incompleta de los principios de la orientación a objetos. Algunos ejemplos son:
  - Condicionales complejos.
  - Atributos condicionales o temporales.
  - Herencia incompleta o condicionada.
  - Clases iguales con interfaces diferentes.
- Inconveniente de cambios: Al realizar una modificación a un bloque de código, es necesario también realizar modificaciones en una gran cantidad de bloques diferentes. Algunos ejemplos son:
  - Cambios divergentes: Una vez realizado un cambio, es necesario hacer ajustes en otros bloques que no están relacionados con la funcionalidad modificada.
  - Operaciones dispersas: Un cambio cualquiera implica realizar una gran cantidad de pequeños ajustes en otros bloques del código.
  - Herencias paralelas: Cuando se crea una subclase, es necesario crear otras subclases para otras clases no relacionadas.
- Desechables: Cualquier cosa que puede ser eliminada del código sin afectar su funcionamiento. Algunos ejemplos son:
  - Comentarios.
  - Código duplicado.
  - Clases innecesarias.
  - Código muerto.
- Acopladores: Cuando el código favorece el acoplamiento o genera una delegación excesiva. Algunos ejemplos son:
  - Envidia de funcionalidad: Los métodos no deben acceder datos de otros objetos.
  - Poca intimidad: Las clases no deben acceder a los atributos de otras clases.
  - Cadenas de mensajes: El código no debería seguir una estructura `a() -> b() -> c() -> d()`.

Existen diversas herramientas para detectar code smells:

- [SonarQube](https://www.sonarsource.com/products/sonarqube/)
- [JDeodorant](https://github.com/tsantalis/JDeodorant)
- [Infusion](https://www.intooitus.com/products/infusion/)
- [Codebeat](https://codebeat.co/)
- [Jetbrains Upsource](https://www.jetbrains.com/upsource/)
- [PMD](https://pmd.github.io/)
- [CodeClimate](https://codeclimate.com/)

---

<mark>Nota: Cuando se cambia el comportamiento del código fuente, ya no se está realizando refactoring, se está realizando reingeniería.</mark>

## Reingeniería

La reingeniería es un proceso de transformación profunda del software para mejorar su arquitectura, diseño y código. Se centra en modificar la estructura fundamental del software para hacerlo más moderno, adaptable y mantenible. En última instancia, la reingeniería puede desencadenar una migración completa del software hacia una arquitectura, motor de base de datos, lenguaje de programación o patrones de diseño más adecuados a los nuevos requerimientos. Dependiendo de la madurez, tamaño y complejidad del software (comprendiendo aquí también a las personas detrás de este software, así como sus procesos empresariales y logísticos), los procesos de reingeniería pueden ser más o menos comunes, complejos y profundos.

Los objetivos de la reingeniería son:

- Modernizar el software: Adaptar el software a las tecnologías y frameworks modernos.
- Mejorar la arquitectura: Simplificar la arquitectura del software para hacerlo más modular y flexible.
- Reestructurar el código: Reorganizar el código para hacerlo más legible, mantenible y reutilizable.
- Eliminar código obsoleto: Eliminar código innecesario o no utilizado que dificulta la comprensión y el mantenimiento del software.

En cuanto a las técnicas, podemos destacar:

- Análisis estático: Analizar el código fuente para identificar problemas de diseño, errores y código obsoleto.
- Reestructuración de la arquitectura: Modificar la arquitectura del software para mejorar su modularidad, separación de preocupaciones y patrones de diseño.
- Reescritura del código: Reescribir el código desde cero utilizando tecnologías y frameworks modernos.

## Migración

En ocasiones, los productos de software requieren una reestructuración completa en su ambiente de ejecución, por ejemplo, mover el software de una nube pública a una privada o viceversa; este proceso es conocido como migración. Algunos ejemplos son:

- Migración de arquitectura
- Migración de sistema operativo
- Migración a la nube
- Migración a SAP

Existen diversos patrones para ejecutar migraciones, conocidos como Rs:

- Reubicar/ realojar (rehost): esta estrategia suele ser más rápida en comparación, lo que reduce costos. La idea es mover la aplicación de un servidor físico local (on-premise) a una máquina virtual alojada en la nube sin realizar cambios mayores al software.
- Reingeniería: implica realizar cambios a la aplicación para adaptarse a nuevas funcionalidades, mejorar su rendimiento y escalar de manera más eficiente. Un caso común es separar una aplicación monolítica en un grupo de servicios o microservicios.
- Cambio de plataforma (replatform): es una combinación de la reingeniería y la reubicación. La idea es hacer cambios menores a la aplicación para que esta se adapte mejor a las nuevas condiciones, por ejemplo, convertir la aplicación en contenedores o modificarla para que soporte bases de datos en la nube.
- Retirar/ reemplazar: en ocasiones tiene sentido simplemente retirar la aplicación. Las razones pueden variar e incluir poco valor, capacidades duplicadas o limitadas, o altos costos de operación.

Dado que las aplicaciones de software están diseñadas para ser ejecutadas en sistemas operativos específicos, con arquitecturas de red, datos y nube particulares, determinar una estrategia de migración implica conocer y entender cada componente de la aplicación de forma individual. Algunos de los factores a considerar cuando se evalúan componentes del sistema candidatos a migración son:

- Complejidad
- Importancia
- Implicaciones de cumplimiento
- Disponibilidad
- Aplicación de pruebas

Realizar una migración conlleva una serie de riesgos, los cuales deben ser considerados antes de tomar la decisión de migrar un sistema:

- Retos técnicos: la aplicación puede tener dependencias críticas o una gran cantidad de dependencias, lo que agrega complejidad a la migración.
- Costos inesperados: si la planificación no se realiza correctamente, la organización puede incurrir en costos que no se encontraban en el presupuesto planeado, como pueden ser costos de licencias o entrenamientos relacionados con las nuevas herramientas o plataformas.
- Inoperabilidad: es posible que al realizar cambios en la aplicación, esta falle o presente errores que causen tiempos de inoperabilidad inesperados.
- Diferencias culturales o de administración: dado que cada organización es diferente, cada una utiliza los productos de software de maneras diferentes, lo que puede causar fricción y ralentizar los procesos de migración.

## Requerimientos

Así como el software tiene un ciclo de vida, el mantenimiento tiene internamente su propio ciclo de vida. Este es similar al ciclo de vida del software, y dependiendo de las metodologías de cada equipo, puede variar. Sin embargo, básicamente cuenta con las fases de planeación, diseño, implementación, pruebas y despliegue. De manera similar al ciclo de vida del desarrollo de software, en el mantenimiento se deben recolectar y analizar los requerimientos de las actualizaciones del software.

- La IEEE presentó en 1980 el estándar *IEEE830* que propone especificaciones de requerimientos de software que deben cumplirse, y estos pueden ser funcionales o no funcionales. Los principales objetivos que se identifican en la especificación de requisitos del software son los siguientes:

  - Ayudar a los clientes a describir claramente lo que quieren de un programa de software.
  
  - Ayudar a los desarrolladores a entender lo que quiere el cliente, incluso si ellos mismos no saben exactamente lo que quieren.
  
  - Servir de base para el desarrollo de normas ERS (Especificación de Requisitos de Software) específicas para cada organización. Esto ayudará a los desarrolladores a entender exactamente lo que quiere el cliente.
  
- ### Requerimientos funcionales

  Los requerimientos funcionales se refieren a qué debe hacer el software. Es de suma importancia que estos requerimientos, así como su contexto y alcance, se definan con alto nivel de detalle y claridad; de lo contrario, se corre el riesgo de que el equipo de desarrollo realice interpretaciones subjetivas, lo que puede generar reprocesos, introducir regresiones, reducir la calidad y la mantenibilidad del software.

  En general, los requerimientos funcionales describen los requerimientos que pueden tener el usuario y el sistema. Los tipos más comunes de requerimientos funcionales son:
  - Regulaciones comerciales
  - Requisitos de Certificación
  - Requisitos de Información
  - Funciones Administrativas
  - Niveles de Autorización
  - Seguimiento de Auditoría
  - Interfaces Externas
  - Administración de Datos
  - Requisitos Legales y Reglamentarios

  Algunos ejemplos de requerimientos funcionales son:
  - Descripciones de los datos a ser ingresados en el sistema.
    - "El campo país consistirá en una lista de preselección. El país asociado a una dirección debe ser previamente registrado en el sistema."
  - Descripciones de las operaciones a ser realizadas por cada pantalla.
    - "Un usuario podrá iniciar sesión en el sistema utilizando su nombre de usuario y contraseña, en la pantalla de *acceder*."
  - Descripción de los flujos de trabajo realizados por el sistema.
    - "El proceso de compras en el sistema abarcará los siguientes pasos y transacciones: Ingreso de la requisición, emisión de la solicitud de cotización y emisión de la orden de compra."
  - Descripción de los reportes del sistema y otras salidas.
    - "El sistema enviará un correo electrónico cuando se registre alguna de las siguientes transacciones: pedido de venta de cliente, despacho de mercancía al cliente, emisión de factura a cliente y registro de pago de cliente."
  - Definición de seguridad.
    - "El sistema enviará una alerta al administrador del sistema cuando ocurra alguno de los siguientes eventos: Registro de nueva cuenta, ingreso al sistema por parte del cliente, 2 o más intentos fallidos en el ingreso de la contraseña de usuario y cambio de contraseña de usuario."
  - Cómo el sistema cumplirá los reglamentos y regulaciones del sector o generales que le sean aplicables.
    - "El sistema permitirá elaborar y emitir el reporte regulatorio XX, según los requerimientos establecidos en el reglamento y ley aplicable."

- ### Requerimientos no funcionales

   Los requerimientos no funcionales se refieren a los requisitos específicos que se pueden usar para juzgar la operación del software y sus características de funcionamiento; por esto también son llamados requerimientos de calidad. Son vitales para determinar si el software cumple con las necesidades establecidas por el usuario.
   En general, los requerimientos no funcionales se pueden agrupar en requerimientos de producto, organizacionales y externos. Cada uno de estos agrupa diversos tipos de requerimientos no funcionales.
   Algunos ejemplos son:

- ### Producto

  - Eficiencia: "El sistema debe ser capaz de operar adecuadamente con hasta 100.000 usuarios con sesiones concurrentes."
  - Seguridad: "Todos los sistemas deben respaldarse cada 24 horas. Los respaldos deben ser almacenados en una localidad segura ubicada en un edificio distinto al que reside el sistema."
  - Seguridad del hardware: "El sistema no continuará operando si la temperatura externa es menor a 4 grados Celsius."
  - Usabilidad: "El sistema debe contar con un módulo de ayuda en línea."
  - Disponibilidad: "El tiempo para iniciar o reiniciar el sistema no podrá ser mayor a 5 minutos."

- ### Organizacionales

  - "Debe especificarse un plan de recuperación ante desastres para el sistema a ser desarrollado."
  - "Cada dos semanas deberán producirse reportes gerenciales en los cuales se muestre el esfuerzo invertido en cada uno de los componentes del nuevo sistema."
  - "Las pruebas de software se ejecutarán utilizando Selenium y Ruby como herramienta y lenguaje Scripting para automatización de software testing."

- ### Externos

  - El nuevo sistema se acogerá a las reglas de las licencias generales públicas (GNU), es decir, será gratuito, código abierto en el que cualquiera podrá cambiar el software, sin patentes y sin garantías.
  - Las páginas web a ser desarrolladas deben cumplir con la ley de tratamiento en condiciones de igualdad para personas con discapacidad.
  - El sistema no revelará a sus operadores otros datos personales de los clientes distintos a nombres y números de referencia.

## Modelos de mantenimiento
- **Quick Fix**: Este método consiste en priorizar las soluciones más rápidas por encima de las de mayor calidad. Por lo general, implica realizar un cambio rápido y localizado para brindar una solución inmediata a los problemas del software. Sin embargo, puede generar un rápido deterioro del software, agregar deuda técnica y reducir la calidad general del sistema. Se recomienda utilizar solo en casos de emergencia y complementarlo con un análisis "post mortem" para identificar la causa raíz del problema.

- **Modelo de Bohem**: Propuesto por Barry Bohem en 1983, este modelo se basa en principios de economía para mejorar el desarrollo de software. Consiste en un ciclo circular que parte de las decisiones administrativas, donde el equipo administrativo tiene la responsabilidad de alinear los objetivos de la compañía con las labores de mantenimiento del software y balancearlos con las limitaciones del proyecto.

- **Modelo de Osborne**: Enfocado en el proceso de mantenimiento desde una perspectiva realista, trata el mantenimiento como una serie de iteraciones continuas del ciclo de vida del software. Se propone la hipótesis de que muchos problemas técnicos en el mantenimiento se deben a una mala administración o falta de comunicación, y propone estrategias para mitigar estos problemas.

- **Modelo de Taute**: Propuesto por B.J. Taute en 1983, este modelo describe el mantenimiento de software como un ciclo cerrado de 8 fases que van desde la solicitud de cambio hasta la operación del software. Cada fase incluye actividades como estimación, planeación, desarrollo, pruebas, documentación, despliegue y operación.

- **Modelo Iterativo**: Parte de la premisa de que la implementación del software es un proceso iterativo que implica mejorar el sistema con el tiempo. Consiste en analizar el sistema, proponer soluciones candidatas y luego implementar esas soluciones. Requiere una documentación rigurosa del sistema y sus ciclos de vida.

- **Modelos de Reuso**: Basado en la idea de reutilizar partes existentes del sistema y construir componentes que puedan ser reutilizados posteriormente. Este modelo consta de cuatro etapas: identificación de candidatos a reuso, análisis de los componentes del sistema, adaptación de los componentes a reusar e integración del nuevo componente al sistema.

- **Modelo Reactivo**: Aplica la estrategia de esperar a que los componentes del software fallen para repararlos. Puede ser de mantenimiento de avería, correctivo o de emergencia, y se suele aplicar a componentes no esenciales o con poco impacto en la operabilidad del sistema.

- **Open Source**: El software libre no suele contar con un equipo establecido de mantenimiento, sino que sus comunidades se encargan de administrar y realizar dicha labor. En estos casos, el ciclo de vida puede estar a cargo de diversas personas de la comunidad.

| Tarea | Descripción | Encargado |
|---|---|---|
| Analisis inicial | Puede ser el reporte de un incidente, su verificación y documentación o la solicitud de una nueva funcionalidad. | Cualquier persona (usuario, desarrollador, autor).   |
| Asignación      | Uno o varios desarrolladores se encargarán de implementar el requerimiento.                          | Cualquier desarrollador (es común que un desarrollador se asigne tareas a sí mismo). |
| Implementación  | Uno o varios desarrolladores implementan y documentan el requerimiento.                               | Desarrollador(es) asignado(s).                        |
| Enviar la modificación | La implementación es enviada para su revisión y validación, estos cambios se almacenan y administran usando diversas herramientas, por ejemplo, GitHub. | Desarrollador(es) asignado(s).                        |
| Revisión        | Implica la discusión y posterior aceptación o rechazo de la solución propuesta.                     | Comunidad.                                            |
| Pruebas         | Se ejecuta un plan de pruebas sobre la implementación, que puede variar según el proyecto.          | Moderadores/testers/autores.                          |
| Despliegue      | Dependiendo del proyecto, puede existir una serie de ambientes previos a producción (stage, QA, lab). | Moderadores/autores.                                  |
| Anuncio         | Implica comunicar las nuevas funcionalidades del proyecto, además de información relevante, como fechas de despliegue. | Moderadores/autores.                                  |
| Publicación     | Consiste en desplegar la nueva versión del software, para que esté disponible a los usuarios; dependiendo del proyecto, desplegar una nueva versión puede ser más o menos complejo. | Moderadores/autores.                                  |
