
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
