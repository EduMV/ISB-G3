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

1. [MATERIALES Y EQUIPOS](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#materiales-y-equipos)

2. [ENTREGABLES](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#entregables)

    * [Fotos de conexión usada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#fotos-de-conexi%C3%B3n-usada)
    * [Video de señales](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#videos-de-se%C3%B1ales)
    * [Ploteo de la señal en OpenBCI GUI](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#ploteo-de-la-se%C3%B1al-en-openbci-gui)
    * [Resumen y explicación de la señal ploteada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#resumen-y-explicaci%C3%B3n-de-la-se%C3%B1al-ploteada)
    * [Archivos](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#archivos)
    * [Ploteo en Python](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#ploteo-en-python)
 
 3. [BiTalino](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#bitalino)
 
 4. [Referencias]() 

#
## Materiales y equipos

| Modelo | Descripción | Cantidad |
| :---         |     :---:      |          ---: |
| (R)EVOLUTION   | Kit BiTalino     | 1    |
| Mark IV   | Ultracortex     | 1    |
| -     | Laptop o PC       | 1      |

#
## Entregables


### Fotos de conexión usada

#### Ultracortex - Cabeza

El Ultracortex es un casco de electroencefalografía (EEG) creado por la empresa estadounidense OpenBCI. Este casco está diseñado para medir la actividad eléctrica del cerebro y permitir a los usuarios controlar dispositivos externos mediante la actividad cerebral.

El Ultracortex Mark IV utiliza electrodos secos y está diseñado para ser fácil de usar y personalizable para diferentes tamaños y formas de cabeza. [1]


![UltraCortexC](https://user-images.githubusercontent.com/101833633/233152489-14532158-1393-401c-a0c9-7eb27bccf9d6.jpg)


#
### Videos de señales
1. Video de la toma de la señal en 30 segundos de reposo

https://user-images.githubusercontent.com/101833633/233154183-65b76ee1-6e41-48bd-b43b-dd9630645551.mp4

2. Video de la toma de señal al parpadear

https://user-images.githubusercontent.com/101833633/233154499-89ecab99-5001-4c26-905d-204fc39281aa.mp4

3. Video de la toma de señal al hacer preguntas

https://user-images.githubusercontent.com/101833633/233154563-866179cd-5d1a-457a-b5bd-b9b06e368aa4.mp4

#


#
### Ploteo de la señal en OpenBCI GUI

   
   
#
### Resumen y explicación de la señal ploteada

<p align="justify">TEXTO</p>




#
### Archivos



#
### Ploteo en Python
#### Gráfica adquirida completa


#### Reposo, fase activa y potencial de acción


#### Análisis en frecuencia de la señal



#

## BiTalino
### Fotos de conexión usada

#### BiTalino - Cables
<p align="justify">Para esta conexion nos guiamos de la guia de usuario de BiTalino y usamos el cable de hilos para la EMG.
Cabe resaltar que los cables deben estar bien conectados, ya que eso puede afectar la lectura de la señal. En un primer momneto, no nos percatamos que el cable de hilos no estaba bien conectado al BiTalino lo que ocasiono que no se observara ninguna variacion cuando el usuario flexionaba el brazo.</p>

![BiTalino_Cables](https://user-images.githubusercontent.com/101833633/230154500-41b3b224-94dd-451f-acdf-21d5016db301.jpg)

#### Electrodos - Cabeza
<p align="justify">La conexión de los electrodos se basó de la guía “Home-Guide #3 Electroencephalography (EEG)”, en el inciso “5.1.2 How to acquire an EEG” donde se menciona el método reconocido internacionalmente conocido como International 10-20 system el cual comprende un sistema de electrodos que se colocan alrededor de toda la cabeza para evaluar las diferentes ubicaciones de los lóbulos como se observa en la siguiente imagen:.</p>

|   Guia | Posicionamiento |
| :---         |          ---: |
| ![Imagen de WhatsApp 2023-04-19 a las 23 15 17](https://user-images.githubusercontent.com/128626501/233256722-7d8ceecd-2c5c-4b3c-ab01-97ba094d01e9.jpg) |![Imagen de WhatsApp 2023-04-19 a las 23 15 40](https://user-images.githubusercontent.com/128626501/233256741-59434d18-7366-4b10-af49-f948e9251270.jpg) | 
Guia extraido de: https://www.uptodate.com/contents/image?imageKey=RHEUM%2F78990


<p align="justify"> Por otro lado, se establece la existencia de una medición bipolar de electrodos (IN+/-), las cuales van sobre los puntos frontales guiados por las posiciones de los electrodos establecidos en el sistema 10-20, este consiste en la colocación de un sistema de 2 electrodos separados pre-definido por el ensamblaje de electrodos. 

Sin embargo por limitaciones del curso, no hemos podido acceder a este sistema de electrodos por lo que hemos hemos implementado un sistema de 3 electrodos como se observa en la siguiente figura. 
.</p>

|   Guia | Posicionamiento |
| :---         |          ---: |
| ![Guia_Cabeza](https://user-images.githubusercontent.com/101833633/233151417-b5095453-2bae-4ee0-89d2-19750891834c.jpg) | ![Electrodos_cabeza](https://user-images.githubusercontent.com/101833633/233156729-f74a55a0-a56f-40b5-9f54-7d9fb7cb4862.jpg) | 
Guia extraido de: https://www.uptodate.com/contents/image?imageKey=RHEUM%2F78990



#
### Videos de señales
1. Video de la toma de la señal en 30 segundos de reposo

https://user-images.githubusercontent.com/101833633/233158980-2dae1dd7-8348-4e97-ab1e-bc2ea8dcc4b3.mp4


2. Video de la toma de señal al parpadear

https://user-images.githubusercontent.com/101833633/233159517-b9094434-98ef-4c13-8cf5-7177b9f29c20.mp4


3. Video de la toma de señal al hacer preguntas

https://user-images.githubusercontent.com/101833633/233159841-0813d4a8-1e1b-443e-a220-80982bf7150e.mp4




#
### Ploteo de la señal en OpenSignals
| Reposo             | Flexión                                              |
| ----------------- | ------------------------------------------------------------------ |
|  |  |
|  |  | 

#
### Explicación de señal obtenida


#
## Referencias

[1] https://shop.openbci.com/products/ultracortex-mark-iv 
