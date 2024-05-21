# Manual general de mantenimiento

## Tabla de Contenidos

1. [Introducción](#introducción)
2. [Recomendaciones generales](#recomendaciones-generales)
3. [Procesos de mantenimiento](#procesos-de-mantenimiento)
4. [Estudio de casos](#estudios-de-caso)
5. [Fuentes](#fuentes)
6. [Contacto](#contacto)

## Introducción

Este manual tiene como finalidad recopilar información valiosa para las labores de mantenimiento de diversos productos de software.
con el fin de democratizar el conocimiento, estará abierto para recibir aportes de la comunidad, por favor lea la guia de aportes aquí(#a la guia de aportes)

## Recomendaciones Generales

independientemente del tipo de mantenimiento a realizar, hay varios factores a tener en cuenta para el desarrollo de las labores de mantenimiento.
considere siempre las herramientas que tenga a la mano, aquí algunas:

- Herramientas de depuración: Estas herramientas ayudan a identificar la causa de los errores en el software.
la mayoría de los IDEs tienen integradas herramientas para las labores de depuración, es muy importante conocer estas herramientas y tomar su maximo provecho.
- Herramientas de pruebas: Estas herramientas ayudan a garantizar que el software funciona correctamente.
es critico mantener el software al tanto en el plan de pruebas, siempre realice pruebas a su software además de las pruebas unitarias y de integración; las cuales deberian estar siempre presentes en cualquier funcionalidad o labor de mantenimiento de software, considere:
  - pruebas de estrés y rendimiento
  - pruebas de seguridad
  - pruebas de usabilidad y aceptación
  - pruebas funcionales
  - pruebas de humo
  - pruebas de extremo a extremo

#### nota: recuerde que las pruebas ayudan a incrementar la calidad y fiabilidad del software

- Herramientas de monitoreo: Estas herramientas ayudan a rastrear el rendimiento del software y a identificar posibles problemas.
- Herramientas de gestión de configuración: Estas herramientas ayudan a realizar un seguimiento de los cambios en el software.
independientemente si las labores de mantenimiento son realizadas por una o varias personas, es importante mantener un control de versiones optimo y organizado, esto con el fin de evitar errores de versionamiento y despliegue, ademas de permitir una transisión entre vesiones muy comoda y segura.

no solamente las herramientas de control de versiones deben ser consideradas, es importante notar que las herramientas de integración continua son vitales para el software moderno y por ende vitales para las labores de mantenimiento de este.

- Herramientas de documentación: Estas herramientas ayudan a crear y mantener la documentación del software.
es imperativo mantener un software bien documentado

## 1. Considere patrones de diseño y arquitectura

Al inicio del proyecto de software, se realizó una serie de sesiones de diseño; donde considerando los diversos requerimientos del producto que se iba a construir, se tomaron decisiones de diseño y arquitectura, es posible que a medida que el producto haya madurado, se  hayan tomado nueevas decisiones y modificado el diseño original. De cualquier manera, busque los diseños, arquitecturas de referencia, diagramas, entre otros documentos de diseño que puedan ser utiles y estudielos conciensudamente.

Es fundamental que el ingeniero de software comprenda a fondo los patrones de diseño y arquitectura utilizados en la construcción de la aplicación que se está manteniendo. Esto le permitirá:

- Comprender la estructura y organización del código: Al conocer los patrones de diseño, podrá entender cómo se han organizado los componentes del software y cómo interactúan entre sí. Esto facilita la identificación de las áreas que necesitan ser modificadas o actualizadas.
- Tomar decisiones informadas sobre las modificaciones: La comprensión de la arquitectura del software permite tomar decisiones informadas sobre cómo realizar las modificaciones sin afectar negativamente el funcionamiento general de la aplicación.
- Evitar introducir nuevos errores: Al seguir los patrones de diseño adecuados, reduce el riesgo de introducir nuevos errores en el código durante el proceso de mantenimiento.
- Mantener la coherencia del código: Al utilizar patrones de diseño consistentes, se mantiene la coherencia del código y se facilita su comprensión y mantenimiento a largo plazo.
notas sobre arquitectura(#arquitectura de software) y diseño(#patrones de diseño)

## 2. Evalue el impacto

Seguramente el software que está manteniendo pertenezca a una empresa u organización; es muy importante que de manera colectiva y/o individual según el caso, se evalúe cuidadosamente el impacto que las modificaiones tendrán en la aplicación. Esto implica considerar:

- Funcionalidad: ¿Las modificaciones afectarán la funcionalidad existente de la aplicación?
- Rendimiento: ¿Las modificaciones afectarán el rendimiento de la aplicación?
- Seguridad: ¿Las modificaciones introducirán nuevas vulnerabilidades de seguridad?
- Usabilidad: ¿Las modificaciones afectarán la usabilidad de la aplicación para los usuarios?
- Compatibilidad: ¿Las modificaciones afectarán la compatibilidad de la aplicación con otros sistemas o plataformas?

## 3. Considere el plan de pruebas

Una vez realizadas las modificaciones, es crucial realizar pruebas exhaustivas y diversas para garantizar que la aplicación funciona correctamente y que no se han introducido nuevos errores. Las pruebas deben cubrir como minimo:

- Casos de uso: Todos los casos de uso de la aplicación deben probarse para garantizar que funcionan correctamente.
- Regresión: Se deben realizar pruebas de regresión para garantizar que las modificaciones no han afectado negativamente la funcionalidad existente.
- Rendimiento: Se deben realizar pruebas de rendimiento para garantizar que la aplicación sigue funcionando con el rendimiento esperado.
- Seguridad: Se deben realizar pruebas de seguridad para garantizar que las modificaciones no han introducido nuevas vulnerabilidades.

Es importante mencionar que la mayoría de los proyectos de software tienen un plan de pruebas, que suele ser definido en las etapas iniciales del ciclo de vida(planificación y diseño) y posteriormente ejecutado en la etapa de pruebas; generalmente los planes de pruebas quedan documentados al igual que la arquitectura y el diseño, por lo tanto, es importante buscar tener acceso a estos documentos, para cumplir con las pruebas que sugiera el diseño del proyecto de software. De igual manera, si el plan de pruebas por alguna razón ya no es pertinente a los nuevos desarrollos en el mantenimiento del producto, entonces es imperativo el definir un nuevo plan de pruebas, donde se contemplen, segun las necesidades, estandares y demás lineamientos pertinentes a la naturaleza del proyecto de software, las pruebas que se realizarán en el ciclo de mantenimiento.

## 4. documente y comunique

la documentación es sumamente valiosa, para poder transmitir el conocimiento dentro de las organizaciones a cargo del mantenimiento y desarrollo de los productos de software
Es fundamental mantener una comunicación fluida y transparente con todas las partes interesadas durante el proceso de mantenimiento de software. Esto incluye:

Usuarios: Informar a los usuarios sobre las próximas modificaciones y el tiempo de inactividad potencial.
Equipo de desarrollo: Colaborar con el equipo de desarrollo original para comprender mejor el código y la arquitectura de la aplicación.
Gerentes: Mantener a los gerentes informados sobre el progreso del mantenimiento y cualquier problema potencial.

además es importante mantener la documentación del software actualizada para reflejar los cambios realizados durante el mantenimiento. Esto incluye:

Documentación del código: Actualizar la documentación del código para reflejar las modificaciones realizadas.
Documentación de usuario: Actualizar la documentación del usuario para reflejar los cambios en la funcionalidad o la interfaz de usuario.
Documentación de la arquitectura: Actualizar la documentación de la arquitectura para reflejar los cambios en la arquitectura del software.

es muy importante mantener documentos relacionados con las labores de mantenimiento del software, el conocimiento y las experiencias obtenidas al realizar mantenimiento a aplicaciones de software, son enriquecedores y proveen al ingeniero de una perspicacia y habilidad que solamente se obtienen al realizar labores de mantenimiento; el problema radica en que esta caja de herramientas se queda en la cabeza del ingeniero y solo le será util a este, en lugar de a su equipo, su organización o el resto del mundo.
es por esto que siempre las labores de mantenimiento deben ser documentadas, no solo a nivel tecnico, lo cual también es de suma importancia, sino que en la medida de lo posible, compartidas, en blogs, foros, o iniciativas abiertas, como este manual.

### <mark>  NOTA: siempre tenga en cuenta los lineamientos de privacidad de su organización, tenga cuidado de la información que publica en internet y siempre consulte con el area a cargo de la seguridad de la información antes de realizar la publicación de sus articulos, notas, etc.</mark>

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

HERRAMIENTAS
-

-
-
-

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

---

### Refactoring

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

- sonarqube
- eslint
- aaa

<mark> nota: cuando se detectan code smells es muy importante atacarlos lo antes posible.  

---

## metodologias de refactoring

aaaasd

<mark>nota: cuando se cambia el comportamiento del código fuente, ya no se está realizando refactoring, se está realizando reingeniería</mark>
---

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

---

### patrones de diseño

Una vez que se identifican los requerimientos en el mantenimiento, será el momento de identificar y definir los patrones de diseño que apliquen en el desarrollo; en este sentido, es importante tener en cuenta si bien en las etapas anteriores del ciclo de vida del software se realizó un proceso detallado de analisis y definición de patrones de diseño; en las labores de mantenimiento también puede ser necesario aplicar nuevos patrones, adicionales a los que el softwre ya presenta.

Los patrones de diseño son de suma importancia en el software ya que un alto porcentaje de los incidentes de mantenimiento correctivo, pueden ser rastreados hacia una causa raiz que tiene que ver con un diseño ineficiente o degradado; así mismo, un software con antipatrones tiende a sufrir mas fallos y a una mayor entropía, consecuentemente  a ser menos mantenible en el tiempo.
los patrones de diseño, varian según su complejidad nivel de detalle y aplicabilidad. Todos los patrones pueden clasificarse según su proposito, así:

- **Los patrones creacionales**
  : proporcionan mecanismos de creación de objetos que incrementan la flexibilidad y la reutilización de código existente.

- **Los patrones estructurales**
  : explican cómo ensamblar objetos y clases en estructuras más grandes a la vez que se mantiene la flexibilidad y eficiencia de la estructura.

- **Los patrones de comportamiento**
  : se encargan de una comunicación efectiva y la asignación de responsabilidades entre objetos.

|nombre del patrón| descripción  | tipo de patrón |
| --- | --- | --- |
| Factory method (fabrica) | proporcionar una interfaz para crear objetos en una superclase, mientras permite a las subclases alterar el tipo de objetos que se crearán. | Creacional |
| Abstract factory (fabrica abstracta) | producir familias de objetos relacionados sin especificar sus clases concretas. | Creacional |
| Builder (constructor) |  construir objetos complejos paso a paso. El patrón permite producir distintos tipos y representaciones de un objeto empleando el mismo código de construcción. | Creacional |
| Prototype/clone (prototipo, clon) |  copiar objetos existentes sin que el código dependa de sus clases. | Creacional |
| Singleton (unica instancia)| asegurar que una clase tenga una única instancia, a la vez que proporciona un punto de acceso global a dicha instancia. | Creacional |
| Adapter/Wrapper (adaptador, envoltorio) | permitir la colaboración entre objetos con interfaces incompatibles. |Estructural |
| Bridge (puente) | dividir una clase grande, o un grupo de clases estrechamente relacionadas, en dos jerarquías separadas (abstracción e implementación) que pueden desarrollarse independientemente la una de la otra. |Estructural |
| Composite/ object tree (objeto compuesto, arbol de objetos) | componer objetos en estructuras de árbol y trabajar con esas estructuras como si fueran objetos individuales. |Estructural |
| Decorator (decorador) | añadir funcionalidades a objetos colocando estos objetos dentro de objetos encapsuladores especiales que contienen estas funcionalidades. |Estructural |
| Facade (fachada) | proporcionar una interfaz simplificada a una biblioteca, un framework o cualquier otro grupo complejo de clases. |Estructural |
| Flyweight (peso mosca, cache) | mantener más objetos dentro de la cantidad disponible de RAM compartiendo las partes comunes del estado entre varios objetos en lugar de mantener toda la información en cada objeto. |Estructural |
| Proxy | proporcionar un sustituto o marcador de posición para otro objeto. Un proxy controla el acceso al objeto original, permitiéndote hacer algo antes o después de que la solicitud llegue al objeto original.|Estructural |
| Chain of responsability (cadena de responsabilidad) | pasar solicitudes a lo largo de una cadena de manejadores. Al recibir una solicitud, cada manejador decide si la procesa o si la pasa al siguiente manejador de la cadena. |Comportamental |
| Command/ transaction (comando/ transacción) | convertir una solicitud en un objeto independiente que contiene toda la información sobre la solicitud. Esta transformación permite parametrizar los métodos con diferentes solicitudes, retrasar o poner en cola la ejecución de una solicitud y soportar operaciones que no se pueden realizar. |Comportamental |
|Iterator (iterador) | recorrer elementos de una colección sin exponer su representación subyacente (lista, pila, árbol, etc.). |Comportamental |
|Mediator/ controller ( mediador, controlador) | reducir las dependencias caóticas entre objetos. El patrón restringe las comunicaciones directas entre los objetos, forzándolos a colaborar únicamente a través de un objeto mediador. |Comportamental |
| Memento (recuerdo) | guardar y restaurar el estado previo de un objeto sin revelar los detalles de su implementación. |Comportamental |
| Observer (observador) |  definir un mecanismo de suscripción para notificar a varios objetos sobre cualquier evento que le suceda al objeto que están observando. |Comportamental |
| State (estado) |  permitir a un objeto alterar su comportamiento cuando su estado interno cambia. Parece como si el objeto cambiara su clase |Comportamental |
| Strategy (estrategia) | definir una familia de algoritmos, colocar cada uno de ellos en una clase separada y hacer sus objetos intercambiables. |Comportamental |
| Template method (plantilla de metodos) | definir el esqueleto de un algoritmo en la superclase pero permite que las subclases sobrescriban pasos del algoritmo sin cambiar su estructura. |Comportamental |
| Visitor(visitante) | separar algoritmos de los objetos sobre los que operan. |Comportamental |

<Mark> nota: los patrones de diseño mas básicos suelen llamarse *idioms* y suelen aplicar solamente a un lenguaje de programación; por otra parte cuando un patrón aplica a mas alto nivel y se hace mas universal, se considera un patrón de arquitectura </Mark>

## Antipatrones de diseño

Analogamente a los patrones de diseño, existen prácticas en el desarrollo de software, que deben evitarse, en general son patrones de diseño que en lugar de mejorar la calidad del software y ayudar a resolver algun problema, terminan teniendo el efecto opuesto. por ejemplo:

- PATRONES:::::

## Patrones de arquitectura

Si bien en las labores de mantenimiento del software, muchas decisiones de arquitectura y patrones ya se tomaron, a medida que el software evoluciona, también lo debe hacer su arquitectura; en este orden de ideas, podemos destacar la importancia de tomar decisiones respecto a los patrones de arquitectura del software.

Los patrones de arquitectura aplicables a un producto de software, dependen de los requerimientos funcionales y no funcionales; así mismo, los requerimientos, pueden ser satisfechos con diferentes arquitecturas y un producto de software puede estar construido usando más de un patrón de arquitectura; por lo que es imperativo, conocer los patrones arquitectonicos, sus ventajas y desventajas.Algunos patrones son:

 *"la arquitectura son las cosas importantes, independiente de lo que sean"* - Ralph Jonhson.

- **arquitectura monolítica**:este es considerado el punto de entrada del diseño del sistema; en muchos casos las primeras versiones de productos de software siguen este patrón, el cual consiste en construir toda la aplicación en un contenedor unico y unificado, es decir, todos los componentes, modulos y funcionalidades están integradas en un solo ejecutable. El patrón no especifica como se deben organizar estos componentes, por lo general se complementa con un patrón de capas, para separar los componentes funcionales; aunque también se utilizan otros métodos como la separación por módulos o subdominios. En cualquier caso siempre se debe apuntar a tener alta cohesión y bajo acoplamiento en este patrón, con el fin de hacerlo más durable y eficiente.
Adicionalmente, en la arquitectura monolítica son cuciales los [patrones de diseño](#patrones-de-diseño) de software, ya que en este patrón mientras aumenta la complejidad del sistema se hace cada vez mas dificil de mantener lo que lleva a un desgaste mas acelerado.

  las aplicaciones monolíticas pueden tener un buen rendimiento y suelen ser faciles de gestionar en las fases inciales de los proyectos de software; a medida que el software evoluciona suelen ser escalables hasta alguna medida dependiendo de la naturaleza del software, pero eventualmente pueden hacerse casi implosibles de escalar, patrón tiene una desventaja notable frente a otros, los despliegues e integraciones suelen hacerse más lentos y complejos, también Las aplicaciones monoliticas suelen ser dificiles de probar y mantener a medida que se hacen mas complejas, el acoplamiento entre los componentes, la deuda tecnica y la dificultad para separar las responsabilidades pueden ser factores de riesgo para este patrón.

- **arquitectura de capas( N layers)**: este patrón, suele ser complementario a aplicaciones monolíticas; consiste en organizar los componentes de la aplicación en capas horizontales, cada capa tiene una responsabilidad especifica ( ej. lógica de negocio, lógica de presentación ). El patrón no especifica la cantidad ni el tipo de capas, esta decision depende del equipo de desarrolladores; aún así, la mayoria de las arquitecturas de capas, cuenta con 4 capas principales: presentación, negocio, persistencia y datos. En algunos casos, las capas de persistencia y negocio se combinan en una sola capa.
  
  En la arquitectura de capas, las capas deben estar separadas e independientes. es decir que por ejemplo la capa de negocio, no debería tener información de como se muestra la información al usuario en la capa de presentación, tampoco debería necesitarla; lo mismo aplica para las demás capas, ya que cada capa debe proveer una abstración de sus funcionalidades, que permita la interación con el resto de los componentes de la aplicación.
  
  En general este patrón permite un prototipado y desarrollo rapidos, además de adaptarse a una gran variedad de necesidades de negocio, sin embargo tiene una desventaja de escalabilidad; ya que a medida que el software se hace más complejo, puede ser dificil organizar las capas y separar sus responsabilidades. Además, es facil caer en el antipatrón de sumidero, es decir una solicitud a un servicio de arquitectura en capas debe pasar por todas las capas sin aplicar ninguna lógica empresarial.
- **arquitectura orientada a servicios ( service-oriented )**: este patrón consiste en separar los componentes del software en servicios desacoplados e independientes que se encargan de una fracción de la logica de negocio y se comunican entre ellos mediante peticiones de red( tradicionalmente http ). esta arquitectura le permite a los desarrolladores aprovechar codigo heredado, así como reutilizar componentes ya construidos e integrar nuevos facilmente.
  Este patrón consta de cuatro componentes principales:
  
  - Servicios: este es el componente basico de la arquitecura, pueden ser privados dentro de equipos y organizaciones o ser expuestos para el uso del publico en general. Internamente los servicios se componen de tres partes principales:
    - implementación: contiene toda la lógica necesaria para que el servicio realice sus funciones
    - contrato: define la naturaleza del servicio y sus condiciones, por ejemplo requisitos para su funcionamiento, tipo de datos, entre otros.
    - interfas: esta es la cara visible del servicio para los demás servicios, en ella se define que como se accede a los metodos del servicio.
  - proveedor de servicios: este crea mantiene y provee los servicios para ser usados
  - consumidor de servicios: es quien sea que utilice los servicios, puede ser una aplicación o otro servicio. entre el proveedor y consumidor debe haber un contrato, que indique como interactuan ambas partes.
  - registry (registro/ repositorio): en este componente se almacenan los servicios, consiste en un directorio que puede ser accedido por los consumidores para acceder a los servicios que necesiten.

   en este patrón se requiere implementar un contrato de comunicación,como puede ser: protocolo de acceso simpe a objetos (SOAP), RESTfull HTTP, colas de mensajes, entre otros; en general se suele usar una combinación de varios patrones y  es común el uso de un patrón complementario: *bus de servicios empresariales ESB por sus siglas en ingles*.
  un ESB, es en escencia un componente encargado de la comunicación entre otros componentes del software, en el caso de la arquitectura orientada a servicios, se encarga de gestionar: modelos, conecciones, mensajería, patrones de comunicación, entre otras. haciendo que los servicios puedan integrarse entre ellos y a otras aplicaciones de forma rapida y sencilla.
  si no se implementa un ESB o cualquier otro patrón de integración y comunicación, este patrón pierde su proposito, pues los servicios estarian aislados.
  
  <Mark>Nota: los servicios en este patrón deben ser desacoplados e independientes, sin embargo, cuando se implementa un ESB, este suele ser centralizado.</Mark>

  en terminos generales, este patrón provee una adaptabilidad rendimiento y mantenibilidad altos, gracias a que sus componentes son independientes y están desacoplados; por otra parte, el ESB puede ser un factor de riesgo en esta arquitectura, siendo un componente centralizado en la arquitectura, si este falla, la aplicación no funcionará.
   Mientras el software evoluciona y se hace mas complejo, también se hacen mas complejas las comunicaciones entre los servicios, así mismo, un diseño ineficiente del ESB afecta el rendimiento y la escalabilidad del producto en su conjunto.
  La escalabilidad es limitada en este patrón de arquitectura, ya que varios servicios pueden necesitar uno o varios recursos simultaneamente y necesitan ser orquestados; sumado a esto, el acoplamiento en los servicios y el antipatrón de sumidero puede generar inconvenientes, a medida que la red de servicios crece, pueden darse casos de servicios repetidos y relaciones circulares
- **arquitectura de eventos ( event-driven )**: Esta arquitectura se compone de diversos servicios altamente desacoplados y con responsabilidad unica, los cuales reciven y procesan eventos de manera asincrona. En este patrón hay dos formas principales de organizar los componentes dependiendo de las necesidades: mediador( mediator ) y agente o corredor ( broker )
  - Mediador: esta topología consiste en delegar la orquestación de diversos pasos a un servicio; por ejemplo: al realizar una orden de compra en una aplicación de e-comerce, podria ser necesario verificar si el producto solicitado está en el inventario, luego verificar la información bancaria del usuario, la cobertura del envio y la confirmación de pago, para posteriormente generar un recibo de pago, enviar un correo electrónico de confirmación de orden y mostrar información sobre el envio del producto.
  
      todos estos pasos necesitan ser orquestados, para determinar el orden de los pasos y cuales se pueden ejecutar en paralelo o son dependientes de otros.

      el patrón de mediador consta de cuatro partes principales:
    - la cola de eventos: este componente actua como punto de entrada, recibe los eventos y los transporta al mediador. El patrón no especifica que tipo de cola implementar, esta puede ser una cola de mensajes, el endpoint de un servicio web o una combinación de ambos.

    - el mediador: es el responsable de recibir el evento inicial y orquestar los pasos que este contenga, al ejecutar cada uno de estos pasos, el mediador emite un mensaje de procesamiento al canal de eventos que será luego procesado. Es importante anotar que el mediador no ejecuta ni tiene conocimiento de ninguna lógica de negocio, sino mas bien conoce los pasos y el flujo entre los mismos.
    - el canal de eventos: este componente es usado por el mediador para enviar mensajes a los procesadores, los canales pueden ser implementados en forma de colas de mensajes o temas de mensajes; generalmente se implementan temas, ya que permiten un procesamiento paralelo por parte de varios ejecutores
    - el ejecutor o procesador: contiene toda la logica de negocio necesaria para procesar un evento; este componente debería ser autocontenido, indepentiente y altamente desacoplado. según los requerimientos, los procesadores pueden ser más o menos granulares, sin embargo el objetivo es que tengan responsabilidades unicas y no dependan de otros procesadores para realizar su trabajo.
  
  - Agente: esta topología retira la orquestación de los eventos, en este caso, los eventos fluyen a traves de los ejecutores en forma de cadena. en este caso hay solamente dos componentes:
    - el corredor: es equivalente al canal de eventos, y contiene todos los canales pertinentes al flujo de eventos de la aplicación. este puede ser centralizado o distribuido; al igual que en la topología de mediador, se pueden implementar en forma de temas o colas de mensajes.
    - el ejecutor o procesador: cumple la misma función que en la topología de mediador.

    en este patrón, la escalabilidad y el rendimiento de la aplicación son destacables así como la mantenibilidad de los componentes de lógica de negocio sin embargo, el desarrollo puede ser mas compleja, en especial considerando que debido a su naturaleza asincrona y distribuida, se deben abordar requerimientos de disponibilidad y tolerancia a fallas, además de que la mantenibilidad y gobierno de los componentes de mensajería puede hacerse dificil a medida que el software se hace mas complejo.
- **Microkernel ( plug-in )**: esta arquitectura se compone tradicionalmente de 2 componentes basicos: un sistema principal o core y una serie de modulos intercambiables.
  - core: tradicionalmente, este componente debería contener la lógica minima para que el sistema funcione. Adicionalmente debe tener conocimiento de los modulos adicionales conectados y como acceder a estos; existen diversas formas de implementar este requerimiento, una de las más comunes es almacenar el registro de los modulos adicionales junto con datos o meta datos(nombre, protocolo de comunicación, protocolo de datos, datos de entrada y salida, etc.), segun sea el caso en algún formato conveniente.
  - los modulos: este componente debe ser independiente y autocontenido; permitiendo funcionalidades adicionales al sistema principal o apalancando las funcionalidades existentes del mismo. Si bien los modulos deben ser independientes entre sí, es posible diseñar modulos que se apoyen en uno o varios modulos más; siempre teniendo en cuenta que la interacción entre los modulos debe ser minima, para evitar problemas de dependencias y alto acoplamiento.
  
  en este patrón es importante considerar que puede aplicarse facilmente junto con otros patrones, destacando su versatilidad y rendimiento. La mantenibilidad del software con esta arquitectura es alta, ya que es relativamente simple agregar nuevas funcionalidades así como mejorar las existentes, gracias a la separación marcada de responsabilidades. sin embargo, a medida que el sistema se hace más complejo puede tener menos escalabilidad adicionalmente es necesario determinar protocolos y contratos para la conexion de los modulos, junto con protocolos marcadados de gobierno de aplicación y esto puede hacer el desarrollo más complejo.
- **Microservicios**: la idea basica detras de este patrón es tener un conjunto de unidades desplegadas independientemente, estas unidades contienen servicios o componentes del software, y pueden variar en granularidad y complejidad ( similar a las clases en los lenguajes orientados a objetos ).
  
  la arquitectura de microservicios es distribuida, por ende es importante tener en cuenta los protocolos de comunicación entre los servicios que la componen( JMS, AMQP, REST, SOAP, RMI, etc.).
  
  Existen muchas topologías en una arquitectura de microservicios y estas varian segun los requerimientos del software; algunas de las mas populares son:
  
  - API-Rest: en esta topología se organizan varios componentes que tienen responsabilidades simples y especificas de forma independiente entre sí. estos servicios son accedidos a traves de una API desplegada de forma separada
  - aplicaciones Rest: en estos casos los componentes son accedidos a traves de un cliente(una aplicación web o mobil, un servicio en nube, etc) que de forma remota se comunica con servicios desplegados independientemente a traves de protocolos tipo rest. en esta topología los componentes tienden a ser mas complejos.
  - mensajes centralizados/ cola de mensajes: en esta topología un agente de mensajeria se encarga de gestionar la interacción entre los servicios; esta topología ayuda a gestionar aplicaciones con requerimientos mas complejos y es más escalable que las aproximaciones mas simbles basadas en rest.
    En este caso es importante destacar que se requiere implementar un agente de mensajería, así como gestores de errores, monitoreo, operaciones asincronas, balanceo de cargas, entre otros.
  
  La arquitectura de microservicios se creó originalmente para abordar problemas tipicos de la arquitectura monolitica y de la arquitectura basada en servicios(SOA), gracias a esto presenta grandes ventajas con respecto a estas ultimas arquitecturas, entre las principales se destaca la integración y despliegue continuos, brindando un mejor control sobre la interacción de los componentes distribuidos, permitiendo hacer más y mejores pruebas al software, ademas de evitar eventos de tipo "big bang" como puede ocurrir en las arquitecturas monolíticas.

  en este patrón, la mantenibilidad, escalabilidad y versatilidad son altas, además de permitir un proceso de desarrollo y pruebas muy optimo, gracias a la separación marcada de responsabilidades; asún así, estas separaciones pueden ser un arma de doble filo, ya que en un diseño ineficiente, las responsabilidades pueden estar demasiado separadas, o no estarlo lo suficiente; sumado a esto, mantener el rendimiento de la aplicación puede hacerse complicado en el tiempo, ya que cuanto mas complejo es el software, más microservicios podrían ser agregados, esto representa carga sobre el agente de mensajería, integración de más componentes entre sí y en general más partes mobiles en el software, lo que se traduce en más entropía en el sistema.

- **Arquitectura basada en espacio** :  la idea de este patrón es abordar los problemas de escalabilidad que podria tener una aplicacion, apuntando a que tengan el menor impacto posible. esto se logra a traves de un espacio en tuplas o memoria distribuida, en otras palabras, usar una red de datos replicados, en lugar de una base de datos centralizada; los datos de la aplicación son replicados en las unidades de procesamiento activas, estas mismas pueden encenderse o apagarse dinamicamente, segun las necesidades de la aplicación.

  en esta arquitectura hay dos componentes basicos:
  - unidades de procesamiento: en este se despliegan los componentes del software ( en algunos casos parcialmente) que hagan falta, según el caso pueden ser componentes web,lógica de negocio o una combinación de ambos. Todo dependerá del tipo de software. así mismo, dependiendo de la complejidad del sistema, puede haber una o varias unidades de procesamiento.
      adicionalmente en las unidades de procesamiento se despliega una red de almacenamiento de datos y según el caso, un mecanismo para replicar los cambios en el resto de las unidades de procesamiento
  - intermediario o midleware: este componente es el encargado de gestionar las unidades de procesamiento y las comunicaciones. esta conformado por cuatro componentes:
    - red de mensajes: es el encargado de gestionar los datos de entrada y la información de sesión. En este componente se determina que unidades de procesamiento se encuentran disponibles para atender las peticiones y las redirige a la unidad corresponidente.
    - red de datos: este componente es el uno de los ejes centrales de la arquitectura, es el responsable de interactuar con el gestor de replicación de datos y cada una de las unidades de procesamiento para gestionar la replicación de datos cuando hay una actualización en alguna unidad de procesamiento. dado que la red de mensajes puede asignar una tarea a cualquier unidad de procesamiento, es crucial que todas las tengan exactamente los mismos datos.
    - red de procesamiento: este componente es opcional, y se encarga de gestionar peticiones distribuidas cuando las unidades de procesamiento tienen la logica de negocio distribuida en varias unidades de procesamiento( ej: Unidad1: inventario Unidad2: información de pago)
    - gestor de despliegue: está a cargo de gestionar dinamicamente ( encender o apagar ) unidades de procesamiento, según sea el caso, basandose en la carga que esté soportando el sistema. Este componente es muy importante para lograr una escalabilidad variable y optima en el sistema.

    Existen variaciones de este patrón, que incluyen una base de datos centralizada, donde se almacenan datos poco volatiles o para inicializar los datos de las bases de datos distribuidas. esta practica puede ayudar a reducir el estrés en las unidades de procesamiento causado por la red de datos en memoria.
    <mark>este patrón tambien es conocido como arquitecura basada en la nube, sin embargo, no necesariamente debe tener sus componentes alojados en un servicio basado en la nube o en PaaS(plataform as a service).</mark>
    este patrón destaca por la escalabilidad y el rendimiento, ademas de ser muy versatil y poderse aplicar a diversos requerimientos, sin embargo en cuanto a la mantenibilidad, desarrollo y aplicación de puede hacerse complicado, si bien la separacion de responsabilidades puede ser relativamente facil de ejecutar, estos factores deben ser atendidos con especial cuidado, de lo contrario puede verse afectado el rendimiento del software o su escalabilidad.  

|Patrón |mantenibilidad | testeabilidad | rendimiento| escalabilidad| complejidad en desarrollo|
|---|:---:|:---:|:---:|:---:|:---:|
|Monolítica | media | baja | alto | bajo | media |
|N-capas| baja | media | bajo | baja | media |
|orientada a servicios| alta | alta | bajo |media | media |
|orientada a eventos | alto | baja | alto | alto | alta|
|Microkernel| alta | alta | alta| baja| alta|
|Microservicios | alta |alta|  bajo | alta | baja |
|Basado en espacio| baja| baja| alta| alta | alta |  

## Modelos de mantenimiento

- quick fix
- boehm
- osborne
- modelo iterativo
- modelos reuso
- caso open source

## Estudios de caso

- [LinkedIn](#linkedin)
- [Instagram](#instagram)
- [Figma](#figma)
- [khan academy](#khan-academy)
- [airbnb](#airbnb)
- [Reddit](#reddit)
- [Rompiste Reddit](#rompiste-reddit)
- [El fallo de Roblox](#el-fallo-de-roblox)

---

- ### [LinkedIn](https://www.linkedin.com/)

  en el año 2003, LinkedIn se fundó con el objetivo de mejorar las conecciones profesionales de las personas, La primera base de usuarios fue de 2700; al igual que muchos productos, la versión inicial tenia una sencilla arquitectura monolitica, que alojaba la logica de negocio, base de datos servicios web y componentes visuales, este monolito era conocido como Leo.

  Para LinkedIn, las conecciones entre los usuarios son su componente principal, por lo tanto desde las fases iniciales del proyecto, se apuntó a construir un servicio para gestionar la red de conexiones entre los usuarios. En terminos generales, consistia en un grafo donde cada nodo representa un miembro y era almacenado en memoria para maximizar el rendimiento; adicionalmente tenia el requerimiento de poder ser escalable de forma independiente del monolito Leo, este nuevo servicio se nombró Cloud, y se potenció gracias a otro servicio de busqueda [apache Lucene](https://lucene.apache.org/)

  Con el tiempo, el producto tomó fuerza, con lo cual Leo fue haciendose mas complejo; este requerimiento de escalabilidad fue resuelto de manera horizontal e implementando un balanceador de cargas para las diversas instancias desplegadas, sin embargo esta escalada afectó a Cloud, que no se encontraba equipado para asumir las nuevas cargas que infringía el sistema sobre la base de datos de usuarios.
  en un principio, se recurrió a una solución clasica, el escalado vertical; con mas capacidad en procesamiento y memoria. adicionalmente se comenzó a implementar una serie de replicas de las bases de datos, esta replicación necesitaba ser orquestada y para esto se desarrolló [databus](https://github.com/linkedin/databus) que es una herramienta de codigo abierto desde 2013.

  en este punto, comienza a acumularse deuda técnica, no es recomendable ni viable escalar indefinidamente, adicionalmente mientras crece la aplicación, la mantenibilidad se verá afectada, los monolitos más grandes tardan más en desplegarse y el rendimiento de la aplicación tiende a decaer.

  a medida que LinkedIn tenia más trafico, fallos en producción, dificultades para detectar fallos, recuperar la operabilidad y desplegar nuevas funcionalidades, sumado a un decremento en la disponibilidad; llevaron a un proceso de reingeniería en el software.

  progresivamente el equipo de ingeniería aisló varios servicios como las busquedas, comunicaciones, perfiles y grupos. Posteriormente las capas de presentación también fueron aisladas, como las funcionalidades de reclutamiento o perfiles publicos; al mismo tiempo algunas funcionalidades nuevas fueron estructuradas en forma de servicios independientes. en el año 2010 se estimaban mas de 150 servicios independientes y para 2015 más de 750.
  Estos servicios son libres de estado (Stateless), y se escalan de forma horizontal cuando es necesario, en conjunto con diversos tipos de balanceadores de carga; en esta instancia, se tienen datos de las capacidades de los servicios en terminos de carga y rendimiento. adicionalmente se implementaron diversas estrategias de monitoreo de rendimiento y disponibilidad.

  En cuanto a la gestión de datos, el equipo de ingeniería integró una memoria caché de varias capas, estó ayudó a la escalabilidad y reducir la carga sobre la base de datos.
  sin embargo, eventualmente se descartó esta estrategia, ya que se almacenaban datos de diversos dominios y mantener la validez de los datos y el grafo de solicitudes se estaba haciendo demasiado costoso en terminos de esfuerzo.  Por lo cual se adaptó una estrategia de caché más simple y cercana a la fuente de datos, permitiendo una escalabilidad horizontal, reduciendo la latencia y la carga cognitiva.

  eventualmente surgieron diversos requerimientos de flujos de datos, por ejemplo enviar una actualización de perfil al servicio de analítica y hacer logs de la operación, mantener una cola de mensajes para los diversos chats, entre otros.
  para abordar estos requerimients, se desarrolló [kafka](https://kafka.apache.org/), este actua como una gran autopista para alojar los flujos de datos y cuenta con un rendimiento y escalabilidad notables, una de sus mayores ventajas es la baja latencia de acceso a los datos, con estas nuevas capacidades, fue posible construir sistemas de alertas y monitoreo mas eficientes, ademas de herramientas de analitica en tiempo real y la capacidad de realizar seguimientos y visualizar el grafo de solicitudes.

  en la actualidad LinkedIn tiene iniciativas para asegurar una alta mantenibilidad en su producto:
  - Inversion: esta iniciativa surgió en 2011, la idea era poner en pausa el desarrollo de nuevas funcionalidades para centrar los esguerzos en mejorar las estrategias de despliegue, realizar refactoring, evaluar la productividad de desarrollo, considerar la infraestructura, entre otras actividades, que aumentan el conocimiento general del producto, incrementan la agilidad de los equipos y permiten desarrollar software de mejor calidad.
  - Superblocks: en escencia, es un grupo de servicios que realizan una serie de tareas en un solo acceso a la API del sistema. La iniciativa surgió con el llamado *call graph* o grafo de solicitudes; una solicitud simple como ver el perfil personal, requiere recolectar y organizar datos de diversos dominios que se alojan en diferentes servicios, todas estas solicitudes pueden ser complicadas de administrar y darles seguimiento. La idea es que equipos especificos se encarguen de administrar y gestionar bloques, logrando mantener los grafos de solicitudes optimizados.

- ### Instagram

- ### [Figma](https://www.figma.com/)

  Esta plataforma de diseño colaborativo, ha crecido aproximadamente un 200% desde el 2018, a la fecha cuenta con cerca de 3 millones de usuarios mensuales. La escalabilidad ha sido un reto constante para el equipo de ingeniería de este producto; la base de datos, representa un componente critico para esta plataforma, ya que de esta depende la funcionalidad del producto, en el componente de base de datos se gestiona metadata como los datos de autorización, información de los archivos compartidos, comentarios, cambios, entre otros.
  En 2020, Figma utilizaba una base de datos alojada en AWS para almacenar la mayoria de la metadata; esta solución cumplia con los requerimientos sin mayores inconvenientes, sin embargo, durante la pandemia del Covid-19, se vio un incremento de usuarios que no se tenia previsto; así durante los picos de uso, el uso de recursos de CPU se incrementaba por encima del 65%, esto causaba inestabilidad en la colaboración y latencias impredecibles en la base de datos.

  Aunque el pico de saturacion del sistema aún no era evidente, el equipo de infraestructura decidió proactivamente abordar los inconvenientes de escalabilidad, previendo posibles puntos de fallo, implementaron:
  - una actualización en la base de datos
  - replicación de base de datos
  - implementación de nuevas bases de datos
  - implementar [PgBouncer](https://www.pgbouncer.org/)

  Estas estrategias permitieron que el equipo pudiera preparar un plan para escalar el componente de datos.

  La primera fase, consistió en realizar una particion vertical de la base de datos; de forma simplificada, esto significa mover tablas a una nueva base de datos.
  Para identificar que tablas serian reubicadas, se consideraron dos factores:
  - Impacto: al mover la tabla, se separaría una porción significativa de la carga de trabajo
  - Aislamiento: la tabla no debía tener dependencias fuertes con otras tablas
  
  una vez identificadas las tablas, era necesario migrarlas sin afectar la disponibilidad de la información para los usuarios, es decir, no era viable "apagar" la plataforma para realizar la migración. Los requerimientos eran:
  - el impacto de la disponibilidad de los datos debe ser menos de 1 minuto
  - el proceso debe ser automatizado, para poder repetirlo facilmente
  - el proceso debe poderse deshacer
  
  dado que no fue posible encontrar un servicio o herramienta de software que cumpliera con estos requerimientos, Figma desarrolló su propia herramienta de software, este opera así:
  - prepara la aplicación para buscar en diferentes particiones de la base de datos
  - replica las tablas de la base de datos original en una nueva base de datos
  - pausa la actividad en la base de datos original
  - sincronizar bases de datos
  - redirigir el trafico a la nueva base de datos
  - reanudar la actividad.
  
  Adicionalmente, se usaron instancias replicadas de PgBouncer para mantener la consistencia del trafico y orquestar la concurrencia en los datos, ademas de permitirle al equipo detectar inconsistencias y corregirlas de ser necesario.

  con el tiempo, la cantidad de usuarios en Figma se incrementó, desde 2020 se estima que ha crecido aproximadamente cien veces; con este incremento la carga en las bases de datos también se incrementó, dada la naturaleza de las tablas en Figma, las cuales en ocasiones pueden tener varios terabytes de información y millones de filas, no es viable mantenerlas en una sola base de datos.
  El equipo de infraestructura notó dos potenciales puntos de fallo:
  - Postgres Vacumm: Postgresql cuenta con un proceso que se ejecuta en segundo plano, que consiste en recuperar el espacio que ocupan las filas obsoletas o eliminadas (similar a los procesos de garbage collection); si la base de datos no se aspira regularmente, eventualmente no podrá ejecutar más operaciones. Sin embargo, este proceso consume muchos recursos en las tablas grandes y puede causar problemas de rendimiento e incluso inoperabilidad.
  - IOPS Limit: Amazon RDS, tiene un limite de operaciones de entrada y salida (IO) por segundo, el cual evetualmente seria excedido por las tablas más exigentes de la aplicación.
  
  para abordar estas problematicas, se implementó una estrategia de fragmentación horizontal, que consiste en separar la base de datos principal en bases de datos más pequeñas y alojarlas en varios servidores.
  el equipo de Ingeniería exploró diversas alternativas tanto SQL como NoSQL y eventualmente optaron por construir una solución adaptada al modelo de partición vertical. algunas de las razones para tomar esta decision fueron:
  - menor carga cognitiva: al no necesitar adaptarse a otro tipo de modelo de datos y poder aprovechar la experiencia obtenida con el tiempo en RDS Postgres
  - control sobre la solución: al ser una herramienta internamente desarrollada, estaría hecha a la medida de los requerimientos del equipo y sus necesidades especificas.
  - posibilidad de descartar: en caso de que demasiados inconvenientes se presentaran o la solución no funcionara como debía, podian regresar a la versión anterior de la base de datos con relativa facilidad.
  
  algunas de las caracteristicas de la implementación de fragmentación horizontal, son:
  - Colocaciones para grupos de tablas relacionados (Colos): Figma introdujo el concepto de colos, que son simplemente un grupo de tablas relacionadas que comparten una identificación de fragmento o un fragmento fisico.
  
    para crear los colos, se seleccionaron algunas llaves de fragmentación, como id de usuario, id de archivo, id de organización, entre otros; casi cualquier tabla de la organización puede ser compartida usando alguna de las llaves, esta estrategia permite a los ingenieros interactuar con las tablas distribuidas a traves de una abstracción simple.

    las tablas en un colo, aceptan combinaciones cruzadas y transacciones en la misma llave de fragmento; la aplicación ya interactuaba con la base de datos, de una forma similar, lo cual redujo al minimo la cantida de esfuerzo para hacer que las tablas pudieran ser fragmentadas y para adaptar la aplicación.

  - Fragmentación logica y fisica: se separaron las fragmentaciones logicas en la capa de aplicación de las fragmentaciones fisicas en la capa de datos
  esta separación permitió desacoplar dos partes de la migración e implementarlas de manera independiente; la fragmentación logica, implica crear multiples vistas por tabla, cada una correspondiente a un fragmento especifico. todas las operaciones de lectura y escritura se ejecutan meidante esta vista, haciendo que la tabla parezca estar fragmentada horizontalmente aún con los datos fisicamente alojados en una base de datos unica.

    Así fue posible realizar fragmentaciones de manera mas segura, faciles de deshacer y con menos riesgo, antes de ejecutar las fragmentaciones fisicas, que son mas riesgoas y complejas.

  - DBProxy: este servicio, se ubica en medio de la aplicación y el banco de conexiones, consta de tres componentes:
    - un traductor de consultas, que lee el SQL enviado por la aplicación y lo transformas en arbol de sintaxis abstracto (AST)
    - un planeador logico, que traduce el AST extrae la consulta y el id lógico del fragmento
    - un planeador fisico, que toma el id lógico y lo mapea a la base de datos fisica, para luego reescribir la consula a ejecutar en la base de datos correspondiente.
  
  en septiembre de 2023 Figma desplegó la primera versión del proyecto de fragmentación horizontal, que resultó en un exito rotundo, con un impacto minimo en la operabilidad del sistema; además de que no se observaron regresiones ni afectaciones de rendimiento luego de la ejecución de la fragmentación.
  El objetivo final de Figma es fragmentar todas las tablas de su base de datos; esto representa una escalabilidad casi infinita.
  
- ### khan academy

- ### airbnb

- ### reddit

- ### "rompiste reddit"

- ### el fallo de roblox

## Fuentes

este manual se ha construido con una variedad de publicaciones cientificas, blogs y articulos de la web, esta es la lista de las fuentes consultadas en el dia 05/05/2024
****

-

.
.

## Contacto

Información de contacto para soporte.
