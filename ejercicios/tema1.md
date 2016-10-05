#EJERCICIOS TEMA 1. Jiaqi Wang

##EJERCICIO-1:
###Consultar en el catálogo de alguna tienda de informática el precio de un ordenador tipo servidor y calcular su coste de amortización a cuatro y siete años.
El servidor que he elegido es un [HP ProLiant BL460c Gen9 E5-2620v3](https://www.pccomponentes.com/hp-proliant-bl460c-gen9-e5-2620v3)
![](https://img.pccomponentes.com/articles/10/103334/hp-proliant-bl460c-gen9-e5-2620v3.jpg =250x)
Tiene un coste de __2157€ *IVA incluido* (1782.64€ sin IVA)__

####Amortización de 4 años y 7 años.
Consultado en la [tabla de amortización](https://ayuda.cuentica.com/anos-y-porcentaje-de-amortizacion-para-sociedades/), los equipos para tratamiento de información (nº6 en la tabla) tiene un coeficiente máximo de 25%, mínimo 4 años y máximo 8 años.

Entonces para calcular la cuota de amortización de **4 años** sería el coste sin IVA divido entre 4 años:
**1782,64€/4=445,66€** cada año. El coeficiente de amortización es un 25%.

Calculando de la misma forma la cuota de amorización para **7 años** es **1782,64€/7=254,66€** cada año, con un coeficiente de 14.28%.

##EJERCICIO-2:
###Usando las tablas de precios de servicios de alojamiento en Internet y de proveedores de servicios en la nube, Comparar el coste durante un año de un ordenador con un procesador estándar (escogerlo de forma que sea el mismo tipo de procesador en los dos vendedores) y con el resto de las características similares (tamaño de disco duro equivalente a transferencia de disco duro) en el caso de que la infraestructura comprada se usa sólo el 1% o el 10% del tiempo.  
####Servidores elegidos:
1-Servidor dedicado: [XL12i](https://www.1and1.es/server-dedicated-tariff#server)

      -CPU:Intel®Xeon® E5-2640, 6 Cores (HT) x 2,5 GHz

      -Memoria Ram: 32GB

      -Disco Duro:2000GB

      -Precio:169,99€/mes

2-Servidor cloud: [Servidor Cloud XXL axarnet](https://www.axarnet.es/servidores-cloud/)

      -CPU: 6 vCPU

      -Memoria Ram: 32GB

      -Disco Duro:750GB

      -Precio: 119,95€/mes

Calculamos el gasto anual de ambos servidores:

  El gasto usando 1% del tiempo:

        -Servidor dedicado: **169,99€ x 12 meses =2039,88€ / año**.

        -Servidor cloud: **119,95€ x 12 meses x 0,01 =14,394 / año**.

  El gasto usando 10% del tiempo:

        -Servidor dedicado: **169,99€ x 12 meses =2039,88€ / año**.

        -Servidor cloud: **119,95€ x 12 meses x 0,10 =143,94 / año**.


##EJERCICIO-3:
###1.¿Qué tipo de virtualización usarías en cada caso? Comentar en el foro
[Comentado en el foro]()

###2.Crear un programa simple en cualquier lenguaje interpretado para Linux, empaquetarlo con CDE y probarlo en diferentes distribuciones.

Usaremos el lenguaje Python para crear un programa que simplemente imprime "Hello world!"
```#!/usr/bin Python
   print "Hello world!"
```
Para poder empaqutar con CDE, tenemos que instalar primero CDE usando `sudo apt-get install cde`
Los siguientes pasos se pueden observar en la captura del terminal:
![captura de pantalla](https://github.com/JiaqiWa/IV-16-17/blob/hit0/CapturasDePantalla/Ejecicio3.2.PNG))
Para usarlo otras distrubuciones solo tiene que descomprimir el paquete y luego acceder al directorio correspondiente para poder ejecutarlo.


##EJERCICIO-4:
###Comprobar si el procesador o procesadores instalados tienen estos flags. ¿Qué modelo de procesador es? ¿Qué aparece como salida de esa orden?
Para conocer el modelo del procesador usaremos el comando ```cat /proc/cpuinfo```
![captura pantalla](https://github.com/JiaqiWa/IV-16-17/blob/hit0/CapturasDePantalla/cpuinfo.PNG)

Mi procesador es un **Intel(R) Core(TM) i7-6500U CPU @ 2.50GHz**

Estoy usando ubuntu 16.04 instalado en VirtualBox, por lo tanto, al ejecular el comando '''egrep '^flags.\*(vmx|svm)' /proc/cpuinfo''' no muestra ningún salida, pero el sistema window 10 sí soporta la virtualización a nivel hardware. Activé la virtualización en BIOS y además podemos ver en la siguiente captura que VT-x está habilitada:
![captura](https://github.com/JiaqiWa/IV-16-17/blob/hit0/CapturasDePantalla/vt-x.PNG)


##EJERCICIO-5:
###1.Comprobar si el núcleo instalado en tu ordenador contiene este módulo del kernel usando la orden kvm-ok.

Al ejecutar este comando, la información que muestra es:
![captura](https://github.com/JiaqiWa/IV-16-17/blob/hit0/CapturasDePantalla/kvm-ok.PNG)

###2.Instalar un hipervisor para gestionar máquinas virtuales, que más adelante se podrá usar en pruebas y ejercicios.
Ya dispondo el hipervisor VirtualBox en mi equipo.
