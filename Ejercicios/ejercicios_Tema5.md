<h2><b>Ejercicio T5.1:</b></h2>
<b>Buscar información sobre cómo calcular el número de conexiones por segundo.</b>

Podemos saberlo con el comando:

    apache2ctl status |grep request

También existe el siguiente comando:

    netstat -lpan | grep :80 | wc -l

Para tener más información de las conexiones se puede usar iptstate, que puedes filtrar la 
salida del comando para que te diga el número de conexiones a un puerto determinado de una 
dirección IP, por ejemplo:

    iptstate -1 -d 192.168.0.100 -D 80


<h2><b>Ejercicio T5.2:</b></h2>
<b>Instalar wireshark y observar cómo fluye el tráfico de red en uno de los 
servidores web mientras se le hacen peticiones HTTP.</b>

Lo he instalado pero no me dejaba utilizarlo para poder observar lo pedido en el ejercicio. 

<h2><b>Ejercicio T5.3:</b></h2>
<b>Buscar información sobre características, disponibilidad para
diversos SO, etc de herramientas para monitorizar las
prestaciones de un servidor.</b>

 <b>top:</b>
    Sirve para supervisar el rendimiento, muestra todo el funcionamiento y los procesos en tiempo real, el uso de CPU, de memoria, la memoria de intercambio, la caché, tamaño de búfer, PID de proceso, usuario, carga de memoria...

 <b>vmstat:</b>
    Proporciona datos sobre la memoria virtual, hilos kernerl, discos, da información sobre procesos de sistema, memoria, bloques de E / S, interrupciones y actividad de la CPU.

 <b>netstat:</b>
     Es una herramienta de línea de comandos que muestra un listado de las conexiones
     activas, tanto entrantes como salientes y las estadísticas de la interfaz.

 <b>lsof:</b>
    Se utiliza para hacer reportes de archivos y los procesos que están utilizando a éstos. Se puede utilizar para revisar que procesos están haciendo uso de  directorios, archivos ordinarios, tuberías (pipes), sockets y dispositivos.

