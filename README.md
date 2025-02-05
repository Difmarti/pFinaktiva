# pFinaktiva

# En Construcción

Este proyecto está actualmente en construcción. Por favor, evalualo  más tarde para más actualizaciones.

Estare terminando en la noche 5 de febrero

# Prueba teórica o de conocimientos técnicos

1. Actualmente dispone de un servidor web alojado sobre su LAN (e.g
192.168.0.10), en el cual tiene instalado un apache-tomcat sobre la cual ha
alojado la página web de la empresa por el puerto 8080, y Web Services
desplegados sobre el puerto 8443. Se solicita hacer uso del dominio
mipruebaFinaktiva.com.co para publicar a internet tanto la página web, como
los web services. No obstante, se requiere que ambos sean accesibles por la
misma URL y puerto (HTTPS -443). Describa al menos 2 soluciones para resolver
este requerimiento, es libre de disponer el uso de cualquier dispositivo y/o
aplicación conocida para dar solución a lo anterior.

 Rta: Podria ser un Balanceador ha proxy configurando de tal manera que permita visualizar ambos por el mismo dominio, de la misma forma pero en aws con alb configurando los destinos 

2. Un cliente indica que está intentando conectarse los servicios
https://mipruebaFinaktiva.com.co/servicio pero que cuando carga la página
web en su navegador no carga. sin embargo, al realizar usted la prueba
internamente si logra ver disponible los servicios. Describa y enuncie 5 razones
por la cual puede estar pasando el problema y como ayudar al cliente a resolverla
con su ayuda.

 Rta: Validar que el usuario no tenga ningun firewall o antivirus que le bloquee el acceso, validar que al usuario le resuleva el dominio con la ip correcta, Limpiar cache, Si el dominio tiene restriciones por firewall de geo localizacion validar que el usaurio este en una zona disponible, conexion a internet 

3. Un balanceador de carga dispone de diferentes algoritmos de balanceo como:
round robin, round robin weight, least connection, source, URI para tráfico TCP
y HTTP. Describa cada uno de estos y en qué casos ustedes utilizarían cada uno
de estos, su comportamiento para tráfico TCP y HTTP, además de las ventajas y
desventajas de estos.

 Rta: 
  Round Robin: Permite hacer cargas equilibradas entre los servidores asociados, cluster de alta disponibilidad con un rto bajo.
  Round Robin Weight: Se configura los servidores con porcentaje de peso distinto para que distribuya las cargas segun el performance del servidor es decir un 60% 40% se utiliza cuando los servidores no tiene la misma capacidad.
  Source:  Mantiene la sesion activa del usuario durante toda la operacion, necesario segun el tipo de aplicacion.
  least connection: Balancea dependiendo de las conexiones activas, por lo cual monitorea las conexiones en cada servidor.
  URI: Balancea segun el la url o destino de url que uno especifique util para  en el caso de que de que se tenga uun solo sominio y sequiera apuntar a dos  servidores internos  distintos. 
