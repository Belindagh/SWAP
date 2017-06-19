<h2><b>Ejercicio T7.1:</b></h2>
<b>¿Qué tamaño de unidad de unidad RAID se obtendrá al configurar 
    un RAID 0 a partir de dos discos de 100 GB y 100 GB?</b>

    100GB + 100GB = 200GB ,en los RAID de nivel 0 la información no se duplica.

<b>¿Qué tamaño de unidad de unidad RAID se obtendrá al configurar 
    un RAID 0 a partir de tres discos de 200 GB cada uno?</b>    

    200GB + 200GB + 200GB = 600 GB ,en los RAID de nivel 0 la información no se duplica.

<h2><b>Ejercicio T7.2:</b></h2>
<b>¿Qué tamaño de unidad de unidad RAID se obtendrá al configurar 
    un RAID 1 a partir de dos discos de 100 GB y 100 GB?</b>

    100 GB, en los RAID de nivel 1 se replican los datos en ambos discos, por lo tanto,
    la unidad RAID solo tiene el valor de un disco.

<b>¿Qué tamaño de unidad de unidad RAID se obtendrá al configurar 
  un RAID 1 a partir de tres discos de 200 GB cada uno?</b>

    200GB, en los RAID de nivel 1 se replican los datos en ambos discos, por lo tanto,
    la unidad RAID solo tiene el valor de un disco.

<h2><b>Ejercicio T7.4:</b></h2>
<b>Buscar información sobre los sistemas de ficheros en red más 
 utilizados en la actualidad y comparar sus características. 
 Hacer una lista de ventajas e inconvenientes de todos ellos, 
 así como grandes sistemas en los que se utilicen. </b>

El Network File System (Sistema de archivos de red), o NFS, es un protocolo de nivel de aplicación, 
según el Modelo OSI. Es utilizado para sistemas de archivos distribuido en un entorno de red de 
computadoras de área local. Posibilita que distintos sistemas conectados a una misma red accedan 
a ficheros remotos como si se tratara de locales. Originalmente fue desarrollado con el objetivo de 
que sea independiente de la máquina, el sistema operativo y el protocolo de transporte, esto fue 
posible gracias a que está implementado sobre los protocolos XDR (presentación) y ONC RPC.

    El sistema NFS está dividido al menos en dos partes principales: un servidor y uno o más clientes. 
    Los clientes acceden de forma remota a los datos que se encuentran almacenados en el servidor.

    Las estaciones de trabajo locales utilizan menos espacio de disco debido a que los datos se 
    encuentran centralizados en un único lugar pero pueden ser accedidos y modificados por 
    varios usuarios, de tal forma que no es necesario replicar la información.

    Los usuarios no necesitan disponer de un directorio “home” en cada una de las máquinas de la organización. 
    Los directorios “home” pueden crearse en el servidor de NFS para posteriormente poder acceder a ellos 
    desde cualquier máquina a través de la infraestructura de red.

    También se pueden compartir a través de la red dispositivos de almacenamiento como disqueteras, 
    CD-ROM y unidades ZIP. Esto puede reducir la inversión en dichos dispositivos y mejorar 
    el aprovechamiento del hardware existente en la organización.
