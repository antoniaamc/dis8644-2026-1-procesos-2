# sesion-08a  
28 de Abril

Llegué muy tarde ups... trabajamos en Kicad por primera vez  
***recordar: traer coyacs para prestar atención***  

FALTA: Terminar esquemáticos, revisar la cápsula de la clase, subir capturas y lo que se vio en el archivo de Kicad

## Metodología

1) Dibujar esquemático (.kicad_sch)  
2) Asociar huellas a símboloes  
3) Abrir PCB New (para crear la PCB), intérprete del esquemático  
4) Definir tamaño de las pistas  
5) Repartir componentes físicamente  
6) Rutear componentes  
7) Ornamentar y exportar para fabricación

## Atajos

- `M` Move: se mueve el componente **sin** el cable  
- `G` Grab: se mueve el componente **con** el cable
- `R` Rotate: rotación en 90°
- `X` : reflejar en torno al eje X
- `W` Wire: modo cable

Para ver más atajos, en el editor de esquemas seleccionar `Ayuda` Listar atajos de teclado → ctrl+`F` / cmd+`F`

- *Mantener click*   
⬆️ Selecciona todo lo que toca  
⬇️ Selecciona todo lo que envuelve

--------------------------------------------

## Componentes (nombres en librería)  
- Resistencias → `R` / `Device:R`  
- Capacitores:
  - `C` → no polarizado  
  - `CP` → polarizado  
- Potenciómetro → `R_Potentiometer` (valor ej: 100k)  
- Batería → `Device:Battery` (valor: 9V)  
- Parlante → `Device:Speaker`  
- LED → `LED`

---

## Footprints (tipos físicos)  
- Capacitor cerámico → `Disc` (no polarizado)   
- Capacitor electrolítico → `Radial` (polarizado)  
- Resistencia → `Axial` (ej: DIN0207)  
- LED → `LED_D5.0mm`  
- Potenciómetro → tipo panel (ej: Alps)

---

## Dimensiones y estándares  
🟡 !!! ***Atención*** con la búsqueda y uso de componentes, hay que prestar **especial atención** a las dimensiones físicas de cada uno. En general no es necesario buscar componentes con capacidades de voltaje demasiado altas (perdida de plata, mejor quedarse con lo necesario. A menos que...)

Para encontrar dimensiones exactas, recomendación práctica:

1. Usar footprint de KiCad
2. Leer sus dimensiones
3. Solo si es crítico → confirmar con datasheet (hoja de datos o ficha técnica)  
Ejemplo:  
- *resistor 1/4W datasheet*

- Los fabricantes usan **estándares comunes** → DIN, JEDEC, EIA  
Ejemplo:  
- `DIN0207` → resistencia axial típica (~1/4W)

**Parámetros:**  
- `L` → largo  
- `D` → diámetro  
- `P` → pitch (distancia entre patas)

---

## Conceptos clave  
- `P (pitch)` = distancia entre patas  
- Un mismo componente puede tener distintas huellas  
- En asignación de huellas:
  - se puede copiar/pegar → mismo componente, distinta huella

---

## Capacitores  
- Polarizado → electrolítico (`CP`)  
- No polarizado → cerámico (`C`)  

**nota:** `µ` (micro) y `n` (nano) **NO indican polaridad**, solo unidad  

  - µF = microfaradios  
  - nF = nanofaradios  

---

## Conexiones en esquemático
- `●` → conexión real (nodo)
- cruce sin punto → conexión  
- `▢` → punto de edición (no conexión)

---

## Capas PCB 
(7) Capas principales en PCB de 2 capas:

- `F.Cu` / `B.Cu` → cobre  
- `F.SilkS` / `B.SilkS` → serigrafía  
- `F.Mask` / `B.Mask` → máscara de soldadura  
- `Edge.Cuts` → borde de la placa  

- Son las capas básicas más usadas en el curso.

---

## Edición / visualización
- Propiedades de texto → `E` o doble clic  
- Render PCB → `Alt + 3`

---

## Edición PCB
- Cambiar dimensiones del borde:  
  - seleccionar borde → `E`

---

## Guardado de proyecto  
- Guardar desde `.kicad_pro`  
- Contiene:  
  - esquemático  
  - PCB  
  - config general  

---

## Notas
- las resistencias más largas → dependen de estándar (ej: DIN0207, DIN0309)  
- los fabricantes usan las mismas dimensiones (estandarización industrial)

---

# !!!!!! Por revisar / corroborar

1. **“que el filtro corresponda a la librería de la izquierda”**  

2. **Dimensiones exactas de resistencias “largas”**  

3. **Asignación de huellas (copiar/pegar)**  
   → importante: 
   - solo válido si el componente físico es equivalente  
   - no siempre intercambiable (ej: radial vs axial)
  

bibliografia y anexos arreglar despues: https://cursos.mcielectronics.cl/2019/06/18/identificacion-de-condensadores/




