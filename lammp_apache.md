# Inicialización del servidor local

muy amenudo cuando deseo usar apache, mysql en un servidor local
previa instalación de **xampp** lo que queda es inicializarlo pero
comunmente esto no sale de la manera esperada suelen haver fallos en
apache, myslqd.

```sh
#Inicializar el servidor local

sudo /opt/lampp/lampp start

#el fallo mas común es que  mysqld no se inicia con este comando
#esto debido a que están activos de manera automática para lo cual es necesario
#desactivarlo con el siguiente comando

sudo service mysql stop

#una vez mas ejecutamos el comando
sudo /opt/lampp/lampp start

#pero el siguiente fallo mas común es apache
#para ello ejecutamos el administrador gráfico para visualizar si esta apache
#activo o no.

sudo /opt/lampp/manager-linux-x64.run

#verificamos que estén activos si apache esta inactivo después de intentar 
#activarlo, correr el siguiente comando.

sudo /opt/lampp/bin/apachectl -kstart

#una vez finalizado volvemos a correr el comando que inicializa lampp

sudo /opt/lampp/lampp/ start

#con esto los servidores ya debería estar activos y para verificar podemos 
#ejecutar el administrador gráfico o poner localhost en el navegador





```
