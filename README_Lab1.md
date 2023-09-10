

# Robotica Laboratorio 1

## Integrantes

- Norma Lorena Martinez Zavala
- Miguel Angel Sarmiento Cabarcas
- Jaime Andres Sanchez Peralta


### 1. Descripción de la solución planteada.

Para la solución de este problema, debe crearse un nuevo proyecto, seleccionandose un robot tipo IRB140_6_81, la referencia que se encuentra en el laboratorio. Se seleccionó un controlador virtual 6.15.03 Build 3019.
Se crea un objeto de trabajo(El pastel) y se coloca en el cuarto cuadrante (+ -) con respecto al eje de coordenadas wobj0, el cual es creado en el centro de la base del robot.

<img src="/cuadrantes.png">

Se puede evidenciar en la imagen un bloque de dimensiones 18cmx18cmxN, sobre las que se encuentran las coordenadas que conforman los nombres y la figura.

<img src="/curvas.png">

En esta imagen se puede observar mejor detalladas las curvas de los trazos.

<img src="/BrazoF2.png">
<img src="/BrazoFisico.png">


En estas imagenes se muestra como se posiciona el robot sobre el area de trabajo.

Los materiales necesarios para la construcción de la herramienta, serán detallados con precios más adelante en el documento, aquí se presenta el resultado físico de la implementación del modelo:


<img src="/Herramienta.png">




### 2. Diagrama de flujo de acciones del robot <p>
[![Whats-App-Image-2023-09-09-at-8-21-37-PM.jpg](https://i.postimg.cc/63Y674s5/Whats-App-Image-2023-09-09-at-8-21-37-PM.jpg)](https://postimg.cc/tZnGwTCL) <p>
### 3. Plano de planta de la ubicación de cada uno de los elementos.
Se presenta a continuación una imagen del plano de planta, el cual se puede encontrar como /layout.pdf
 ![image](https://github.com/misarmientoc/Robotica/assets/66492359/f284043a-641f-4f7f-bf3f-3810d222082f)
  
### 4. Descripción de las funciones utilizadas.

El código está organizado en módulos y procedimientos (PROC). Cada procedimiento representa una secuencia la secuencia de movimientos que el robot debe llevar a cabo.
Como primera función, se tiene la función main(), que es el punto de entrada principal del programa. Cuando se ejecuta el programa, la ejecución comienza en esta función la cual llama a las funciones Path_10(), Path_20(), Path_30(), y Path_40(). Siendo estas las funciones que contienen las secuencias de movimientos específicos que el robot debe realizar. <p>
 [![Captura.png](https://i.postimg.cc/sgHfTrBT/Captura.png)](https://postimg.cc/68RNQFfZ) <p>
Ilustración 1. Función main() <p>

Posterior al main(), se tiene la función Path10(), la cual corresponde al primer nombre en el pastel. En esta función, se definen los parámetros con los que el robot va a trabajar. Primero tenemos el comando “MovelJ”, la cual le indica al robot que debe moverse al punto especificado.
Después se indica la velocidad con la que va a trabajar el robot, en este caso fue configurada a 100, tanto para la velocidad general como para la velocidad en el eje z (v100 y z100, respectivamente).
Después, simplemente se específica la herramienta con la que se va a trabajar y el área de trabajo (ToolR\WObj:=Caja).><p>
[![Captura1.png](https://i.postimg.cc/7Z5rYT6N/Captura1.png)](https://postimg.cc/zyYcxvTL) <p>
 
Ilustración 2. Función Path10()
Como se puede visualizar en la imagen 2, se manda esta serie de instrucciones para cada uno de los puntos dónde se moverá el robot.
Cada palabra realizada por el robot está contenida en una función Pathx(). <p>

•	Path10(): Corresponde a la primera palabra “JAIME”. <p>
•	Path20(): Corresponde a la segunda palabra “LOREN”. <p>
•	Path30(): Corresponde a la tercera palabra “MIGUE”. <p>
•	Path40(): Corresponde al dibujo hecho en el pastel. <p>

Al final de cada procedimiento de movimiento, se llama a otro procedimiento, como Path_50(), Path_60(), Path_70(), que también son secuencias de movimiento específicas, estas corresponden a la transición que hay de una palabra a otra. <p>
[![Captura2.png](https://i.postimg.cc/4dZ0tKJq/Captura2.png)](https://postimg.cc/McPtJpfm) <p>
 
Ilustración 3. Funciones de transición de palabras. <p>

### 5. Diseño de la herramienta.
   
   Se busco que la heraramienta fuera lo mas sencillo de construir y de facil montaje, ademas que evitara singularidades por angulos no permitidos en el robot, es decir que la linea del eje de las articulaciones no fuera    perpendicular a la linea de accion de la herramienta, tambien se coloco una almohadilla en caucho para darle flexibilidad y evitar que se dañara la punta del marcador, los materiales y su costo fueron

| Item | Descripción      | Costo |
|------|------------------|-------|
| 1    |Brida MDF         | $6.000|
| 2    |Tubo PVC 1/2"     | $1.000|
| 3    |Unión PVC         | $2.000|
| 4    |Colgante galvaza  | $2.000|
| 5    |Tornillos golosos | $  600|
| 6    |Caucho almohadilla| $1.000|
| 6    |Marcador          | $3.000|
|      |Total             |$12.600|


<img src="/Plano_planta.png">

El archivo STEP del modelo de la herramienta se encuentra en el siguiente link 

https://github.com/misarmientoc/Robotica/blob/main/Herramienta.stp

   
### 6. Código en RAPID del m´odulo utilizado para el desarrollo de la práctica.

   El código en RAPID se encuentra en la siguiente direción 

https://github.com/misarmientoc/Robotica/blob/main/Module1.mod
   
### 7. Vídeo que contenga la simulación en RobotStudio así como la implementación de la práctica con los robots
reales.

### Simulación 

- https://youtu.be/F7px0tGtAVw

- https://youtu.be/npnxBCHKuRM


  




 


