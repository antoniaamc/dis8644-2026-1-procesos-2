# Sesión 10a - martes 19 mayo 2026

Esta sesión fue súper completa porque mezclamos una charla inspiradora en el auditorio con un repaso técnico bien denso en la sala, enfocado en cómo vamos a armar el proyecto final de filtros.

1. Charla en el auditorio: Escaneo LiDAR 🌸

Vinieron Jim, Patrick y Simon a mostrarnos su trabajo. Lo que más me voló la cabeza fue el modelo 3D de una flor hecho con un escáner LiDAR.

* **Dato técnico:** El láser solo captura la superficie exterior (donde rebota), por lo que el interior queda vacío. Es como una "cáscara" de puntos con colores reales y transparencias.
* **Mi lectura:** Cada punto que marca el láser es como un dato que el sistema procesa. Me hizo clic con lo que vemos en electrónica: sensores que captan la realidad y la convierten en información.

2. Pensamiento Sistémico: El "Bosque" y no solo el "Árbol" 🌲

Antes de lanzarnos a los chips, hablamos de una metodología clave: el Pensamiento Sistémico.

* **¿Qué es? Entender que todo está conectado. Si mueves una pieza aquí, hay una consecuencia allá.**
* **Ejemplo práctico:** Si mi LED no prende, el pensamiento lineal dice "el LED está quemado". El pensamiento sistémico me hace preguntar: "¿Será el código?, ¿la conexión a internet?, ¿o es que la protoboard no tiene energía?".

3. Repaso de Chips para el Proyecto de Filtros 

Después de la charla, bajamos a tierra con el profe para ver qué integrados nos sirven para "limpiar" el audio.
Los osciladores y la lógica:

* **CD4046:** Es una máquina que convierte gestos en frecuencia. A mayor voltaje, frecuencia más rápida. Es un oscilador controlado por voltaje (VCO). Según lo que entendí, sirve más para secuenciadores, así que para mi grupo de filtros quizás no sea el protagonista.
* **CD4093:** Este es pura lógica. Convierte resistencia en frecuencia.
* **CD4040 (Binary Counter):** Este es interesante. Recibe un clock y sus salidas entregan la mitad de esa frecuencia (va dividiendo). Hace que el sonido cambie según la salida que elijas (0,1,2,3,40,1,2,3,4).

Los Amplificadores Operacionales (Op-Amps) - El corazón del filtro:

Como nuestro proyecto es de filtros, necesitamos "limpiar" la señal (input y output). Estas son las opciones que barajamos:

* **TL072 / TL082:** Mis favoritos. Son de bajo ruido (ideal para audio) y traen dos operacionales en un solo chip.
* **LM358:** El plan B. Consume poquísima batería, ideal si queremos que el filtro sea portátil, aunque no es tan "limpio" como el TL072.
* **LM324:** Si el filtro es muy complejo (de cuarto orden, por ejemplo), este nos salva porque trae cuatro operacionales adentro.

### Libro Hacia una filosofía de la fotografía, continuación de la lectura...

Cap. 6: La recepción de la fotografía (De consumidores a sujetos críticos)

Este capítulo me hizo mucho sentido por lo que vivimos en el Proyecto 1. Flusser dice que la gente ya no 'lee' las imágenes técnicas, solo las consume pasivamente. Con mi grupo anterior, nos propusimos justamente romper eso, queríamos que las personas vieran el funcionamiento detrás de la secuencia de sonidos y notas. No queríamos que solo escucharan, sino que entendieran la lógica del circuito. Fue súper efectivo porque surgieron preguntas y la gente empezó a cuestionarse cosas, les abrimos un mundo nuevo. Eso es lo que busco como diseñadora, que mi trabajo no sea algo que se recibe 'porque sí', sino que invite a entender el concepto que hay detrás, ya sea un sonido o un filtro de frecuencias.

Cap. 7: El universo fotográfico (No perderse en la simulación)

En este capítulo, Flusser plantea que hemos llegado a un punto donde la realidad parece existir solo si tiene una imagen técnica que la respalde. En el contexto del diseño electrónico, este fenómeno se observa cuando la atención se desplaza del objeto físico hacia su representación digital, es decir, cuando el diseño parece quedar validado únicamente por el render 3D o la simulación en KiCad.

El riesgo que advierte el autor es la inversión de la realidad, diseñar exclusivamente para satisfacer los parámetros del software, olvidando que la función real del objeto ocurre fuera de la pantalla. Para un diseño consciente, la simulación debe ser entendida como una herramienta predictiva, pero el valor final no reside en la estética de la imagen digital, sino en cómo el dispositivo interactúa y funciona eficazmente en el mundo físico.

Cap. 8: El diccionario de conceptos básicos (La libertad como juego)

En este capítulo, Flusser define los términos clave para entender la relación entre el ser humano y la técnica:

   1. El Programa: El conjunto de posibilidades limitadas que el software o la máquina ya tiene definidas.
   2. El Funcionario: El usuario que opera el aparato siguiendo solo las reglas previstas, sin cuestionar el sistema.
   3. La Libertad: La capacidad de "jugar contra el aparato", forzándolo a generar resultados que no estaban en su manual original.

Este glosario nos advierte sobre el riesgo de convertirnos en simples funcionarios de la herramienta. En el diseño de máquinas, la madurez profesional consiste en entender el programa para no ser dominados por él. La verdadera libertad creativa aparece cuando dejamos de ejecutar procesos automáticos y empezamos a proponer soluciones originales que desafían la lógica del software.

Cap. 9: El objetivo de la filosofía (La meta del diseñador rebelde)

El libro cierra diciendo que la filosofía sirve para entender cómo los aparatos nos programan. Mi conclusión es que, para ser una verdadera artesana tecnológica, tengo que ser capaz de ver el bosque completo. Como mencioné anteriormente, "No te fijes solo en los árboles, fíjate en quién plantó el bosque". Cuestionar quién puso las reglas del sistema es lo que me permite ser original. 

 *Al final, la técnica debe ser el pincel, nunca el artista...*

### Referencias

- [Polycam — app de escaneo 3D](https://poly.cam)
- [TL072 — datasheet y aplicaciones](https://www.ti.com/lit/ds/symlink/tl072.pdf)
- [LM358 — características y usos](https://wraycastle.com/es/blogs/knowledge-base/lm358-pinout)
- [LM324 — amplificador operacional cuádruple](https://www.ti.com/lit/ds/symlink/lm324.pdf)

