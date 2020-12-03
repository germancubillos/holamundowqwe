
| **Escenario** | El tiempo de carga de la página principal y el catálogo no debe ser superior a 1 segundo para los usuarios que acceden al sitio web o a la app mediante una conexión móvil 4G. | 
| --- | --- |
| **Atributo de Calidad** | Desempeño - Actuación |
| **Ambiente** | Operación Normal, Operación Modo emergente, Operación con Sobrecarga. |
| **Fuente del Estimulo** | Puede ser un usuario final o administrador |
| **Estimulo** | El usuario ingresa al home de toures balón y realiza la consulta del catálogo de productos y servicios, realizando transacciones que están centradas en la búsqueda. |
| **Respuesta** | En condiciones de funcionamiento normal con 4 usuarios concurrentes usan el sistema, con tiempos de respuesta dentro de niveles esperados, en condiciones de sobrecarga con 10 usuarios concurrente los tiempos deben estar sobre los aceptados. |
| **Medición Respuesta** | Se debe cargar la pantalla del home y del catálogo en un tiempo menor a 1000 milisegundos: 800 milisegundos – Esperado; 1000 - 1200 milisegundos – Aceptable; > 1200 - No tolerable |
| **Decisiones de Arquitectura** | Para garantizar el desempeño solicitado se decide desplegar los servicios en una infraestructura en la nube, que permiten escalar a nivel horizontal máquinas y a nivel vertical capacidad de CPU, Memoria y Disco. Se plantea sobre una arquitectura de microservicios para tener definidas las responsabilidades de la carga y poder soportar grandes masas de clientes en épocas especiales como Black Friday y otros de mayor cantidad de consumos. |
| **Puntos de Sensibilidad** | Un mal diseño e implementación en los componentes y artefactos podría incrementar los recursos usados y a la vez el auto escalado no sería el óptimo. |
| **Trade-Off** | La imagen de la empresa con respecto a la disponibilidad y capacidad de respuesta será percibida por el usuario como optima ya que estaremos respondiendo en tiempos menores a 1 segundo, sin embargo, esto traduce es posible incremento en el OPEX |
| **Riesgos** | Se pueden evidenciar cobros variantes y no fijos en los servicios de tecnología que ofrece el servidor de nube; La empresa podrá crecer o decrecer su capacidad de tecnología acorde a las necesidades de negocio. |


| **Escenario** |	En operación de alta carga se debe soportar hasta 24 usuarios concurrentes por segundo, equivalentes a 240 transacciones por segundo. |
| --- | --- |
| **Atributo de Calidad** |	Desempeño - Rendimiento |
| **Ambiente** |	Operación con Sobrecarga. |
| **Estimulo** |	El usuario ingresa al home de toures balón y realiza la consulta y/o compra de un evento del catálogo, realizando transacciones que están centradas en la búsqueda y adquisición. |
| **Respuesta** |	En condiciones de sobrecarga con 24 usuarios concurrentes usando el sistema, se deben evidenciar tiempos de respuesta dentro de niveles aceptados
| **Medición Respuesta** |	Se debe cargar la pantalla del home y del catálogo en un tiempo menor a 1000 milisegundos: 1000 milisegundos – Esperado; 1200 - 1600 milisegundos – Aceptable; > 1600 milisegundos  - No tolerable |
| **Decisiones de Arquitectura** |	Para garantizar este desempeño se decide desplegar los servicios en una infraestructura en la nube, los cuales permiten realizar un escalamiento horizontal y vertical de los recursos. En los servicios o artefactos donde la persistencia de datos es alta se priorizará la gestión sobre base de datos en memoria/cache. Los servicios no deben tener una orquestación de más de 3 servicios para cumplir su funcionalidad.  Con el fin de soportar la carga de usuarios se opta por contenido almacenado en la nube y gestionado por el proveedor de nube pública. |
| **Puntos de Sensibilidad** |	Una mala implementación en los servicios podría incrementar el uso de recursos y también el proceso de auto escalado. |
| **Trade-Off** |	La imagen de la empresa con respecto a la disponibilidad y capacidad de respuesta será percibida por el usuario como optima ya que estaremos respondiendo en tiempos menores a 1 segundo, sin embargo, esto traduce es posible incremento en el OPEX |
| **Riesgos** | La empresa podrá crecer o decrecer su capacidad de tecnología acorde a las necesidades de negocio; Se pueden evidenciar cobros variantes y no fijos en los servicios de tecnología que ofrece el servidor de nube; Ante la caída de alguno de los recursos se podrán presentar latencias mientras se realiza el aprovisionamiento de los recursos nuevamente. |


+*********************+

