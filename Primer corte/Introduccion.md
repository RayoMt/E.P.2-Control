# Autores:
* Juan Diego Alvarez Beltran 120688
* Nicolas Rodriguez Diaz 112572
# Control de movimiento 
En la clase se reconoceran las implementaciones del control de movimiento y su importancia en la industria, donde por medio de diferentes ejemplos comprenderemos la importancia de este y el por que la implementacion de esta resulta en el crecimiento de la industria. 

## Uso de control de movimiento en la industria

- El uso del control de movimento en la industria se lleva acabo por la union de varios ejes, donde todos se sincronizaran para poder cumplir con una tarea especifica, estos ejes seran los actuadores que me aseguren un movimiento, donde en cada eje se colocara una especie de "set point" donde al asegurar la posicion de cada eje nos asegurara el control final, es decir el control de la posicion de todos los ejes, la seleccion de nuestros ejes dependera de los requisitos necesarios y de la carga que se desea mover, los controles de movimiento usan diferentes tipos de sistemas como el hidraulico, neumatico o electromecanico.
Los sistemas electromecanicos son los mas utilizados a la hora de aplicar el control de movimiento, ya que este sistema permite una alta presicion, los motores son los actuadores o ejes que son utilizados en los sistemas electromecanicos. Por este motivo los requisitos a controlar en un motor seran:

- 1. Posicion
- 2. Torque
- 3. velocidad 
- 4. Aceleracion 

Para nuestro eje como servomotor hay que tener en cuenta el como se genera el movimiento de este, mediante la interaccion de campos electromagneticos se genera la energia para vencer la inersia del motor y llevarlo a generar movimiento rotacionales o lineales, no es necesario tener que controlar las 4 variables del motor para obtener el control de movimiento, podemos controlar un conjunto de estas o una sola variable y asi obtener de igual manera control de movimiento esto dependera de la complejidad de cada sistema. 

En la aplicacion de control de movimiento es escensial poder realizar cambios en el proceso sin que se vea afectada, es decir que es posible realizar diferentes procesos con el mismo sistema y esto permite flexibilidad que solo se puede conseguir controlando todos los procesos.

![control de movimiento](https://www.a-m-c.com/wp-content/uploads/images/university%20outreach/servoloop.jpg)
>imagen tomada de: https://www.a-m-c.com/es/experiencia/tecnologias/motion-control/resumen/
En la imagen anterior se puede ver el diagrama de un sistema de retroalimentacion que es usado para controlar la posicion velocidad y aceleracion.
### Componentes para el control de movimiento
- Interfaz de usuario: con la interfaz de usuario se hace posible la interaccion con el sistema, validar el estado de las variables y asi mismo ajustarlas "set point".
- Controladores: Estos dispositivos son los encargados de procesar la informacion de los sensores y asi de esta manera ajustar y enviar la señal a los actuadores para el control de movimiento 
- Driver de potencia: Los drivers de potencia son necesarios para las cargas que se presentan en el sistema. 
- Actuadores : los actuadores o "ejes" seran los encargados de realiazar el movimiento.
- Sensores quienes nos dara nuestra señal de retroalimentacion de nuestras variables
- Elementos mecanicos: los elementos mecanicos son los componentes fisicos  que trasmiten el movimiento como poleas engranajes etc.
#### Diagrama de flujo del control de movimiento
```mermaid
graph LR
Interfaz_de_usuario --> A[Controlador_de_movimiento] --> B[driver_de_potencia]
 --> Actuador
 -->  C[Elementos_mecanicos] --> 
   D[Cargas]
D --> Retroalimentacion_Sensores --> A 
A --> Interfaz_de_usuario
```
Algunos inconvenientes fisicos que se pueden presentar en el control de movimiento sera la inercia de las cargas a las que se condicionara el controlador, entre la carga mas grande, la potencia requerida para el movimiento sera mayor. Por este motivo en el control de movimiento siempre se hara necesario controlar el torque de los ejes para evitar este inconveniente.

## Esquema de control en cascada

![Esquema control de movimiento de un motor](https://controlautomaticoeducacion.com/wp-content/uploads/Control-en-Cascada-1-scaled.jpg)
>imagen tomada de: https://controlautomaticoeducacion.com/control-realimentado/control-en-cascada/

En la imagen anterior se puede ver el diagrama de un sistema de retroalimentacion que es usado para controlar la posicion velocidad y torque de un motor. Cada lazo de retroalimentacion es el control de cada una de las variables del motor, donde la variable mas rapida en este caso el torque $C_{i}$ sera la primera variable que controlaremos de esta manera venceremos las perturbaciones del sistema en cuanto a corriente se refiere, tambien sera la encargada de vencer la inercia de la carga a la que nos enfrentamos, nuestra segundo lazo es el lazo de velocidad $C_{w}$ y nuestro tercer lazo $C_{θ}$

Una de las caracteristicas de nuestro lazo en cascada es que las variables mas internas $C_{i}$ y $C_{w}$ seran las que rechazaran las perturbaciones del sistema, otra caracteristica es que la señal de setpoint de cada lazo es la respuesta del lazo anterior, es decir que nuestro setpoint de la velocidad sera dado por la posicion y nuestro set point de torque sera dada por la velocidad. siempre nuestra variable mas rapida sera el lazo mas interno en nuestro esquema asi de esta manera la respuesta del sistema sera mas rapida

# Concluciones
- Con la implementacion del control de movimiento se han venido ampliando la cantidad de aplicaciones, funcionalidades y automatizaciones de los sistemas facilitando asi la industria y ayudando a su crecimiento
- la versatilidad y adaptavilidad que el control de movimiento nos brinda es muy grande, es posible adaptarse a diferentes aplicaciones 
# Referencias
- https://www.a-m-c.com/es/vista-general-del-control-de-movimiento/?
- https://aulas.ecci.edu.co/mod/resource/view.php?id=217529
- [Fundamentos de Control de Movimientos:Fundamentos de Control de Movimientos.qxd](https://www.infoplc.net/files/documentacion/motion_control/infoPLC_net_Fundamentos_de_Control_de_Movimientos.pdf?form=MG0AV3)
- [content](https://repositorio.utb.edu.co/server/api/core/bitstreams/795fc241-425a-47b9-9275-7a8a5453ce57/content)

