# sesion-09b
## 15, May
### Apuntes
En esta clase vimos diferentes dudas entre todos, nos ayudamos y se resolvieron muchas trancas que yo también tenía :) ¡Así que esta sesión fue de mucha ayuda!

#### **1. Conceptos de PCBs y Chips**

* **Conexiones eléctricas:** Las PCBs se conectan de varias formas a la corriente. Si tienes varios circuitos, Aaron recomendó hacer los esquemáticos y las placas por separado, porque cada una actúa sola y así es más limpio.
* **Tipos de encapsulado:** No hay que confundirse entre **THT** (los componentes con patas largas que atraviesan la placa) y **SMD** (los chiquititos que van soldados directo sobre la superficie).
* **El estándar:** Nosotros vamos a usar el encapsulado **DIP de 7.62 mm (LongPads)**, que es el chip típico de patitas, el más común y cómodo para soldar a mano.
* **Dato útil:** Misa subió un glosario de KiCad al grupo por si nos perdemos con los nombres :)

#### **2. Hacks y Comandos para el Esquemático en KiCad**

* **Personalizar símbolos:** Si queremos cambiar la posición de las patitas de un chip (como el 555) o editar nombres de pines, seleccionamos el componente y apretamos la tecla **E** ➞ *Edit Symbol*. Para mover las cosas adentro usamos la **M**. ¡Ojo! No hay que romper los símbolos originales de las librerías de KiCad, para eso se hace un fork (copia).
* **Crear tu propia biblioteca:** Vas al *Symbol Editor* dentro de tu proyecto con extensión `.pro` ➞ Menú superior: *View* ➞ *Panels* ➞ *Library Tree*. Con las librerías activadas pones *File* ➞ *New Library* y guardas tu carpeta. Ahí puedes copiar cualquier componente común, pegarlo en tu carpeta, editarlo y darle *Ctrl + S* para guardar.
* **Etiquetas (Labels):** Para conectar cosas en el esquemático sin llenar todo de líneas y cables raros, apretamos la **L**. Esto te salva del típico error de "pin no conectado".
* **¡Truco de alimentación!** Para la salida de la batería hay que conectar la etiqueta **PWR_FLAG** para que KiCad sepa de dónde viene la energía y no tire alertas.

#### **3. Botones, Interruptores y Modelado 3D**

* **Botones temporales (Pulsadores / Pushbuttons / Timbres):** Los más comunes son los **NO** (*Normally Open* / Normalmente Abierto, que solo conducen cuando los dejas apretados). También están los **NC** (*Normally Closed* / Normalmente Conectado, que cortan la corriente al pulsarlos).
* **Interruptores de palanca (Switches):** Dependen de las patitas que tengan: **SPST** (2 patas), **SPDT** (3 patas), **DPST** (4 patas) y **DPDT** (6 patas). Para buscarlos en el programa pones `SW_SPST` o `SW_SPDT` y les asignas la huella (*footprint*): `Button_Switch_THT:SW_PUSH_6mm`.
* **Cambiar de cara:** Si quieres pasar un componente de la cara de arriba a la de abajo de la placa, lo seleccionas y usas la **F** (Flip).
* **Modelado 3D:** En el archivo `.pcb`, seleccionas la huella del componente $\rightarrow$ apretas la **E** $\rightarrow$ menú *3D Models* y cargas el archivo que hayas descargado. Para exportar la placa completa lista para mandar a fabricar o mostrar, vas a *File* $\rightarrow$ *Export* $\rightarrow$ *STEP/STL*.

---

#### **4. Reflexiones de Lectura: Capítulos 2 y 3 de Vilém Flusser ("Hacia una filosofía de la fotografía")**

Estuvimos discutiendo el libro en clase y salieron cosas muy locas sobre cómo las imágenes nos confunden de la realidad, limitan la imaginación y nos hacen perder el foco de quiénes somos. Nos meten como en un velo y dejamos de ver el mundo real (como pasa hoy con Instagram).

* **Capítulo 2: La imagen técnica**
Flusser explica la diferencia entre las imágenes tradicionales (los dibujos prehistóricos hechos a mano que significan fenómenos del mundo) y las **imágenes técnicas** (las que produce un aparato, como una cámara o un escáner). Las técnicas son "pos-históricas" porque nacen de textos científicos y tienen un nivel de abstracción gigante (son imágenes de imágenes de imágenes, abstracciones de tercer grado).
Lo peligroso es que las imágenes técnicas parecen una ventana objetiva y real del mundo (como una huella digital o una foto de celular), entonces confiamos en ellas como si fueran nuestros propios ojos. Pero la verdad es que son puras construcciones simbólicas. La famosa **caja negra** es todo lo que pasa en el interior del aparato; el fotógrafo y la máquina deciden cómo se va a interpretar esa realidad.
*Mi reflexión:* Tiene todo el sentido con las redes sociales de ahora, donde vemos miles de fotos al día y nos creemos todo sin saber con qué intención las armaron ni cómo se hicieron.
* **Capítulo 3: Los aparatos**
Acá Flusser dice que la cámara es el ejemplo perfecto de "aparato" (un objeto cultural). Explica que las herramientas antiguas eran una prolongación de nuestro cuerpo (un martillo es como un puño duro, una flecha es como el dedo que apunta), pero los aparatos son distintos: **no transforman el mundo, sino que transforman el significado del mundo** <3
Por eso el fotógrafo no es un trabajador común (*homo faber*), sino un jugador (*homo ludens*) y la cámara es su juguete. Lo que me pareció más brígido es que el fotógrafo cree que elige libremente qué capturar, pero el aparato ya tiene un programa interno escrito por científicos que define de antes qué se puede fotografiar y qué no. Es como jugar al ajedrez: juegas libre, pero solo dentro de las reglas del tablero. Y más encima, ese programa está controlado por la industria, que está controlada por el sistema... o sea, una caja negra metida dentro de otra caja negra.
*Mi reflexión:* Es increíble, onda cuando sacas una foto con el celular, el "modo retrato" ya sabe de antes cómo debe verse un retrato bonito y el "modo noche" ya decidió cómo se tiene que ver la oscuridad . Al final uno solo decide cuándo apretar el botón, pero la máquina ya eligió qué es fotografiable y de qué forma. Su idea es que despertemos para que la tecnología no termine decidiendo por nosotros cómo vemos el mundo.
