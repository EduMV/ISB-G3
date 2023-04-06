# Uso de BiTalino para EMG y ECG

### Laboratorio 3

### Fecha: 05 Abril 2023

#
## Objetivos
* Adquirir señales biomédicas de EMG y ECG.
* Hacer una correcta configuración de BiTalino.
* Extraer la información de las señales EMG y ECG del software OpenSignals (r)evolutio

#

## Tabla de contenidos

1. [MATERIALES Y EQUIPOS](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Lab3.md#materiales-y-equipos)

2. [ENTREGABLES](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Lab3.md#entregables)

    * [Fotos de conexión usada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Lab3.md#fotos-de-conexi%C3%B3n-usada)
    * [Video de señal en silencio eléctrico o reposo](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Lab3.md#video-de-se%C3%B1al-en-silencio-el%C3%A9ctrico-o-reposo)
    * [Ploteo de la señal en OpenSignals](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Lab3.md#ploteo-de-la-se%C3%B1al-en-opensignals)
    * [Resumen y explicación de la señal ploteada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Lab3.md#resumen-y-explicaci%C3%B3n-de-la-se%C3%B1al-ploteada)
    * [Archivos](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Lab3.md#archivos)
    * [Ploteo en Python](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L3_BiTalino/Lab3.md#ploteo-en-python)

#
## Materiales y equipos

| Modelo | Descripción | Cantidad |
| :---         |     :---:      |          ---: |
| (R)EVOLUTION   | Kit BiTalino     | 1    |
| -     | Laptop o PC       | 1      |

#
## Entregables


### Fotos de conexión usada

#### BiTalino - Cables
Para esta conexion nos guiamos de la guia de usuario de BiTalino y usamos el cable de hilos para la EMG.
Cabe resaltar que los cables deben estar bien conectados, ya que eso puede afectar la lectura de la señal. En un primer momneto, no nos percatamos que el cable de hilos no estaba bien conectado al BiTalino lo que ocasiono que no se observara ninguna variacion cuando el usuario flexionaba el brazo.

![BiTalino_Cables](https://user-images.githubusercontent.com/101833633/230154500-41b3b224-94dd-451f-acdf-21d5016db301.jpg)

#
#### Electrodos - Cuerpo
Para la conexion electrodos - cuerpo nos guiamos del "BiTalino - Electromyography (EMG) Sensor User Manual" del capitulo 2 "Application Notes" para el posicionamiento de electrodos de EMG en el ***musculo biceps braquial***.

Algunos puntos a tener en cuenta para esta conexión son que el paciente debe relajar el cuerpo, para evitar que otros paquetes musculares interfieran con la señal del musculo que queremos. Además los electrodos no deben chocar con otros objetos del medio para evitar interferencia.
Finalmente, el electrodo de referencia lo conectamos a un "punto muerto" que son puntos oseos o articulaciones que llevan a puntos oseos, como el codo.

![BiTalino EMG positioning](https://user-images.githubusercontent.com/101833633/230150043-aaa692d3-2491-48af-9c2a-a407265479c9.png)
      Extraido de: P. W. B. S.A., “Electromyography (EMG) Sensor User Manual,” p. 19, 2020.


|   Vista Superior | Vista Lateral | Vista Inferior |
| :---         |     :---:      |          ---: |
|  ![Vista Superior EC](https://user-images.githubusercontent.com/101833633/230156288-009943e3-3f63-4313-95ec-763d77b7698f.jpg)  |    ![Vista Lateral EC 1](https://user-images.githubusercontent.com/101833633/230159803-535ae53d-0d39-47d5-94a3-ede9b937d791.jpg)  | ![Vista Inferior EC](https://user-images.githubusercontent.com/101833633/230152224-b7e9eff4-c24e-4a49-a534-36e7bd36999c.jpg)
    


#
### Video de señal en silencio eléctrico o reposo
https://user-images.githubusercontent.com/101833633/230154928-bd204d2a-512e-4fab-b185-a44e321d57e1.mp4


#
Tambien realizamos pruebas con movimiento de **flexión del musculo**, que adjuntamos a continuación.

https://user-images.githubusercontent.com/101833633/230157275-fe89bc35-8fbc-4023-80ea-8ae2af22d2e1.mp4



#
### Ploteo de la señal en OpenSignals
| Reposo             | Flexión                                              |
| ----------------- | ------------------------------------------------------------------ |
| ![Señal_R](https://user-images.githubusercontent.com/101833633/230158425-db118e18-542d-4abc-932c-cfc610b1e3aa.jpg) | ![Señal_F](https://user-images.githubusercontent.com/101833633/230158740-4b5261ed-487f-4525-b1f4-98da88abd7ed.jpg) |
| ![Señal_F_Cerca](https://user-images.githubusercontent.com/101833633/230159110-87fb82a1-cbe6-48ad-80ad-2950d67c7295.jpg) | ![Señal_R_Cerca](https://user-images.githubusercontent.com/101833633/230159070-8c4fa2b6-b52c-402a-b606-9de3d2ead65d.jpg) | 
   
   
#
### Resumen y explicación de la señal ploteada

Para la señal estamos usando el musculo bíceps braquial, como mencionamos anteriormente.


#### Reposo
Para la medicion de la actividad EMG en reposo, el  musculo debe ser silente (en silencio) y detectar actividad podria señalar la existencia de una patologia del nervio o del musculo.

Podemos observar en el ploteo que la señal tiene una amplitud de muy pocos mV que pueden ser ruido electrico o la actividad de otros musculos.

#### Flexión
Al realizar la flexión del antebrazo e iniciar la actividad muscular, podemos observar la aparición de potenciales eléctricos, la amplitud aumenta de forma correspondiente con la actividad muscular.

La forma de onda del potencial de acción de mayor amplitud fue registrado y sus componentes se describen a continuación:

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


