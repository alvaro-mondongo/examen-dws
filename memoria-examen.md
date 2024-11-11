## Ejercicio 2
### Primer paso
Primero me he conectado al servidor remoto mediante ssh.
~~~
ssh usuario@192.168.0.185
~~~  
Luego he introducido la contraseña
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
