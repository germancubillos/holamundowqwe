<table>
   <thead>
      <tr>
         <th rowspan=2>FIABILIDAD</th>
         <td colspan=2 align="left">Capacidad de un sistema o componente para desempeñar  las funciones especificadas, cuando se usa bajo unas condiciones y periodo de tiempo determinados.</td>
      </tr>
      <tr>
         <th>DISPONIBILIDAD</th>
         <td align="left">Capacidad del sistema o componente de estar operativo y accesible para su uso cuando se requiere</td>
      </tr>
   </thead>
   <tbody>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Cuanto tiempo esperamos soportar ante la indisponibildiad de un proveedor?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿Que estrategia se realizará para garantizar la dispoinilidad de .999?</td>
      </tr>
      <tr>
         <td align="center">3</td>
         <td colspan=2>¿Que estrategia se realizará para cumplir el tiempo medio de reparacion del sistema (5 minutos) ante una caida?</td>
      </tr>
      <tr>
         <td align="center">4</td>
         <td colspan=2>¿Que estrategia se realizará si el sistema del proveedor no se encuentra disponible?</td>
      </tr>
      <tr>
         <td align="center">5</td>
         <td colspan=2>¿Como se asegura la disponibildiad de los datos?</td>
      </tr>
      <tr>
         <td align="center">6</td>
         <td colspan=2>¿Que tipo de redudancia se utilizará en la arquitectura y cómo se seleccion que componentes deben ser redundantes?</td>
      </tr>
      <tr>
         <td></td>
         <td><b>TOLERANCIA A FALLOS<b></td>
         <td>Capacidad del sistema o componente para operar según lo previsto en presencia de fallos hardware o software.</td>
      </tr>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Como se realizará la identifiacion de los fallos?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿Como se comportaria el sistema ante una falla masiva?</td>
      </tr>
      <tr>
         <td align="center">3</td>
         <td colspan=2>¿Como se comportaria el sistema ante una falla de los sistemas del proveedor?</td>
      </tr>
      <tr>
         <td align="center">4</td>
         <td colspan=2>¿Como se comportaria el sistema ante una falla de la capa de red?</td>
      </tr>
      <tr>
         <td align="center">5</td>
         <td colspan=2>¿Como se comportaria el sistema ante una falla en la capacidad de los servidores?</td>
      </tr>
      <tr>
         <td align="center">6</td>
         <td colspan=2>¿Como se comportaria el sistema ante la caida de un componente?</td>
      </tr>
      <tr>
         <th rowspan=2>PORTABILIDAD</th>
         <td colspan=2 align="left">Capacidad del producto o componente de ser transferido de forma efectiva y eficiente de un entorno hardware, software, operacional o de utilización a otro.</td>
      </tr>
      <tr>
         <th>ADAPTABILIDAD</th>
         <td align="left">Capacidad del producto que le permite ser adaptado de forma efectiva y eficiente a diferentes entornos determinados de hardware, software, operacionales o de uso.</td>
      </tr>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Cuales protocolos utilizaremos para integrarnos con los proveedores?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿Qué estandares de comunicación utilizaremos internamente?</td>
      </tr>
      <tr>
         <td align="center">3</td>
         <td colspan=2>¿Cual es la mejor estrategia para realizar una comunicacion entre los componentes de manera adaptable?</td>
      </tr>
      <tr>
         <td align="center">4</td>
         <td colspan=2>¿A que componentes somos adaptables y a que componentes no somos adaptables?</td>
      </tr>
      <tr>
         <td align="center">5</td>
         <td colspan=2>¿Que esfuerzo requerira adaptar un nuevo componente sin encesidad de cambiar la definicion de la arquitectura?</td>
      </tr>
      <tr>
         <td align="center">6</td>
         <td colspan=2>¿Si un proveedor cambiara su estandar de integracion que tanto afectara nuestra arquitectura?</td>
      </tr>
      <tr>
         <td></td>
         <th>CONFIGURABILIDAD</th>
         <td align="left">capacidad de cambiar los parámetros operativos de un sistema sin escribir código.</td>
      </tr>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Que componentes y procesos se deben/pueden/no deben configirarse?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿Cual es el alcance de las configuraciones sobre la definicion de la arquitectura?</td>
      </tr>
      <tr>
         <td align="center">3</td>
         <td colspan=2>¿Cómo se garantiza que los usuarios adecuados puedan hacer configuraciones sensibles del sistema? </td>
      </tr>
      <tr>
         <td align="center">4</td>
         <td colspan=2>¿Como se realizaran las configuraciones?</td>
      </tr>
      <tr>
         <td align="center">5</td>
         <td colspan=2>¿Como se asegurara que al ralizar una configuracion no se afectara el sistema?</td>
      </tr>
      <tr>
         <td align="center">6</td>
         <td colspan=2>¿Se pueden hacer cambios sin necesidad de reiniciar el sistema?</td>
      </tr>
      <tr>
         <td align="center">7</td>
         <td colspan=2>¿Como se asegura que el realizar cambios en la configuracion en cualqueir horario no impacte la operación del sistema y del negocio?</td>
      </tr>
      <tr>
         <td align="center">8</td>
         <td colspan=2>¿Que configuración se realizará en la infraestrcutura para operar ante la indisponibildiad de un servidor/componente?</td>
      </tr>
      <tr>
         <th rowspan=2>MANTENIBILIDAD</th>
         <td colspan=2 align="left">Esta característica representa la capacidad del producto software para ser modificado efectiva y eficientemente, debido a necesidades evolutivas, correctivas o perfectivas.</td>
      </tr>
      <tr>
         <th>MODIFICABILIDAD</th>
         <td align="left">Capacidad del producto que permite que sea modificado de forma efectiva y eficiente sin introducir defectos o degradar el desempeño.</td>
      </tr>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Que impacto tiene el sistema ante el cambio de uno de sus componentes?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿ante el cambio de un componente del sistema como se garantiza su interiorabildiad?</td>
      </tr>
      <tr>
         <td align="center">3</td>
         <td colspan=2>¿Como se garantizara que el cambio del componente actualice/no impacte los respositorios de datos del sistema?</td>
      </tr>
      <tr>
         <td align="center">4</td>
         <td colspan=2>¿Como se asegura que el realizar cambios en los componentes en cualqueir horario no impacte la operación del sistema y del negocio?</td>
      </tr>
      <tr>
         <td align="center">5</td>
         <td colspan=2>Si esta arquitectura incluye un repositorio de datos, ¿cuántas ubicaciones distintas en la arquitectura tienen conocimiento directo de sus tipos de datos y diseño?</td>
      </tr>
      <tr>
         <td align="center">6</td>
         <td colspan=2>Si cambia un tipo comando, artefacto o un mensajes, ¿cuántas partes de la arquitectura se ven afectadas?</td>
      </tr>
      <tr>
         <td></td>
         <th>MODULARIDAD</th>
         <td align="left">Capacidad de un sistema o programa de ordenador (compuesto de componentes discretos) que permite que un cambio en un componente tenga un impacto mínimo en los demás.</td>
      </tr>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Ante la necesidad del cambio de un componente cuantas funcinalidades/artefactos de negocio/tecnicas se estan afectando?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿Que estrategia se realizará para asegurar que un modulo no realice mas de dos respondabilidades?</td>
      </tr>
      <tr>
         <td align="center">3</td>
         <td colspan=2>¿que estrategia se realizara para asegurar la conhesión de los componentes del sistema?</td>
      </tr>
      <tr>
         <td align="center">4</td>
         <td colspan=2>¿Como se asegura que el cambio en un componente del sistema no afecte a operabilidad del mismo?</td>
      </tr>
      <tr>
         <th rowspan=2>EFICIENCIA DE DESEMPEÑO</th>
         <td colspan=2 align="left">Esta característica representa el desempeño relativo a la cantidad de recursos utilizados bajo determinadas condiciones. </td>
      </tr>
      <tr>
         <th>COMPORTAMIENTO TEMPORAL</th>
         <td align="left">Los tiempos de respuesta y procesamiento y los ratios de throughput de un sistema cuando lleva a cabo sus funciones bajo condiciones determinadas en relación con un banco de pruebas (benchmark) establecido.</td>
      </tr>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Cuál es el impacto en el rendimiento en la integracion de un proveedor delgado frente a uno pesado?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿Cual es la estrategia que garantizará la distribucion y el equilibrio de la carga de hits en el sistema?</td>
      </tr>
      <tr>
         <td align="center">3</td>
         <td colspan=2>Si varios mensajes de eventos llegan a una cola de mensajes compartida, ¿cuál es la estrategia de priorización en el procesamiento/atención? </td>
      </tr>
      <tr>
         <td></td>
         <th>UTILIZACIÓN DE RECURSOS</th>
         <td align="left">Las cantidades y tipos de recursos utilizados cuando el software lleva a cabo su función bajo condiciones determinadas.</td>
      </tr>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Que componentes/artefactos utilizan un protocolo de comunicacion sincrónico o asincrónico?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿Qué información se debe almacenar en caché o cual se debe persistir?</td>
      </tr>
      <tr>
         <td align="center">3</td>
         <td colspan=2>¿Si hay varios procesos que compiten por un recurso compartido, ¿cómo se asignan las prioridades a estos procesos y al proceso que controla el recurso?</td>
      </tr>
      <tr>
         <td align="center">4</td>
         <td colspan=2>¿Cuál es la ubicación física del hardware y su conectividad?</td>
      </tr>
      <tr>
         <td></td>
         <th>CAPACIDAD</th>
         <td align="left">Grado en que los límites máximos de un parámetro de un producto o sistema software cumplen con los requisitos.</td>
      </tr>
      <tr>
         <td align="center">1</td>
         <td colspan=2>¿Cuáles deben ser las características del ancho de banda de la red de comunicación para garantizar la interoperabilidad efectiva del sistema?</td>
      </tr>
      <tr>
         <td align="center">2</td>
         <td colspan=2>¿Cómo caracterizamos la carga de clientes? (por ejemplo, cuántas sesiones concurrentes, cuántos usuarios)?</td>
      </tr>
   </tbody>
</table>
