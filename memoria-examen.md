# Examen Despliegue Aplicaciones Web
## Ejercicio 2
### Primer paso
Primero me he conectado al servidor remoto mediante ssh.
Luego he introducido la contraseña  
~~~
ssh usuario@192.168.0.185
~~~  
![1](https://github.com/user-attachments/assets/7ddab2bc-502c-4071-ac1f-7f11ad23dd02)

### Segundo paso
Después he comprobado los directorios, y navegado hasta el escritorio.  
~~~
ls
cd Escritorio
~~~  
![2](https://github.com/user-attachments/assets/bef8814c-31dc-4951-8fcc-da02929a857a)

### Tercer paso
Luego creo el archivo vacío.   
~~~
echo > alvaroCollado.txt
~~~  
![3](https://github.com/user-attachments/assets/3e0f4dd7-2831-4a94-99cc-6a7e00051d00)

### Cuarto paso
Después he guardado el resultado de _whoami_ dentro del .txt   
~~~
whoami > alvaroCollado.txt
~~~  
![4](https://github.com/user-attachments/assets/7458d661-9660-4f04-8178-bba9977f0bf4)  
**Nota:** si nos saltamos el tercer paso y hacemos este directamente, se creará el archivo automaticamente. Por lo que el tercer paso  no es necesario, pero lo he incluido por ir por partes. 

### Quinto paso
Y por último he concatenado el comando _who_ que es el necesario para listar quienes están conectados por ssh.
~~~
echo "who" >> alvaroCollado.txt
~~~  
![5](https://github.com/user-attachments/assets/a3b231b2-c5c5-4307-9ee2-ed585359ba65)

## Ejercicio 3
### Primer paso
Primero creamos el directorio donde almacenaremos el html.
~~~
cd /var/www
mkdir miWeb
~~~  
![1](https://github.com/user-attachments/assets/26dbf36d-f8bd-45fc-bbd0-4dddf087b872)

### Segundo paso
Damos permisos con este comando:
~~~
sudo chown -R $USER:$USER /var/www/miWeb
~~~  
![1](https://github.com/user-attachments/assets/30964f96-39bc-44f8-bd03-d07409c0438a)

### Tercer paso
He creado/rellenado el archivo de html.
~~~
cd miWeb
sudo nano index.html
~~~
Luego he introducido el codigo html.  
![1](https://github.com/user-attachments/assets/b46b403c-d236-4b19-8cbc-53d2c4500222)


### Cuarto paso
He ido al directorio adecuado y creado el archivo .conf 
~~~
cd /etc/apache2/sites-available
sudo nano daw.ejercicio3.conf
~~~
Luego he rellenado el archivo con el siguiente texto.  
![1](https://github.com/user-attachments/assets/dcaf9659-e056-4907-98b0-2da81f8cdcc9)


### Quinto paso
He habilitado la configuración que acabo de crear. Y luego he recargado apache.
~~~
sudo a2ensite daw.ejercicio3.conf
sudo systemctl reload apache2
sudo systemctl restart apache2
~~~  
![1](https://github.com/user-attachments/assets/2db05630-ac30-490f-bcf1-483ab56c635d)

### Sexto paso
Ya funciona.  
![1](https://github.com/user-attachments/assets/4f3ad81d-389b-416c-a506-1d7199419fe8)
