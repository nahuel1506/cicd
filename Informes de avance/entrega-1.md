# Entrega 1

## Definición de marco de gestión basado en Kanban. Roles y ceremonias. 

Para definir los roles y ceremonias del marco de gestión, se tomaron algunos elementos del marco de gestión SCRUM. Como lo indica la letra, todos los miembros del equipo tomarán el rol de desarrolladores y testers en todas las etapas. Por otro lado, se definió un Product Owner para cada entrega, quien definirá y priorizará las tareas a realizar, y se asegurará que las tareas realizadas estén alineadas con lo solicitado por el usuario. En esta primera entrega, este rol lo asumirá Sofía. 

Además, el equipo definió un rol de facilitador o líder de flujo. Este rol se encarga de que el equipo pueda avanzar sin problemas, promoviendo un flujo de trabajo continuo. Las responsabilidades principales del facilitador es detectar cuellos de botella, fomentar la comunicación y organización del equipo y mantener actualizado el tablero visibilizando el estado real de las tareas. 

Se definieron las siguientes ceremonias:
-	Reunión semanal: Elegir tareas a hacer, asignar responsables y ordenar prioridades. 
-	Revisión de entrega: Al finalizar cada entrega validar con el PO los avances realizados. 
-	Retrospectiva: Al final de cada entrega reflexionar como equipo, para ver qué funcionó, qué no y qué mejorar.
-	Reuniones esporádicas: En caso de ser necesario, ya sea por bloqueos, dudas o algún problema que surja, cualquier integrante del equipo puede solicitar realizar una reunión con el resto del equipo. 

## Definición de un primer proceso de ingeniería.

Como se mencionó previamente, el marco de gestión a utilizar es Kanban. En principio, se decidió comenzar con un tablero simple, con tres columnas: _ToDo_, _Doing_ y _Done_. En la columna Backlog se ubicarán todas las tareas a realizar, priorizadas por el PO en cada etapa. En la columna Doing se ubicarán las tareas que están en proceso, y en la columna _Done_ se ubicarán las tareas que fueron finalizadas.  Este tablero será gestionado desde GitHub Proyects y las columnas se irán modificando a medida que el proyecto avance. 

Para que una tarea pueda avanzar de una columna a otra, se definieron los siguientes criterios:
-	Backlog a Doing: La tarea debe estar asignada a un responsable y el PO debe validar que la tarea esté lista para comenzar.
-	Doing a Done: La tarea debe estar finalizada y el PO debe validar que la tarea cumpla con los criterios de aceptación definidos.

Todos los integrantes del equipo contribuirán a la creación de tareas, y estas se ubicarán en el tablero a medida que se analice el sistema y se descubran nuevas oportunidades de mejora o errores. A cada tarea se le asignará una prioridad (alta, media o baja) y un responsable, y dependiendo de la necesidad, se comenzará como un borrador (draft) o como un issue. Los issues se podrán crear a partir de plantillas si corresponde, o de cero siguiendo un formato estructurado. Además, para facilitar el flujo de trabajo, no se asignarán tipos a las tareas, y solo se le asignará como máximo una tarea a cada integrante del equipo por vez.

En cuanto a los pull requests (PR), estos serán creados cada vez que los integrantes del equipo tengan cambios listos para ser integrados al código base. El PR deberá estar asociado a un issue o tarea especifíca, y deberá ser revisado por al menos un integrante del equipo antes de realizarse el merge. Además, los PR deberán superar los controles de calidad, que incluyen pruebas unitarias y de integración, y revisiones de código.

## Configuración del repositorio en GitHub: archivos y directorios, estrategia de branching, estándares de nomenclatura. 

Para mantener un trabajo ordenado y colaborativo, se definió utilizar como base la estructura de carpetas proporcionada por los docentes. El repositorio está organizado de la siguiente manera:

**Código**: contiene los dos proyectos principales que conforman la aplicación, es decir, el backend y el frontend.

**Documentación**: incluye los informes entregados por los autores originales del proyecto, así como los requerimientos iniciales definidos.

**Base de Datos**: almacena los scripts necesarios para la creación de la base de datos y sus datos de prueba.

**Exportations**: contiene los archivos generados al exportar datos desde la aplicación.

**Informes de avance**: directorio creado para colocar la documentación correspondiente a cada una de las entregas del equipo.

