# Filtros IIR y FIR

### Laboratorio 7

### Fecha: 05 Mayo 2023

#
## Objetivos
* Diseñar un filtro de tipo FIR usando el dataset de ECG obtenido el laboratorio pasasdo
* Diseñar un filtro de tipo IIR usando el dataaset de ECG obtenido el laboratorio pasado 
* Presentar una tabla resumen comparando la señal cruda con la señal filtrada  

#

## Tabla de contenidos

1. [Conceptos previos](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#entregables)

    * [Filtros analógicos](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#fotos-de-conexi%C3%B3n-usada)
    * [Filtros digitales](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#videos-de-se%C3%B1ales-sujeto-de-prueba)
      * [Filtros IIR](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#archivos)
      * [Filtros FIR](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#ploteo-de-la-se%C3%B1al-en-openbci-gui)

 
 2. [Comparación: IIR vs FIR](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#bitalino)
 
 3. [Tabla resumen](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#referencias) 

#

## Conceptos previos


### Filtros analógicos
Podemos definirlo como un filtro usado para procesos analógicos o señales de tiempo continuo. Estos se dividen en filtros pasivos y activos, dependiendo del tipo de elemento empleado para su realización [x1]
Además, se pueden clasificar de acuerdo a la aplicación específica que realizan en los siguientes: pasa-bajas, pasa-altas,pasa-banda y rechaza-banda.

![four_major_filters](https://user-images.githubusercontent.com/89672526/236079088-30b7a022-c477-40c4-b70f-d155825426e6.jpeg)

El diseño de este tipo de filtros en general involucra especificaciones de frecuencia (para la bandas de paso y rechazo) y especificaciones de magnitud (atenuación máxima para la banda de paso y mínima para la de rechazo) para generar una función de transferencia de mínima fase con el orden más pequeño que reúne o excede las especificaciones. [x]

### Filtros digitales

Un filtro digital es un sistema discreto que modifica el espectro de una señal muestreada (señal de entrada) transformándola en otra secuencia numérica llamada señal de salida de acuerdo a ciertas especificaciones. Matemáticamente se representa con una ecuación de diferencia o una función de transferencia (FT) en la variable compleja z.
Mientras que los filtros analógicos se representan matemáticamente mediante ecuaciones diferenciales; los filtros digitales, por el contrario, se representan mediante ecuaciones de diferencia. La forma de la ecuación de diferencia dependerá del tipo de filtro que se represente.

Se clasifican en filtros de respuesta al impulso infinita (IIR) y filtros de respuesta al impulso finita (FIR). [y]


#### Filtro IIR

También conocidos como  filtros digitales con respuesta al impulso infinito (IIR), producen una respuesta de impulso infinito de un sistema dinámico. Estos filtros son recursivos, ya que la salida no solo depende de la entrada actual, sino de valores pasados de la salida (filtros con retroalimentación). [y] Por ello, son utilizados en sistemas que requieren una respuesta infinita como, por ejemplo, en el procesamiento de señales de audio [x3]


![structure-of-IIR-filter](https://user-images.githubusercontent.com/89672526/236084195-e633ec51-9a22-43ff-b0cc-406a6d73c685.jpg)



#### Filtro FIR

Definido como filtro digital que produce una respuesta finita al impulso de un sistema dinámico. Se denomina FIR o “respuesta finita al impulso” porque la respuesta se fija en cero en un tiempo finito. Además, estos filtros no tienen retroalimentación lo que significa que solo trabajan con valores de entrada del pasado y del presente, por tanto, la salida es la suma de una cantidad finita de muestras de los valores de entrada, lo que lo hace altamente estables ya que evita la posibilidad de de oscilaciones en la salida. [x3]

![structure-of-FIR-filter](https://user-images.githubusercontent.com/89672526/236084136-94ee7cd8-3965-4c4c-bbaa-5190511e978b.jpg)



#
## Comparación IIR vs FIR

<img width="781" alt="cuadro_comparativo" src="https://user-images.githubusercontent.com/89672526/236084473-6c2f9ab5-c446-46f4-bd53-37f105c2d050.png">


## Tabla resumen


#
## Referencias

[1] https://shop.openbci.com/products/ultracortex-mark-iv

[2] https://docs.openbci.com/Cyton/CytonDataFormat/

[3] https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide3_EEG.pdf

[4] https://www.emotiv.com/eeg-guide/

[5] https://www.ncbi.nlm.nih.gov/books/NBK539805/

[6] https://www.bitalino.com/storage/uploads/media/revolution-eeg-sensor-datasheet-revb.pdf


