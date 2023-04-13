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
    * [Video de señal después de actividad física](https://github.com/EduMV/ISB-G3/blob/main/Documentaci%C3%B3n/L4%20BiTalino%20ECG/L4_ECG.md#video-de-se%C3%B1al-despu%C3%A9s-de-actividad-f%C3%ADsica)
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
<p align="justify">Para esta conexion nos guiamos de la guia de usuario de BiTalino [1] y usamos el cable de hilos para la señal ECG.[2]
Cabe resaltar que los cables deben estar bien conectados, ya que eso puede afectar la lectura de la señal. </p>

![BiTalino_Cables](https://user-images.githubusercontent.com/101833633/231526748-466001e1-cd68-4bbe-9241-2360801a1a27.jpg)



#
#### Electrodos - Cuerpo

Para el posicionamiento de los electrodos, usamos como guia el documento "BITalino (r)evolution Home Guide". [3]

Los electrodos se ubican en esas posiciones (cerca a huesos) para evitar captar el movimiento de los músculos.

![Imagen_1](https://user-images.githubusercontent.com/89672526/231577174-f517be3b-53c2-4101-880d-68be6c65eedd.png)

Entonces, posicionamos los electrodos positivos y negativos en las muñecas y el de referencia en la cresta iliaca. 

|   Vista Frontal | Vista Superior | 
| :---         |     :---:      |
|  ![FrontalECG](https://user-images.githubusercontent.com/101833633/231612994-cf0127ef-a98b-4fe8-a6b1-52b380366ad4.jpg)  |    ![Vista_Superior_ECG](https://user-images.githubusercontent.com/101833633/231528901-c54d7486-4f94-4764-a065-ddda56eddc25.jpg)  |

Cabe resaltar que para esta práctica de laboratorio realizamos la prueba en 2 alumnos y el posicionamiento de electrodos en el segundo alumno fue el siguiente:
|   Referencia | Posicionamiento | 
| :---         |     :---:      |
|   ![BiTalino_guia_conexion2of](https://user-images.githubusercontent.com/101833633/231614819-e85cac50-2ecf-4bbe-bde6-d4ec18c68100.png) |   ![E2](https://user-images.githubusercontent.com/101833633/231614564-a13d49b0-f58b-4447-90a6-5bb589fcba12.jpg)  |

#
### Video de señal después de actividad física

Antes de realizar la actividad física, capturamos la señal en reposo
![Señal_ECG_R](https://user-images.githubusercontent.com/101833633/231530311-87a5de4a-0d3a-488f-9e4f-16aca5d80480.jpg)


Para medir la señal despues de la actividad física, el paciente realizo ejercicio (burpees) durante 2 minutos, para asegurar que su ritmo cardiaco este acelerado

https://user-images.githubusercontent.com/101833633/231529945-f8db88ee-2fae-48c0-aac2-90ec54d865d1.mp4



#



#
### Ploteo de la señal en OpenSignals


#### Alumno 1
| Reposo primera toma | Reposo electrodos invertidos |
| :---         |       ---: |
| ![Rep_falla](https://user-images.githubusercontent.com/101833633/231533739-022c6741-6cc5-4309-8258-fc8a4b1ff357.jpg) | ![Reposo_ECG](https://user-images.githubusercontent.com/101833633/231533781-911559ac-7d96-4235-8a32-348fbe3f9d1b.jpg) 
| Análisis de señales |
| ![Fig1](https://user-images.githubusercontent.com/128626501/231598791-787bb2a1-3ae0-4c08-b6e0-184d8de73a2c.jpg)| ![Fig2](https://user-images.githubusercontent.com/128626501/231598808-a98c34ce-8d77-419c-9c82-90da8c1b99e7.jpg)

**Análisis y discusión de resultados**

Debemos tomar en cuenta que el estudio se realizo con un sistema bipolar de derivaciones de extremidades el cual se compone de 3 derivaciones. La derivacion I representa la diferencia de potencial entre el brazo derecho y el brazo iquierdo; un impulso eléctrico que se mueve de derecha a izquierda genera una desvicacion de ECG positiva. La derivación II es la diferencia de potencial entre el brazo derecho y la pierna izquierda, se produce una desviación positiva del ECG. Por otro lado la derivación III es la diferencia de potencial entre el brazo y pierna izqueirads, de forma reiterada la dirección del impulso es positivo[6].

Se observa que la primera señal muestra una normalidad en la Onda P y T, sin embargo el Complejo QRS presenta un comportamiento negativo. Como mencionamos anteriormente este ultimo debéria tener un comportamiento positivo, esto se podria deber a que los electrodos capturan el voltaje de forma inversa. Una posible razón seria una patalogía llamada Dextrocardia, sin embargo serian necesarias analizar las derivacines unilaterales precordiales, ya que en pacientes diagnosticados con esta condición se determina un comportamiento normal en las derivaciones I, II y III[7]. 

   
|   Respiraciones pausadas | Post-ejercicio     |
| :---         |       ---: |
| ![Ag_resp](https://user-images.githubusercontent.com/101833633/231534957-fcd76388-b02a-4ffb-8795-9f750b401bcc.jpg) |![ECG_Agitada](https://user-images.githubusercontent.com/101833633/231535010-576ecdef-6f97-46ee-9f36-c5799d104a89.jpg)  |

#

#### Alumno 2

Análogamente, para medir la señal después del ejercicio, el paciente realizó burpees durante 2 minutos, para asegurar que su ritmo cardiaco este acelerado.


https://user-images.githubusercontent.com/89672526/231628614-39187a4e-713e-4e6d-863c-84fa8f2e99eb.mp4

Luego, capturamos la señal inmediatamente después del ejercicio y durante la realización de respiraciones pausadas después de contener la respiración

|   Respiraciones pausadas | Post-ejercicio     |
| :---         |       ---: |
|  ![Rep2](https://user-images.githubusercontent.com/101833633/231613916-e45e91e4-4661-4e4a-b86c-54fbb4159fd1.jpg) |   ![Post_ej2](https://user-images.githubusercontent.com/101833633/231613989-55727e56-0cff-4e50-ac88-9522841d46d7.jpg) |


#
### Resumen y explicación de la señal ploteada
En la señal, podemos observar las siguientes ondas [4]

1. *Onda P:* Primera deflexión hacia arriba. Representa la activación eléctrica que produce la contracción de las aurículas, también conocida como despolarización auricular. La onda P debe ser suave, redondeada y positiva (hacia arriba).
2. *Segmento P-R*: Tramo de la línea isoeléctrica que se encuentra entre el final de la onda P y la siguiente deflexión. En este periodo, las aurículas terminan de vaciarse y se produce desaceleración en la transmisión de la corriente eléctrica, justo antes del inicio de la contracción de los ventrículos
3. *Complejo QRS:* Despolarización ventricular. En este periodo ocurre la activación eléctrica que produce la contracción de los ventrículos. En un ECG normal se deben observar ondas Q de tamaño pequeño (no mayores a un cuadrado pequeño tanto en longitud como profundidad) y encontrarse solo en ciertas derivaciones. En general, el complejo QRS no debe exceder en duración más de dos cuadrados pequeños.
4. *Segmento ST:* En este segmento, los ventrículos están totalmente despolarizados. Tiene valor como herramienta diagnóstica ya que su elevación o descenso en relación con la línea basal puede significar insuficiencia en la irrigación del corazón
5. *Onda T:* Repolarización ventricular, es el proceso eléctrico que permite a los ventrículos relajarse y prepararse para el siguiente ciclo cardíaco. La onda T es normalmente una deflexión positiva (hacia arriba)
6. *Segmento TP:* Ventrículos completamente relajados y en reposo.


![Fases_ciclo_cardiaco](https://user-images.githubusercontent.com/89672526/231572623-14b1062d-7c16-4698-a4f1-126b2e973a98.jpeg)

*Extraído de The Art of Daniel Bernal*



Las ondas observadas tienen relación con los eventos que ocurren en las fases del ciclo cardiaco. Estos se pueden resumir acontinuación:

![ezgif com-resize](https://user-images.githubusercontent.com/89672526/231580414-300b236c-9a75-4501-8ff2-cfa5d4007d9f.gif)

*Extraído de Human Bio Media*

#
### Archivos


#
### Ploteo en Python
#### Gráfica adquirida completa

#### Reposo, fase activa y potencial de acción


#### Análisis en frecuencia de la señal


#
### Referencias biblográficas
[1] PLUX Wireless Biosignals, “BITalino (r)evolution User Manual,” 2020, [Online]. Available: http://bitalino.com/.

[2] “Using BITalino Mini with Electrocardiography (ECG) Sensor Application Notes,” pp. 1–23, 2020.

[3] M. Proença and K. Mrotzek, “BITalino (r)evolution Home Guide,” 2020.

[4] L. Azcona, “Estructura del corazón Capítulo 4 El electrocardiograma.” Accessed: Apr. 11, 2023. [Online]. Available: [https://www.fbbva.es/microsites/salud_cardio/mult/fbbva_libroCorazon_cap4.pdf#:~:text=La actividad eléctrica del corazón recogida en el](https://www.fbbva.es/microsites/salud_cardio/mult/fbbva_libroCorazon_cap4.pdf#:~:text=La%20actividad%20el%C3%A9ctrica%20del%20coraz%C3%B3n%20recogida%20en%20el)

‌[5] “BITalino (r)evolution Lab Guide.” Available: [https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide2_ECG.pdf](https://support.pluxbiosignals.com/wp-content/uploads/2022/04/HomeGuide2_ECG.pdf)

[6]“Bipolar limb lead system”. Uptodate, 2023. https://www.uptodate.com/contents/image?imageKey=CARD%2F65289.

[7] C. Mozayan and J. T. Levis, “ECG Diagnosis: Dextrocardia,” The Permanente Journal, vol. 23, no. 4, Dec. 2019, doi: https://doi.org/10.7812/tpp/18.244. ‌


