# Procedimiento de registro EEG

### Laboratorio 5

### Fecha: 19 Abril 2023

#
## Objetivos
* Adquirir señales biomédicas de EEG.
* Hacer un correcto uso del Ultracortex.
* Extraer la información de la señal EEG del software Open BCI

#

## Tabla de contenidos

1. [MATERIALES Y EQUIPOS]()

2. [ENTREGABLES]()

    * [Fotos de conexión usada]()
    * [Video de señales]()
    * [Ploteo de la señal en OpenBCI GUI]()
    * [Resumen y explicación de la señal ploteada]()
    * [Archivos]()
    * [Ploteo en Python]()
 
 3. [BiTalino]()
 
 4. [Referencias]() 

#
## Materiales y equipos

| Modelo | Descripción | Cantidad |
| :---         |     :---:      |          ---: |
| (R)EVOLUTION   | Kit BiTalino     | 1    |
| Ultracortex   | -     | 1    |
| -     | Laptop o PC       | 1      |

#
## Entregables


### Fotos de conexión usada

#### BiTalino - Cables
<p align="justify">Para esta conexion nos guiamos de la guia de usuario de BiTalino y usamos el cable de hilos para la EMG.
Cabe resaltar que los cables deben estar bien conectados, ya que eso puede afectar la lectura de la señal. En un primer momneto, no nos percatamos que el cable de hilos no estaba bien conectado al BiTalino lo que ocasiono que no se observara ninguna variacion cuando el usuario flexionaba el brazo.</p>

![BiTalino_Cables](https://user-images.githubusercontent.com/101833633/230154500-41b3b224-94dd-451f-acdf-21d5016db301.jpg)

#
#### Electrodos - Cabeza
<p align="justify">Para la conexion electrodos - cuerpo nos guiamos del "BiTalino - Electromyography (EMG) Sensor User Manual" del capitulo 2 "Application Notes" para el posicionamiento de electrodos de EMG en el ***musculo biceps braquial***.</p>

<p align="justify">Algunos puntos a tener en cuenta para esta conexión son que el paciente debe relajar el cuerpo, para evitar que otros paquetes musculares interfieran con la señal del musculo que queremos. Además los electrodos no deben chocar con otros objetos del medio para evitar interferencia.
Finalmente, el electrodo de referencia lo conectamos a un "punto muerto" que son puntos oseos o articulaciones que llevan a puntos oseos, como el codo.</p>

***FOTO***
      Extraido de: P. W. B. S.A., “Electromyography (EMG) Sensor User Manual,” p. 19, 2020.


|   Vista Superior | Vista Lateral | Vista Inferior |
| :---         |     :---:      |          ---: |
| Foto1 |   Foto2 | foto3 |
    


#
### Videos de señales
Videos

#


#
### Ploteo de la señal en OpenSignals
| Reposo             | Flexión                                              |
| ----------------- | ------------------------------------------------------------------ |
|  |  |
|  |  | 
   
   
#
### Resumen y explicación de la señal ploteada

Para la señal estamos usando el musculo bíceps braquial, como mencionamos anteriormente.


#### Reposo
<p align="justify">Para la medicion de la actividad EMG en reposo, el  musculo debe ser silente (en silencio) y detectar actividad podria señalar la existencia de una patologia del nervio o del musculo.</p>

<p align="justify">Podemos observar en el ploteo que la señal tiene una amplitud de muy pocos mV que pueden ser ruido electrico o la actividad de otros musculos.</p>

#### Flexión
<p align="justify">Al realizar la flexión del antebrazo e iniciar la actividad muscular, podemos observar la aparición de potenciales eléctricos, la amplitud aumenta de forma correspondiente con la actividad muscular.</p>

<p align="justify">La forma de onda del potencial de acción de mayor amplitud fue registrado y sus componentes se describen a continuación:</p>

![WhatsApp Image 2023-04-05 at 9 36 46 PM](https://user-images.githubusercontent.com/86316349/230261594-b771fb3a-1f04-4de7-8494-a53862ff275b.jpeg)

#
### Archivos

- [Datos obtenidos de la señal](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Se%C3%B1al%20en%20formato%20txt/signal_emg.txt)
- [Notebook de ploteo en python](https://github.com/EduMV/ISB-G3/blob/main/Software/L3_BiTalino/lectura_se%C3%B1al.ipynb)

#
### Ploteo en Python
#### Gráfica adquirida completa
![complete_signal](https://user-images.githubusercontent.com/86316349/230258967-1a80a539-b3fc-4fca-be03-8b9d22786080.png)
#### Reposo, fase activa y potencial de acción
![emg](https://user-images.githubusercontent.com/86316349/230259118-b1795785-6214-4c7b-8c9e-5de9e32773a8.png)

- *Podemos observar que la señal en reposo aún presenta ruido eléctrico, sin embargo la amplitud de este es baja*

- *Con el aumento gradual de la fuerza muscular, se observa un aumento correspondiente en la amplitud de la señal*

- *Se observa además un potencial de acción, la señal EMG está compuesta por varios de ellos*

#### Análisis en frecuencia de la señal
![fft](https://user-images.githubusercontent.com/86316349/230259150-ca063181-1f26-404f-a6c6-ab62eedd2dcf.png)
