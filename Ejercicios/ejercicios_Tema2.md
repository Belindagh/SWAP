##Ejercicio T2.1: 
**Calcular la disponibilidad del sistema si tenemos dos**
**réplicas de cada elemento (en total 3 elementos en cada subsistema).**

web3 = 97'75 + (1 - 97'75)*85 = 99'6625
ap = 99 + (1 - 99)*90 = 99'9
BD = 99.9999 + (1 - 99'9999)*99'9 = 99'99999
DNS = 99.96 + (1 - 99'96)*98 = 99'9992
Firewall = 97'75 + (1 - 97'75)*85 = 99'6625
switch = 99.99 + (1 - 99'99)*99 = 99'9999
DC = 99.99 + (1 - 99'99)*99'99 = 99'9999
ISP = 99'75 + (1 - 99'75)*95 = 99'9875

Disponibilidad=0,996625×0,999×0,999999×0,999992×0,996625×0,999999×0,9999×0,999875=99,2034961%

##Ejercicio T2.2:
**Buscar frameworks y librerías para diferentes lenguajes que**
**permitan hacer aplicaciones altamente disponibles con relativa facilidad.**

**IBM PowerHA**, alta disponibilidad y recuperación en caso de desastre en entornos UNIX.
Representa una solución de agrupación en clústeres basada en almacenamiento de IBM 
que despliegan clientes de gran y pequeño tamaño de todo el mundo.
PowerHA está basado en Cluster Aware AIX (CAA).


**YII**, es un framework orientado a objetos, software libre, PHP basado en componentes 
de alto rendimiento para desarrollar aplicaciones Web de gran escala. El mismo permite
la máxima reutilización en la programación web y puede acelerar el proceso de desarrollo.


**Symfony**, este FrameWork PHP es útil para acelerar la creación y el mantenimiento
de sus aplicaciones web. Proporciona un conjunto de elementos prefabricados que se 
pueden integrar rápidamente en su aplicación, combinada con una metodología clara 
para ayudarle a trabajar de forma eficiente y eficaz en las tareas más complejas.


##Ejercicio T2.3:
**¿Cómo analizar el nivel de carga de cada uno de los subsistemas en el servidor?**
 
+Podemos usar el comando "top" que nos muestra el uso de CPU y de memoria que 
están haciendo los procesos que se están ejecutando en nuestra máquina.

+Gnome System Monitor,muestra qué programas están en ejecución y cuánto 
procesador, tiempo, memoria y espacio en disco están usando.

+GTmetrix, es una de las herramientas más completas que podemos emplear a la hora de evaluar
la carga de una página web: unifica Google Page Speed y Yahoo! YSlow en una sola interfaz. 
Muestra recomendaciones de mejora mediante gráficas de color, a las que puntúa de la A a
la F (A es mejor; F, peor) y de 0 a 100. 

+WebPageTest, establece el análisis en base a continentes (América del Norte, 
América del Sur, Europa, África, Asia y Oceanía), ciudades y navegadores. 
Dispone de opciones para elegir la velocidad de conexión a internet, 
así como, por ejemplo, desactivar Javascript e ignorar errores de certificados SSL.
El resultado del test puntúa de la A a la F (A es la mejor puntuación posible; F, la peor).

##Ejercicio T2.4:
**Buscar ejemplos de balanceadores software y hardware (productos comerciales).**
	
Balanceadores software:

+HAProxy
+Pound
+Nginx

Balanceadores hardware:

+Cisco
+LoadMaster


**Buscar productos comerciales para servidores de aplicaciones.**

+Servidor de aplicaciones Microsoft
+WebLogic (Oracle)
+WebSphere (IBM)

**Buscar productos comerciales para servidores de almacenamiento.**

+DELL: Dell Storage SC9000 , Dell KACE, Dell Compellent FS8600.


