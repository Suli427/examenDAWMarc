# DOCUMENTACIÓN EXAMEN MARC SOLER
## EJ 2
Para realizar este ejercicio, he empezado ejecutando el comando *sudo ssh usuario@192.168.0.185* para conectarme al equipo remoto. Una vez dentro he ejecutado el comando *whoami* que muestra el nombre del usuario (en este caso el nombre es usuario).

Seguidamente he creado un archivo txt con el comando *nano MarcSoler.txt* con el nombre de usuario que aparece al ejecutar el comando anterior.

Finalmente, he concatenado al archivo el nombre del comando que permite ver quienes están conectados a la máquina mediante ssh (who) con el comando *echo*y he mostrado con el comando cat el contenido del archivo para comprobar que todo ha sido realizado correctamente.
!["examenDAWMarc/imagenesej2/cap1.png](https://raw.githubusercontent.com/Suli427/examenDAWMarc/refs/heads/main/imagenesej2/cap1.png)

## EJ 3
Para realizar este ejercicio, he empezado creando el directorio miWeb con el comando *mkdir* y el archivo html de mi web con el comando *nano*.
!["examenDAWMarc/imagenesej3/cap1.png](https://raw.githubusercontent.com/Suli427/examenDAWMarc/refs/heads/main/imagenesej3/cap1.png)
!["examenDAWMarc/imagenesej3/cap2.png](https://raw.githubusercontent.com/Suli427/examenDAWMarc/refs/heads/main/imagenesej3/cap2.png)

Seguidamente he modificado el archivo */etc/hosts* con el comando *nano* introduciendo daw.ejercicio3.com.
!["examenDAWMarc/imagenesej3/cap3.png](https://raw.githubusercontent.com/Suli427/examenDAWMarc/refs/heads/main/imagenesej3/cap3.png)

Una vez modificado este archivo, he realizado una copia del archivo */etc/apache2/sites-available/000-default.conf* con el comando cp y lo he llamado daw.conf. En este archivo he puesto mi correo en el apartado de ServerAdmin, la ruta del html en DocumentRoot y daw.ejercicio3.com en ServerName. Todas estas modificaciones las he realizado con el comando *nano*.
!["examenDAWMarc/imagenesej3/cap5.png](https://raw.githubusercontent.com/Suli427/examenDAWMarc/refs/heads/main/imagenesej3/cap5.png)

Finalmente le he puesto a la carpeta */var/miWeb* permisos a todos los usuarios de lectura, escritura y ejecución con el comando *chmod*.
!["examenDAWMarc/imagenesej3/cap7.png](https://raw.githubusercontent.com/Suli427/examenDAWMarc/refs/heads/main/imagenesej3/cap7.png)

En teoría con todo esto, debería funcionar si iniciara apache con el comando *sudo systemctl start apache* y poniendo daw.ejercicio3.com en el navegador.
!["examenDAWMarc/imagenesej3/cap6.png](https://raw.githubusercontent.com/Suli427/examenDAWMarc/refs/heads/main/imagenesej3/cap6.png)

Como no funcioanaba he movido la carpeta /*var/miWeb* a */var/www* y he modificado el DocumentRoot de daw.conf con la nueva ruta.
!["examenDAWMarc/imagenesej3/cap9.png](https://raw.githubusercontent.com/Suli427/examenDAWMarc/refs/heads/main/imagenesej3/cap9.png)