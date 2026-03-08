# Representación de la información

La transmisión de información entre el ser humano y la computadora puede hacerse de muchas formas:​

* Mediante caracteres alfanuméricos (letras {a, b, ..., z} y números {0, 1, ..., 9}). Por ejemplo, los introducidos al ordenador mediante un teclado.​

* Mediante sonidos: como los introducidos al ordenador a través de un micrófono, o que salen del ordenador por los altavoces.​

* Mediante vídeos: como las imágenes obtenidas a través de una cámara de vídeo.​

* Mediante gráficos e imágenes: por ejemplo, una imagen introducida por un escáner, o fotografías descargadas de una cámara de fotos digital.​

* En general, cualquier tipo de dato enviado por un periférico del ordenador capaz de tomar datos de cualquier tipo y enviarlo al ordenador, o a la inversa.​

En cada caso el canal es diferente, y para proceder a la comunicación de los datos es necesario cambiar la forma en que estos se representan. Por lo tanto, los datos deben ser traducidos o codificados. La traducción o codificación es necesaria cuando los códigos utilizados por el emisor, el canal y el receptor son diferentes.​

## Sistemas de numeración

Se define **sistema de numeración** como el conjunto de símbolos o dígitos utilizados para la representación de cantidades, así como las reglas que rigen dicha representación.​

Un sistema de numeración se distingue por su base, que es el número de símbolos que utiliza, y se caracteriza por ser el coeficiente que determina cuál es el valor de cada símbolo dependiendo de su posición (peso).​

- Símbolos → Dependen de la base del sistema:​

- Sistema decimal → 10 símbolos → {0,1,2...9}​

- Sistema binario → 2 símbolos→ {0,1}​

- Sistema octal → 8 símbolos → {0,1,...7}​

- Sistema hexadecimal →16 símbolos →{0,1,...9,A,B,C,D,E,F}​​

## Sistema de numeración decimal

**Base=10**

El sistema de numeración decimal, es un sistema de numeración posicional en el que las cantidades se representan utilizando como base aritmética el número diez. ​

Es el sistema de numeración que utilizamos normalmente y utiliza diez dígitos o símbolos: 0, 1, 2, 3, 4, 5, 6, 7, 8, 9​

![image](https://github.com/user-attachments/assets/e465d908-8889-43a2-b6e9-873c01bacca3)

## Sistema de numeración binario

**Base=2**

El sistema de numeración binario utiliza sólo dos dígitos (0 y 1) para representar cantidades, por lo que su base es 2. Cada dígito de un número representado por este sistema se denomina bit (binary digit).​

Los bits tienen distinto valor dependiendo de la posición que ocupan; por eso este sistema también es posicional. Estos valores vienen determinados por una potencia de base 2 que la vamos a llamar peso.

![image](https://github.com/user-attachments/assets/30f2fbd4-f864-4f60-8dfb-0367883f2390)

### Conversión binario a decimal 

![image](https://github.com/user-attachments/assets/fe9c391d-4391-4d18-900e-b75b47d2d89f)

### Conversión decimal a binario.

Para representar un número decimal  en binario, realizaremos divisiones sucesivas por 2 hasta obtener un cociente menor de 2.​ El número resultante será el último cociente y tras él los restos obtenidos en cada una de las divisiones, empezando por el último.​

![image](https://github.com/user-attachments/assets/1fe2a142-c188-48c1-9874-020eb2e28482)


![image](https://github.com/user-attachments/assets/926b216f-0514-4c97-b057-c0926b9e2e7d)

## Sistema de numeración hexadecimal

**Base=16**

La notación Hexadecimal se utiliza para reducir grandes cadenas de números binarios en conjuntos de cuatro dígitos, que se pueden de esta forma comprender fácilmente.

![image](https://github.com/user-attachments/assets/d17c9672-c4dd-4134-8543-9f9c581c1959)

### Conversión hexadecimal a decimal

![image](https://github.com/user-attachments/assets/74f3275e-b89c-4e2d-b348-40a6050e074a)

### Conversión decimal a hexadecimal

![image](https://github.com/user-attachments/assets/21d6eb8f-8f72-4dab-8689-1a2df6e3be90)

# Unidades de medida de la información.

Un byte es la unidad de información fundamental usada en informática y telecomunicaciones. Está compuesta por 8 bits contiguos, razón por la que también se le denomina octeto. Para representarlo usamos la B MAYÚSCULA.​ 

**1 Byte=8 bits // 1B=8b**



* Para pasar de Bytes a bits solamente tendremos que multiplicar el valor por 8.​

100 Bytes = 100*8 = 800 bits


* Para pasar de bits a Bytes tendremos que dividir el valor.​

256 bits = 256/8 = 32 bytes

## kilobyte VS kibibyte.​

Los prefijos empleados para los múltiplos del byte normalmente son los mismos del **Sistema internacional**, pero también se utilizan los **prefijos binarios**, existiendo diferencias entre ellos, ya que según el tipo de prefijo utilizado los bytes resultantes tienen valores diferentes.​ Esto se debe a que los prefijos del SI se basan en base 10 (sistema decimal), y los prefijos binarios se basan en base 2 (sistema binario), por ejemplo:​

![image](https://github.com/user-attachments/assets/b42f074d-96be-4de9-ab06-1f7a559ada44)

### Unidades Sistema internacional

![image](https://github.com/user-attachments/assets/22308a20-9fd7-46b3-b301-ef9f5516f7c0)

### Unidades Sistema Binario

![image](https://github.com/user-attachments/assets/884d16d6-3e97-4630-bab1-24fd230f181a)

### Conversiones de Sistema internacional a Sistema Binario

Para convertir en Sistema Binario es necesario multiplicar o dividir por 2^10 o lo que es lo mismo por 1024 por cada salto de unidad.

* 2 MiB = 2 * 210=2*1024 = 2048 KiB (1 salto)​

* 2TiB =2* 230 = 2* 1024*1024*1024 = 21.47.483.648 KiB (3 saltos)​

* 6.000.000 KiB = 6.000.000/1024 = 6.000.000/210  = 5859,375 MiB (1 salto)​

* 6.000.000 KiB = 6.000.000 /1024/1024/1024/1024= 6.000.000 / 240= 5,45*10-7 PiB (4 saltos)

### Espacio en disco
Un fabricante nos dice que un SSD tiene 500 GB que según el SI son 500.000.000.000 Bytes​

A nivel binario, 1 KiB equivale a 1024 Bytes y no 1000 Bytes, por tanto un MiB son 1024 KB y un GiB son 1024 MB. Así, el cálculo siguiendo el ejemplo del SSD de 500 GB es que tendremos 500.000.000.000 dividido entre (1024 x 1024 x 1024), y el resultado nos da 465.66GiB y no 500 GB.​

500,000,000,000 / 1024/1024/1024 = 465.66 GiB​

Para pasar 465.66 GiB a B.​

De la tabla anterior tenemos que 1 GiB = 230 =  1 073 741 824  bytes​

Por tanto 465GiB = 465*1 073 741 824  = 499.289.948.160 bytes​
