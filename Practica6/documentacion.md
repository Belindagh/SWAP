<h1><b>PRÁCTICA 6 -- Discos en RAID</b></h1>

<h3><b> 1.Realizar la configuración de dos discos en RAID 1 bajo Ubuntu, automatizando 
        el montaje del dispositivo creado al inicio del sistema. 
</h3></b>
        Tras añadir los dos discos del mismo tipo y capacidad, instalamos el software
        mdadm, creamos el RAID, le damos formato y creamos el directorio en el que se
        va a montar la unidad del RAID. 
        En la imagen1 lo podemos comprobar:

        ![imagen1]mount

        Ahora comprobamos el estado del RAID:

        ![imagen2]estadoRAID

        Para obtener los UUID de todos los dispositivos de almacenamiento que tenemos,

        ![imagen3]UUID

        Añadimos al archivo /etc/fstab:

        ![imagen4]raidd

        para que monte automáticamente el dispositivo RAID. 

 <h3><b> 2.Simular un fallo en uno de los discos del RAID(mediante comandos con el mdadm),
           retirarlo "en caliente", comprobar que se puede acceder a la información que hay
           almacenada en el RAID, y por último, añadirlo al conjunto y comprobar que se 
           reconstruye correctamente.
</h3></b>  

          En la imagen podemos ver primero, como simulamos un fallo en uno de los discos,
          luego como retiramos en caliente el disco que está marcado como que ha fallado
          y por último, añadimos en caliente un nuevo disco que vendría a reemplazar al 
          disco que hemos retirado.

          ![imagen5] resultado

            

        
