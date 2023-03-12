# Sistema-de-alarma-digital
Es un diseño e implementación de un sistema de alarmas(botón antipánico) digital.

--Descripción--
Este sistema permitirá a distintas empresas que utilicen este producto, contar con un sistema que permita a los empleados disparar a través de un sistema instalado en sus respectivos puestos de trabajo distintos tipos de alerta de acuerdo con las circunstancias.

--Versión 1--
Hay solo interacción entre una aplicacion emisora y una receptora, sin interacción de un servidor.

Características:
1- En los puestos de trabajo de los empleados, la aplicación permitirá optar por el tipo de situación que quiere reportar: solicitud de asistencia médica, solicitud de personal de seguridad o notificar un foco de incendio.
2- En distintos puestos estratégicos, se instalará una aplicación tipo panel donde se indicará desde que lugar se está solicitando la asistencia, el tipo de notificación y la hora. Cada uno de estos puestos debe ser configurado para indicar el tipo de 
eventos que puede recibir.
3- La aplicación de envío de solicitud debería indicar si la misma fue o no recibida por el destinatario. La aplicación receptora debería emitir una señal sonora al recibir la notificación. 

--Versión 2--
En esta implementación se diseño una arquitectura centralizada.

Características:
1- La aplicación emisora de eventos debe enviar los mensajes directamente al servidor. El servidor debe enviar los mensajes a los receptores.
2- La aplicación receptora debe registrarse en el servidor indicando el tipo/s de mensaje que desea recibir.
3-  En el servidor se debe llevar un registro de todos los eventos recibidos (IP, puerto,tipo de notificación, fecha y hora). Solo en memoria (sin persistencia).

--Versión 4--
En este caso de utiliza una arquitectura de alta disponibilidad.
Se utilizan técnicas de disponibilidad como:
-Redudancia activa.
-Monitor
-Ping/echo
