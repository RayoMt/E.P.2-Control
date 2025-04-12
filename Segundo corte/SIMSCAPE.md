# Autores 
Nicolas Rodriguez Diaz 112572
Juan Diego Alvarez Beltran 120688
# Simscape
- Continuamos en simscape realizando diferentes modelos para la comprension de los bloques y la practica con estos.

# Articulaciones rotacionales
El primer modelo a realizar se trata de un conjunto de 3 eslabones unidos por articulaciones rotacionales.

![](https://static.wixstatic.com/media/ac2048_f751c60d66f148cebfdc4538df82bd56~mv2.png/v1/fill/w_762,h_333,al_c,q_85,enc_avif,quality_auto/ac2048_f751c60d66f148cebfdc4538df82bd56~mv2.png)

Para comenzar con cualquier modelo recordemos que siempre se debe de cambiar el eje donde se efectuara la gravedad.

![1rotacional](c2/rotacional/1.png)

Ya que nuestro mecanismo tiene el eslabon junto a una articulacion rotacional debemos generar un frame donde podamos unir nuestra articulacion con este eslabon, de igual manera creamos un frame pero ahora sobre el borde y no sobre la cara para unirlo al otro eslabon.

![2rotacional](c2/rotacional/2.png)
![3prismatica](c2/rotacional/3.png)
![4prismatica](c2/rotacional/4.png)
![5prismatica](c2/rotacional/5.png)
Ya habiendo generado nuestro primer eslabon podemos copiar y pegar para usar el mismo diseño para nuestro 2 y 3 eslabon, pero teniendo en cuenta que la ubicacion de los frames en cada eslabon son deferentes.

Por este motivo en nuestro segundo eslabon cambiaremos la posicion del frame de union con los eslabones recordando que cada eslabon tiene una junta rotacional.

![6rotacional](c2/rotacional/6.png)
![7rotacional](c2/rotacional/7.png)
![8rotacional](c2/rotacional/8.png)

De igual manera cambiamos los frames de nuestro tercer eslabon para lograr unirlos al segundo eslabon.

![9rotacional](c2/rotacional/9.png)
![10rotacional](c2/rotacional/10.png)

Cuando realizamos la simulacion lograremos ver que nuestro modelo no quedo igual al modelo planteado y esto se debe a la implementacion de un nuevo bloque que se llama  trasformacion rigida.

![11rotacional](c2/rotacional/11.png)
![12rotacional](c2/rotacional/12.png)

Esta trasformacion rigida nos permite realizar 2 tipos de trasformaciones sobre los ejes que son la rotacion de los ejes y la traslacion de los ejes, en este caso ultilizaremos la tarslacion del eje para que nuestro 3er eslabon no se una al incio de nuestro mundo al mismo lugar donde se une nuestro primer eslabon.

![13rotacional](c2/rotacional/13.png)

De esta manera ya comprendimos el uso de las articulaciones rotacionales y la implementacion de estas.

# Articulaciones prismaticaas
Las articulaciones prismaticas son articulaciones que nos permiten generar movimiento de igual manera que las rotacionales, las dos generan movimiento en el eje z solo que de manera recta.

![1prismatica](c2/prismatica/1.png)
De la misma forma que en todos nuestros modelos anteriores cambiamos la gravedad de nuestro mundo.

![2prismatica](c2/prismatica/2.png)
En las articulaciones que nos permiten movimiento tienen configuraciones para estipular condiciones de este movimiento, para la articulacion rotacional nos ayudamos de la gravedad, en este caso induciremos el movimiento.
![3prismatica](c2/prismatica/3.png)
![4prismatica](c2/prismatica/4.png)
![5prismatica](c2/prismatica/5.png)
De igual manera las articulaciones que nos permiten movimiento nos permiten sensar y verificar las condiciones y acciones que estan sucediendo sobre este.
![6prismatica](c2/prismatica/6.png)

En este caso como le induciremos un movimiento verificaremos la posicion de la articulacion.
![7prismatica](c2/prismatica/7.png)

Para generar nuestro movimiento aplicaremos una señal senosoidal a la entreda generada en nuestro bloque que conectaremos por medio de un bloque de conversion.

![8prismatica](c2/prismatica/8.png)
![9prismatica](c2/prismatica/9.png)
En el bloque de conversion debemos realizar unos ajustes debido al movimiento inducido, ya que este bloque nos solicita que le indiquemos la posicion velocidad y aceleracion, pero como en esta ocacion solo realizaremos posicion activaremos un filtro para que el bloque calcule la velocidad y aceleracion.
![10prismatica](c2/prismatica/10.png)

de esta manera ya tendremos movimiento en nuestro bloque y podemos verificar la posicion por medio de nuestro scope.

![11prismatica](c2/prismatica/11.png)

![13prismatica](c2/prismatica/13.png)

El movimiento generado por la articulacion siempre sera en el eje Z pero por medio de nuestro bloque de trasformacion rigida y la opcion que nos permite rotar los ejes podremos realizar movimiento sobre cualquier eje, esta opcion de rotacion tiene muchas formas de parametrizar, utiliaremos el metodo de alineacion de ejes donde le indicaremos al bloque cuales seran nuestro ejes que rotan y como quedaras alineados.

![12prismatica](c2/prismatica/12.png)

En este caso como queremos que nuestro movimiento sea en el eje X y como sabemos que la articulacion efectua el movimiento en el eje Z asignaremos como base el eje Z y en la actualizacion siguiente asignaremos el eje donde queremos el movimiento en este caso el eje X, como en este metodo de asignacion hay 2 pares asignaremos en el segundo caso la alineacion de el eje Y en ambos ya que no es necesario rotar este eje.

![14prismatica](c2/prismatica/14.png)
De esta manera ya tendremos el movimiento en el eje X.
![15prismatica](c2/prismatica/15.png)
![16prismatica](c2/prismatica/16.png)
![17prismatica](c2/prismatica/17.png)

# Biela manivela corredera

![](https://clanhackerspace.wordpress.com/wp-content/uploads/2015/02/biela_manivela_ensamblaje.jpg)

Utilizaremos lo aprendido y practicado para realizar un mecanismo un poco mas complejo que se usa en la industria para tareas repetitivas.

Para empezar cambiaremos la posicion de la gavedad, fabricaremos el primer solido que sera nuesta biela y colorcaremos los frames en las caras externas de la biela.
![1biela_manivela](c2/biela/1.png)
![2biela_manivela](c2/biela/2.png)
![3biela_manivela](c2/biela/3.png)
Uniremos la biela que generamos por el frame 1 a una articulacion de rotacion, de igual manera como nuestra manivela se unira a la biela.

![4biela_manivela](c2/biela/4.png)
al finalizar las conexiones de nuestros eslabones por medio de las articulaciones podemos simular el proceso de las uniones y visualizaremos las rotaciones de las articulaciones, 

![5biela_manivela](c2/biela/5.png)
![6biela_manivela](c2/biela/6.png)

Para realizar la rotacion prismatica de nuestro efector final es necesario conectar nuestro bloque de movimiento prismatico al mundo pero realizar una rotacion de los ejes con el bloque de trasformaciones rigidas de los ejes.

en este caso tendremos que cambiar 2 veces nuestros ejes, en la salida de nuestra manivela al conector de nuestra corredera ya que nuestro movimiento de rotacion viene en el eje Z y para el desplazamiento de la corredera es necesario mantenerlo en el eje Y por esta razon la base de nuestra rotacion es el eje Z y nuestro seguidor sera el eje Y mientras mantenemos el eje X fijo.

![7biela_manivela](c2/biela/7.png)

En la segunda rotacion que sera de nuestra corredera al inicio del mundo no dejaremos un eje fijo ya que en la primera trasformacion utilizamos el eje Y para cambiar el eje de rotacion con la corredera, por este motivo cambiaremos este eje Y por el eje X, y de igual manera como nuestro bloque prismatico solo permite el movimiento en el Z reasignaremos el eje X al eje Z.
![8biela_manivela](c2/biela/8.png)
![9biela_manivela](c2/biela/9.png)
![10biela_manivela](c2/biela/10.png)
# Concluciones
- En la aplicacion de bloques de movimiento es necesario tener claridad en la ubicacion de los ejes para cumplir con el requerimiento ya que la fallar en la ubicacion de estos evitara el movimiento del modelo.
- Con la trasformacion de los ejes por medio del bloque de trasformacion rigida se crean diferentes maneras de resolver sistemas pero para esto es necesario tener claridad de las dimensiones de los objetos como su ubicacion en el plano.
- Con la facilidad de los bloques a la hora de medir variables nos permite tener una compresion mas clara y sencilla de las acciones que esta realizando nuestro modelo.
