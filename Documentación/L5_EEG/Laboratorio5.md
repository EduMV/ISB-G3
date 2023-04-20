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
    * [Video de señales](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#videos-de-se%C3%B1ales-sujeto-de-prueba)
    * [Archivos](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#archivos)
    * [Ploteo de la señal en OpenBCI GUI](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#ploteo-de-la-se%C3%B1al-en-openbci-gui)
    * [Ploteo en Python](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#ploteo-en-python)
    * [Resumen y explicación de la señal ploteada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#resumen-de-la-se%C3%B1al-ploteada)
 
 3. [BiTalino](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#bitalino)
 
 4. [Referencias](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#referencias) 

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
### Videos de señales (Sujeto de prueba)
1. Video de la toma de la señal en 30 segundos de reposo

https://user-images.githubusercontent.com/101833633/233154183-65b76ee1-6e41-48bd-b43b-dd9630645551.mp4

2. Video de la toma de señal al parpadear

https://user-images.githubusercontent.com/101833633/233154499-89ecab99-5001-4c26-905d-204fc39281aa.mp4

3. Video de la toma de señal al hacer preguntas

https://user-images.githubusercontent.com/101833633/233154563-866179cd-5d1a-457a-b5bd-b9b06e368aa4.mp4

#

### Archivos

- [Notebook de ploteo en python EEG Ultracortex](https://github.com/EduMV/ISB-G3/blob/main/Software/L5_EEG/lectura_se%C3%B1al_eeg_ultracortex.ipynb)
- [Notebook de ploteo en python EEG BiTalino](https://github.com/EduMV/ISB-G3/blob/main/Software/L5_EEG/lectura_se%C3%B1al_eeg_BiTalino.ipynb)
- [Señales en formato txt](https://github.com/EduMV/ISB-G3/tree/main/Documentaci%C3%B3n/L5_EEG/Se%C3%B1ales%20en%20formato%20txt)
- [Videos de uso de OpenBCI GUI en las diferentes pruebas](https://github.com/EduMV/ISB-G3/tree/main/Documentaci%C3%B3n/L5_EEG/Videos%20de%20OpenBCI%20GUI)


#
### Ploteo de la señal en OpenBCI GUI
#### En reposo

![OpenBCI_reposo](https://user-images.githubusercontent.com/86316349/233408193-785c0e3b-faf4-4751-b155-50c3caca9e20.png)

#### Parpadeando

![OpenBCI_parpadeando](https://user-images.githubusercontent.com/86316349/233408397-0692a13f-c5ca-4930-85a4-c3d39a55eb47.png)

#### Esfuerzo mental (preguntas)

![OpenBCI_calculos](https://user-images.githubusercontent.com/86316349/233408523-62a8c734-af8c-428f-80ff-237d7b189fac.png)

### Ploteo en Python de la señal adquirida por el Ultracortex Mark IV

Para el [ploteo en python](https://github.com/EduMV/ISB-G3/blob/main/Software/L5_EEG/lectura_se%C3%B1al_eeg_ultracortex.ipynb) se tomó en consideración la frecuencia de muestreo de 250Hz, además de el factor de escalamiento por bits de 0.02235 y 24 bits. (Datos obtenidos de la documentación)[2].
Adicionalmente, se empleó un filtro pasabanda de 0.8 a 48 Hz [3] para eliminar los componentes no deseados de la señal:

|   Sin filtro | Con filtro |
| :---         |          ---: |
| ![sin_filtro](https://user-images.githubusercontent.com/86316349/233429127-d19832cc-3cd7-4733-98ba-912edf60c658.jpeg) | ![con_filtro](https://user-images.githubusercontent.com/86316349/233429271-b44e8370-3bc3-4047-b72b-e9e4e3a3f03f.jpeg)  | 


#### Gráfica adquirida completa

![EEG_total](https://user-images.githubusercontent.com/86316349/233415262-acabc64f-016c-4ee3-bb20-b4bba8cc7b2a.png)

#### En reposo
- **Primera fase de referencia**
![EEG_reposo](https://user-images.githubusercontent.com/86316349/233409938-089d6fcd-9f7c-4455-8f9c-9b8f91abee8a.png)

- **Segunda fase de referencia**

![EEG_reposo2](https://user-images.githubusercontent.com/86316349/233410194-606f9727-75fb-4a9b-95b7-af5f74b2b787.png)

#### Durante el parpadeo

![EEG_parpadeo](https://user-images.githubusercontent.com/86316349/233410234-aff0df37-7199-4c06-965a-fe8ca437da89.png)


#### Durante el esfuerzo mental (Preguntas)

![EEG_esfuerzo_mental](https://user-images.githubusercontent.com/86316349/233410304-4dc2b162-5a2a-4dd2-a903-af34924bb779.png)

#
### Resumen de la señal ploteada

***Frecuencias del EEG:***
<p align="justify">Los electrodos de un EEG capturan la actividad eléctrica expresada en varias subfrecuencias de EEG, este utiliza un algoritmo llamado Transformada Rápida de Fourier (FFT). Las señales EEG sin procesar pueden identificarse como ondas distintas con diferentes frecuencias, siendo las principales: beta, alfa, theta y delta [4]</p>

* Onda beta (13 a 30 Hz):
Estrechamente asociadas con estar consciente, atento y alerta. Tener ondas betas de baja amplitud se asocia con la concentración activa, estas ondas también están asociadas con decisiones motoras como supresión de movimiento y retroalimentación sensorial de movimiento

* Onda alfa (8 a 12 Hz):
Se asocia con un estado mental relajado, tranquilo y lúcido. Se pueden inducir cerrando los ojos y relajándose, y no se observan frecuentemente en procesos cognitivos intensos. En los adultos generales varía en frecuencia de 9 a 11 Hz.


* Onda theta (4 a 7 Hz):
Ritmo provocado por la somnolencia y las primeras etapas del sueño. Resulta más prominente en las regiones frontocentrales de la cabeza y migra lentamente hacia atrás reemplazando el ritmo alfa.


* Onda delta (0,5 a 4 Hz):
Observado principalmente en el sueño profundo, es prominente en las regiones frontocentrales de la cabeza. Un ritmo delta patológico se evidencia en estados de vigilia en caso de encefalopatía generalizada y disfunción cerebral focal.

[5]

<p align="justify">En este caso podemos observar que los picos, o potenciales más grandes de la señal se encuentran principalmente durante los tiempos de parpadeo, o tiempos intermedios entre pruebas. Esto implica que la señal obtenida del EEG es altamente sensible a los parpadeos, sin embargo, no es tan sensible al razonamiento lógico empleado durante las preguntas, ya que no se nota una diferencia significativa</p>


#
## BiTalino
### Fotos de conexión usada

#### BiTalino - Cables
<p align="justify">Para esta conexion nos guiamos de la guia de usuario de BiTalino y usamos el cable de hilos para la EMG.
Cabe resaltar que los cables deben estar bien conectados, ya que eso puede afectar la lectura de la señal. En un primer momneto, no nos percatamos que el cable de hilos no estaba bien conectado al BiTalino lo que ocasiono que no se observara ninguna variacion cuando el usuario flexionaba el brazo.</p>

![BiTalino_Cables](https://user-images.githubusercontent.com/101833633/230154500-41b3b224-94dd-451f-acdf-21d5016db301.jpg)

#### Electrodos - Cabeza
<p align="justify">La conexión de los electrodos se basó de la guía “Home-Guide #3 Electroencephalography (EEG)”, en el inciso “5.1.2 How to acquire an EEG” donde se menciona el método reconocido internacionalmente conocido como International 10-20 system el cual comprende un sistema de electrodos que se colocan alrededor de toda la cabeza para evaluar las diferentes ubicaciones de los lóbulos como se observa en la siguiente imagen:</p>

|   Vista superior | Vista lateral |
| :---         |          ---: |
| ![Guia1](https://user-images.githubusercontent.com/128626501/233256722-7d8ceecd-2c5c-4b3c-ab01-97ba094d01e9.jpg) |![Guia2](https://user-images.githubusercontent.com/128626501/233256741-59434d18-7366-4b10-af49-f948e9251270.jpg) | 
Guia extraido de: https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide3_EEG.pdf


<p align="justify"> Por otro lado, se establece la existencia de una medición bipolar de electrodos (IN+/-), las cuales van sobre los puntos frontales guiados por las posiciones de los electrodos establecidos en el sistema 10-20, este consiste en la colocación de un sistema de 2 electrodos separados pre-definido por el ensamblaje de electrodos. 

Sin embargo por limitaciones del curso, no hemos podido acceder a este sistema de electrodos por lo que hemos hemos implementado un sistema de 3 electrodos como se observa en la siguiente figura: 
</p>

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
| Reposo (Primera toma) | Reposo(Segunda toma) |
| ----------------- | ------------------------| 
| ![image](https://user-images.githubusercontent.com/86316349/233412689-7e273fb6-6c22-49b7-932a-1a59dd7be738.png) | ![image](https://user-images.githubusercontent.com/86316349/233412525-e92d8195-a4f0-4f8a-8d11-6767fa431ef7.png) |


| Parpadeo    | Exposición repentina a la luz | Esfuerzo mental (Preguntas) |
|---------- | ---------- | ---------- |
| ![image](https://user-images.githubusercontent.com/86316349/233412287-e5fb9127-4fcf-4b67-8319-9541cf8ddf85.png) | ![image](https://user-images.githubusercontent.com/86316349/233411902-b05e07bc-b3a0-411b-b9b4-ec0bc0c38adb.png) | ![image](https://user-images.githubusercontent.com/86316349/233412074-11978ed5-a217-44e9-b296-7c5a3b7dca9b.png) |
#
### Ploteo en Python de la señal obtenida en OpenSignals

Para el [ploteo en Python](https://github.com/EduMV/ISB-G3/blob/main/Software/L5_EEG/lectura_se%C3%B1al_eeg_BiTalino.ipynb) de la señal obtenida por BiTalino, se utilizó una frecuencia de muestreo de 1000 Hz, se tomó en cuenta la resolución de 10 bits del sensor y su rango de 78.98 uV, tomado de la documentación [6].

#### Ploteo según el contexto

![EEG_bitalino_total](https://user-images.githubusercontent.com/86316349/233420314-6d880d25-c28a-44cf-876d-bf7bdf549b68.png)

#### Ploteo del análisis en frecuencia

![FFT_EEG](https://user-images.githubusercontent.com/86316349/233420358-97cd5d24-ad17-43c1-9bda-73e0d349ebee.png)

### Explicación de señal obtenida

<p align="justify">Se puede observar en este caso que los principales picos en la señal EEG, se dan durante los tiempos de parpadeo o en la exposición repentina a la luz tras el vendaje de ojos. La señal responde de manera significativa ante los movimientos oculares. En cuanto a la prueba de las preguntas, se no se observa mayor amplitud en la señal EEG obtenida, sin embargo si se observan mayores frecuencias respecto a las otras pruebas.</p>

<p align="justify">
Es posible que la señal sea más sensible a los movimientos oculares debido a que el electrodo de referencia fue ubicado en el hueso cigomático, donde la señal podría adquirir ruidos de la señal EMG de los músculos faciales oculares. Sería útil experimentar con más ubicaciones estándar para observar las principales diferencias.
</p>

#
## Referencias

[1] https://shop.openbci.com/products/ultracortex-mark-iv

[2] https://docs.openbci.com/Cyton/CytonDataFormat/

[3] https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide3_EEG.pdf

[4] https://www.emotiv.com/eeg-guide/

[5] https://www.ncbi.nlm.nih.gov/books/NBK539805/

[6] https://www.bitalino.com/storage/uploads/media/revolution-eeg-sensor-datasheet-revb.pdf


