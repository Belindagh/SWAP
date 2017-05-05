<h2><b>Ejercicio T4.1:</b></h2>
<b>Buscar información sobre cuánto costaría en la actualidad
un mainframe. Comparar precio y potencia entre esa
máquina y una granja web de unas prestaciones similares.</b>

Un mainframe de IBM, el z13, puede costar aproximadamente 75.000 dólares.
No he encontrado más información para comparar las prestaciones de esta
con una granja web similar.

<h2><b>Ejercicio T4.2:</b></h2>
<b>Buscar información sobre precio y características de
balanceadores hardware específicos. Compara las
prestaciones que ofrecen unos y otros.</b>

En estas imágenes se muestra una comparación de: 


    KEMP LoadMaster

    F5 Big-IP LTM

    Citrix Netscaler MPX

[imagen1](https://github.com/Belindagh/SWAP/blob/master/imagenes_ejers/ejercicio2.png?raw=true)
[imagen2](https://github.com/Belindagh/SWAP/blob/master/imagenes_ejers/ejercicio2_.png?raw=true)


<h2><b>Ejercicio T4.3:</b></h2>
**Buscar información sobre los métodos de balanceo que**
**implementan los dispositivos recogidos en el ejercicio 4.**

**KEMP LoadMaster:**
    -round-robin
    -weighted round-robin
    -least connections
    -weighted least connections
    -fixed weighting
    -Request switching
    -Application switching
    -Content based routing


<h2><b>Ejercicio T4.4:</b></h2>
**Instala y configura en una máquina virtual el balanceador**
**ZenLoadBalancer.**

Hay que descargarse e instalarse la ISO desde este link [aquí](https://sourceforge.net/projects/zenloadbalancer/files/latest/download) ,
una vez instalado el sistema basado en Debian GNU/Linux, lo configuramos
para poder acceder desde otra máquina y así conseguir un resultado similar
al de la práctica 3.

<h2><b>Ejercicio T4.5:</b></h2>
**Probar las diferentes maneras de redirección HTTP.**
**¿Cuál es adecuada y cuál no lo es para hacer balanceo de**
**carga global? ¿Por qué?**

La manera más adecuada de redirección es la 302 dado que es temporal
y así sería posible redirigir el tráfico a otras direcciones
temporales.

<h2><b>Ejercicio T4.7:</b></h2>
**Buscar información sobre métodos y herramientas para implementar GSLB.**
Una herramienta para implementar un GSLB puede ser NetScaler, para configurarlo
mediante la línea de comandos de NetScaler
En el símbolo del sistema NetScaler, escriba:
    •set ns config -ipaddress<IPAddress> -netmask<subnetMask> 
    •add ns ip<IPAddress> <subnetMask> -type<type>   
    •add route Network<subnetMask> <gateway> 
    •set system user<userName> <password>   
    •save ns config           
    • reboot
