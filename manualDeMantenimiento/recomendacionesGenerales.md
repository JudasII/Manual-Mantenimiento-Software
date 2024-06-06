# Recomendaciones Generales

Independientemente del tipo de mantenimiento a realizar, hay varios factores a tener en cuenta para el desarrollo de las labores de mantenimiento.

Considera siempre las herramientas que tengas a mano, aquí algunas:

- Herramientas de depuración: Estas herramientas ayudan a identificar la causa de los errores en el software. La mayoría de los IDEs tienen integradas herramientas para las labores de depuración. Es muy importante conocer estas herramientas y tomarles máximo provecho.
- Herramientas de pruebas: Estas herramientas ayudan a garantizar que el software funcione correctamente. Es crítico mantener el software al tanto en el plan de pruebas. Siempre realiza pruebas a tu software además de las pruebas unitarias y de integración. Considera:
  - Pruebas de estrés y rendimiento
  - Pruebas de seguridad
  - Pruebas de usabilidad y aceptación
  - Pruebas funcionales
  - Pruebas de humo
  - Pruebas de extremo a extremo

## <mark> Nota: Recuerda que las pruebas ayudan a incrementar la calidad y fiabilidad del software</mark>

- Herramientas de monitoreo: Estas herramientas ayudan a rastrear el rendimiento del software y a identificar posibles problemas.
- Herramientas de gestión de configuración: Estas herramientas ayudan a realizar un seguimiento de los cambios en el software. Independientemente de si las labores de mantenimiento son realizadas por una o varias personas, es importante mantener un control de versiones óptimo y organizado. Esto con el fin de evitar errores de versionamiento y despliegue, además de permitir una transición entre versiones muy cómoda y segura.
- Herramientas de documentación: Estas herramientas ayudan a crear y mantener la documentación del software. Es imperativo mantener un software bien documentado.

No solamente las herramientas de control de versiones deben ser consideradas, es importante notar que las herramientas de integración continua son vitales para el software moderno y por ende vitales para las labores de mantenimiento de este.

---

## 1. Considere patrones de diseño y arquitectura

Al inicio del proyecto de software, se realizaron una serie de sesiones de diseño donde, considerando los diversos requerimientos del producto que se iba a construir, se tomaron decisiones de diseño y arquitectura. Es posible que a medida que el producto haya madurado, se hayan tomado nuevas decisiones y modificado el diseño original. De cualquier manera, busque los diseños, arquitecturas de referencia, diagramas, entre otros documentos de diseño que puedan ser útiles y estúdielos concienzudamente.

Es fundamental que el ingeniero de software comprenda a fondo los patrones de diseño y arquitectura utilizados en la construcción de la aplicación que se está manteniendo. Esto le permitirá:

- Comprender la estructura y organización del código: Al conocer los patrones de diseño, podrá entender cómo se han organizado los componentes del software y cómo interactúan entre sí. Esto facilita la identificación de las áreas que necesitan ser modificadas o actualizadas.
- Tomar decisiones informadas sobre las modificaciones: La comprensión de la arquitectura del software permite tomar decisiones informadas sobre cómo realizar las modificaciones sin afectar negativamente el funcionamiento general de la aplicación.
- Evitar introducir nuevos errores: Al seguir los patrones de diseño adecuados, se reduce el riesgo de introducir nuevos errores en el código durante el proceso de mantenimiento.
- Mantener la coherencia del código: Al utilizar patrones de diseño consistentes, se mantiene la coherencia del código y se facilita su comprensión y mantenimiento a largo plazo.
Notas sobre [arquitectura y diseño](./patrones.md)

## 2. Evalúe el impacto

Seguramente el software que está manteniendo pertenece a una empresa u organización; es muy importante que de manera colectiva y/o individual, según el caso, se evalúe cuidadosamente el impacto que las modificaciones tendrán en la aplicación. Esto implica considerar:

- **Funcionalidad**: ¿Las modificaciones afectarán la funcionalidad existente de la aplicación?
- **Rendimiento**: ¿Las modificaciones afectarán el rendimiento de la aplicación?
- **Seguridad**: ¿Las modificaciones introducirán nuevas vulnerabilidades de seguridad?
- **Usabilidad**: ¿Las modificaciones afectarán la usabilidad de la aplicación para los usuarios?
- **Compatibilidad**: ¿Las modificaciones afectarán la compatibilidad de la aplicación con otros sistemas o plataformas?

