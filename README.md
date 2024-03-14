# LAB-2

Reporte de la segunda práctica de LRT4012

Diego de Jesús Gutiérrez Reyes 165096

# Introducción
## Creando paquetes catkin en ROS##
Para que un paquete de ROS se considere catkin, es necesario que cumpla unas erie de parámetros, dentro de los cuales destacan lo siguientes:

1.- El paquete debe contener un archivo package.xml compatible con catkin.

2.- El paquete debe contener un CMakeLists.txt que usa Catkin.

3.- Cada paquete debe tener su propia carpeta.

Para crear un nuevo paquete es necesario ejecutar los siguientes comandos en orden:

$ cd ~/catkin_ws/src

$ catkin_create_pkg *Nombre del paquete* std_msgs rospy roscpp

Esto crea un paquete dependiente de std_msgs, rospy y roscpp. Dentro de los paquetes es posible introducir la información y códigos necesarios para que funcione el proyecto.

## Publisher and Writing Nodes ##
Un nodo es el término para un ejecutable que está conectado a la red ROS, estos nodos psoeen características especiales que se les pueden programar, dos nodos altamente empleados son el *talker* y *listener*, los cuales permiten el envío y recepción de nformación respectivamente.

Ambos nodos se pueden programar directamente en python, de modo que al ejecutar el espacio de trabajo catkin, estos comenzarán a funcionar.

## TurtleSim de ROS ##
ROS posee diversas herramientas destinadas al propio aprendizaje de sus sistema, una de estas herramientas en el robot TurtleSim (Figura 1), el cual simula unat tortuga, a partir de la cual se le ueden hacer modificaciones para practicar el uso de nodos y paquetes en ROS.

![image](https://github.com/DiegoJGutierrezReyes/LAB-2/assets/132300202/2f4c3d2d-9671-4e91-9da9-64c6f77424f1)

## Controladores P, PI y PID ##
Los controladores de procesos son necesarios para diseñar sistemas seguros y productivos, gracias a estos es que es posible que el sistema se regule a sí misma a partir de un resultado, existen una gran cantidad de controladores, algunos de los más básicos son el P, PI y PID.

El controlador proporcional (P), es la forma más sencilla de control y se caracteriza por minimizar la fluctuación en la variable de procesos, proporciona una respuesta rápida, pero al aplicarse en un sistema complejo, la diferencia de tiempo de respuesta se acumula, lo que provoca que el controlador responda más tarde  lo requerido, lo que genera desviación.

El controlador Proporcional-Integral (PI), es un controlador que mezcla el control poroporcional e integral, de este último se destaca porque es capaz de corregir cualqueir desviación que exista, de modo que el controlador PI, si bien es más lento en respeusta que el controlador P, posee la capacidad de devolver al sistema a su punto de ajuste, este controlador correlaciona la salida del controlador con el error y la integral del error.

Por último, el controlador Proporiconal-Integral-Derivado, es la mezcla del controlador PI sumándole un controlador derivado (D), la adición de este útlimo permite aumentar la respuesta del controlador porque predice perturbaciones al sistema midiendo el cambio en el error. Este controlador correlaciona la salida del controlador con el error, la integral del error y la derivada del error, si bien es el que mejor funciona de los 3, también es el más caro y complciado de diseñar.

# Nivel Básico

Para completar el nivel básico de la practica, se requiere crear un paquetes denominado "practicas_lab" de ros con las dependencias rospy, roscpp y std_msgs, esto se realiza mediante los siguientes comandos:

$ cd ~/catkin_ws/src
$ catkin_create_pkg practicas_lab std_msgs rospy roscpp

Posteriormente se requiere agregar archivos correspondientes a nodos listener y talker dentro de esta carpeta, para ello es necesario acceder al siguiente repositorio de GitHub:

https://github.com/cesar-martinez-torres/Formatos_LRT4102/tree/main/Codigos_clase/Lab2/Basic

Con la dirección URL obtenida, se deben de clonar los archivos de Python en nuestra carpete practicas_lab, para ello es posbile emplear el siguiente comando:

git clone https://github.com/cesar-martinez-torres/Formatos_LRT4102/tree/main/Codigos_clase/Lab2/Basic

Con los archivos copiados dentro de nuestra carptea, es necesario compilar el paquete, una vez compilado se abre el Visual Code Studio para ejecutar los archivos de Python, cuandos se ejecuten, el archivo talker.pt comenzará a emitir un mensaje, el cual se podrá ver desde el programa listener.py

[IMAGENE DEL TALKER Y LISTERNER, TANTO CÓDIGO COMO RESULTADO].


# Nivel Intermedio

Para el nivel intermedio se requieren cumplir 2 objetivos, el primero es crear un control por teclado para el turtle sim, de modo que el usuario pueda controlar por si mismo el movmiento de la torturga. El segundo objetivo es dibujar un cuadrado y un triángulo equilatero de forma automática.

## Control por teclado

Para controlar mediante el teclado el turtlesim, el nodo Publisher contendrá la solicitud de introducción de la información, que en este caso corresponde al teclado, por su parte, el nodo Listener será el Turtle Bot.

Para leer las teclas en Python se emplea la función *input()*, la cual solicita una entrada de datos y la guarda en una variable de tipo cadena, en caso de requerir otro tipo de variable se debe de emplear el uso de un tipo de variable y colocar la función input dentro de esta.

Las teclas empleadas para el movimiento de la tortuga son: **LETRAS DEL TECLADO** 

Tras la solicitud e ingreso de la información, se manda al Turtlesim, de modo que este realizará lsos movimientos según indiquen los mensajes.

En la siguiente Figura se observa una ruta de la tortuga realizada por el usuario, mientras que en la segunda imagen se observa los mensaje senvíados para realizar dichos movimientos.


## Dibujar cuadrado y tríangiulo de modo autónomo

Para realizar este objetivo se requiere mandar las rutas predeterminadas al robot, de modo que al ejecutar el programa el robot ejecute la secuencia. Las Figuras creadas se muestran en las siguientes Figuras.



# Nivel Avanzado

## Controlador P



## Controlador PI


## Controlador PID




