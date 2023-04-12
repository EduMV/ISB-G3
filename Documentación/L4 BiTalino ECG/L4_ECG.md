# Uso de BiTalino para ECG

### Laboratorio 4

### Fecha: 12 Abril 2023

### Integrantes
* Gonzalo Povea - gonzalo.povea@upch.pe
* Edu Marin - roberto.marin@upch.pe
* Maria Miranda - maria.miranda.s@upch.pe
* Fernando Panduro - luis.panduro@upch.pe 
* Fernanda Ramirez: - fernanda.ramirez@upch.pe
* Ximena Roldán - ximena.roldan@upch.pe
 
#
## Objetivos
* Adquirir señales biomédicas de ECG.
* Hacer una correcta configuración de BiTalino.
* Extraer la información de las señales ECG del software OpenSignals (r)evolution

#

## Tabla de contenidos

1. [MATERIALES Y EQUIPOS](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#materiales-y-equipos)

2. [ENTREGABLES](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#entregables)

    * [Fotos de conexión usada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#fotos-de-conexi%C3%B3n-usada)
    * [Video de señal en silencio eléctrico o reposo](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#video-de-se%C3%B1al-en-silencio-el%C3%A9ctrico-o-reposo)
    * [Ploteo de la señal en OpenSignals](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#ploteo-de-la-se%C3%B1al-en-opensignals)
    * [Resumen y explicación de la señal ploteada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#resumen-y-explicaci%C3%B3n-de-la-se%C3%B1al-ploteada)
    * [Archivos](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#archivos)
    * [Ploteo en Python](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#ploteo-en-python)

3. [REFERENCIAS BIBLIOGRÁFICAS](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#referencias-biblogr%C3%A1ficas)

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
<p align="justify">Para esta conexion nos guiamos de la guia de usuario de BiTalino y usamos el cable de hilos para la señal ECG.
Cabe resaltar que los cables deben estar bien conectados, ya que eso puede afectar la lectura de la señal. </p>

![BiTalino_Cables](https://user-images.githubusercontent.com/101833633/231526748-466001e1-cd68-4bbe-9241-2360801a1a27.jpg)



#
#### Electrodos - Cuerpo

Para el posicionamiento de los electrodos, usamos como guia el documento "BITalino (r)evolution Home Guide". [3]

![BiTalino_guia_conexion](https://user-images.githubusercontent.com/101833633/231528251-4b7a1e8a-0da4-4af1-9bdc-7c9ee8793f3b.png)

Entonces, posicionamos los electrodos positivos y negativos en las muñecas y el de referencia en la cresta iliaca.

|   Vista Frontal | Vista Superior |
| :---         |     :---:      |
|  ![Vista_Frontal_nombres](https://user-images.githubusercontent.com/101833633/231528863-8773ec5a-b523-4d4f-a9d1-9a6be0dde8bc.jpg)  |    ![Vista_Superior_ECG](https://user-images.githubusercontent.com/101833633/231528901-c54d7486-4f94-4764-a065-ddda56eddc25.jpg)  |
    


#
### Video de señal en silencio eléctrico o reposo


#



#
### Ploteo de la señal en OpenSignals
| Reposo             | Flexión                                              |
| ----------------- | ------------------------------------------------------------------ |
| Foto | Foto |
| Foto | Foto | 
   
   
#
### Resumen y explicación de la señal ploteada

Para la señal estamos usando el musculo bíceps braquial, como mencionamos anteriormente.


#### Reposo
<p align="justify">Para la medicion de la actividad EMG en reposo, el  musculo debe ser silente (en silencio) y detectar actividad podria señalar la existencia de una patologia del nervio o del musculo.</p>

<p align="justify">Podemos observar en el ploteo que la señal tiene una amplitud de muy pocos mV que pueden ser ruido electrico o la actividad de otros musculos.</p>

#### Flexión
<p align="justify">Al realizar la flexión del antebrazo e iniciar la actividad muscular, podemos observar la aparición de potenciales eléctricos, la amplitud aumenta de forma correspondiente con la actividad muscular.</p>

<p align="justify">La forma de onda del potencial de acción de mayor amplitud fue registrado y sus componentes se describen a continuación:</p>

**Foto**

#
### Archivos


#
### Ploteo en Python
#### Gráfica adquirida completa

#### Reposo, fase activa y potencial de acción


#### Análisis en frecuencia de la señal


#
### Referencias biblográficas
[1] “Using BITalino Mini with Electrocardiography (ECG) Sensor Application Notes,” pp. 1–23, 2020.
[2] PLUX Wireless Biosignals, “BITalino (r)evolution User Manual,” 2020, [Online]. Available: http://bitalino.com/.
[3] M. Proença and K. Mrotzek, “BITalino (r)evolution Home Guide,” 2020.
[4] L. Azcona, “Estructura del corazón Capítulo 4 El electrocardiograma.” Accessed: Apr. 11, 2023. [Online]. Available: [https://www.fbbva.es/microsites/salud_cardio/mult/fbbva_libroCorazon_cap4.pdf#:~:text=La actividad eléctrica del corazón recogida en el](https://www.fbbva.es/microsites/salud_cardio/mult/fbbva_libroCorazon_cap4.pdf#:~:text=La%20actividad%20el%C3%A9ctrica%20del%20coraz%C3%B3n%20recogida%20en%20el)
‌[5] “BITalino (r)evolution Lab Guide.” Available: [https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide2_ECG.pdf](https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide2_ECG.pdf)


