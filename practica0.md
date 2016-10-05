# Práctica 0
##Semana del 22 al 28 de septiembre de 2017

## Prerrequisitos#
- [x] Rellenar en la hoja de cálculo correspondiente la equivalencia entre nombre real y nick en GitHub.
- [x] Cumplir los objetivos de la primera sesión.

### Objetivos de la primera Sesión
- [x] Entender la metodología docente, de evaluación y de interacción de la asignatura.
- [x] Darse de alta y comprender el funcionamiento básico de GitHub y la lista de correo de la asignatura; conocer el resto de los recursos de la asignatura y darse de alta en la lista de Telegram si lo considera conveniente.
- [x] Entender el concepto de software libre y su aplicación práctica en esta asignatura.
- [x] Explicar la práctica 0.
ar
##Explicación de práctica 0

###1-Creación de par de claves y subida de clave a GitHub
Para la creacion de clave, utilizamos el comando:

``` $ ssh-keygen -t rsa -C "susanajiaqi@correo.ugr.es" ```

Nos pide que introduzca el nombre de un archivo para guardar la clave, pulsar ENTER y la clave se guardará en el archivo predeterminado. En este caso es ``~/.ssh/id_rsa.pub``.
Después introducimos la clave, dos veces.

Una vez hecho esto, ya tenemos nuestro clave generado en el archivo ``~/.ssh/id_rsa.pub``. El siguiente paso es copiar el contenido de este archivo en el portapapeles.
Utilizando el comando:

```$ clip <~/.ssh/id_rsa.pub  ```

El siguiente paso es añadir esta clave a nuestro cuenta de Github. Los pasos son:

1- Ir a ```Settings```, click en nuestro foto del perfil situado en la esquina superior y luego hacer click en Settings.

2- Click en ```SSH and GPG keys``` situado en la barra lateral.

3- Click en ```New SSH key```

4- Poner una etiquita descriptiva en el campo ```Title``` (se me he olividado poner)

5- Pegar la clave en el campo ```key``` y click en ```Add SSH Key```.


###2-Configuración correcta del nombre y correo electrónico para que aparezca en los commits.
Utilizamos los comandos:

```$ git config --global user.name "JiaqiWa"```

```$ git config --global user.email susanajiaqi@correo.ugr.es```

Al usar la opción ```--global``` Git siempre usará esta información para todo lo que hacemos en ese sistema.


###3-Edición del perfil para que aparezca nombre completo y ciudad.
Se realiza a través del interfaz de Github. En el ```Settings```  --> ```Profile```.

###4-Creación de nuevo hito
Para crear nuevo hito o branch usamos el comando:

```$ git checkout -b hit0```

Y luego un push de este hito:

```$ git push origin hit0 ```

###5-Commit
```$git add practica0.md ```

```$git commit -m "close #9"```

```$git push origin master```
