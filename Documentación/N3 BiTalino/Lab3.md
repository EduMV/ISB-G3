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

1. [MATERIALES Y EQUIPOS](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/N3%20BiTalino/Lab3.md#materiales-y-equipos)

2. [ENTREGABLES](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/N3%20BiTalino/Lab3.md#entregables)

    * [Fotos de conexión usada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/N3%20BiTalino/Lab3.md#fotos-de-conexi%C3%B3n-usada)
    * [Video de señal en silencio eléctrico o reposo](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/N3%20BiTalino/Lab3.md#video-de-se%C3%B1al-en-silencio-el%C3%A9ctrico-o-reposo)
    * [Ploteo de la señal en OpenSignals](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/N3%20BiTalino/Lab3.md#ploteo-de-la-se%C3%B1al-en-opensignals)
    * [Resumen y explicación de la señal ploteada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/N3%20BiTalino/Lab3.md#resumen-y-explicaci%C3%B3n-de-la-se%C3%B1al-ploteada)
    * [Archivo de los datos de la señal ploteada](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/N3%20BiTalino/Lab3.md#archivo-de-los-datos-de-la-se%C3%B1al-ploteada)
    * [Ploteo en Python](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/N3%20BiTalino/Lab3.md#ploteo-en-python)

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


#### Electrodos - Cuerpo
Para la conexion electrodos - cuerpo nos guiamos del "BiTalino - Electromyography (EMG) Sensor User Manual" del capitulo 2 "Application Notes" para el posicionamiento de electrodos de EMG en el musculo biceps braquial.
![BiTalino EMG positioning](https://user-images.githubusercontent.com/101833633/230150043-aaa692d3-2491-48af-9c2a-a407265479c9.png)
      Extraido de: P. W. B. S.A., “Electromyography (EMG) Sensor User Manual,” p. 19, 2020.

***Imagenes Electrodos Cuerpo***
|   Vista Superior | Vista Lateral | Vista Inferior |
| :---         |     :---:      |          ---: |
|  ![Vista Superior EC](https://user-images.githubusercontent.com/101833633/230156288-009943e3-3f63-4313-95ec-763d77b7698f.jpg)  |    ![Vista Lateral Of1](https://user-images.githubusercontent.com/101833633/230156077-ec2c9211-fe71-45e9-8145-b83835f89a0e.jpg)  | ![Vista Inferior EC](https://user-images.githubusercontent.com/101833633/230152224-b7e9eff4-c24e-4a49-a534-36e7bd36999c.jpg)
    


#
### Video de señal en silencio eléctrico o reposo
https://user-images.githubusercontent.com/101833633/230154928-bd204d2a-512e-4fab-b185-a44e321d57e1.mp4


#
### Ploteo de la señal en OpenSignals

#
### Resumen y explicación de la señal ploteada
Se estudia trabajo, no tanto anomalias
Se debe relajar el cuerpo porque los paquetes musculares deben estar relajados
Ningun electrodo debe chocar con otras cosas
Se busca plotear la flexion porque la señal es mas grande 
Solo se levante el antebrazo.
El paciente ejerce fuerza hacia arriba 

Punto muerto: punto oseo o de articulaciones que lleve a punto oseo 



#
### Archivo de los datos de la señal ploteada

#
### Ploteo en Python