## 3. Considere el plan de pruebas

Una vez realizadas las modificaciones, es crucial realizar pruebas exhaustivas y diversas para garantizar que la aplicación funciona correctamente y que no se han introducido nuevos errores. Las pruebas deben cubrir como mínimo:

- Casos de uso: Todos los casos de uso de la aplicación deben probarse para garantizar que funcionan correctamente.
- Regresión: Se deben realizar pruebas de regresión para garantizar que las modificaciones no han afectado negativamente la funcionalidad existente.
- Rendimiento: Se deben realizar pruebas de rendimiento para garantizar que la aplicación sigue funcionando con el rendimiento esperado.
- Seguridad: Se deben realizar pruebas de seguridad para garantizar que las modificaciones no han introducido nuevas vulnerabilidades.

Es importante mencionar que la mayoría de los proyectos de software tienen un plan de pruebas, que suele ser definido en las etapas iniciales del ciclo de vida (planificación y diseño) y posteriormente ejecutado en la etapa de pruebas. Generalmente, los planes de pruebas quedan documentados al igual que la arquitectura y el diseño. Por lo tanto, es importante buscar tener acceso a estos documentos, para cumplir con las pruebas que sugiera el diseño del proyecto de software. De igual manera, si el plan de pruebas por alguna razón ya no es pertinente a los nuevos desarrollos en el mantenimiento del producto, entonces es imperativo definir un nuevo plan de pruebas, donde se contemplen, según las necesidades, estándares y demás lineamientos pertinentes a la naturaleza del proyecto de software, las pruebas que se realizarán en el ciclo de mantenimiento.

## 4. Documente y comunique

La documentación es sumamente valiosa para poder transmitir el conocimiento dentro de las organizaciones a cargo del mantenimiento y desarrollo de los productos de software. Es fundamental mantener una comunicación fluida y transparente con todas las partes interesadas durante el proceso de mantenimiento de software. Esto incluye:

- Usuarios: Informar a los usuarios sobre las próximas modificaciones y el tiempo de inactividad potencial.
- Equipo de desarrollo: Colaborar con el equipo de desarrollo original para comprender mejor el código y la arquitectura de la aplicación.
- Gerentes: Mantener a los gerentes informados sobre el progreso del mantenimiento y cualquier problema potencial.

Además, es importante mantener la documentación del software actualizada para reflejar los cambios realizados durante el mantenimiento. Esto incluye:

- Documentación del código: Actualizar la documentación del código para reflejar las modificaciones realizadas.
- Documentación de usuario: Actualizar la documentación del usuario para reflejar los cambios en la funcionalidad o la interfaz de usuario.
- Documentación de la arquitectura: Actualizar la documentación de la arquitectura para reflejar los cambios en la arquitectura del software.

Es muy importante mantener documentos relacionados con las labores de mantenimiento del software. El conocimiento y las experiencias obtenidas al realizar mantenimiento a aplicaciones de software son enriquecedores y proveen al ingeniero de una perspicacia y habilidad que solamente se obtienen al realizar labores de mantenimiento. El problema radica en que esta caja de herramientas se queda en la cabeza del ingeniero y solo le será útil a este, en lugar de a su equipo, su organización o el resto del mundo. Es por esto que siempre las labores de mantenimiento deben ser documentadas, no solo a nivel técnico, lo cual también es de suma importancia, sino que, en la medida de lo posible, compartidas, en blogs, foros, o iniciativas abiertas, como este manual.

### <mark> **NOTA IMPORTANTE SOBRE LA PRIVACIDAD Y SEGURIDAD DE LA INFORMACIÓN:**

Es fundamental cumplir rigurosamente con los lineamientos de privacidad de las organizaciones en las que estamos o hemos estado involucrados. En caso de que deseen contribuir con información que pueda considerarse privada o sensible para el presente manual, es imperativo consultar con el departamento encargado de la seguridad de la información en su respectiva organización antes de realizar cualquier publicación. 

Asimismo, es crucial prestar especial atención a la seguridad de la información en todas las iniciativas abiertas, como es el caso de este manual. Cualquier dato que se comparta en internet debe ser cuidadosamente evaluado para garantizar la protección adecuada de la privacidad y la integridad de la información de la organización y de sus usuarios.</mark>
