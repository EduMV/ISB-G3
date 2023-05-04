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

1. [Conceptos previos](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/Lab7_Filtros_IIR_FIR/Laboratorio7.md#conceptos-previos)

    * [Filtros analógicos](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/Lab7_Filtros_IIR_FIR/Laboratorio7.md#filtros-anal%C3%B3gicos)
    * [Filtros digitales](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/Lab7_Filtros_IIR_FIR/Laboratorio7.md#filtros-digitales)
      * [Filtros FIR](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/Lab7_Filtros_IIR_FIR/Laboratorio7.md#filtro-fir)
      * [Filtros IIR](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/Lab7_Filtros_IIR_FIR/Laboratorio7.md#filtro-iir)

 
 2. [Comparación: FIR vs IIR](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/Lab7_Filtros_IIR_FIR/Laboratorio7.md#comparaci%C3%B3n-iir-vs-fir)
 
 3. [Tabla resumen](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L5_EEG/Laboratorio5.md#referencias) 
 
 4. [Referencias](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/Lab7_Filtros_IIR_FIR/Laboratorio7.md#referencias) 


#

## Conceptos previos


### Filtros analógicos
Podemos definirlo como un filtro usado para procesos analógicos o señales de tiempo continuo. Estos se dividen en filtros pasivos y activos, dependiendo del tipo de elemento empleado para su realización [1]
Además, se pueden clasificar de acuerdo a la aplicación específica que realizan en los siguientes: pasa-bajas, pasa-altas,pasa-banda y rechaza-banda.

![four_major_filters](https://user-images.githubusercontent.com/89672526/236079088-30b7a022-c477-40c4-b70f-d155825426e6.jpeg)

El diseño de este tipo de filtros en general involucra especificaciones de frecuencia (para la bandas de paso y rechazo) y especificaciones de magnitud (atenuación máxima para la banda de paso y mínima para la de rechazo) para generar una función de transferencia de mínima fase con el orden más pequeño que reúne o excede las especificaciones. [2]

### Filtros digitales

Un filtro digital es un sistema discreto que modifica el espectro de una señal muestreada (señal de entrada) transformándola en otra secuencia numérica llamada señal de salida de acuerdo a ciertas especificaciones. Matemáticamente se representa con una ecuación de diferencia o una función de transferencia (FT) en la variable compleja z. Mientras que los filtros analógicos se representan matemáticamente mediante ecuaciones diferenciales; los filtros digitales, por el contrario, se representan mediante ecuaciones de diferencia. La forma de la ecuación de diferencia dependerá del tipo de filtro que se represente.

Algunas de las ventajas de un filtro digital con respecto a uno analógico son: una respuesta a la frecuencia más cercana a la ideal, no requieren sintonización, sus componentes son independientes de la frecuencia de operación del filtro, entre otros. Por otro lado, una desventaja de estos filtros es que la máxima frecuencia de operación es igual a la mitad de la frecuencia de muestreo (Teorema de Shannon) [3]

Se clasifican en filtros de respuesta al impulso infinita (IIR) y filtros de respuesta al impulso finita (FIR). [4]


#### Filtro FIR

Definido como filtro digital que produce una respuesta finita al impulso de un sistema dinámico. Se denomina FIR o “respuesta finita al impulso” porque la respuesta se fija en cero en un tiempo finito. Además, estos filtros no tienen retroalimentación lo que significa que solo trabajan con valores de entrada del pasado y del presente, por tanto, la salida es la suma de una cantidad finita de muestras de los valores de entrada, lo que lo hace altamente estables ya que evita la posibilidad de de oscilaciones en la salida. [5]

![structure-of-FIR-filter](https://user-images.githubusercontent.com/89672526/236084136-94ee7cd8-3965-4c4c-bbaa-5190511e978b.jpg)

*Extraído de Circuit Globe [5]*

#### Filtro IIR

También conocidos como  filtros digitales con respuesta al impulso infinito (IIR), producen una respuesta de impulso infinito de un sistema dinámico. Estos filtros son recursivos, ya que la salida no solo depende de la entrada actual, sino de valores pasados de la salida (filtros con retroalimentación). [4] Por ello, son utilizados en sistemas que requieren una respuesta infinita como, por ejemplo, en el procesamiento de señales de audio [5]


![structure-of-IIR-filter](https://user-images.githubusercontent.com/89672526/236084195-e633ec51-9a22-43ff-b0cc-406a6d73c685.jpg)

*Extraído de Circuit Globe [5]*

#
## Comparación IIR vs FIR

<img width="781" alt="cuadro_comparativo" src="https://user-images.githubusercontent.com/89672526/236084473-6c2f9ab5-c446-46f4-bd53-37f105c2d050.png">

*Elaboración propia. Adaptado de: Circuit Globe [5]*

## Tabla resumen


#
## Referencias

[1] “INTRODUCCIÓN A FILTROS ANALÓGICOS CAPÍTULO 1.” Available: http://catarina.udlap.mx/u_dl_a/tales/documentos/lem/torres_d_ld/capitulo1.pdf

[2] “ELECTRONICA II -BIOINGENIERIA -1ra. Parte FILTROS ANALOGICOS.” Available: http://dea.unsj.edu.ar/pdselo/Apuntes/Filtros-analogicos-1ra-parte.pdf

[3] M. de J. García Ortega, “Introducción a filtros digitales,” Apr. 2003. https://tesis.ipn.mx/bitstream/handle/123456789/683/253_2005_CITEDI_MAESTRIA_manuel_garcia.pdf?sequence=1&isAllowed=y (accessed May 03, 2023).
‌
[4] M. de J. G. Ortega, “Introducción a filtros digitales,” mexculture.citedi.mx, 2003, Accessed: May 04, 2023. [Online]. Available: http://mexculture.citedi.mx/handle/123456789/1466


[5] Roshni Y, “Difference Between FIR Filter and IIR Filter (with Comparison chart) - Circuit Globe,” Circuit Globe, Mar. 24, 2020. https://circuitglobe.com/difference-between-fir-filter-and-iir-filter.html (accessed May 04, 2023).



