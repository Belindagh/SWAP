**Configurar una máquina e instalarte nginx como balanceador de carga**
[nginx]


**Configurar una máquina e instalarte nginx como balanceador de carga**
[haproxy]


En ambas imágenes, comprobamos que realmente se reparte la carga y se comprueba
además el funcionamiento del algoritmo de balanceo round-robin.


**Someter a la granja web a una alta carga, teniendo primero nginx y después haproxy**
Con nginx, 50000 conexiones, 22.772 segundos.
Con haproxy, 50000 conexiones, 25.920 segundos.
