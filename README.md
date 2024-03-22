# Lab1Robotica_JD
Integrantes: David Santiago Rodriguez Almanza / Juan Carlos Naranjo Jaramillo.
## Introducción

En un contexto empresarial altamente competitivo y en constante evolución, la publicidad y el marketing han surgido como elementos esenciales para destacar en el mercado y consolidar la identidad de marca. Sin embargo, con el avance imparable hacia la robotización de las industrias, surge la pregunta crucial: ¿Es viable llevar a cabo estos procesos de manera eficiente mediante la implementación de robots industriales? Esta interrogante plantea un debate sobre la intersección entre la tecnología, la publicidad y la producción industrial, y cómo estas fuerzas convergen para moldear el panorama empresarial contemporáneo.

En base a lo anterior, como parte de una campaña publicitaria se propone exaltar la identidad de marca haciendo uso de robots industriales los cuales deben dibujar el logotipo de una reconocida marca sobre varias superficies en base a ciertos parámetros de funcionamiento que debe tener el robot.
## Procedimiento
### Diseño de la herramienta
En primer lugar se requería diseñar un gripper que fuera capaz de sostener un marcador firmemente para seguir de manera correcta las trayectorias programadas dibujando el logotipo de adidas, la marca elegida por nosotros.

El problema de diseñar el gripper era un problema muy abierto, por lo cual se decidió tomar inspiración del software robotStudio, más específicamente de la herramienta MyTool utilizada en varios de los tutoriales que la empresa ABB y posteriormente los profesores de la Universidad Nacional de Colombia pusieron a nuestra disposición, esto debido a que esta herramienta se utiliza como un entrenamiento para seguir trayectorias, justamente el trabajo que debe hacer el robot.
<div style="text-align: center;">
  <img width="300" alt="image" content="width=device-width, initial-scale=1.0" src="https://github.com/davidSRA/Lab1Robotica_JD/assets/95663629/a56113d8-924f-4176-bf59-bc94ebdf0328"><br>
</div>


Se adoptó la geometría propuesta en el software y se adecuó para nuestros propósitos, un requerimiento que se debía tener era la sujeción del marcador, ya que la posición óptima para escribir es con el marcador completamente recto, es decir, si no se tenía un buen sistema de sujeción, el marcador terminaría por caer. La solución propuesta e implementada para este problema fue utilizar un gripper construido en dos partes, la primer parte que denominaremos el cuerpo, era la pieza que se encargaba de almacenar el marcador por lo cual se restringía el tamaño mínimo que debía tener la pieza y además tenía como función acoplar la herramienta el robot, la segunda pieza la denominaremos la tapa, la cual se introducía en la parte superior del cuerpo y mediante un roscado tanto en la tapa como en cuerpo, se juntaban para formar en conjunto el gripper, cabe destacar que la tapa tenía un pequeño agujero para permitir que la punta del marcador saliera.

Sin embargo las condiciones del laboratorio no son perfectas y existía la posibilidad de tener que lidiar con ciertas irregularidades en el nivel de la superficie, por lo que además se propuso que la herramienta tuviera un amortiguador para permitir una variación pequeña en la altura de la herramienta, tal variación debería responder a los cambios de nivel que puedan existir en el laboratorio, la solución propuesta fue colocar un resorte dulce tal que aprisionara el marcador contra la tapa y además permitiera un rango elástico en el cuál el marcador pudiera introducirse un poco más hacia el cuerpo del gripper.


A continuación se presenta un modelo 3D del gripper diseñado en función a los criterios de diseño seleccionados (Sujeción del marcador y variación de la longitud):<br>
<div style="text-align: center;">
<img width="363" alt="image" src="https://github.com/davidSRA/Lab1Robotica_JD/assets/95663629/0d863200-19ed-48c5-8464-c6c917e9801b"><br>
<img width="359" alt="image" src="https://github.com/davidSRA/Lab1Robotica_JD/assets/95663629/3e68d28a-ddf1-45d4-9d03-80d0e94f4f18"><br>
<img width="273" alt="image" src="https://github.com/davidSRA/Lab1Robotica_JD/assets/95663629/5e54d542-e61e-4449-aa3d-d890483815c8"><br>
<img width="365" alt="image" src="https://github.com/davidSRA/Lab1Robotica_JD/assets/95663629/7d5d24f7-ace1-443d-be3d-ac72fc84bc07">

</div>

### Configuración en RobotStudio