Escenario	El sitio debe soportar Full-Text Search en la búsqueda de productos. Debe soportar resultados similares para nunca mostrar 0 resultados.
Atributo de Calidad	Usabilidad – Capacidad de descubrimiento
Ambiente	Operación Normal, Operación Modo emergente, Operación con Sobrecarga.
Fuente del Estimulo	Puede ser un usuario final o administrador
Estimulo	El usuario ingresa al home de toures balón y realiza la consulta del catálogo de productos y servicios, realizando transacciones que están centradas en la búsqueda.
Respuesta	El sistema debe realizar búsqueda por palabras en el almacenamiento por el índice de texto.
Medición Respuesta	Se debe retornar los resultados de dos formas posibles:
- Retornar todas las coincidencias encontradas del texto ingresado
- Retornar un mensaje indicando resultados similares según el top de busquedas, no se debe retornar nunca el mensaje 0 resultados encontrados
Decisiones de Arquitectura	Para poder satisfacer esta necesidad, se decide realizar la implementación del índice de texto en la base de datos, lo que permite encontrar rápidamente todas las instancias de un término (palabra) en una tabla sin tener que escanear filas y sin tener que saber en qué columna se almacena un término. En caso de no encontrar ningún resultado se devolverán los resultados de las búsquedas mas utilizadas en la ultima hora.
Puntos de Sensibilidad	Mala implementación del índice de texto, lo que afecta el rendimiento y resultados de las búsquedas.
Trade-Off	Brindar al usuario final una buena experiencia en el sitio, ya que no se muestran mensajes negativos o que frustren sus necesidades de búsqueda.
Riesgos	- Bajo rendimiento en las búsquedas de la base de datos.
- Demora en las respuestas al usuario final con respecto a las búsquedas que realice.


***********************

Escenario	Un usuario no autorizado intenta acceder al sistema de compras en un entorno operativo normal. Los procesos de seguridad en el sistema deben garantizar que los usuarios no autenticados no tengan acceso. El sistema debe mantener las contraseñas y la información confidencial relacionada con el usuario de forma adecuada.
Atributo de Calidad	Seguridad – Autenticación
Ambiente	Operación Normal, Operación Modo emergente, Operación con Sobrecarga.
Fuente del Estimulo	Usuario final
Estimulo	El usuario ingresa al home de toures balón, intenta acceder por medio de url a la sección de compra de paquetes o productos sin registrarse en el sistema.
Respuesta	El sistema realiza la validación de usuario en dos frentes, frontend y backend por medio de token de autenticación.
Medición Respuesta	Retorna un mensaje de error en el cual se informe que no se tiene acceso al recurso requerido
Decisiones de Arquitectura	Para cubrir este requerimiento de seguridad, se realizará la implementación del patrón API Gateway el cual permite la configuración para evitar inyecciones de Código y control de acceso a recursos por medio de autenticación de usuarios.
Puntos de Sensibilidad	Error de configuración en los recursos que permitan el acceso no autorizado
Trade-Off	Brindar al usuario final una alta garantía de seguridad con respecto al resguardo de su información privada.
Riesgos	- Errores en la configuración de seguridad de los recursos que la requirieren


*************************


Escenario	El sistema debe tener la capacidad de cambiar condiciones o reglas de negocio sin tener que re-desplegar el sistema y sin generar indisponibilidades.
Atributo de Calidad	Modificabilidad
Estímulo	Despliegue de las nuevas reglas de negocio
Fuente del estímulo	Usuario administrativo realiza cambio de regla de negocio
Ambiente de operación	Ambiente de operación Normal
Respuesta	Las nuevas transacciones (órdenes de pago) deberán ser evaluadas con el valor de las nuevas reglas de negocio
Medición de la respuesta	Las nuevas transacciones deberán ser registradas en la base de datos de reglas de negocio con el nuevo código de la regla de negocio que la evaluó
Decisiones de Arquitectura	En la implementación de la arquitectura se desplegará un aplicativo que permita la configuración y despliegue de reglas de negocio sin la necesidad de redesplegar todo el sistema y que actualizará los cambios de forma automática sin ser retroactiva.
Puntos de Sensibilidad	El número concurrente de consulta afecta el desempeño del motor de reglas.
Trade-Off	El rendimiento del motor de reglas de negocio podrá afectar el tiempo de respuesta del sistema dada una contención de recursos.
Riesgos	Rendimiento del sistema y tiempo de respuesta en las transacciones de compra


**********************************

