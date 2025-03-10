# Autores:
* Juan Diego Alvarez Beltran 120688
* Nicolas Rodriguez Diaz 112572
# Servomotores
Los servomotores mueven una variable hacia un punto especifico donde seguiran comandos de posicion, velocidad, torque.
Estas variables controladas (posicion, velocidad, torque) seran las que nos aseguraran el control de el servomotor, la posicion sera nuestro objetivo final.

### Tipos de motores utilizados en la industria y sus caracteristicas

- Motores Dc : Son los menos utilizados en el control de movimiento ya que el costo de estos es muy altos y sus aplicaciones en la industria son muy limitadas, estos son utilizados normalmente para aplicaciones pequeñas en la industria ya que para mover cargas grandes necesita de mayor bobinado lo que resulta en un mayor tamaño, el desgaste de este es mayor en comparacion a los motores AC, su mantenimiento es complejo y la parte mecanica suele desgastarse con mayor facilidad y producen polucion.

- Motores Ac induccion o asincronos: estos motores a diferencia de los motores Ac sincornos no tienen imanes de neodimio que me generen un campo magnetico para realizar el movimiento, estos tienen un bobinado en el rotor al igual que el sincrono pero el estator tambien tiene bobinado, al exitar el estator estos inducen una corriente en el embobinado que no esta energizado generando asi un campo magnetico que produce el movimiento, a diferencia de los sincronos estos motores al necesitar mover una carga mayor requieren un mayor bobinado es decir un mayor tamaño por esta razon los motores sincronos son los mas utilizados en el campo de control de movimiento, requieren poco mantenimiento y son muy eficazes para altas velocidades y grandes torques.
![Esquema control de movimiento de un motor](https://www.editores-srl.com.ar/sites/default/files/ricardo_berizzo_20211117_figura_1_full.jpg)
foto sacada de:https://automatismoindustrial.com/curso-servomotores-ejes-electricos/el-motor-sincrono/:
- Motores Ac Sincronos: los motores sincronos son motores que tienen una combinacion de enbobinado e imanes de neodimio, de esta manera se genera un campo magnetico que permite el movimiento de este cuando el rotor es exitado, este es atraido por los imanes de neodimio que iran cambiando de polaridad para que el movimiento de este sea constante, es un motor sincrono por que el rotor gira a la misma velocidad del campo magnetico que genera el estator, son poco ruidosos y muy efectivos para la aplicacion en control de movimiento ya que son muy eficientes en la generacion de grandes torques, requiere poco mantenimiento, gracias a su rotor y a los imanes de neodimio puede generar demasiada energia para ser tan compactos.

![Esquema control de movimiento de un motor](https://i0.wp.com/automatismoindustrial.com/wp-content/uploads/2021/10/sin2.png?ssl=1)
foto sacada de: https://automatismoindustrial.com/curso-servomotores-ejes-electricos/el-motor-sincrono/

En el control de movimiento no solo es importante conocer el comportamiento de los motores y la forma en la que trabajan, ya que la seleccion de los motores no puede ser al azar, para la saleccion de este tenemos que tener en cuenta las curvas caracteristicas de los motores y como estan diseñados estos para saber si van a cumplir con la tarea seleccionada. 

![Esquema control de movimiento de un motor](https://lh5.googleusercontent.com/proxy/6AF0DV3Ypke6tw9VYi_eJv6sUbGC4OJIQ1Eklh-3HOvrhQKZkK_--ffMYjnu7aIBnUiNlTB8OHCGaGF-njc9BmEEHfY0r5hyU0Q)
![Esquema control de movimiento de un motor](https://www.editores-srl.com.ar/sites/default/files/ricardo_berizzo_20211117_figura_3.jpg)

En esta imagen podemos ver el comportamiento de un motor de induccion donde vemos el comprotamiento del torque de este motor al momento de variar la frecuencia nominal con la que se esta trabajando. se deduce que al aumentar la frecuencia nominal de este motor el torque decaera de manera significativa.
![Esquema control de movimiento de un motor](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9c/Control_3.jpg/1402px-Control_3.jpg)
Cada motor tiene su propio datasheet donde nos indicaran el comportamiento del motor, en la imagen anterior podemos ver la curva de torque vs velocidad de un motor sincrono, se nos muestran 2 torques un torque nominal (1475) que esta representado por la linea punteada -- - --  y un torque incial (1500) representado por la linea continua -- cuando la velocidad es 0 este sera el torque necesario para vencer toda la inercia del motor, al momento del que motor vence la inercia mecanica y logra el moviemiento, el torque ira disminuyendo hasta llegar al torque nominal que es donde el motor trabajara la mayor parte del tiempo.


![Esquema control de movimiento de un motor](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQaFpg5bteckxYopAobIASoYY4m9Dk_1hB8YxZDKTCUpSs5fEkc)


Hay motores que tienen un diseño diferente y es posible trabajarlos a alto torque pero durante un periodo muy corto, en caso de que el torque supere su torque pico el motor se quemara y no sera posible trabajar con el. 
![Esquema control de movimiento de un motor](https://www.avigan.com.ua/library/Content/G_D212_XX_00004.JPG)


# Concluciones
- Los servomotores como actuadores son posibles de controlar, pero no siempre significa que esten aptos para cumplir con los requerimientos del sistema, es necesario saber seleccionar el tipo de motor dependiendo de las caracteristicas especificas de cada uno y la aplicacion para la que se requiera.
- Es posible realizar diferentes tipos de validacion previos a el uso fisico de un motor, para obtener los valores aproximados a los datos dados por el fabricante y asi entender el comportamiento y poder controlar el motor de manera eficiente.

# Referencias 
- [Qué es un servomotor: Definición, orígenes, componentes, tipos y aplicaciones - ADVANCED Motion Controls](https://www.a-m-c.com/es/servomotor/?form=MG0AV3)
- https://aulas.ecci.edu.co/mod/resource/view.php?id=217536
- [Servomotores: una guía completa sobre tipos, construcción, trabajo, control y aplicaciones industriales - Electrocenter](https://electrocentercol.com/blog/servomotores-tipos-construccion-trabajo-control-y-aplicaciones/?form=MG0AV3)
- https://automatismoindustrial.com/curso-servomotores-ejes-electricos/el-motor-sincrono/

