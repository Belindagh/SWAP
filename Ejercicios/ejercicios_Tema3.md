**Ejercicio T3.1:**

**Buscar con qué órdenes de terminal o herramientas gráficas podemos**
**configurar bajo Windows y bajo Linux el enrutamiento del tráfico de**
**un servidor para pasar el tráfico desde una subred a otra.**

Para activar el enrutamiento en un sistema Linux, tan solo basta con 
poner a '1' la variable ip_forward del sistema, es decir,
basta con ejecutar desde una consola de root:

    // Activar el enrutamiento en un sistema Linux
    sudo echo "1" > /proc/sys/net/ipv4/ip_forward


Posteriormente tendríamos que configurar el filtrado para que acepte 
el redireccionamiento de paquetes desde dentro hacia fuera de nuestra 
red y mediante NAT permita que los PCs de la red interna naveguen con 
la dirección IP 'publica' del servidor.

Tendríamos que indicar que se acepten todos los paquetes que son para reenviar,
es decir, aquellos que llegan a nuestra máquina pero que no es ella la destinataria. 
Para ello, tendríamos que aceptar los paquetes de tipo FORWARD, como veremos en la 
siguiente sección. Por otro lado, tendríamos que indicar que los paquetes que llegan 
desde nuestra red interna (-s 10.0.0.0/8) y que salgan por la interfaz eth0 hacia el 
router (-o eth0), después de enrutarlos en nuestra máquina (POSTROUTING), debemos 
enmascararlos (MASQUERADE), es decir, hacer NAT. Los comandos a ejecutar serían:

    // Haciendo NAT en el servidor
    sudo iptables -A FORWARD -j ACCEPT
    sudo iptables -t nat -A POSTROUTING -s 10.0.0.0/8 -o eth0 -j MASQUERADE


En Windows, en administrador del servidor, seleccionamos servicio de enrutamiento y acceso remoto.

**Ejercicio T3.2:**

**Buscar con qué órdenes de terminal o herramientas gráficas**
**podemos configurar bajo Windows y bajo Linux el filtrado**
**y bloqueo de paquetes.**

La principal orden en Linux es iptables, que permite incluir reglas
para dejar pasar o bloquear paquetes.

En Windows, con el propio Firewall, a través de su interfaz podemos 
administrar funciones simples de su comportamiento.
