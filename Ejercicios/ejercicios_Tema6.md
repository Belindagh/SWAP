<h2><b>Ejercicio T6.1:</b></h2>
<b>Aplicar con iptables una política de denegar todo el tráfico
en una de las máquinas de prácticas.
Comprobar el funcionamiento.</b>

En esta imagen se ve como es a la máquina 2 a la que se le deniega el tráfico.

[ej1_parte1](https://github.com/Belindagh/SWAP/blob/master/imagenes_ejers/ej1_parte1.png?raw=true)

<b>Aplicar con iptables una política de permitir todo el tráfico
en una de las máquinas de prácticas.
Comprobar el funcionamiento.</b>

En esta imagen comprobamos que funcionan correctamente al permitir todo el tráfico.

[ej1_parte2](https://github.com/Belindagh/SWAP/blob/master/imagenes_ejers/ej1_parte2.png?raw=true)

<h2><b>Ejercicio T6.2:</b></h2>
<b>Comprobar qué puertos tienen abiertos nuestras máquinas,
su estado, y qué programa o demonio lo ocupa.</b>


PROTOCOLO   DIRECCIÓN     ESTADO           PROGRAM_NAME 

tcp         3306          ESCUCHAR          mysqld
tcp         22            ESCUCHAR          sshd
tcp         80            ESCUCHAR          apache2
tcp         22            ESCUCHAR          sshd
udp         68                              dhclient


<h2><b>Ejercicio T6.3:</b></h2>
<b>Buscar información acerca de los tipos de ataques más
comunes en servidores web (p.ej. secuestros de sesión).
Detallar en qué consisten, y cómo se pueden evitar.</b>


 <b>Los ataques de inyección, SQLI (Structured Query Language Injection):</b> es una técnica para modificar
  una cadena de consulta de base de datos mediante la inyección de código en la consulta. El SQLI explota 
  una posible vulnerabilidad donde las consultas se pueden ejecutar con los datos validados.
  SQLI siguen siendo una de las técnicas de sitios web más usadas y se pueden utilizar para obtener acceso 
  a las tablas de bases de datos, incluyendo información del usuario y la contraseña. Este tipo de ataques 
  son particularmente comunes en los sitios de empresas y de comercio electrónico donde los hackers esperan 
  grandes bases de datos para luego extraer la información sensible.Los ataques sqli también se encuentran 
  entre los ataques más fáciles de ejecutar, que no requiere más que un solo PC y una pequeña cantidad de 
  conocimientos de base de datos.

            Cómo evitar estos ataques:

                La solución sería evitar que se pudieran introducir caracteres especiales (comillas)
                sin haberlas transformado antes (por ejemplo, una comilla doble: " debería de transformarse en \" 
                que así interpretará como texto la comilla y no como el carácter que cierra o abre el una texto en 
                la consulta, pero según el lenguaje se puede implementar de distintas formas y algunas son automáticas 
                y más optimizadas.

     
 <b>DDoS :</b>
    Formas más común para congelar el funcionamiento de un sitio web. Estos son los intentos de inundar 
    un sitio con solicitudes externas, por lo que ese sitio no podría estar disponible para los usuarios reales. 
    Los ataques de denegación de servicio por lo general se dirigen a puertos específicos, rangos de IP o redes completas,
    pero se pueden dirigir a cualquier dispositivo o servicio conectado.
    Los ataques DDoS vienen en 3 variedades principales:
        1.Los ataques de volumen, donde el ataque intenta desbordar el ancho de banda en un sitio específico.
        2.Los ataques de protocolo, donde los paquetes intentan consumir servicios o recursos de la red.
        3.Ataques a aplicaciones, donde las peticiones se hacen con la intención de “explotar” el servidor web, mediante la capa de aplicación.


        Cómo evitar estos ataques:
        
            Se debe saber identificar las partes más propensas a ser atacadas como el ancho 
            de banda a internet, firewalls, prevención de intrusiones, balanceadores de carga
            o servidores. Conocer el tráfico (monitorizar tanto el tráfico de entrada como
            el de salida para ganar visibilidad en volúmenes poco usuales o diseños que
            puedan identificar sitios target o revelar botnets dentro de la red.)
 

  <b>Cross Site Scripting: </b>
       XSS es un estilo de ataque en el que la parte delantera de la página web actúa como un
       punto de lanzamiento para ataques a otros usuarios que visitan el sitio web. Esto 
       sucede cuando los desarrolladores no prueban correctamente su código para posibilidad 
       de permitir scripts de ser inyectados. Los scripts pueden ser ejecutados sin
       funcionalidad original del sitio de la intención que sean.
       Si una vulnerabilidad XSS está presente en un sitio web, entonces un atacante puede 
       crear código que se ejecuta cuando otros usuarios abren el mismo sitio web. Esto hace 
       que los nuevos usuarios interactúen con la entidad fondo malicioso creado por el 
       atacante. Una vez que una conexión se ha iniciado, por lo general a través de tácticas 
       de ingeniería social para convencer a un usuario a hacer algo que no debe, el atacante 
       es capaz de infiltrarse en las computadoras de sus visitantes del sitio web.


         Cómo evitar estos ataques:
            Para evitar eso en PHP existe la función strip_tags que dada una cadena de texto 
            limpia todas las etiquetas HTML que encuentre.

            En javascript podemos encontrar una función adaptada de strip_tags que hace lo 
            mismo.
