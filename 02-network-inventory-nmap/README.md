En los resultados de un escaneo de puertos, encontramos ciertas caracteristicas, principalmente: "open", "closed" y 
"filtered", Mientras que open significa que Nmap ha detectado que un servicio esta escuchando en ese puerto
y con ello, aceptando conexiones, mientras que closed, indica que Nmap puede comunicarse con el dispositivo, pero 
no hay servicio aceptando conexiones por ese puerto

Por otro lado filtered indica que Nmap no puede determinar si el puerto esta abierto o cerrado, ya que un mecanismo 
de filtrado impide obtener una respuesta definitiva, el servicio puede estar funcionando, pero un firewall, reglas de 
filtrado de trafico, listas de control de acceso o dispositivos de seguridad podrian descartar la solicitud y generar 
una respuesta indeterminada 


Tabla de inventario
Host			IP		Puerto		Servicio	Versión			Función
Equipo Princip.		192.168.56.1	(no escaneado)			Anfitrión
DHCP de VirtualBox	192.168.56.100	(no escaneado)			Asigna IP
Debian servidor		192.168.56.102	22/tcp		ssh		OpenSSH 9.2p1		Administración
Debian servidor		192.168.56.102	80/tcp		http		Apache httpd 2.4.68	Servidor web

Resultado de ndiff 

ndiff base-1.xml base-2.xml
-Nmap 7.93 scan initiated Mon Oct 26 18:30:48 2026 as: nmap -sS -p- -T4 -oA base-1 192.168.56.102
+Nmap 7.93 scan initiated Mon Oct 26 18:48:56 2026 as: nmap -sS -p- -T4 -oA base-2 192.168.56.102

 192.168.56.102, 08:00:27:E2:49:26:
-Not shown: 65533 closed ports
+Not shown: 65534 closed ports
 PORT   STATE SERVICE VERSION
-80/tcp open  http