En cuanto a la estrategia de branching, para esta primera entrega no se implementó una metodología compleja, ya que el trabajo se centró principalmente en tareas de documentación. Por lo tanto, se creó una rama entrega-1, que será mergeada a main al final de la iteración.

Para las siguientes iteraciones se adoptará la estrategia Git Flow, que implica la creación de una rama develop como base de desarrollo, desde la cual se derivarán ramas específicas para nuevas funcionalidades (feature), correcciones (hotfix) y otras necesidades del proyecto.

Respecto a los estándares de nomenclatura, se acordó el uso de nombres descriptivos y consistentes tanto para las ramas como para los commits. Las ramas seguirán el formato <tipo>/<descripción-corta>, por ejemplo: feature/login-usuario o hotfix/fix-error-login. En cuanto a los mensajes de commit, se busca que sean breves pero claros, utilizando verbos en infinitivo.

## Análisis de deuda técnica y gestión de la calidad: definición de un modelo de calidad y un análisis de deuda técnica en base a ese modelo de calidad. 

### Modelo de Calidad

El sistema desarrollado por la startup tiene como objetivo principal facilitar la búsqueda y adquisición de medicamentos, así como la gestión interna de farmacias, con usuarios que poseen distintos perfiles. Por esta razón, se decidió adoptar un modelo de calidad centrado en los siguientes atributos, derivados de las normas ISO/IEC 25010:

**Capacidad de interacción y/o usabilidad**

El sistema será utilizado por usuarios no técnicos, como empleados y dueños de farmacia, y también por usuarios anónimos que acceden desde la web. Por lo tanto, la interfaz debe ser intuitiva, clara y fácil de navegar. Para garantizar esto, se busca que la aplicación cumpla criterios como:

- Operabilidad: es importante que el usuario sea capaz de acceder y realizar las distintas operaciones que la aplicación ofrece de manera fácil. Por ejemplo, que exista un botón de login en la página de inicio, y la posibilidad de volver a la página anterior, entre otros.

- Aprendabilidad y protección contra errores: para esto, es necesario que el sistema tenga flujos de interacción consistentes, con validaciones claras y mensajes de error comprensibles para el usuario.

- Inclusividad: el sistema debe ser accesible para personas con discapacidades, por lo que se deben seguir las pautas de accesibilidad web (WCAG). Para ello, se utilizarán herramientas como WAVE y Lighthouse para verificar que la aplicación cumpla con los estándares de accesibilidad.

**Seguridad**

Se busca que el sistema tenga un control de acceso seguro en el que solo los usuarios autenticados y autorizados pueden realizar ciertas acciones según su rol (ej.: solo empleados pueden dar de alta medicamentos). También, es importante que se prevenga el acceso no autorizado a funcionalidades sensibles mediante mecanismos de autenticación y autorización.

### Análisis de la deuda técnica



## Definición de issues y clasificación.

Se decidió clasificar los issues siguiendo los siguientes criterios: 

- **Prioridad**: Determina el nivel de urgencia con el que debe ser corregido el issue. Alta, Media, Baja.
- **Tipo**: Identifica la naturaleza del issue. Se utilizará Feature cuando se trate de una nueva funcionalidad o mejora del sistema y Bug si es un error o comportamiento incorrecto. 
- **Responsable**: Indica el área principal a la que corresponde resolver el issue. Las categorías que se definieron inicialmente son: Base de datos, Backend, Frontend, Testing. 

## Registro de actividades realizadas.
El registro de actividades realizadas se encuentra en el archivo [registro-horas.xlsx](./registro-horas.xlsx).

## Mejoras en la calidad y evidencia de revisión con el PO (uno de los integrantes debe tomar el rol en cada etapa)

Dado que en esta primera entrega no se realizaron modificaciones en el código, no se puede afirmar que existan mejoras directas en la calidad del sistema. No obstante, la definición del modelo de calidad y el análisis de deuda técnica permitieron identificar áreas de mejora a desarrollar en las próximas entregas, lo que constituye una mejora indirecta en la calidad del sistema.

Por otro lado, en todas las reuniones realizadas estuvo presente el PO, Sofía, que validó los avances y estuvo de acuerdo con todos los puntos definidos anteriormente. 

![Evidencia de revisión con el PO](evidenciaPO.png)

## Retrospectiva y acciones de mejora
