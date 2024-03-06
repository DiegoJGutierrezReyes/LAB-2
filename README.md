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

El controlador proporcional (P), es la forma más sencillad e control y se caracteriza por minimizar la fluctuación en la variable de procesos, proporciona una respuesta rápida, pero al aplicarse en un sistema complejo, la diferencia de tiempo de respuesta se acumula, lo que provoca que el controlador responda más tarde  lo requerido, lo que genera desviación.

El controlador Proporcional-Integral (PI), es un controlador que mezcla el control poroporcional e integral, de este último se destaca porque es capaz de corregir cualqueir desviación que exista, de modo que el controlador PI, si bien es más lento en respeusta que el controlador P, posee la capacidad de devolver al sistema a su punto de ajuste, este controlador correlaciona la salida del controlador con el error y la integral del error.

Por último, el controlador Proporiconal-Integral-Derivado, es la mezcla del controlador PI sumándole un controlador derivado (D), la adición de este útlimo permite aumentar la respuesta del controlador porque predice perturbaciones al sistema midiendo el cambio en el error. Este controlador correlaciona la salida del controlador con el error, la integral del error y la derivada del error, si bien es el que mejor funciona de los 3, también es el más caro y complciado de diseñar.




