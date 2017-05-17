<h1><b>PRÁCTICA 4</b></h1>

<h2><b>1.Instalar un certificado SSL autofirmado para configurar el acceso HTTPS a los
servidores. </h2></b>

    Tras activar el módulo SSL de Apache, generar los certificados y especificarle la ruta 
    a los certificados en la configuración, completamos los datos de configuración del dominio 
    y editamos el archivo default-ssl mostrado en la imagen, lo activamos y reiniciamos.
    Se puede comprobar que funciona correctamente.

![parte1](https://github.com/Belindagh/SWAP/blob/master/Practica4/imagenes/parte1.png?raw=true)


<h2><b> 2.Configurar las reglas del cortafuegos con IPTABLES para asegurar el acceso a
los servidores web, permitiendo el acceso por los puertos de HTTP y HTTPS.
Esta configuración la vamos a hacer en una de las máquinas servidoras finales
(p.ej. en la M1). Se debe poner en un script que se ejecute en el arranque del
sistema (poner que se ejecute el script con las reglas del cortafuegos en el
archivo /etc/rc.local ).</h2></b>
    
    Creamos un script que contenga: 

        # (1) Eliminar todas las reglas (configuración limpia)
        iptables -F
        iptables -X
        iptables -Z
        iptables -t nat -F

        # (2) Política por defecto: denegar todo el tráfico
        iptables -P INPUT DROP
        iptables -P OUTPUT DROP
        iptables -P FORWARD DROP

        # (3) Permitir cualquier acceso desde localhost (interface lo)
        iptables -A INPUT -i lo -j ACCEPT
        iptables -A OUTPUT -o lo -j ACCEPT

        # (4) Abrir el puerto 22 para permitir el acceso por SSH
        iptables -A INPUT -p tcp --dport 22 -j ACCEPT
        iptables -A OUTPUT -p tcp --sport 22 -j ACCEPT

        # (5) Abrir los puertos HTTP (80) de servidor web
        iptables -A INPUT -p tcp --dport 80 -j ACCEPT
        iptables -A OUTPUT -p tcp --sport 80 -j ACCEPT


Para que se ejecute en el arranque del sistema lo guardamos con iptable-save.

En la imagen, comprobamos que funciona correctamente.

![parte2](https://github.com/Belindagh/SWAP/blob/master/Practica4/imagenes/parte2.png?raw=true)