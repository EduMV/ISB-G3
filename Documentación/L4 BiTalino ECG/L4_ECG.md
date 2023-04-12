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
* Extraer la información de las señales ECG del software OpenSignals (r)evolutio

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
<p align="justify">Para esta conexion nos guiamos de la guia de usuario de BiTalino y usamos el cable de hilos para la EMG.
Cabe resaltar que los cables deben estar bien conectados, ya que eso puede afectar la lectura de la señal. En un primer momneto, no nos percatamos que el cable de hilos no estaba bien conectado al BiTalino lo que ocasiono que no se observara ninguna variacion cuando el usuario flexionaba el brazo.</p>

**Foto**

#
#### Electrodos - Cuerpo


|   Vista Superior | Vista Lateral | Vista Inferior |
| :---         |     :---:      |          ---: |
|  Foto  |    Foto  | Foto
    


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


