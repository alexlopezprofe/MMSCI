# UNIDAD 5. Componentes internos del ordenador y periféricos
1. Memorias RAM
2. Dispositivos de almacenamiento
3. Tarjetas gráficas
4. Adaptadores de red
5. Periféricos

# Memorias RAM
# Definición de memoria RAM

La RAM o memoria de acceso aleatorio (en inglés: Random Access Memory), es la memoria principal de un equipo microinformático y se encarga de almacenar de manera _temporal_ tanto las instrucciones como los datos que ejecuta el microprocesador.

Es una memoria volátil, es decir, la información se pierde al interrumpirse el flujo eléctrico (apagar el ordenador).

Se denominan «de acceso aleatorio» porque se puede leer o escribir en una posición de memoria con un tiempo de espera igual para cualquier posición.

![alt text](image-1.png)

Físicamente es un conjunto de chips soldados sobre una PCB, a este conjunto de chips, se le denomina **módulo** de memoria RAM.

Los fabricantes tienen que fabricar los módulos de memoria siguiendo los estándares marcados por **JEDEC** (Joint Electron Device Engineering Council)
(https://www.jedec.org/)

![](assets/img/Unidad05/Unidad51.png)

![](assets/img/Unidad05/Unidad52.png)

# Estructura módulo memoria RAM

![](assets/img/Unidad05/Unidad53.png)


![](assets/img/Unidad05/Unidad55.png)


ESTRU
## SPD. Serial Presence Detect chip

**El Circuito SPD (Serial Presence Detect Chip):** Es el encargado de almacenar datos relativos al módulo de memoria RAM, como el tamaño de la memoria, el tiempo de acceso, la velocidad y el tipo de memoria. De esta forma el ordenador conocerá que memoria RAM tiene instalada de manera automática sin intervención del usuario.

![](assets/img/Unidad05/Unidad54.png)

![](assets/img/Unidad05/Unidad57.png)




## PMIC - Power management integrated circuits

**PMIC (Power management integrated circuits o Circuitos integrados de gestión de energía)**

* Exclusivo de DDR5
* Chip situado en el centro de las memorias DDR5 y se encarga de gestionar la energía (voltajes) del módulo
* Permite, entre otras cosas, la implementación de una tecnología de sincronización multifásica. Una novedad que permite realizar transmisiones a un voltaje más bajo o más alto si es necesario. Ahora será siempre gestionado desde el propio módulo de memoria DDR5.

![](assets/img/Unidad05/Unidad59.png)

![](assets/img/Unidad05/Unidad510.png)


[https://www.crucial.es/articles/about-memory/how-is-memory-made](https://www.crucial.es/articles/about-memory/how-is-memory-made)




# Características de la memoria RAM
## Capacidad

La  capacidad hace referencia a la cantidad de datos que se pueden almacenar en la RAM. La memoria RAM es un almacén de datos y lógicamente una característica importante es cuántos datos puede almacenar. 

Los transistores del interior de los bancos de memoria tienen un determinado tamaño, con lo cual a menor tamaño de transistor mayor densidad de celdas lo que implica más capacidad.

Esta capacidad se mide actualmente en los módulos DDR en **GB (GigaBytes)**.

La cantidad de memoria estará directamente relacionada con el uso que hagas del equipo. Cada uso requiere una cantidad de RAM diferente. No se necesita la misma memoria RAM para navegar, que para jugar o editar vídeo o fotos.

![](assets/img/Unidad05/Unidad527.png)

## Velocidad o frecuencia de reloj

* Los chips de memoria integrados en cada módulo de memoria funcionan a una frecuencia de trabajo determinada.
* Este valor se mide en MHz, por lo tanto, a mayor cantidad de Megahercios, mayor velocidad tendrá el módulo.
* En las memorias de tipo DDR (DOUBLE data rate) se realizan 2 operaciones por cada ciclo de reloj  y no una como en las SDR, por tanto  los 3200 MHz anunciados serían en realidad 3200 MT/s (millones de transferencias por segundo) y la frecuencia real sería la mitad, es decir 1600MHz.
* Por ejemplo, 3200 MHz significa que se tardan 1/3200MHz = 0,3125 nanosegundos por cada ciclo de reloj.
* Al elegir la memoria RAM, hay que asegurarse de que la placa base soporta la frecuencia de trabajo de la memoria RAM.
* Al instalar algunos módulos de memoria, la placa puede configurarlos para que trabajen a una frecuencia inferior a la que el fabricante prometía. En ese caso se tendrá que configurar la frecuencia de la memoria RAM manualmente desde la BIOS o UEFI para subir el multiplicador de sus frecuencias y hacer que funcionen a la velocidad correcta.

*

## Latencia

La estructura interna de la memoria RAM es como la de un tablero de ajedrez tridimensional en el que cada cuadro del tablero es una celda en la que se escriben los datos que se almacenan.

La latencia es el tiempo que tarda la memoria RAM en situarse en una determinada celda para leer o escribir su contenido. Cuanto mayor sea la latencia de la memoria RAM, mayor es el tiempo que “pierde” en llegar a una determinada celda y, por lo tanto, menos eficiente en su trabajo.

Por lo tanto, a igualdad de frecuencias de reloj para un módulo de memoria RAM, es preferible elegir una memoria RAM con una latencia baja.



## Tipos de memoria RAM DDR

![](assets/img/Unidad05/Unidad538.png)

## Factor de forma

* **DIMM:** <span style="color:#333333">El término  style="color:#333333"> DIMM  style="color:#333333"> es el acrónimo de la expresión “Dual In-line Memory Module”
* **SO-DIMM:** “Small Outline Dual In-line Memory Module”, y es precisamente esas palabras «Small Outline» lo que las diferencia de los módulos DIMM habituales. La diferencia es meramente física, ocupan un menor espacio y así se pueden instalar en equipos de tamaño reducido como los portátiles.

![](assets/img/Unidad05/Unidad537.png)

![image](https://github.com/alexlopezprofe/MyM/assets/148449360/15094c21-30ad-4f5d-9b0a-d85c3fbf072f)



| Tipo | Pines | Longitud |
| :-: | :-: | :-: |
| SO-DIMM DDR | 200 | 67.6 mm |
| SO-DIMM DDR2 | 200 | 67.6 mm |
| SO-DIMM DDR3 | 204 | 67.6 mm |
| SO-DIMM DDR4 | 260 | 69.6 mm |
| SO-DIMM DDR5 | 262 |  |

![](assets/img/Unidad05/Unidad541.png)

[Detalle de la muesca](https://upload.wikimedia.org/wikipedia/commons/9/95/Laptop_SODIMM_DDR_Memory_Comparison_V2.svg)




## Perfiles

* La memoria está preparada para trabajar a diferentes frecuencias y diferentes latencias. Cada configuración de frecuencias, latencias y voltaje se conoce como perfil, y el fabricante asegura que el rendimiento es óptimo con esos perfiles. Estos perfiles se almacenan en el circuito SPD de la memoria.
* Existen dos tipos de perfiles, dentro de cada tipo, el fabricante puede configurar diferentes variantes.
* Perfiles JEDEC: son configuraciones aprobadas por el organismo encargado de la estandarización de la memoria RAM. Estas configuraciones son muy seguras pero no aprovechan las altas frecuencias de las memorias RAM actuales. Suelen venir indicadas con un número, por ejemplo, JEDEC #4, JEDEC #5, etc.
* Perfiles XMP (Intel eXtreme Memory Profile) o DOCP/EXPO (AMD): son configuraciones aprobadas por Intel  y AMD  para conseguir obtener frecuencias de funcionamiento de la memoria superiores a las aprobadas por JEDEC. Suelen venir indicadas con un número, por ejemplo, XMP-3200, XMP-4000, etc.
  * _[https://www.asus.com/latin/support/FAQ/1042256/](https://www.asus.com/latin/support/FAQ/1042256/)_
* Por defecto la placa base sólo funciona con perfiles JEDEC, detectando automáticamente el perfil que mejor rendimiento tenga. Si la placa base está preparada para admitir perfiles XMP o  DOCP/EXPO , estos se podrán configurar desde la BIOS/ UEFI .

![](assets/img/Unidad05/Unidad546.png)



# Dispositivos de almacenamiento

# Definición

Los dispositivos de almacenamiento de un equipo microinformático, también conocidos como memoria secundaria, es el lugar donde se almacenan permanentemente los programas y datos con los que se trabaja en el mismo. Se caracteriza por tener gran capacidad de almacenamiento, ser no volátil y por un tiempo de acceso más lento que el acceso a la memoria principal.

![](assets/img/Unidad06/Unidad062.png)

# Unidad de almacenamiento principal

Actualmete los dispositivos de almacenamiento secundario principal en un equipo microinformático y donde se suele instalar el sistema operativo, además de tener la posibilidad de almacenar programas y datos son los **discos duros magnéticos o HDD (Hard Disk Drive)** y las **unidades de estado sólido o SDD (Solid State Drive)**

Sus características principales son:

* Gran capacidad de almacenamiento.
* No volátil.
* Acceso más lento que la memoria principal(RAM).

![](assets/img/Unidad06/Unidad063.png) ![](assets/img/Unidad06/Unidad064.png) ![](assets/img/Unidad06/Unidad065.png)


## Tipos de conexión

![](assets/img/Unidad06/Unidad0628.jpg)

![](assets/img/Unidad06/Unidad0629.jpg)

![](assets/img/Unidad06/Unidad0630.jpg)



# Características generales de las unidades de almacenamiento

* Interfaz. ( Conexión al PC o dispositivo ). Podemos encontrar discos duros con la interfaz IDE, SATA, SCSI, SAS o SATA Express, pero también interfaces de conexión externos como USB, Thunderbolt, Firewire o eSATA.
* Factor de forma: El factor de forma nos da las dimensiones del disco duro. Se mide en pulgadas, las cuales indican el diámetro de los platos (en el caso de que lleven). Podemos encontrar los siguientes factores de forma
    * 3,5" pulgadas o LFF
    * 2,5" pulgadas o SFF
    * M.2
    * U.2
    * U.3
* Capacidad de almacenamiento. Se mide GB o TB
* Memoria caché. La memoria caché del disco duro almacenará la información más solicitada, de manera que la controladora pueda acceder a ella de manera más rápida sin tener que ir a leerla internamente. Esta memoria se mide en Megabytes.
* Tiempo de acceso. El tiempo de acceso es el tiempo medio que tarda el disco duro en estar preparado para transferir datos (ya sea de lectura o de escritura). Este tiempo se mide en nanosegundos (ns)
* Velocidad de rotación del motor de los discos duros magnéticos. Marca la velocidad de giro en los discos duros magnéticos. Los discos con interfaz IDE y SATA giran a 5.400 o 7.200 rpm (revoluciones por minuto). En los discos duros con interfaz SCSI o SAS las velocidades de giro son mayores, de 10.000 e incluso 15.000 rpm, aunque son ruidosos y consumen más energía.
* Velocidad lectura/escritura \_\_en discos SSD. Velocidad a la que el disco es capaz de leer y escribir información. 
* Temperatura. Indica el rango de temperaturas a las que el disco puede funcionar.
* Nivel sonoro: Nos indica el nivel de ruido que emitirá el disco duro en funcionamiento. Se mide en decibelios (dB).
* Resistencia a golpes: Mediría el golpe máximo que el disco duro es capaz de soportar sin romperse. Se utiliza la medida de fuerza (G), donde 1G es la fuerza de la gravedad cuando estás parado, sentado o acostado.
* Vida útil - Terabytes Written (TBW ). Se define por el JEDEC como el número de terabytes que pueden ser escritos en un SSD hasta que sus células de memoria se «agoten»
* Tiempo medio entre fallos - Mean Time Between Failures (MTBF) \_\_en discos SSD.
* Humedad. Indica el rango de humedad a las que el disco puede funcionar.
* Altitud. Indica el rango de altitud a las que el disco puede funcionar.



## Factor de forma

![](assets/img/Unidad06/Unidad0659.png)

### Factor de forma 3\,5” o LFF

3.5" o 3.5 pulgadas o LFF(Large Form Factor) Se refiere a los discos duros "grandes" usados comúnmente en los ordenadores de sobremesa y servidores.

Discos duros actuales →  Interfaz SATA / SAS

Medidas típicas de 101 x 25,4 x 146 mm.

![](assets/img/Unidad06/Unidad0660.png)

### Factor de forma 2\,5” o SFF

2.5" o 2.5 pulgadas o SFF(Short Form Factor) Se refiere a los discos duros "grandes" usados comúnmente en los ordenadores de sobremesa y servidores

Suelen tener unas dimensiones de 6,9 x 10 x 9,7 centímetros

Podemos encontrar unidades de 2.5” tanto magnéticos, SSD SATA o SSD U.2

Actualmente → Interfaz SATA.

![](assets/img/Unidad06/Unidad0661.png)

![](assets/img/Unidad06/Unidad0662.png)

![](assets/img/Unidad06/Unidad0663.png)


### NVMe M.2

El formato **NVMe M.2** se ha convertido en el más popular para la construcción de discos SSD de altas prestaciones, pues permite la construcción de modelos muy rápidos, con una alta capacidad y con un tamaño muy reducido.

Se conectan mediante tecnología PCI-Express a la placa base para evitar los cuellos de botella.

Se elimina el conector de la alimentación, pues los M.2 se alimentan directamente desde la ranura PCI Express X4. (Actualmente existe PCI Express V5)

Dentro del formato M.2 existen varios tipos, por ejemplo M.2 2242, M.2 2260 y M.2 2280, esto hace referencia a las dimensiones del dispositivo, en el primer caso son 22 mm de ancho x 42 mm de largo mientras que en el segundo tiene un largo de 60 mm y el último un largo de 80 mm.

![](assets/img/Unidad06/Unidad0665.png)

![](assets/img/Unidad06/Unidad0666.png)


![image](https://github.com/alexlopezprofe/MyM/assets/148449360/3423e367-3467-4c21-97cc-72cfcd331045)

![](assets/img/Unidad06/Unidad0639.png)



# Dispositivos de almacenamiento en red

## NAS
El almacenamiento conectado en red, Network Attached Storage (NAS), es el nombre dado a una tecnología de almacenamiento dedicada a compartir la capacidad de almacenamiento de un computador/ordenador (servidor) con computadoras personales o servidores clientes a través de una red (normalmente TCP/IP), haciendo uso de un sistema operativo optimizado para dar acceso con los protocolos CIFS, NFS, FTP o TFTP.

Suelen tener varios discos y se pueden configurar en *[RAID](https://es.wikipedia.org/wiki/RAID)*

Hay discos duros exclusivos para NAS que tienen más durabilidad, los discos utilizados suelen ser magnéticos de 3,5”

![](assets/img/Unidad06/Unidad0667.png)

![](assets/img/Unidad06/Unidad0668.png)

![](assets/img/Unidad06/Unidad0669.png)

## Cabina de discos. Servidores de almacenamiento

![](assets/img/Unidad06/Unidad0670.png)

![](assets/img/Unidad06/Unidad0671.png)

![](assets/img/Unidad06/Unidad0672.png)

*[https://www1.la.dell.com/ue/es/gen/Empresarial/pvaul_md1000/pd.aspx?refid=pvaul_md1000&s=gen](https://www1.la.dell.com/ue/es/gen/Empresarial/pvaul_md1000/pd.aspx?refid=pvaul_md1000&s=gen)*

# RAID

Un RAID es un grupo de discos duros independientes configurados para funcionar como uno solo, ya sea sumando su espacio total, mejorando la velocidad de lectura y escritura o configurados para duplicar la información para estar seguros de que, en caso de que uno de los discos duros se rompa, no vamos a perder los datos.

Existen varios tipo de RAID

![](assets/img/Unidad06/Unidad0673.png)

## RAID 0

En esta configuración todos los discos duros funcionan como un único volumen, y su espacio total es la suma del espacio de todos los discos duros.

Doble velocidad de lectura y escritura.

No hay paridad de datos ni volumen de respaldo.

![](assets/img/Unidad06/Unidad0674.png)

## RAID 1

Es uno de los tipos de RAID más utilizados para quienes buscan duplicidad de los datos para estar seguros de que los datos nunca se pierden. En este tipo de RAID, los datos se duplican en los discos duros como si fuese un espejo.

Mayor velocidad de lectura. Sin mejora en la velocidad de escritura.

Un disco duro espejo. Si falla uno de los discos duros se puede reemplazar sin perder datos.

Perdemos el 50% del espacio total de los discos. El espacio total de un RAID 1 es la mitad del espacio total de los discos duros. Por ejemplo, si hacemos un RAID 1 con dos discos duros de 4 TB solo tendremos un espacio total de 4 TB.

![](assets/img/Unidad06/Unidad0675.png)

## RAID 5

La información se distribuye a lo largo de todos los discos duros, aunque se reserva dicho espacio (el tamaño de una de las unidades) para paridad. Esta paridad, además, se reparte entre todos los discos duros.

Si fallan dos discos se pierde absolutamente toda la información del RAID.

La mejora de velocidad de lectura es también X-1 veces el número de discos usados.

El espacio total de los discos es X-1, El espacio total de un RAID 5 es el espacio de todos los discos duros menos 1, es decir, si vamos a usar 4 discos duros de 4 TB el espacio total será de 12 TB.

Si falla uno de los discos duros, cualquiera de ellos, se puede reemplazar y recuperar todos los datos.

![](assets/img/Unidad06/Unidad0676.png)

## RAID 6

Prácticamente igual que el RAID 5, pero añade un segundo nivel de paridad, lo que nos permite que fallen hasta dos discos duros del RAID y poder sustituirlos. Si fallan 3, entonces toda la información del RAID se pierde.

El espacio total de los discos es X-2, igual que la mejora de la velocidad de lectura. A cambio de esta doble paridad incluida en el RAID 6 se pierde el espacio total de dos de los discos duros. Por ejemplo, en una configuración de 4 discos duros de 4 TB, el espacio total que tendríamos es de 8 TB, con el doble de velocidad de lectura.

![](assets/img/Unidad06/Unidad0677.png)

# Almacenamiento en la nube

![](assets/img/Unidad06/Unidad0678.png)

Un sistema de almacenamiento en la nube o Cloud Storage es un modelo de almacenamiento de datos basado en redes de ordenadores donde nuestros datos están alojados en espacios de almacenamiento virtualizados. Por lo tanto, el espacio no se encuentra en el propio equipo físico del usuario, sino en uno o varios servidores ofrecidos por la compañía que contratemos el servicio.




# Unidad 6. Tarjetas de expansión y periféricos.

# Tarjetas de expansión
# Tarjetas gráficas


La tarjeta gráfica, también llamada tarjeta de vídeo, adaptador de pantalla o simplemente GPU (heredado del nombre de su procesador gráfico) es una tarjeta de expansión o un circuito integrado que se encarga de procesar los datos que le envía el procesador del ordenador y transformarlos en información visible y comprensible para el usuario, representándolos en el dispositivo de salida, el monitor.

Tipos:
* Integradas en CPU(iGPU - Integrated GPU): Estas gráficas integradas tienen normalmente una potencia reducida y además necesitan recursos de memoria RAM del sistema.
  * Intel
  * Amd → APU
  * Apple M
* Tarjetas de expansión
  * PCI-Express x16
  * PCI → Obsoleto
  * AGP → Obsoleto

## Componentes tarjetas gráficas

![](assets/img/Unidad07/u71.png)


### GPU - Graphics Processing Unit

La GPU, o Unidad de Procesamiento de Gráficos, se encarga de procesar los gráficos que utiliza el sistema de computación, es decir es una unidad de procesamiento gráfico con una alta capacidad de paralelizado, capaz de trabajar y de procesar gráficos, y de convertir información y datos en elementos visibles por el usuario, pero que también de sacar adelante tareas que requieran de la realización de una gran cantidad de operaciones concurrentes en paralelo

Físicamente es un circuito muy complejo que integra varios miles de millones de transistores y varios núcleos que tienen capacidad de procesamiento independiente.

Así como las CPU, están diseñados con pocos núcleos pero altas frecuencias de reloj, las GPU tienden al concepto opuesto, contando con grandes cantidades de núcleos con frecuencias de reloj relativamente bajas.

![](assets/img/Unidad07/u73.png)


### Características GPU

**Núcleos**. Cada uno de ellos contribuye al rendimiento en conjunto de la tarjeta gráfica. Cada fabricante utiliza diferentes arquitecturas, y no es un buen dato para comparar modelos de fabricantes distintos.

* Los núcleos en chips AMD se denominan **Stream Processors**
* Los núcleos en chips NVIDIA se denominan **CUDA Cores**



### VRAM

La Video Ram o memoria de vídeo está integrada en forma de chips sobre el PCB de la tarjeta gráfica, y que cuenta con su propio bus de datos. Es un tipo de memoria diseñada especialmente para llevar a cabo un tipo concreto de tareas en aplicaciones gráficas y videojuegos.

En la memoria VRAM se cargan las texturas y los modelos que la GPU va a utilizar y procesar para crear la imagen después. Por tanto, es muy importante que nuestra tarjeta gráfica posea suficiente memoria VRAM.



### Alimentación

Cuanto más potente sea una tarjeta gráfica mayor es su consumo eléctrico, y el problema radica en que todas las gráficas que necesitan alimentación adicional consumen más energía de lo que el zócalo PCI-Express es capaz de proporcionar, limitado actualmente en 75 vatios. En otras palabras, cualquier tarjeta gráfica que tenga un consumo mayor de 75W necesitará alimentación adicional, y la manera de proporcionársela es conectándola directamente a la fuente de alimentación mediante los cables PCI-E de 6 y 8 pines.

Cada uno de los conectores de los cables PCIe de la fuente de alimentación es capaz de proporcionar 12,5 vatios adicionales. En otras palabras, un conector PCIe de 6 pines es capaz de entregar hasta 75 vatios, mientras que esto se eleva hasta los 100 vatios en los conectores de 8 pines.

![](assets/img/Unidad07/u724.png)
![](assets/img/Unidad07/u725.jpg)

Una tarjeta gráfica que tenga un consumo eléctrico de 150 vatios, necesitaría los 75 que proporciona la placa base y otros 75 a través de la alimentación adicional de la fuente. En este ejemplo, necesitaríamos 75 vatios adicionales, y con un conector de 6 pines sería suficiente. Si la gráfica tuviera un consumo de 225 vatios, necesitaríamos los 75 de la placa y otros 150 adicionales, que podríamos proporcionarle mediante dos conectores de 6 pines, o incluso uno de 6 y otro de 8 para alcanzar los 250 vatios

![](assets/img/Unidad07/u726.png)


#### Conector 12VHPWR

Es un nuevo tipo de conector de alimentación utilizado por tarjetas de gama alta de NVIDIA.

Tiene la capacidad de entregar 600W de potencia bajo un voltaje de 12V, es decir, 50 amperios en un pequeño conector. Sus dimensiones son de apenas 0.7cm para los 12 pines que proporcionan energía, a lo que les suma 4 pequeños pines sensoriales que no dan energía. y que llevan la anchura. total a 0.845cm y 1.4cm de largo.

![image](https://github.com/alexlopezprofe/MyM/assets/148449360/2f05d45f-44ac-40d0-9a30-d513bf24d360)

![image](https://github.com/alexlopezprofe/MyM/assets/148449360/9d3175e9-b96d-45f0-8fb2-8eec9e4c7633)


**¿Qué ocurre si no tenemos este comector en nuestra fuente de alimentación?**  Se puede utilizar un adaptador

![image](https://github.com/alexlopezprofe/MyM/assets/148449360/918e50e5-8c90-4185-bd35-dd0daace354c)

![image](https://github.com/alexlopezprofe/MyM/assets/148449360/4744f138-f1af-419e-a33e-e7ff4c128d64)



### TDP vs TGP vs TBP

* **TDP - Thermal Design Power.** En tarjetas gráficas el término TDP se refiere al consumo de energía que tiene la **GPU** de la tarjeta.
* **TGP - Total Graphics Power**. Cantidad máxima de potencia que la fuente de alimentación del sistema debería ser capaz de proveer a la tarjeta gráfica. Es decir se tiene en cuenta el consumo de la GPU, que nos lo daba el TDP,  y se le suma el consumo de todo el sistema de memoria (que es bastante significativo) y el del VRM que alimenta a la gráfica. Se usa en gráficas con chip **Nvidia**.
* **TBP - Total Board Power.** Concepto equivalente a TGP pero para gráficas con chip **AMD**

![](assets/img/Unidad07/u727.png)

[Power Consumption: TDP, TBP and TGP for Nvidia and AMD](https://www.igorslab.de/en/performance-tdp-tbp-and-tgp-at-nvidia-and-amd-graphics-cards-demystified-and-calculated-igorslab/)


👉 **Ejemplo especificaciones tarjeta** 

Los fabricantes nos darán las siguientes especificaciones

![](assets/img/Unidad07/u731.png)



## Conectores de señales de video

Las tarjetas gráficas disponen de unos conectores de salida que sirven para conectarla con los monitores, algunas de estas tarjetas también pueden emitir audio digital.

![](assets/img/Unidad07/u743.png)

### VGA. Video Graphics Array

Sólo puede llevar información analógica de tipo RGBHV (Red, Green, Blue, frecuencia Horizontal, frecuencia Vertical)

Resolución máxima: 2048 x 1536 píxeles a 85 Hz

Conector DB de 15 pines

![](assets/img/Unidad07/u744.png)

![](assets/img/Unidad07/u745.png)

![](assets/img/Unidad07/u746.png)

![](assets/img/Unidad07/u747.png)

### DVI (Digital Visual Interface)

Su parte izquierda está destinada a llevar las señales digitales de la tarjeta gráfica al monitor, mientras  que en su lado derecho están los pines destinados a transmitir la señal analógica.

Los tres tipos de conectores DVI que podemos encontrar son:
* DVI-A (analógico)
* DVI-D (digital)
* DVI-I (integrado; analógico y digital).

Además los conectores DVI-I y DVI-D tienen dos velocidades de datos distintas, conocidas como Single-Link (SL) y Dual-Link(DL)
* SL →1.65 Gbps de ancho de banda lo que permite llegar a 1920 x 1200 píxeles a 60Hz
* DL→ 2 Gbps de ancho de banda lo que permite llegar 2560 x 1600 píxeles a  60 Hz

![](assets/img/Unidad07/u748.png)

![](assets/img/Unidad07/u749.png)

![](assets/img/Unidad07/u750.png)

![](assets/img/Unidad07/u751.png)

### HDMI (High-Definition Multimedia Interface)

**HDMI** responde a las siglas High Definition Multimedia Interface (interfaz multimedia de alta definición) y hace referencia a la norma de conexión que permite transmitir audio y vídeo digital sin comprimir desde un equipo a otro y con un único cable.

![](assets/img/Unidad07/u753.png)

![](assets/img/Unidad07/u754.png)

![](assets/img/Unidad07/u756.png)

![](assets/img/Unidad07/u757.png)


### DisplayPort

**DisplayPort** es una interfaz digital para todo tipo de dispositivos, la cual ha sido desarrollada por VESA, por lo que estamos ante una interfaz que está **libre** de cualquier tipo de licencia o canon.

![](assets/img/Unidad07/u758.png)

![](assets/img/Unidad07/u759.png)

![](assets/img/Unidad07/u760.png)




### Adaptadores de video

![](assets/img/Unidad07/u765.png)
![](assets/img/Unidad07/u766.png)
![](assets/img/Unidad07/u767.png)
![](assets/img/Unidad07/u768.png)
![](assets/img/Unidad07/u769.png)
![](assets/img/Unidad07/u770.png)



### Multi-monitor

Conexión de varios monitores a un adaptador:
* Duplicación de pantalla
* Extensión de escritorio

![](assets/img/Unidad07/u771.png)

![](assets/img/Unidad07/u772.png)

![](assets/img/Unidad07/u773.png)



# Adaptadores de red 

## Red de área local

Un sistema en red, o una red, es aquel que está formado por dos o más dispositivos conectados entre sí para compartir información, recursos y servicios.

Si nos centramos en una red de área local o LAN es una red de datos de alta velocidad y bajo nivel de errores que abarca un área geográfica relativamente pequeña. La penetración en el mercado de las redes LAN es muy alto ya que están 

Según el medio de transmisión podemos encontrar redes de área local:

* Cableadas basadas en el estándar Ethernet o IEEE 802.3.
 * Par trenzado (RJ45)
 * Fibra óptica (SPF)
 * Coaxial (BNC) obsoleto

* Inalámbricas basadas en el estándar WiFi o IEEE 802.11 → Aire o vacío (Ondas electromagnéticas)
* Combinación de ambas ya que que con los elementos hardware adecuados son compatibles entre sí.

## Interfaz de red

Los adaptadores de red, tarjeta de red, interfaz de red o NIC (Network interface card) es la parte hardware que comunica los diferentes nodos (ordenador, dispositivos móviles, televisiones….) de la red con el medio de transmisión que a su vez interconecta con los demás dispositivos que conforman la red. Pueden ser cableados o inalámbricos.

### Interfaces de red cableados

![](assets/img/Unidad07/u778.png)

RJ45→ cable par trenzado

SPF→ fibra óptica



![](assets/img/Unidad07/u779.png)

![](assets/img/Unidad07/u780.png)

### Interfaces de red RJ45

![](assets/img/Unidad07/u781.png)

 <img src="assets/img/Unidad07/u782.png" width="200" height="200">

![](assets/img/Unidad07/u783.png)

![](assets/img/Unidad07/u784.png)

### Interfaces de red fibra óptica

Un transceptor SFP (small form-factor pluggable transceptor ) o Mini_GBIC permiten conectar cables de fibra óptica de diferentes tipos, como son monomodo y multimodo, así como diferentes velocidades.

![](assets/img/Unidad07/u785.png)

![](assets/img/Unidad07/u786.png)

![](assets/img/Unidad07/u787.png)

![](assets/img/Unidad07/u788.png)





### Tarjetas de red inalámbricas

![](assets/img/Unidad07/u794.png)

Las redes Wi-Fi permiten la conectividad de equipos y dispositivos mediante ondas de radio.

El estándar para las redes inalámbricas es el **IEEE 802.11** → WiFi

![](assets/img/Unidad07/u795.png)

![](assets/img/Unidad07/u796.png)

![](assets/img/Unidad07/u797.png)

![](assets/img/Unidad07/u798.png)

![](assets/img/Unidad07/u799.png)

![](assets/img/Unidad07/u7100.png)

![](assets/img/Unidad07/u7101.png)

### Bluetooth



El Bluetooth es un estándar de conectividad inalámbrica presente en nuestros dispositivos electrónicos

IEEE 802.15.1

Frecuencia 2,402 GHz y los 2,480 GHz

![](assets/img/Unidad07/u7102.png)

![](assets/img/Unidad07/u7103.png)



# Tarjetas multimedia


## Tarjetas de sonido

Es un dispositivo que permite la reproducción, la grabación y la digitalización del sonido, normalmente a través de un software específico.

Las placas base de los equipos actuales normalmente disponen del sistema de sonido integrado y suelen ser de gran calidad. Es por lo tanto poco usual que se amplíen estos equipos con tarjetas de expansión de sonido, salvo en casos muy específicos, como pueden ser una avería o la necesidad de un sistema profesional de sonido, como los usados por músicos o compositores.

Las operaciones más usuales que ejecuta una tarjeta de sonido son:

* Grabación. El sonido que se recoge normalmente a través de un micrófono llega a la tarjeta a través de los conectores. Esta señal se recoge, se procesa y se almacena en el formato seleccionado.
* Reproducción. La señal digitalizada de un sonido se envía a la tarjeta que la procesa y la manda a través de los conectores de salida hacia los altavoces, auriculares, etcétera.
* Síntesis. Es el procedimiento mediante el cual estas tarjetas reproducen sonidos a partir de datos o representaciones simbólicas.

### Tarjetas de sonido Sound Blaster

La familia Sound Blaster de tarjetas de sonido, ha sido durante muchos años el estándar para el audio de los PC, antes de que el audio de PC se hiciera común. El creador de Sound Blaster es una empresa de Singapur llamada Creative Technology, también conocida por el nombre de su empresa satélite en los Estados Unidos, Creative Labs.

![](assets/img/Unidad07/u7108.png)

![](assets/img/Unidad07/u7109.png)


### Componentes de una tarjetas de sonido

![](assets/img/Unidad07/u7110.jpg)

### In/Out de una tarjeta de sonido

![](assets/img/Unidad07/u7111.png)

* Analógicos
 * Verde __ : Salida de línea. Altavoces frontales. Auriculares.
 * Rosa__ : Micrófono
 * Azul claro__ : Entrada de Línea
 * Naranja:__  Altavoz Subwoofer y Altavoz Central
 * Negro:__  Altavoces de sonido envolvente 5.1 ó 7.1 traseros
* Digitales S/PDIF
  * Coaxial
  * Óptico

![](assets/img/Unidad07/u7112.png)



### Tipos de tarjetas de sonido

#### Integradas en placa base: 

![](assets/img/Unidad07/u7118.png)

#### PCI/PCI Express

![](assets/img/Unidad07/u7119.png)

![](assets/img/Unidad07/u7120.png)

#### USB:

![](assets/img/Unidad07/u7121.png)

![](assets/img/Unidad07/u7122.png)


#### Conectores de audio

![](assets/img/Unidad07/u7127.png)










# Bibliografía


_[https://computerhoy.com/reportajes/tecnologia/latencia-vs-megahercios-importante-elegir-ram-pc-420979](https://computerhoy.com/reportajes/tecnologia/latencia-vs-megahercios-importante-elegir-ram-pc-420979)_

_[https://computerhoy.com/noticias/hardware/todo-que-necesitas-saber-memoria-ram-37541](https://computerhoy.com/noticias/hardware/todo-que-necesitas-saber-memoria-ram-37541)_

_[https://hardzone.es/2018/01/17/asi-funciona-atencia-memoria-ram-ddr4/](https://hardzone.es/2018/01/17/asi-funciona-atencia-memoria-ram-ddr4/)_   

_[https://www.profesionalreview.com/2018/07/21/latencia-memoria-ram/](https://www.profesionalreview.com/2018/07/21/latencia-memoria-ram/)_

_[https://www.anandtech.com/show/3851/everything-you-always-wanted-to-know-about-sdram-memory-but-were-afraid-to-ask/2](https://www.anandtech.com/show/3851/everything-you-always-wanted-to-know-about-sdram-memory-but-were-afraid-to-ask/2)_   

_[https://hardzone.es/2019/01/06/single-rank-vs-dual-rank-amd-ryzen/](https://hardzone.es/2019/01/06/single-rank-vs-dual-rank-amd-ryzen/)_   

_[https://hardzone.es/tutoriales/componentes/tipos-memoria-ram-pc-historia/](https://hardzone.es/tutoriales/componentes/tipos-memoria-ram-pc-historia/)_

_[https://hardzone.es/tutoriales/componentes/diferencias-memoria-ram-ddr/](https://hardzone.es/tutoriales/componentes/diferencias-memoria-ram-ddr/)_

_[https://lau-re.wixsite.com/laure/post/dimm-vs-so-dimm-hay-diferencia-de-rendimiento](https://lau-re.wixsite.com/laure/post/dimm-vs-so-dimm-hay-diferencia-de-rendimiento)_

_[https://www.ionos.es/digitalguide/servidores/know-how/memoria-ecc-almacenamiento-seguro-de-datos/](https://www.ionos.es/digitalguide/servidores/know-how/memoria-ecc-almacenamiento-seguro-de-datos/)_   

_[https://infopcgamer.com/gddr5-vs-gddr5x-vs-hbm-vs-hbm2-vs-gddr6/](https://infopcgamer.com/gddr5-vs-gddr5x-vs-hbm-vs-hbm2-vs-gddr6/)_   

_[https://hardzone.es/reportajes/que-es/vram-tarjeta-grafica/](https://hardzone.es/reportajes/que-es/vram-tarjeta-grafica/)_   

_[https://www.ticarte.com/contenido/especificaciones-tecnicas-de-la-memoria-ram](https://www.ticarte.com/contenido/especificaciones-tecnicas-de-la-memoria-ram)_   

[https://www.ticarte.com/contenido/caracteristicas-fisicas-de-los-discos-duros-magneticos](https://www.ticarte.com/contenido/caracteristicas-fisicas-de-los-discos-duros-magneticos)

[https://www.adslzone.net/reportajes/internet/comparativa-almacenamiento-nube/](https://www.adslzone.net/reportajes/internet/comparativa-almacenamiento-nube/)

[https://www.seagate.com/es/es/tech-insights/what-is-nas-master-ti/](https://www.seagate.com/es/es/tech-insights/what-is-nas-master-ti/)

[https://pokde.net/system/pc/storage/sd-card-types-speed-class-explained](https://pokde.net/system/pc/storage/sd-card-types-speed-class-explained)

[https://www.xataka.com/basics/tipos-tarjetas-sd-que-significan-sus-clases-tipos-numeraciones](https://www.xataka.com/basics/tipos-tarjetas-sd-que-significan-sus-clases-tipos-numeraciones)

[https://www.xataka.com/basics/pen-drive-memoria-usb-que-sirve](https://www.xataka.com/basics/pen-drive-memoria-usb-que-sirve)

[https://es.wikipedia.org/wiki/Disco_compacto](https://es.wikipedia.org/wiki/Disco_compacto)

[https://hardzone.es/reportajes/que-es/que-es-blu-ray/](https://hardzone.es/reportajes/que-es/que-es-blu-ray/)

[https://www.ticarte.com/contenido/el-cd-rom-dvd-y-blu-ray-de-los-equipos-microinformaticos](https://www.ticarte.com/contenido/el-cd-rom-dvd-y-blu-ray-de-los-equipos-microinformaticos)

[http://cuartoinformatica.tecnojulio.com/2015/10/22/estructura-logica-del-disco-duro-actividad_12/](http://cuartoinformatica.tecnojulio.com/2015/10/22/estructura-logica-del-disco-duro-actividad_12/)

[http://www.carm.es/edu/pub/04_2015/2_5_2_contenido.html](http://www.carm.es/edu/pub/04_2015/2_5_2_contenido.html)

[https://informaticoalrescate.com/2019/08/08/diferencias-entre-los-sistemas-de-archivos/](https://informaticoalrescate.com/2019/08/08/diferencias-entre-los-sistemas-de-archivos/)

[https://www.kingston.com/spain/es/solutions/pc-performance/difference-between-slc-mlc-tlc-3d-nand#:~:text=SLC%20ofrece%20el%20mejor%20rendimiento,utilizarse%20en%20productos%20de%20consumo](https://www.kingston.com/spain/es/solutions/pc-performance/difference-between-slc-mlc-tlc-3d-nand#:~:text=SLC%20ofrece%20el%20mejor%20rendimiento,utilizarse%20en%20productos%20de%20consumo)\_ .

[https://www.profesionalreview.com/2018/03/10/discos-mbr-y-gtp-diferencias-entre-los-dos-estandares-de-la-actualidad/](https://www.profesionalreview.com/2018/03/10/discos-mbr-y-gtp-diferencias-entre-los-dos-estandares-de-la-actualidad/)

[http://www.carm.es/edu/pub/04_2015/2_5_1_contenido.htmlb](http://www.carm.es/edu/pub/04_2015/2_5_1_contenido.htmlb)

[https://www.idiskhome.com/resource/backup/mbr-vs-gpt.shtml](https://www.idiskhome.com/resource/backup/mbr-vs-gpt.shtml)

[https://www.profesionalreview.com/disco-duro/](https://www.profesionalreview.com/disco-duro/)

[https://www.diskmfr.com/know-how-internal-structure-details-of-solid-state-drives/](https://www.diskmfr.com/know-how-internal-structure-details-of-solid-state-drives/)

[https://computerhoy.com/noticias/hardware/que-es-ssd-como-funciona-que-tipos-existen-50726](https://computerhoy.com/noticias/hardware/que-es-ssd-como-funciona-que-tipos-existen-50726)

https://gamersnexus.net/guides/1497-ssd-architecture-1-what-is-tlc-nand-mlc-anatomy

https://www.profesionalreview.com/2023/01/22/u-2-vs-u-3/

Libro Montaje y Mantenimiento de Equipos Editorial: McGraw Hill

_[https://hardzone.es/reportajes/que-es/gpu-caracteristicas-especificaciones/](https://hardzone.es/reportajes/que-es/gpu-caracteristicas-especificaciones/)_

_[https://www.xataka.com/basics/tarjeta-grafica-que-que-hay-dentro-como-funciona](https://www.xataka.com/basics/tarjeta-grafica-que-que-hay-dentro-como-funciona)_ .

_[https://www.adslzone.net/2017/03/16/guia-como-entender-las-especificaciones-tecnicas-de-la-tarjeta-grafica-gpu/](https://www.adslzone.net/2017/03/16/guia-como-entender-las-especificaciones-tecnicas-de-la-tarjeta-grafica-gpu/)_

_[https://www.adslzone.net/2017/03/16/guia-como-entender-las-especificaciones-tecnicas-de-la-tarjeta-grafica-gpu/](https://www.adslzone.net/2017/03/16/guia-como-entender-las-especificaciones-tecnicas-de-la-tarjeta-grafica-gpu/)_

_[https://hardzone.es/2018/08/26/vga-dvi-hdmi-displayport-salidas-video/](https://hardzone.es/2018/08/26/vga-dvi-hdmi-displayport-salidas-video/)_

_[https://hardzone.es/reportajes/comparativas/diferencias-conectores-dvi/](https://hardzone.es/reportajes/comparativas/diferencias-conectores-dvi/)_

_[https://es.wikipedia.org/wiki/Modelo_de_color_CMYK](https://es.wikipedia.org/wiki/Modelo_de_color_CMYK)_

_[https://es.wikipedia.org/wiki/RGB](https://es.wikipedia.org/wiki/RGB)_

_[https://www.hardware-corner.net/guides/guide-to-computer-ports-and-connectors/](https://www.hardware-corner.net/guides/guide-to-computer-ports-and-connectors/)_

_[https://www.adslzone.net/reportajes/tecnologia/bluetooth/](https://www.adslzone.net/reportajes/tecnologia/bluetooth/)_

_[https://www.datacentermarket.es/tendencias-tic/voz-experto/1120929032809/cableado-proxima-oleada-de-redes-inalambricas-empresas.1.html](https://www.datacentermarket.es/tendencias-tic/voz-experto/1120929032809/cableado-proxima-oleada-de-redes-inalambricas-empresas.1.html)_

_[https://es.wikipedia.org/wiki/Sound_Blaster#Primeras_Sound_Blasters:_El_primer_pack](https://es.wikipedia.org/wiki/Sound_Blaster#Primeras_Sound_Blasters:_El_primer_pack)_

_[https://helpx.adobe.com/es/photoshop-elements/key-concepts/raster-vector.html](https://helpx.adobe.com/es/photoshop-elements/key-concepts/raster-vector.html)_

_[https://www.profesionalreview.com/2021/02/07/tgp-vs-tdp-vs-tbp/](https://www.profesionalreview.com/2021/02/07/tgp-vs-tdp-vs-tbp/)_

_[https://www.estudiomarhea.net/manual-de-sonido-08-la-mesa-de-mezclas/](https://www.estudiomarhea.net/manual-de-sonido-08-la-mesa-de-mezclas/)_

_[https://hardzone.es/tutoriales/componentes/tipo-conexiones-audio/](https://hardzone.es/tutoriales/componentes/tipo-conexiones-audio/)_








