### Análisis de los resultados

Durante la práctica se analizó una transferencia de archivos mediante 
el protocolo HTTP utilizando Wireshark. A partir del tráfico capturado 
fue posible identificar la solicitud del archivo `prueba.png` y recuperar 
su contenido mediante la herramienta Export Objects. 
Posteriormente, se calcularon los hashes SHA-256 de la imagen original y 
de la imagen recuperada, comprobando que ambos valores coincidían, lo que 
demuestra que el archivo pudo reconstruirse sin modificaciones.

Este procedimiento evidencia uno de los principales riesgos de utilizar 
HTTP: la información se transmite el claro, por lo que un atacante con 
acceso al tráfico de red podría observar las solicitudes y recuperar los 
datos transmitidos. En este caso, la información expuesta fue el 
contenido de una imagen, aunque el mismo riesgo puede afectar a otros 
archivos y datos sensibles.

La implementación de HTTPS mediante TLS permite proteger la confidencialidad 
e integridad de la comunicación mediante protocolos usando criptografia. 
De esta manera, aunque un tercero capture los paquetes, no podrá 
recuperar directamente el contenido de la imagen utilizando Export 
Objects sin disponer del acceso necesario para descifrar la comunicación. 
