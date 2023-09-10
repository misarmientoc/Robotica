

# Robotica Laboratorio 1

## Integrantes

- Norma Lorena Martinez Zavala
- Miguel Angel Sarmiento Cabarcas
- Jaime Andres Sanchez Peralta


1. Descripción de la solución planteada.

Para la solución de este problema, debe crearse un nuevo proyecto, seleccionandose un robot tipo IRB140_6_81, la referencia que se encuentra en el laboratorio. Se seleccionó un controlador virtual 6.15.03 Build 3019.
Se crea un objeto de trabajo(El pastel) y se coloca en el cuarto cuadrante (+ -) con respecto al eje de coordenadas wobj0, el cual es creado en el centro de la base del robot.

![image](https://github.com/misarmientoc/Robotica/assets/66492359/7813bcfb-5279-479a-8c3e-401e874176ab)

Se puede evidenciar en la imagen un bloque de dimensiones 18cmx18cmxN, sobre las que se encuentran las coordenadas que conforman los nombres y la figura.

![image](https://github.com/misarmientoc/Robotica/assets/66492359/d9059fda-b45f-4b79-b9a3-d2c11496dded)

En esta imagen se puede observar mejor detalladas las curvas de los trazos.

![image](https://github.com/misarmientoc/Robotica/assets/66492359/6251e5ae-a1ab-4e13-8da8-188a36668ead)
![image](https://github.com/misarmientoc/Robotica/assets/66492359/ba61187e-594a-4b40-bf35-d868ee84b68a)

En estas imagenes se muestra como se posiciona el robot sobre el area de trabajo.



2. Diagrama de flujo de acciones del robot
3. Plano de planta de la ubicación de cada uno de los elementos.
4. Descripción de las funciones utilizadas.

El código está organizado en módulos y procedimientos (PROC). Cada procedimiento representa una secuencia la secuencia de movimientos que el robot debe llevar a cabo.
Como primera función, se tiene la función main(), que es el punto de entrada principal del programa. Cuando se ejecuta el programa, la ejecución comienza en esta función la cual llama a las funciones Path_10(), Path_20(), Path_30(), y Path_40(). Siendo estas las funciones que contienen las secuencias de movimientos específicos que el robot debe realizar.
 
Ilustración 1. Función main()

Posterior al main(), se tiene la función Path10(), la cual corresponde al primer nombre en el pastel. En esta función, se definen los parámetros con los que el robot va a trabajar. Primero tenemos el comando “MovelJ”, la cual le indica al robot que debe moverse al punto especificado.
Después se indica la velocidad con la que va a trabajar el robot, en este caso fue configurada a 100, tanto para la velocidad general como para la velocidad en el eje z (v100 y z100, respectivamente).
Después, simplemente se específica la herramienta con la que se va a trabajar y el área de trabajo (ToolR\WObj:=Caja).
 
Ilustración 2. Función Path10()
Como se puede visualizar en la imagen 2, se manda esta serie de instrucciones para cada uno de los puntos dónde se moverá el robot.
Cada palabra realizada por el robot está contenida en una función Pathx().

•	Path10(): Corresponde a la primera palabra “JAIME”.
•	Path20(): Corresponde a la segunda palabra “LOREN”.
•	Path30(): Corresponde a la tercera palabra “MIGUE”.
•	Path40(): Corresponde al dibujo hecho en el pastel.

Al final de cada procedimiento de movimiento, se llama a otro procedimiento, como Path_50(), Path_60(), Path_70(), que también son secuencias de movimiento específicas, estas corresponden a la transición que hay de una palabra a otra.
 
Ilustración 3. Funciones de transición de palabras.

6. Diseño de la herramienta.
   
   Se busco que la heraramienta fuera lo mas sencillo de construir y de facil montaje, ademas que evitara singularidades por angulos no permitidos en el robot, es decir que la linea del eje de las articulaciones no fuera    perpendicular a la linea de accion de la herramienta, tambien se coloco una almohadilla en caucho para darle flexibilidad y evitar que se dañara la punta del marcador, los materiales y su costo fueron

| Item | Descripción      | Costo |
|------|------------------|-------|
| 1    |Brida MDF         | $6.000|
| 2    |Tubo PVC 1/2"     | $1.000|
| 3    |Unión PVC         | $2.000|
| 4    |Colgante galvaza  | $2.000|
| 5    |Tornillos golosos | $  600|
| 6    |Caucho almohadilla| $1.000|
|      |Total             |$12.600|


![image](https://github.com/misarmientoc/Robotica/blob/main/Herramienta.png)

   
7. Código en RAPID del m´odulo utilizado para el desarrollo de la práctica.

   El código en RAPID se encuentra en la siguiente direción 

https://github.com/misarmientoc/Robotica/blob/main/Module1.mod
   
9. Vídeo que contenga la simulación en RobotStudio así como la implementación de la práctica con los robots
reales.

### Simulación 

- https://youtu.be/F7px0tGtAVw

- https://youtu.be/npnxBCHKuRM


  




 


