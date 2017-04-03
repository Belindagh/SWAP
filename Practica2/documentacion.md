**Primera tarea: probar el funcionamiento de la copia de archivos por ssh**

[parte1](https://raw.githubusercontent.com/Belindagh/SWAP/master/Practica2/imagenes/parte1_P2.png)

En la imagen parte1_p2, vemos como en la máquina 1 se crea nuevo.html
y al ejecutar rsync en la máquina 2, también se crea en esta. 



**Segunda tarea: clonado de una carpeta entre las dos máquinas**

[parte2](https://raw.githubusercontent.com/Belindagh/SWAP/master/Practica2/imagenes/parte2_P2.png)

En la imagen parte2_p2, podemos comprobar que también sucede lo mismo 
con las carpetas.


**Tercera tarea: configuración de ssh para acceder sin que solicite contraseña**

[parte3](https://raw.githubusercontent.com/Belindagh/SWAP/master/Practica2/imagenes/parte3_P2.png)

En la imagen parte3_p2, aparece como en la máquina 2 no nos pide introducir
la contraseña, esto es debido a que hemos hecho la clave pública anteriormente
en la máquina 1.

**Cuarta tarea: establecer una tarea en cron que se ejecute cada hora para mantener**
**actualizado el contenido del directorio /var/www entre las dos máquinas.**

[parte4](https://raw.githubusercontent.com/Belindagh/SWAP/master/Practica2/imagenes/parte4_P2.png)

En la imagen parte4_p2, apreciamos como tras un tiempo determinado se ejecuta 
automáticamente rsync ya que se copian los cambios. El tiempo se establece en
la tabla crontab.