Escenario	El sistema debe tener la capacidad de agregar nuevos proveedores/convenios/alianzas sin restricciones de características y sin que esto sea traumático.
Atributo de Calidad	Modificabilidad
Estímulo	Despliegue del nuevo proveedor en la interfaz web administrativa del sitio Web
Fuente del estímulo	Usuario administrativo agrega un nuevo proveedor de transporte/hotel/espectáculo
Ambiente de operación	Ambiente de operación Normal
Respuesta	La página de resultado de búsquedas deberá mostrar las opciones y tarifas de espectáculos/transporte/ hospedaje del proveedor ingresado.
Medición de la respuesta	Integración con el nuevo proveedor.
Decisiones de Arquitectura	Para garantizar la facilidad de ingresar un nuevo proveedor/convenio/alianza se definen un servicio basado en el patrón Intermediate Routing para conectarse a los diferentes servicios de los proveedores sin importar el tipo de tecnología de conexión.
Puntos de Sensibilidad	Aumento de la mantenibilidad de la arquitectura de Toures balón por ser un conjunto de servicios determinados los que tienen la responsabilidad de realizar la integración con los proveedores.
Trade-Off	Disminución o dependencia de la interfaz de comunicación y de datos del nuevo proveedor agregado.
Riesgos	Implementación y complejidad con la adicción de nuevo servicios asociados con auditoria y seguridad

****************************

Escenario	El sistema debe ser capaz de crecer y decrecer dinámicamente según la demanda. Este caso en especial se ve reflejado en las fechas como Cyber-Mondays, Black-Fridays y otros en donde la demanda por los servicios puede crecer hasta 250% sobre la operación normal.
Atributo de Calidad	Escalabilidad
Estímulo	Búsquedas(Transacciones) en el portal Web de Toures balón de un espectáculo o paquete turístico.
Fuente del estímulo	Usuario – Cliente en el portal Web(Pagina de catálogo)
Ambiente de operación	Ambiente de operación con sobre carga
Respuesta	El número de instancias de pods/Docker deberá aumentar según política de escalado horizontal(consumo de CPU - memoria).
Medición de la respuesta	Número de pods/Docker creados dinámicamente durante el ambiente de sobrecarga
Decisiones de Arquitectura	La arquitectura para implementar de Toures balón deberá ser implementada en una tecnología que permite el escalamiento de forma automática (Orquestador de Docker como Kuberntes, RANCHOS o GKC)
Puntos de Sensibilidad	Aumenta la Escalabilidad de la arquitectura
Trade-Off	Aumenta la escalabilidad del sistema al escalar de forma automática el sistema, pero disminuye el rendimiento por la cantidad de 
saltos que puedan presentarse por el orquestador.
Riesgos	Los servicios y/o dockers deberán ser desarrollados para soportar el escalamiento por la plataforma en donde estén desplegados

*****************************

Escenario	El sistema debe poder satisfacer los incrementos de la demanda sin sacrificar su capacidad de respuesta, atender a 100 usuarios o 100 mil usuarios debe ser equivalente.
Atributo de Calidad	Escalabilidad
Estímulo	Búsquedas(Transacciones) en el portal Web de Toures balón de un espectáculo o paquete turístico.
Fuente del estímulo	Usuario – Cliente en el portal Web(Pagina de catálogo)
Ambiente de operación	Ambiente de operación con sobre carga
Respuesta	El tiempo de respuesta de las transacciones(búsquedas) en la página de catálogo de producto no debe ser superior a 1,5 segundos
Medición de la respuesta	Tiempo promedio del tiempo de respuesta de la transacción.
Decisiones de Arquitectura	El despliegue de la arquitectura de Toures balón deberá contar con una forma de cachear la información sin la necesidad de 
ir a consultar la información al servicio correspondiente.
Puntos de Sensibilidad	Aumento del rendimiento del tiempo de respuesta de las transacciones al catálogo de productos.
Trade-Off	Consistencia de la información visualizada por el usuario dado el tiempo de refresco o actualización de la tecnología o método de 
caché
Riesgos	 

**************************************

Escenario	Soporte de operación del negocio 24x7x365, se espera disponibilidad del 99.999%
Atributo de Calidad	Disponibilidad
Estímulo	Falla en la zona en donde se encuentra desplegado el clúster de Kuberntes del proveedor de nube público
Fuente del estímulo	Proveedor de nube publico
Ambiente de operación	Ambiente de operación con falla
Respuesta	Inicio de operación del “clúster” Kubernetes en zona alterna del proveedor de nube público.
Medición de la respuesta	Cluster y pods totalmente funcionando y ejecutándose en la zona alterna soportando la totalidad de la carga.
Decisiones de Arquitectura	La arquitectura desplegada para Toures balón se basará en una arquitectura de nube, mediante la implementación de un cluster
de kubernetes con una disponibilidad del %99,99
Puntos de Sensibilidad	Aumento de la disponibilidad
Trade-Off	Disminuye la mantenibilidad de las aplicaciones y el aumento de la complejidad de la operación.
Tiempo de respuestas mayor debido a la carga total de transacciones sobre la zona que se encuentre activa.
Riesgos	Dependencia de la disponibilidad del proveedor de nube publica.
