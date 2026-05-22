# sesion-09b

# Apuntes clase 15/05

Esta clase se dedicó para resolver todo tipo de dudas que se nos hayan generado en el proceso del encargo anterior el cual fue armar dos PCB dentro de KiCad en base a nuestros sintetizadores. Como se abordaron dudas de todo tipo, esta bitacora será un punteo de cosas que no sabía y me alegro de que se hayan mencionado:

#### Huella con tamaño predeterminado para chips

Al momento de asignar huellas, siempre usaremos la siguiente "base" para encontrarlas: ``dip-(cant. de pins) W (ancho) 7.62 - long pads``, el que sea "long pads" no es obligatorio pero es lo ideal ya que esto nos ayudará a que sea más fácil el soldado de la pieza. Aquí un ejemplo de la huella en el símbolo del chip NE555P:

![Huella longpads en 555](./imagenes/longpads-555.png)

#### Cómo editar un símbolo en el esquemático

Esta fue mi duda, ya que en el caso del chip 555 el pin 5 que va directo a GND está en la parte superior del chip, lo cual me molestaba ya que es más simple si todos los pins que van directo a GND se mantienen abajo.

Para poder editar el símbolo, tenemos que seleccionarlo dentro del esquemático y presionar la tecla ``E`` para poder ver las propiedades del símbolo. Una vez nos aparezca la ventana de propiedades, tenemos que seleccionar la opción de ``Editar símbolo`` y **NINGUNA OTRA OPCIÓN!!** ya que podemos dañar archivos de KiCad y llevarnos la pala (quedaría la pura escoba.. perdón).

![Opciones dentro de las propiedades](./imagenes/editar-simbolo.png)

Una vez ya estemos dentro del editor de símbolos, podemos mover los pines como queramos, añadir más, cambiar el color del símbolo, cambiar los textos, etc. Cuando ya tengamos todo modificado, tenemos que guardar y listo!! 
