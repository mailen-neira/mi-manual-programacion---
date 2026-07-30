# 📖 De Cero a IA

## Mi Manual de Programación

Este repositorio documenta todo lo que voy aprendiendo durante mi camino desde cero en programación hasta especializarme en IA.


# Semana 0 - Pensamiento Computacional

¿Qué es el pensamiento computacional?

Antes de aprender un lenguaje de programación, hay que aprender a pensar como una computadora.

La computadora no "adivina" lo que queremos hacer. Necesita que el problema esté definido de manera clara y ordenada.

Programar consiste, primero, en aprender a resolver problemas paso a paso.

## TODO PROGRAMA REQUIERE 3 PASOS

```
INPUT
   ↓
PROCESO
   ↓
OUTPUT
```

Input: los datos que ingresan al programa.

Proceso: las instrucciones que transforman esos datos.

Output: el resultado que obtiene el usuario.

Ejemplo

Quiero saber cuál es el doble de un número.

```
INPUT
Número: 5
↓
PROCESO
Multiplicar por 2
↓
OUTPUT
10
```

Como calcular la edad de una persona?

```
INPUT
Año de nacimiento
↓
PROCESO
```

Año actual - Año de nacimiento

```
↓
OUTPUT
Edad
```

## COMO ENTIENDE LA COMPUTADORA LA INFORMACION?

La información en una computadora se almacena y procesa utilizando el sistema binario (0 y 1). Para representar caracteres como letras, números y símbolos se utilizan estándares como ASCII y Unicode, que asignan un valor numérico a cada uno.

La unidad mínima de información es el bit, que solo puede tener dos valores:

0 = apagado

1 = encendido

Ocho bits forman un byte.

Cada bit dentro de un byte tiene un valor según su posición:

| Posición del bit |   7 |  6 |  5 |  4 |  3 |  2 |  1 |  0 |
| :--------------: | --: | -: | -: | -: | -: | -: | -: | -: |
|     **Valor**    | 128 | 64 | 32 | 16 |  8 |  4 |  2 |  1 |

De esta forma, un byte puede representar 256 valores diferentes, desde 0 hasta 255.

Ejemplo

La letra A tiene el valor 65 en ASCII.

En binario se representa así:

|   Bit   |   7 |  6 |  5 |  4 |  3 |  2 |  1 |  0 |
| :-----: | --: | -: | -: | -: | -: | -: | -: | -: |
|  Valor  | 128 | 64 | 32 | 16 |  8 |  4 |  2 |  1 |
| Binario |   0 |  1 |  0 |  0 |  0 |  0 |  0 |  1 |

64 + 1 = 65

Por eso el byte:

01000001

Ejemplo: la palabra "HELLO"

Cada letra tiene un valor en ASCII y ese valor se representa en binario.

| Letra | ASCII (decimal) | Binario (8 bits) |
| ----- | --------------: | ---------------- |
| H     |              72 | **01001000**     |
| E     |              69 | **01000101**     |
| L     |              76 | **01001100**     |
| L     |              76 | **01001100**     |
| O     |              79 | **01001111**     |

Entonces, la palabra HELLO se almacena como:

01001000 01000101 01001100 01001100 01001111

Cada grupo de 8 bits representa 1 byte, y cada byte representa una letra.

Idea clave: La computadora no entiende letras, imágenes ni música. Solo entiende bits (0 y 1). Somos nosotros quienes usamos estándares como ASCII o Unicode para interpretar esos bits como texto.

Si la computadora solo entiende 0 y 1... ¿cómo hacemos para decirle qué queremos que haga?

## DEL ALGORITMO AL CODIGO

Primero pensamos la solución.

```
Después la escribimos
Problema
↓
Algoritmo
↓
Pseudocódigo
↓
Código
```

Aunque todavia nos falta definir algunos conceptos

ALGORITMO: es una secuncia ordenada de pasos para resolver un problema. No depende del lenguaje de programacion. 

Ej:

 Problema: calcular el promedio de tres notas.

Algoritmo

Leer las tres notas.

Sumarlas.

Dividir por tres.

Mostrar el promedio.

Idea clave

El algoritmo es el camino que transforma un problema en una solución.

PSEUDOCODIGO: es la forma de escribir un algoritmo usando lenguaje humano, sin respetar la sintaxis de un lenguaje de programacion. 

Ej:

Leer edad

Si edad >= 18

    Mostrar "Mayor de edad"

Sino

    Mostrar "Menor de edad"

CODIGO: es la implementacion de un algoritmo en un lenguaje que la computadora pueda ejecutar. 

Ej: C, Python, Java, Scracht

¿Qué hace que un algoritmo sea bueno?

No alcanza con resolver el problema.

También debe hacerlo de manera:

✔ Correcta.

✔ Eficiente.

✔ Rápida.

Dos algoritmos pueden llegar al mismo resultado, pero uno puede necesitar mucho menos tiempo que otro.

Anatomía de un programa

```c
#include <stdio.h>
int main(void)
{
    printf("Hello, world!\n");
}
```

Si observamos este programa por primera vez, probablemente veamos un conjunto de palabras y símbolos difíciles de entender.

Sin embargo, un programa no es una sola pieza.

Está formado por distintos elementos que cumplen funciones específicas.

Comprender cada uno de ellos nos permitirá entender cómo funciona cualquier programa, sin importar el lenguaje en el que esté escrito.

## 1. FUNCIONES

Una función es un bloque de código diseñado para realizar una tarea específica.

Podemos pensar en una función como un verbo.

Ejemplos:

printf() → mostrar información.

scanf() → leer información.

sqrt() → calcular una raíz cuadrada.

En el programa anterior:

```c
printf("Hello, world!");
```

printf() es una función.

Dónde lo veo en un programa?

En la instrucción:

```c
printf("Hello, world!");
```

printf() es una función. Su trabajo es mostrar información en la pantalla.

## 2. PARAMETROS (Argumentos)

Las funciones muchas veces necesitan información para poder trabajar.

Esa información se llama parámetro o argumento.

Ejemplo:

```c
printf("Hello, world!");
```

El parametro es: 

"Hello, world!"

Si canbiamos el parametro:

```c
printf("Hola Mailen");
```

La funcion sigue siendo la misma. 

Lo unico que cambia es la informacion que recibe.

Una función puede comportarse de distintas maneras según los parámetros que reciba.

¿Dónde lo veo en un programa?

En la misma instrucción:

```c
printf("Hello, world!");
```

"Hello, world!" es el parámetro que recibe la función. Es la información que utilizará para realizar su tarea.

## 3. SIDE EFFECT (efecto secundario)

Al ejecutar una función pueden ocurrir cambios visibles.

Eso se conoce como efecto secundario.

Ejemplo:

```c
printf("Hola");
```

Produce este resultado

HOLA

El texto aparece en la pantalla.

Ese cambio es el efecto secundario de ejecutar printf().

Otros ejemplos de efectos secundarios son:

reproducir un sonido;

mover un personaje;

guardar un archivo;

cambiar un color en pantalla.

¿Dónde lo veo en un programa?

Al ejecutar:

```c
printf("Hello, world!");
```

aparece el texto en la pantalla.

Ese cambio visible es el efecto secundario de ejecutar la función

## 4. RETURN VALUE (valor retorno)

No todas las funciones solo realizan acciones.

Muchas también devuelven un resultado.

Ese resultado se llama valor de retorno.

Por ejemplo:

```c
sqrt(25)
```

La funcion devuelve

5

Otro ejemplo:

2 + 3

Devuelve

5

El valor puede usarse despues en otra parte del programa

Diferencia importante

El efecto secundario es algo que ocurre y podemos observar (como imprimir un mensaje).

El valor de retorno es un dato que la función devuelve al programa.

¿Dónde lo veo en un programa?

En printf() todavía no podemos observar claramente el valor de retorno.

Lo estudiaremos más adelante con funciones que, además de ejecutar una acción, devuelven un resultado para que el programa pueda seguir utilizándolo.

Nota: este concepto se introdujo en la Semana 0 para comprender cómo funcionan las funciones. Lo retomaremos más adelante con ejemplos más completos

## 5. EXPRESIONES BOOLEANAS

Hasta ahora el programa ejecutó todas las instrucciones en orden.

Pero...

¿Qué pasa si queremos que haga algo solamente cuando se cumple una condición?

Para eso existen las expresiones booleanas.

Una expresión booleana solo puede tener dos respuestas:

Verdadero (True) o Falso (False)

Si o No

1 o 0

Ejemplo:

5 > 3

Resultado

Verdadero (true)

¿Dónde la voy a ver en un programa?

Las expresiones booleanas aparecen cuando el programa necesita responder preguntas como:

edad >= 18

El resultado solo puede ser:

true

false

## 6. CONDICIONALES

Las condicionales permiten que el programa tome decisiones según el resultado de una expresión booleana.

Ejemplo cotidiano:

¿Está lloviendo?

Sí → Llevar paraguas.

No → Salir sin paraguas.

En programacion ocurre excatmente los mismo.

¿Dónde lo voy a ver en un programa?

Las condicionales utilizan expresiones booleanas para decidir qué instrucciones ejecutar.

Por ejemplo:

if (edad >= 18)

significa:

"Si la condición es verdadera, ejecutá las instrucciones que siguen."

## 7. LOOPS (bucles)

En lugar de escribir la misma instrucción muchas veces, utilizamos un bucle.

```
Ejemplo:
Repetir 10 veces
↓
```

Dar un paso.

Los bucles permiten automatizar tareas repetitivas.

Dónde lo voy a ver en un programa?

Un bucle permite repetir una misma acción varias veces sin escribir el mismo código una y otra vez.

Más adelante conoceremos estructuras como:

for

while

Que se usan para repetir instrucciones.

Nuestro primer lenguaje de programación: Scratch

Hasta ahora aprendimos los conceptos fundamentales de la programación.

Sin embargo, todavía escribir código puede resultar difícil, ya que debemos recordar la sintaxis de un lenguaje y escribir cada instrucción correctamente.

Por ese motivo, antes de comenzar con un lenguaje como C o Python, introducimos Scratch, un lenguaje de programación visual desarrollado por el MIT (Massachusetts Institute of Technology).

En Scratch no escribimos código: construimos programas uniendo bloques, como si fueran piezas de un rompecabezas.

Esto nos permite concentrarnos en lo más importante:

Aprender a pensar como programadores.

¿Por qué Scratch?

Scratch elimina uno de los mayores problemas de quienes comienzan a programar: los errores de sintaxis.

En lugar de preocuparnos por escribir correctamente cada instrucción, podemos enfocarnos en comprender la lógica del programa.

De esta manera aprendemos conceptos que utilizaremos más adelante en cualquier lenguaje de programación.

Conceptos que ya conocemos y aparecen en scratch:

| Concepto              | ¿Cómo aparece en Scratch?                                                               |
| --------------------- | --------------------------------------------------------------------------------------- |
| Algoritmo             | Secuencia de bloques que resuelven un problema.                                         |
| Funciones             | Bloques que realizan una acción específica.                                             |
| Parámetros            | Valores que modifican el comportamiento de un bloque (por ejemplo, mover **10** pasos). |
| Condicionales         | Bloques **Si... entonces**.                                                             |
| Expresiones booleanas | Preguntas que solo pueden responder verdadero o falso.                                  |
| Bucles                | Bloques **Repetir** o **Por siempre**.                                                  |
| Side Effect           | Un personaje se mueve, habla, cambia de disfraz o reproduce un sonido.                  |

Página oficial

Scratch puede utilizarse de forma gratuita desde:

🔗 https://scratch.mit.edu

Cierre de la Semana 0

Conceptos aprendidos

En esta semana conocimos los fundamentos de la programación.

Aprendimos que:

-Una computadora representa toda la información mediante bits;

-los problemas pueden resolverse mediante algoritmos;

-un algoritmo puede escribirse como pseudocódigo antes de convertirse en código;

-un programa está formado por funciones, parámetros y bloques de instrucciones;

-los programas pueden tomar decisiones mediante expresiones booleanas y condicionales;

-las tareas repetitivas pueden automatizarse mediante bucles;

-Scratch nos permite practicar todos estos conceptos sin preocuparnos todavía por la sintaxis de un lenguaje.

Con estos fundamentos estamos preparados para comenzar a escribir nuestros primeros programas.

## CURSO DE REFERENCIA

Este manual está basado en mi recorrido de aprendizaje a través del curso CS50x: Introduction to Computer Science, desarrollado por la Universidad de Harvard y dictado por el profesor David J. Malan.

CS50 es un curso introductorio de Ciencias de la Computación que enseña los fundamentos de la programación y del pensamiento computacional. A lo largo del curso se trabajan conceptos fundamentales utilizando diferentes lenguajes y herramientas, entre ellos Scratch, C, Python, SQL, HTML, CSS y JavaScript.

El objetivo de este manual no es reemplazar el contenido del curso, sino documentar mi proceso de aprendizaje con mis propias palabras, complementándolo con ejemplos, explicaciones y notas personales que me ayuden a comprender mejor cada tema.

🔗 Curso oficial de CS50: https://cs50.harvard.edu/x/

# CS50x – Semana 1

Introducción al lenguaje C

¿Qué es un lenguaje de programación?

Un lenguaje de programación es un idioma que utilizamos para comunicarnos con la computadora.

Nos permite escribir instrucciones que la computadora ejecutará para realizar una determinada tarea.

En la Semana 1 comenzamos a trabajar con C, uno de los lenguajes de programación más importantes e influyentes de la historia.

Código fuente (Source Code)

El código que escribimos los programadores se llama código fuente.

Está pensado para que los humanos podamos leerlo, escribirlo y entenderlo.

Ejemplo:

```c
printf("¡Hermosa mañana, ¿verdad?\n");
```

Código máquina (Machine Code)

La computadora no entiende lenguaje C.

Solo entiende instrucciones representadas mediante 0 y 1, llamadas código máquina.

Por eso necesitamos traducir nuestro programa antes de ejecutarlo.

¿Qué es un compilador?

Un compilador es un programa que traduce el código fuente escrito por el programador a código máquina.

Es el intermediario entre nuestro lenguaje y el lenguaje que entiende la computadora.

Sin un compilador, la computadora no podría ejecutar un programa escrito en C.

¿Qué significa compilar?

Compilar significa traducir el código fuente a código máquina.

Durante ese proceso, el compilador también verifica que el programa no tenga errores de sintaxis.

Si encuentra un error, detiene la compilación e informa qué ocurrió.

Si todo está correcto, genera un archivo ejecutable.

```
Proceso completo
Programador
      ↓
```

Escribe código fuente (C)

```
      ↓
Compilador
      ↓
```

Traduce a código máquina (0 y 1)

      ↓

Genera un programa ejecutable

      ↓

Computadora ejecuta el programa

En CS50 normalmente utilizaremos:

```c
make hello
```

Este comando compila el programa.

Luego:

```c
./hello
```

Ejecuta el archivo compilado.

Nota personal: El comando ./ significa "ejecutá el programa que está en la carpeta actual"

Esta semana utilizaremos el programa VSC (Visual Studio Code)

VS Code será nuestro entorno de desarrollo durante el curso.

Con él podremos:

escribir programas;

editar archivos;

compilar código;

ejecutar programas;

corregir errores.

Además, VS Code resalta automáticamente la sintaxis utilizando distintos colores, lo que facilita la lectura del código.

GUI (Graphical User Interface)

Es la Interfaz Gráfica de Usuario.

Utilizamos ventanas, botones, carpetas e íconos para interactuar con la computadora.

Ejemplo:

abrir un archivo haciendo doble clic.

CLI (Command Line Interface)

Es la Interfaz de Línea de Comandos.

Aquí escribimos órdenes directamente para que la computadora las ejecute.

Ejemplos:

```c
make hello
./hello
```

En programación se utiliza muchísimo porque brinda mayor control y velocidad que una interfaz gráfica.

La sintaxis

Cada lenguaje de programación tiene reglas propias.

A esas reglas las llamamos sintaxis.

Es el equivalente a la gramática de un idioma.

Si la sintaxis es incorrecta, el programa no podrá compilar.

Errores frecuentes:

olvidar un punto y coma;

escribir mal una función;

olvidar una llave.

Mi primer programa en C

Tradicionalmente, el primer programa imprime el mensaje "Hello, world!".

Es una tradición histórica utilizada para comprobar que el compilador y el entorno funcionan correctamente.

En este manual decidí personalizar ese ejemplo con una frase muy conocida en Argentina.

```c
#include <stdio.h>
int main(void)
{
    printf("¡Hermosa mañana, ¿verdad?\n");
}
```

El funcionamiento es exactamente el mismo.

Simplemente cambiamos el texto que se imprime.

Analizando el programa

```c
#include <stdio.h>
```

Incluye la biblioteca estándar de entrada y salida.

Gracias a ella podemos utilizar funciones como:

```c
printf()
int main(void)
```

Es la función principal del programa.

Todo programa en C comienza ejecutándose aquí.

```c
printf()
```

Es una función que imprime texto en pantalla.

En nuestro ejemplo imprime:

¡Hermosa mañana, ¿verdad?

;

El punto y coma indica el final de una instrucción.

En C casi todas las instrucciones terminan con ;

Secuencias de escape

Son caracteres especiales que modifican la salida del texto.

\n

Nueva línea.

```c
printf("¡Hermosa mañana, ¿verdad?\n");
```

Después de imprimir el mensaje, el cursor baja a la línea siguiente.

\r

Retorno de carro.

Hace que el cursor vuelva al comienzo de la línea.

Me gusta imaginarlo como el movimiento del cabezal al leer una secuencia de ADN: vuelve al inicio para comenzar nuevamente. (direccion  5' ◀────────────── 3' )

\"

Permite imprimir comillas dobles dentro del texto.

\\

Permite imprimir una barra invertida.

Los errores

Cuando escribimos un programa incorrectamente, el compilador informa el problema.

Por ejemplo:

falta un punto y coma;

falta un #include;

escribimos mal una función.

VS Code muestra:

la línea donde ocurrió el error;

el tipo de error;

una explicación para ayudarnos a corregirlo.

Aprender a interpretar estos mensajes será una habilidad fundamental.

Bibliotecas

No hace falta escribir todas las funciones desde cero.

Muchas ya fueron desarrolladas por otros programadores.

Ese conjunto de funciones forma parte de una biblioteca.

Para utilizarlas debemos incluir el archivo correspondiente.

Ejemplo:

```c
#include <stdio.h>
```

Archivos cabecera (.h)

Los archivos que terminan en .h se llaman Header Files o Archivos Cabecera.

Contienen las declaraciones necesarias para utilizar funciones ya existentes.

Por ejemplo:

stdio.h

Nos permite utilizar printf()

Documentación (Manual cs50)

Cuando no sabemos cómo funciona una función, podemos consultar la documentación.

CS50 utiliza las Manual Pages (man pages).

En ellas podemos encontrar:

qué hace una función;

cómo se escribe;

qué parámetros recibe;

qué valor devuelve.

A medida que avancemos en el curso iremos consultando estas páginas con frecuencia.

Ejemplo: get_string()

Uno de los primeros ejemplos que presenta CS50 es la función get_string().

Esta función pertenece a la biblioteca de CS50 y permite solicitar al usuario que escriba un texto.

Ese texto se almacena en una variable de tipo string.

Por ejemplo:

```c
string nombre = get_string("¿Cómo te llamás? ");
```

En este caso:

string indica que la variable almacenará texto.

get_string() solicita ese texto al usuario.

El valor ingresado queda guardado en la variable nombre.

Entrada → Proceso → Salida

Todo programa sigue el mismo esquema.

Input

Información que recibe el programa.

Ejemplo: como te llamas?

Procesamiento

El programa utiliza esa información para realizar una tarea.

Output

Devuelve un resultado.

Ejemplo: Hola, Mailen

Importante: get_string() es solo uno de los muchos comandos y funciones que encontraremos en las Manual Pages de CS50. A medida que avancemos en el curso iremos incorporando nuevas funciones y nuevos tipos de datos.

```
Comparación con Scratch
En Scratch hacíamos:
Preguntar
↓
Esperar respuesta
↓
```

Unir "Hola"

```
↓
Mostrar
```

En C hacemos exactamente lo mismo escribiendo:

```c
string answer = get_string("Como te llamas? ");
printf("Hola, %s\n", answer);
```

Scratch y C: la misma lógica, distinta forma

Hasta ahora vimos que el programa en C hace exactamente lo mismo que hacíamos en Scratch.

En ambos casos el programa sigue tres pasos:

Entrada (Input)

```
        ↓
Procesamiento
        ↓
```

Salida (Output)

La diferencia no está en lo que hace, sino en cómo se lo indicamos.

En Scratch usamos bloques gráficos.

```
Preguntar
↓
Esperar respuesta
↓
```

Unir "Hola"

```
↓
Mostrar
```

En C escribimos instrucciones utilizando texto.

```c
string answer = get_string("¿Cómo te llamas? ");
printf("Hola, %s\n", answer);
```

En ambos casos el programa realiza exactamente la misma tarea.

Lo único que cambió fue la forma de darle las instrucciones.

Entonces... ¿por qué aprender C?

Esta es una muy buena pregunta.

Si Scratch ya funciona, ¿por qué dejar de usarlo?

La respuesta es que Scratch fue diseñado para aprender los fundamentos de la programación.

C, en cambio, es un lenguaje de programación real que nos brinda mucho más control sobre el funcionamiento de la computadora.

Ese mayor control tiene un precio: ahora debemos escribir cada instrucción con precisión.

Por eso C exige respetar una sintaxis estricta.

Un cambio importante

En Scratch casi nunca pensamos dónde está guardado nuestro proyecto.

Simplemente abrimos Scratch y comenzamos a trabajar.

Con C la situación cambia.

Ahora nuestros programas son archivos que viven dentro de carpetas.

Nosotros debemos crearlos, organizarlos, compilarlos y ejecutarlos.

Para poder hacerlo necesitaremos aprender una nueva herramienta: la terminal.

Y ahí recién comenzaría el siguiente capítulo.

Antes de aprender los comandos

Antes de comenzar a utilizar la terminal, es importante conocer los elementos con los que trabajaremos durante todo el curso.

Cada vez que programemos, interactuaremos principalmente con carpetas, archivos y programas ejecutables.

Comprender la diferencia entre ellos hará que los comandos de la terminal tengan mucho más sentido.

La carpeta (Directory)

Una carpeta (o directorio) es un contenedor que sirve para organizar archivos y otras carpetas.

Podemos imaginarla como una carpeta física donde guardamos documentos relacionados con un mismo proyecto.

Por ejemplo, si estamos creando un programa llamado Calculadora, podríamos tener una carpeta llamada:

📁 calculadora

Dentro de esa carpeta guardaremos todos los archivos relacionados con ese proyecto.

El archivo fuente

El archivo fuente es el documento donde escribimos nuestro programa en C.

Siempre tendrá la extensión:

.c

Por ejemplo:

📄 programa.c

o

📄 calculadora.c

La extensión .c le indica a la computadora que ese archivo contiene código escrito en el lenguaje C.

Este archivo todavía no puede ejecutarse.

Primero debe ser compilado.

El programa ejecutable

Cuando compilamos nuestro archivo fuente, la computadora crea un nuevo archivo.

Ese archivo ya contiene instrucciones que el sistema operativo puede ejecutar.

Por ejemplo:

⚙ programa

Observá algo importante.

El archivo fuente se llama:

programa.c

Mientras que el programa ejecutable se llama:

programa

No son el mismo archivo.

Uno contiene el código que escribimos.

El otro contiene el programa listo para ejecutarse.

¿Cómo se relacionan?

Durante el curso trabajaremos siguiendo este proceso:

📁 Mi_Proyecto

│

├── 📄 programa.c

│        │

│        │  (make programa)

│        ▼

│

└── ⚙ programa

Primero escribimos nuestro código en programa.c.

Después utilizamos el compilador para transformarlo en un programa ejecutable llamado programa.

Finalmente ejecutamos ese programa.

Un ejemplo completo

Imaginemos que queremos crear un programa para saludar.

Nuestra carpeta podría verse así:

📁 saludo

│

├── 📄 saludo.c

│

└── ⚙ saludo

La carpeta saludo contiene todo el proyecto.

saludo.c es el archivo donde escribimos el código.

saludo es el programa compilado que podemos ejecutar.

¿Por qué es importante entender esto?

A partir de ahora veremos comandos como:

cd saludo

code saludo.c

```c
make saludo
./saludo
```

Si no entendemos qué representa cada uno de esos nombres, los comandos parecerán confusos.

Pero ahora sabemos que:

saludo puede ser una carpeta.

saludo.c es el archivo fuente.

saludo (sin .c) también puede ser el programa ejecutable, según el contexto.

La terminal distingue entre ellos por el comando que utilizamos y por el lugar donde se encuentran.

¿Qué deberías haber entendido?

Al terminar esta sección deberías poder responder:

¿Qué es una carpeta?

¿Qué es un archivo fuente?

¿Qué significa la extensión .c?

¿Qué es un programa ejecutable?

¿Por qué existen dos archivos llamados casi igual (programa.c y programa)?

Idea

  │

  ▼

Escribimos el código

(programa.c)

  │

  ▼

Compilamos

(make programa)

  │

  ▼

Se crea el ejecutable

(programa)

  │

  ▼

Lo ejecutamos

(./programa)

Comandos esenciales de la terminal

Ahora que conocemos la diferencia entre una carpeta, un archivo fuente y un programa ejecutable, estamos listos para aprender los comandos que utilizaremos durante todo el curso.

No es necesario memorizarlos. A medida que avancemos, iremos aprendiendo cada uno en profundidad.

Por ahora, esta tabla servirá como una guía para entender qué hace cada comando y en qué momento lo utilizaremos.

| Comando | ¿Qué significa? | ¿Qué hace? | ¿Cuándo lo usamos? |
|----------|-----------------|------------|--------------------|
| `pwd` | Print Working Directory | Muestra la carpeta en la que estamos trabajando. | Cuando queremos saber dónde estamos. |
| `ls` | List | Muestra los archivos y carpetas del directorio actual. | Cuando queremos ver qué hay en la carpeta actual. |
| `cd` | Change Directory | Cambia de una carpeta a otra. | Cuando queremos entrar en otra carpeta. |
| `mkdir` | Make Directory | Crea una carpeta nueva. | Cuando comenzamos un proyecto nuevo. |
| `code` | Visual Studio Code | Abre un archivo o una carpeta en VS Code. | Cuando queremos escribir o editar código. |
| `make` | Make | Compila un archivo fuente escrito en C. | Cuando terminamos de escribir el programa y queremos convertirlo en un ejecutable. |
| `./` | Ejecutar programa | Ejecuta un programa compilado. | Cuando queremos probar nuestro programa. |
| `cp` | Copy | Copia un archivo o una carpeta. | Cuando queremos hacer una copia. |
| `mv` | Move | Mueve o cambia el nombre de un archivo o carpeta. | Cuando queremos reorganizar o renombrar archivos. |
| `rm` | Remove | Elimina archivos o carpetas. | Cuando ya no los necesitamos. |

Un flujo de trabajo típico

Durante el curso de CS50, muchas veces seguiremos una secuencia parecida a esta:

Verificamos dónde estamos.

pwd

Vemos qué hay en esa carpeta.

ls

Entramos en la carpeta del proyecto.

cd mi_proyecto

Abrimos el archivo para escribir el código.

code programa.c

Compilamos el programa.

```c
make programa
```

Ejecutamos el programa.

```c
./programa
```

Algo importante

No te preocupes si todavía no entendés completamente algunos comandos.

Por ejemplo, make o ./programa pueden parecer extraños en este momento.

Es completamente normal.

En los próximos apartados estudiaremos cada comando por separado:

¿Qué problema resuelve?

¿Por qué existe?

¿Cómo funciona?

¿Qué ocurre dentro de la computadora cuando lo usamos?

¿Cuáles son los errores más comunes?

Cuando terminemos ese recorrido, esta tabla dejará de ser una lista de comandos y se convertirá en un mapa que entenderás por completo.

El entorno de trabajo del programador

¿Por qué aparece la terminal?

Hasta ahora escribíamos programas, pero todavía no nos habíamos preguntado una cosa muy importante:

¿Dónde vive un programa?

La respuesta es simple.

Un programa es un archivo.

Y, como cualquier archivo, está guardado dentro de una carpeta.

Si queremos crear programas, moverlos, organizarlos, compilarlos o ejecutarlos, primero necesitamos aprender a movernos entre las carpetas de nuestra computadora.

Para eso utilizaremos la terminal.

La terminal es una aplicación que nos permite comunicarnos con la computadora escribiendo comandos en lugar de usar el mouse.

A partir de este momento empezaremos a trabajar como lo hacen la mayoría de los programadores.

¿Qué es la terminal?

La terminal es una aplicación que nos permite comunicarnos con la computadora escribiendo instrucciones en lugar de utilizar el mouse.

En vez de hacer clic sobre carpetas y archivos, escribimos comandos y la computadora los ejecuta.

Por ejemplo, cuando escribimos:

ls

la computadora entiende que queremos ver el contenido de la carpeta actual.

¿Por qué los programadores usan la terminal?

Podríamos pensar:

"Si ya existe el Explorador de archivos de Windows, ¿para qué aprender otra herramienta?"

La respuesta es que muchas herramientas de programación funcionan desde la terminal.

Desde allí podemos:

crear proyectos;

movernos entre carpetas;

compilar programas;

ejecutar programas;

utilizar Git;

instalar bibliotecas;

automatizar tareas.

Por eso la terminal forma parte del trabajo diario de un programador.

¿Qué es Linux?

Antes de continuar, es importante aclarar algo.

Muchos creen que ahora empezamos a aprender otro lenguaje de programación.

No es así.

Linux no es un lenguaje de programación.

Linux es un sistema operativo, igual que Windows o macOS.

Un sistema operativo es el software encargado de administrar los recursos de la computadora y permitir que los programas funcionen.

CS50 utiliza Linux porque es uno de los sistemas operativos más usados en programación, especialmente en servidores y desarrollo de software.

Por eso los comandos que aprenderemos pertenecen a Linux y no al lenguaje C.

La terminal y el sistema operativo

Cuando escribimos un comando como:

ls

no estamos hablando con nuestro programa en C.

Estamos hablando con Linux.

Es Linux quien interpreta ese comando y responde mostrando los archivos de la carpeta actual.

Por eso es importante diferenciar dos cosas:

C → sirve para crear programas.

Linux → sirve para administrar la computadora y ejecutar esos programas.

Son herramientas diferentes que trabajan juntas.

Una analogía

Imaginemos una oficina.

El sistema operativo es el edificio donde todo funciona.

La terminal es la recepción, donde damos instrucciones.

El lenguaje C es el idioma que usamos para escribir documentos (nuestros programas).

El compilador es el traductor que convierte esos documentos en instrucciones que la computadora puede entender.

Cada uno cumple una función distinta, pero todos trabajan en conjunto.

Qué aprenderemos ahora?

A partir de este momento comenzaremos a utilizar los primeros comandos de la terminal.

Cada comando resolverá un problema concreto.

No los aprenderemos para memorizarlos, sino para comprender qué necesidad resuelve cada uno.

Qué deberías haber entendido?

Al terminar de leer deberías poder responder:

¿Qué es una terminal?

¿Por qué los programadores la utilizan?

¿Qué diferencia hay entre Linux y C?

¿Quién ejecuta un comando como ls?

¿Qué relación existe entre la terminal y nuestros programas?

Primer comando: pwd

¿Qué problema resuelve?

Imaginá que entrás a una biblioteca enorme.

Hay miles de estanterías y miles de libros.

De repente alguien te pregunta:

¿En qué pasillo estás?

Si no sabés dónde estás parado, difícilmente puedas encontrar el libro que buscás.

Con la computadora pasa exactamente lo mismo.

Cuando abrimos la terminal, siempre estamos ubicados en alguna carpeta.

Antes de movernos o crear archivos, necesitamos saber cuál es nuestra ubicación actual.

Para resolver ese problema existe el comando pwd.

¿Qué significa pwd?

pwd proviene de:

Print Working Directory

Traducido literalmente significa:

Mostrar el directorio (carpeta) de trabajo actual.

No hace ninguna modificación.

Simplemente responde una pregunta:

¿Dónde estoy?

¿Qué es un directorio?

Antes de continuar necesitamos aprender una palabra nueva.

En informática:

Directorio = Carpeta

Son exactamente lo mismo.

Los programadores suelen decir directorio, mientras que en Windows estamos acostumbrados a decir carpeta.

Durante el curso encontrarás ambas palabras.

📁 mi_proyecto

│

├── 📄 programa.c

│

└── ⚙ programa

¿Cómo se usa?

Simplemente escribimos:

pwd

y presionamos Enter.

¿Qué devuelve?

Por ejemplo:

/workspaces/mi_proyecto

Eso significa que, en este momento, nuestra terminal está trabajando dentro de la carpeta mi_proyecto.

Todo lo que hagamos a continuación ocurrirá dentro de esa carpeta.

¿Por qué es importante?

Imaginemos que queremos crear un archivo.

Si no sabemos en qué carpeta estamos, ese archivo podría terminar guardado en un lugar que no esperábamos.

Por eso muchos programadores tienen el hábito de escribir primero:

pwd

para confirmar su ubicación.

Ejemplo

Supongamos que acabamos de abrir CS50.dev.

Escribimos:

pwd

La terminal responde:

/workspaces/mi_proyecto

Eso nos indica exactamente dónde estamos trabajando.

A partir de ahí ya podemos crear carpetas, movernos o abrir archivos.

Relación con la vida real

Cuando usás Google Maps, lo primero que aparece es un punto azul.

Ese punto responde una pregunta muy simple:

¿Dónde estoy?

pwd hace exactamente lo mismo.

Es el "punto azul" de la terminal.

Antes de indicarte hacia dónde ir, primero te muestra tu ubicación actual.

Resumen

pwd significa Print Working Directory.

Muestra la carpeta donde estamos trabajando.

No modifica ningún archivo.

Es útil para saber dónde nos encontramos antes de ejecutar otros comandos.

¿Qué deberías haber entendido?

Al terminar este tema deberías poder responder:

¿Qué significa pwd?

¿Qué diferencia hay entre directorio y carpeta?

¿Por qué es importante saber dónde estamos antes de crear archivos?

¿Qué información devuelve pwd?

Segundo comando: ls

¿Qué problema resuelve?

Ya sabemos en qué carpeta estamos gracias a pwd.

Ahora imaginemos que entramos a una habitación.

Sabemos que estamos en ella, pero todavía no sabemos qué contiene.

La pregunta natural es:

¿Qué hay aquí?

Para responder esa pregunta existe el comando ls.

¿Qué significa ls?

ls proviene de la palabra inglesa:

List

Su función es muy simple.

Muestra el contenido de la carpeta donde estamos trabajando.

Puede mostrar:

Carpetas.

Archivos.

Ambos.

No modifica nada.

Solo muestra información.

¿Cómo se usa?

Simplemente escribimos:

ls

y presionamos Enter.

¿Qué devuelve?

Por ejemplo:

programa.c

Eso significa que, dentro de la carpeta actual, existe:

un archivo llamado programa.c;

¿Qué significa cada elemento?

Cuando ejecutamos ls, la terminal nos muestra todo lo que existe dentro del directorio actual.

Por ejemplo:

mi_proyecto

Si entramos en esa carpeta y ejecutamos nuevamente ls, antes de escribir nuestro programa podríamos ver:

programa.c

Después de compilar, el resultado cambiará:

programa

programa.c

Podemos interpretarlo así:

⚙ programa    → el programa ejecutable.

📄 programa.c → el archivo fuente escrito en C.

En algunos sistemas, los archivos ejecutables y las carpetas pueden aparecer con colores diferentes para ayudar a distinguirlos.

Relación con la vida real

Imaginemos que abrís el cajón de un escritorio.

No estás cambiando nada.

Solo estás mirando qué hay dentro.

Eso hace exactamente ls.

Abre la "vista" de la carpeta actual y te muestra su contenido.

¿Cuándo lo usamos?

Cada vez que no recordamos qué archivos o carpetas existen.

Por ejemplo:

antes de entrar a una carpeta;

antes de abrir un archivo;

para comprobar si un archivo fue creado correctamente.

Es uno de los comandos que más usan los programadores.

Diferencia entre pwd y ls

Es muy fácil confundirlos al principio.

Comando	Responde la pregunta

pwd	¿Dónde estoy?

ls	¿Qué hay aquí?

Ya estamos listos para empezar a movernos entre las carpetas.

¿Qué está pensando la computadora?

Vos escribís:

ls

La computadora interpreta:

"El usuario quiere conocer el contenido del directorio actual. No debo modificar ningún archivo; solamente debo mostrar una lista con todo lo que hay dentro."

Resumen

ls significa List.

Muestra el contenido de la carpeta actual.

No modifica archivos.

Es uno de los comandos más utilizados en programación.

¿Qué deberías haber entendido?

Al terminar este tema deberías poder responder:

¿Qué significa ls?

¿Qué diferencia hay entre pwd y ls?

¿Qué tipo de elementos puede mostrar ls?

¿Por qué es útil ejecutar ls antes de trabajar con archivos?

Tercer comando: cd

¿Qué problema resuelve?

Hasta ahora aprendimos dos cosas:

Con pwd sabemos dónde estamos.

Con ls sabemos qué hay en esa carpeta.

Pero todavía hay un problema.

Imaginemos que vemos una carpeta llamada mi_proyecto.

Sabemos que existe.

Pero...

¿Cómo entramos en ella?

Con la computadora ocurre exactamente lo mismo.

Podemos ver las carpetas, pero todavía no sabemos cómo movernos entre ellas.

Para resolver ese problema existe el comando cd.

¿Qué significa cd?

cd proviene de las palabras inglesas:

Change Directory

Que significa:

Cambiar de directorio (carpeta).

Su función consiste en cambiar la carpeta donde estamos trabajando.

¿Cómo se usa?

La estructura general es:

cd nombre_de_la_carpeta

Por ejemplo:

cd mi_proyecto

La computadora interpreta:

"Entrá en la carpeta llamada mi_proyecto."

¿Qué ocurre cuando ejecutamos cd?

Imaginemos que estamos aquí:

📁 workspaces

│

└── 📁 mi_proyecto

Nuestra ubicación actual es:

/workspaces

Si escribimos:

cd mi_proyecto

Nuestra nueva ubicación será:

📁 workspaces

│

└── 📁 mi_proyecto   ← Ahora estamos aquí.

No copiamos la carpeta.

No la abrimos en otra ventana.

Simplemente cambiamos nuestro lugar de trabajo.

¿Cómo comprobar que realmente entramos?

Podemos usar nuevamente el comando que ya conocemos:

pwd

Antes de cambiar de carpeta obtenemos:

/workspaces

Después de ejecutar:

cd mi_proyecto

Si escribimos otra vez:

pwd

La terminal responderá:

/workspaces/mi_proyecto

Eso confirma que ahora estamos trabajando dentro de mi_proyecto.

Relación con la vida real

Imaginá un edificio con muchas habitaciones.

Desde el pasillo podés ver las puertas.

Eso sería como ejecutar:

ls

Pero para entrar en una habitación necesitás caminar hasta ella.

Eso es exactamente lo que hace:

cd mi_proyecto

No cambia el edificio.

No cambia las habitaciones.

Solo cambia tu ubicación.

Un ejemplo completo

Supongamos que acabamos de abrir la terminal.

Primero queremos saber dónde estamos.

pwd

La computadora responde:

/workspaces

Ahora queremos ver qué hay allí.

ls

La respuesta es:

mi_proyecto

Queremos trabajar dentro de ese proyecto.

Entonces escribimos:

cd mi_proyecto

Ahora estamos dentro de esa carpeta.

Si ejecutamos nuevamente:

pwd

obtendremos:

/workspaces/mi_proyecto

Y si ahora escribimos:

ls

la terminal podría responder:

programa.c

Eso significa que el archivo programa.c se encuentra dentro de la carpeta mi_proyecto.

¿Qué está pensando la computadora?

Vos escribís:

cd mi_proyecto

La computadora interpreta:

"El usuario quiere que el directorio de trabajo cambie a la carpeta llamada mi_proyecto. A partir de este momento, todos los comandos actuarán dentro de esa carpeta."

Un detalle muy importante

cd no abre archivos.

Tampoco ejecuta programas.

Solo cambia el lugar donde estamos trabajando.

Es parecido a cambiar de habitación dentro de una casa.

La habitación cambia.

Vos seguís siendo la misma persona.

Resumen

cd significa Change Directory.

Permite cambiar de una carpeta a otra.

No modifica archivos.

Cambia el directorio de trabajo actual.

¿Qué deberías haber entendido?

Al terminar este tema deberías poder responder:

¿Qué significa cd?

¿Qué problema resuelve?

¿Qué cambia cuando ejecutamos cd?

¿Cómo podemos comprobar que realmente cambiamos de carpeta?

¿Qué diferencia hay entre ls y cd?

Fijate que los comandos ahora forman una secuencia lógica:

```
pwd
        ↓
```

¿Dónde estoy?

```
ls
        ↓
```

¿Qué hay aquí?

cd mi_proyecto

        ↓

Entro en la carpeta.

```
pwd
        ↓
```

Confirmo que entré.

```
ls
        ↓
```

Ahora veo el contenido de esa carpeta.

Cuarto comando: mkdir

¿Qué problema resuelve?

Hasta ahora aprendimos a:

```c
saber dónde estamos (pwd);
ver qué hay en una carpeta (ls);
```

movernos entre carpetas (cd).

Pero imaginemos que queremos comenzar un proyecto completamente nuevo.

Miramos alrededor y la carpeta todavía no existe.

Entonces surge una nueva pregunta:

¿Cómo creo una carpeta nueva?

Para resolver ese problema existe el comando mkdir.

¿Qué significa mkdir?

mkdir proviene de las palabras inglesas:

Make Directory

Que significa:

Crear un directorio (carpeta).

Su función es crear una nueva carpeta en el directorio donde estamos trabajando.

¿Cómo se usa?

La estructura general es:

mkdir nombre_de_la_carpeta

Por ejemplo:

mkdir mi_proyecto

La computadora interpreta:

"Creá una carpeta llamada mi_proyecto."

¿Qué ocurre cuando ejecutamos mkdir?

Imaginemos que estamos en:

📁 workspaces

Todavía no existe ninguna carpeta para nuestro proyecto.

Si escribimos:

mkdir mi_proyecto

La estructura cambia a:

📁 workspaces

│

└── 📁 mi_proyecto

Acabamos de crear una carpeta nueva.

¿Cómo comprobar que realmente se creó?

Podemos utilizar el comando que ya conocemos:

ls

La terminal responderá:

mi_proyecto

Eso significa que la carpeta fue creada correctamente.

Si luego queremos entrar en ella, utilizamos:

cd mi_proyecto

Y podemos comprobar nuestra ubicación con:

pwd

Resultado:

/workspaces/mi_proyecto

Relación con la vida real

Imaginemos que compramos un archivador vacío.

Todavía no tiene carpetas.

Para organizar nuestros documentos, primero debemos crear una carpeta con una etiqueta.

Eso es exactamente lo que hace mkdir.

Crea un nuevo lugar donde podremos guardar nuestros archivos.

Un ejemplo completo

Supongamos que acabamos de abrir la terminal.

Primero verificamos dónde estamos:

pwd

Resultado:

/workspaces

Queremos comenzar un nuevo proyecto.

Escribimos:

mkdir mi_proyecto

Ahora comprobamos que la carpeta existe:

ls

La terminal responde:

mi_proyecto

Entramos en ella:

cd mi_proyecto

Y verificamos nuevamente nuestra ubicación:

pwd

Resultado:

/workspaces/mi_proyecto

¿Qué está pensando la computadora?

Vos escribís:

mkdir mi_proyecto

La computadora interpreta:

"El usuario quiere crear una carpeta nueva llamada mi_proyecto dentro del directorio actual."

Si no existe ninguna carpeta con ese nombre, la crea inmediatamente.

Un detalle muy importante

mkdir no crea archivos.

Solo crea carpetas.

Después podremos guardar dentro de esa carpeta archivos como:

programa.c

o, más adelante, el programa ejecutable:

programa

Resumen

mkdir significa Make Directory.

Permite crear una carpeta nueva.

No crea archivos.

La carpeta se crea en el directorio donde estamos trabajando.

¿Qué deberías haber entendido?

Al terminar este tema deberías poder responder:

¿Qué significa mkdir?

¿Qué problema resuelve?

¿Qué crea exactamente este comando?

¿Cómo podemos comprobar que la carpeta fue creada?

¿Qué diferencia hay entre mkdir y cd?

💡 Un detalle que me gusta de esta secuencia

Hasta ahora los comandos forman una historia muy natural:

```
pwd
↓
```

¿Dónde estoy?

```
ls
↓
```

¿Qué hay aquí?

mkdir mi_proyecto

↓

Creo una carpeta nueva.

cd mi_proyecto

↓

Entro en esa carpeta.

```
pwd
↓
```

Confirmo que estoy dentro.

```
ls
↓
```

Veo qué contiene.

Quinto comando: code

¿Qué problema resuelve?

Hasta ahora ya sabemos cómo:

```c
crear una carpeta (mkdir);
```

entrar en ella (cd).

Pero todavía nos falta algo muy importante.

Nuestra carpeta está vacía.

Todavía no escribimos ningún programa.

Entonces surge una nueva pregunta:

¿Cómo empezamos a escribir código?

Para resolver ese problema utilizaremos el comando code.

¿Qué significa code?

A diferencia de otros comandos como pwd o ls, code no es un comando propio de Linux.

Es un comando que permite abrir Visual Studio Code (VS Code) desde la terminal.

Gracias a él podemos abrir un archivo o una carpeta para comenzar a programar.

¿Cómo se usa?

Podemos utilizarlo de distintas maneras.

Para abrir un archivo:

code programa.c

Para abrir una carpeta completa:

code .

El punto (.) representa la carpeta actual.

Más adelante aprenderemos por qué.

¿Qué ocurre cuando ejecutamos code programa.c?

Supongamos que estamos dentro de nuestra carpeta de trabajo.

📁 mi_proyecto

Escribimos:

code programa.c

Si el archivo ya existe, VS Code lo abrirá para que podamos editarlo.

Si todavía no existe, VS Code creará un archivo nuevo con ese nombre y lo abrirá automáticamente.

Ahora ya podemos comenzar a escribir nuestro programa.

¿Qué ocurre cuando ejecutamos code .?

También podemos escribir:

code .

En lugar de abrir un solo archivo, VS Code abrirá toda la carpeta del proyecto.

Por ejemplo:

📁 mi_proyecto

│

├── 📄 programa.c

│

└── ⚙ programa

Desde allí podremos ver todos los archivos del proyecto en el panel lateral.

Esta es la forma que utilizaremos con mayor frecuencia durante el curso.

Relación con la vida real

Imaginemos que nuestra carpeta mi_proyecto es una carpeta física llena de documentos.

La terminal nos permite movernos hasta ella.

Pero para escribir un documento necesitamos abrirlo con un editor.

Eso hace exactamente code.

Abre nuestro espacio de trabajo para que podamos comenzar a escribir.

Un ejemplo completo

Supongamos que acabamos de crear nuestro proyecto.

Primero entramos en la carpeta:

cd mi_proyecto

Comprobamos que estamos allí:

pwd

Resultado:

/workspaces/mi_proyecto

Ahora abrimos todo el proyecto en VS Code:

code .

VS Code mostrará la carpeta mi_proyecto, desde donde podremos crear, editar y organizar nuestros archivos.

¿Qué está pensando la computadora?

Vos escribís:

code .

La computadora interpreta:

"El usuario quiere abrir la carpeta actual utilizando Visual Studio Code."

Si escribís:

code programa.c

La computadora interpreta:

"El usuario quiere abrir el archivo programa.c en Visual Studio Code."

Un detalle muy importante

El comando code no compila programas.

Tampoco los ejecuta.

Su única función es abrir archivos o carpetas en Visual Studio Code para que podamos trabajar con ellos.

Resumen

code abre Visual Studio Code desde la terminal.

Puede abrir un archivo específico.

También puede abrir una carpeta completa.

No ejecuta ni compila programas.

¿Qué deberías haber entendido?

Al terminar este tema deberías poder responder:

¿Para qué sirve el comando code?

¿Qué diferencia hay entre code programa.c y code .?

¿Qué representa el punto (.)?

¿Por qué usamos code antes de compilar un programa?

Importante

Aunque todos los comandos que vimos se escriben en la terminal, no todos pertenecen a la misma herramienta.

Los comandos:

pwd

ls

cd

mkdir

son comandos del sistema operativo Linux. Es Linux quien los interpreta y ejecuta.

En cambio:

code

no es un comando de Linux. Es un comando que instala Visual Studio Code para que podamos abrir archivos y carpetas directamente desde la terminal.

Más adelante veremos otros ejemplos, como make, que tampoco pertenecen a Linux, sino a otra herramienta diferente.

Idea clave: La terminal es el lugar desde donde damos instrucciones, pero esas instrucciones pueden ser interpretadas por programas distintos, no solamente por el sistema operativo.

Sexto comando: make

¿Qué problema resuelve?

Hasta ahora ya sabemos cómo:

```c
crear una carpeta (mkdir);
entrar en ella (cd);
```

abrir nuestro proyecto en VS Code (code).

Ahora podemos escribir un programa como este:

```c
#include <stdio.h>
int main(void)
{
    printf("¡Hermosa mañana, ¿verdad?\n");
}
```

Pero aparece un nuevo problema.

Aunque el programa ya está escrito, la computadora todavía no puede ejecutarlo.

¿Por qué?

Porque nuestro archivo programa.c contiene código fuente, un lenguaje pensado para que los seres humanos podamos leerlo y escribirlo.

La computadora, en cambio, solo entiende código máquina.

Entonces surge una nueva pregunta:

¿Cómo traducimos nuestro programa para que la computadora pueda ejecutarlo?

Para resolver ese problema utilizamos el comando make.

¿Qué significa make?

En CS50 utilizaremos una herramienta llamada make.

Su función es muy sencilla:

Compilar nuestro programa.

Es decir, tomar el archivo fuente escrito en C y generar un programa ejecutable.

¿Cómo se usa?

La estructura general es:

```c
make nombre_del_programa
```

Por ejemplo:

```c
make programa
```

Observá un detalle importante.

No escribimos:

```c
make programa.c
```

Sino simplemente:

```c
make programa
make entiende automáticamente que el archivo fuente se llama programa.c y generará un ejecutable llamado programa.
```

¿Qué ocurre cuando ejecutamos make?

Antes de compilar, nuestra carpeta contiene únicamente el archivo fuente.

📁 mi_proyecto

│

└── 📄 programa.c

Ejecutamos:

```c
make programa
```

Después de unos segundos, la carpeta cambia.

📁 mi_proyecto

│

├── 📄 programa.c

│

└── ⚙ programa

Apareció un archivo nuevo.

Ese archivo es el programa ejecutable.

¿Qué hizo realmente make?

No modificó nuestro código.

No borró el archivo fuente.

Simplemente creó un nuevo archivo.

Ahora tenemos dos archivos distintos.

Archivo	¿Qué contiene?

programa.c	El código fuente que escribimos.

programa	El programa compilado que la computadora puede ejecutar.

¿Qué está ocurriendo dentro de la computadora?

Cuando escribimos:

```c
make programa
```

ocurre algo parecido a esto:

programa.c

      │

      ▼

Compilador

      │

      ▼

Código máquina

      │

      ▼

programa

El compilador lee nuestro código línea por línea.

Comprueba que no existan errores de sintaxis.

Si todo está correcto, genera el programa ejecutable.

¿Qué pasa si hay un error?

Supongamos que olvidamos un punto y coma.

```c
printf("Hola")
```

Al ejecutar:

```c
make programa
```

El compilador mostrará un mensaje indicando el error.

No se creará el ejecutable hasta que el programa pueda compilar correctamente.

Por eso muchas veces veremos mensajes de error antes de poder ejecutar nuestro programa.

Relación con la vida real

Imaginemos que escribimos un libro en español.

Una persona que solo habla japonés no podrá leerlo.

Necesitamos un traductor.

Con los programas ocurre exactamente lo mismo.

Nosotros escribimos en C.

El compilador traduce ese programa al lenguaje que entiende la computadora.

```c
make es la herramienta que pone en marcha ese proceso de traducción.
```

Un ejemplo completo

Estamos dentro de nuestra carpeta.

📁 mi_proyecto

│

└── 📄 programa.c

Compilamos.

```c
make programa
```

Ahora la carpeta contiene:

📁 mi_proyecto

│

├── 📄 programa.c

│

└── ⚙ programa

Todavía no ejecutamos nada.

Simplemente acabamos de crear el programa que la computadora podrá ejecutar en el siguiente paso.

Un detalle muy importante

```c
make no ejecuta el programa.
```

Solo lo compila.

El programa recién comenzará a funcionar cuando utilicemos el siguiente comando:

```c
./programa
```

Ese será el próximo tema.

Resumen

```c
make compila un programa escrito en C.
```

Convierte el código fuente en un programa ejecutable.

No modifica el archivo .c.

Si encuentra errores, informa cuáles son y detiene la compilación.

¿Qué deberías haber entendido?

Al terminar este tema deberías poder responder:

¿Qué problema resuelve make?

¿Por qué necesitamos compilar un programa?

¿Qué diferencia hay entre programa.c y programa?

¿Qué hace el compilador durante la compilación?

¿Qué ocurre si existe un error de sintaxis?

Programador

      │

      ▼

Código fuente (programa.c)

      │

      ▼

Compilador

      │

      ▼

Código máquina

      │

      ▼

Programa ejecutable (programa)

Séptimo comando: ./

¿Qué problema resuelve?

Ya escribimos nuestro programa.

Lo compilamos con make.

Ahora nuestra carpeta contiene dos archivos:

📁 mi_proyecto

│

├── 📄 programa.c

│

└── ⚙ programa

Pero todavía falta el paso más esperado.

¡Queremos ver el programa funcionando!

Entonces aparece una nueva pregunta:

¿Cómo le decimos a la computadora que ejecute el programa que acabamos de compilar?

Para resolver ese problema utilizamos:

```c
./programa
```

¿Qué significa ./?

Esta es una de las primeras cosas que suele resultar extraña cuando empezamos a programar.

Podría parecer que ./ forma parte del nombre del programa.

Pero no es así.

En realidad:

./

significa:

"Buscá el programa en la carpeta actual."

Y después escribimos el nombre del ejecutable.

Por eso:

```c
./programa
```

significa:

"Ejecutá el archivo programa que está en esta carpeta."

¿Cómo se usa?

La estructura general es:

```c
./nombre_del_programa
```

Por ejemplo:

```c
./programa
```

¿Qué ocurre cuando lo ejecutamos?

Supongamos que nuestro programa contiene:

```c
#include <stdio.h>
int main(void)
{
    printf("¡Hermosa mañana, ¿verdad?\n");
}
```

Escribimos:

```c
./programa
```

La terminal mostrará:

¡Hermosa mañana, ¿verdad?

Nuestro programa acaba de ejecutarse correctamente.

¿Por qué no escribimos solamente programa?

Esta es una muy buena pregunta.

Cuando escribimos un comando, Linux busca ese programa en determinados lugares del sistema.

Por seguridad, no busca automáticamente en la carpeta donde estamos trabajando.

Por eso debemos indicarle explícitamente:

.

El punto (.) representa la carpeta actual.

Y la barra (/) significa:

"Entrá en esa carpeta."

Entonces:

```c
./programa
```

se interpreta como:

"Ejecutá el archivo programa que está dentro de la carpeta donde estoy ahora."

¿Qué está ocurriendo dentro de la computadora?

Cuando escribimos:

```c
./programa
```

la computadora:

busca el archivo ejecutable llamado programa;

lo carga en memoria;

comienza a ejecutar las instrucciones desde la función main().

A partir de ese momento, el programa empieza a funcionar.

Relación con la vida real

Imaginemos que tenemos un reproductor de música.

Primero escribimos una canción.

Después la grabamos en un CD.

Pero el trabajo todavía no termina.

Todavía falta presionar el botón Play.

Eso hace exactamente:

```c
./programa
```

Hace que el programa empiece a ejecutarse.

Un ejemplo completo

Dentro de nuestra carpeta tenemos:

📁 mi_proyecto

│

├── 📄 programa.c

│

└── ⚙ programa

Ejecutamos:

```c
./programa
```

Resultado:

¡Hermosa mañana, ¿verdad?

Nuestro programa se ejecutó correctamente.

¿Qué está pensando la computadora?

Vos escribís:

```c
./programa
```

La computadora interpreta:

"El usuario quiere ejecutar el archivo programa que se encuentra en el directorio actual."

Un detalle muy importante

Para poder ejecutar:

```c
./programa
```

el archivo ejecutable debe existir.

Si todavía no compilamos el programa con:

```c
make programa
```

la computadora no encontrará ese archivo y mostrará un mensaje de error.

Por eso, normalmente seguimos este orden:

```c
make programa
./programa
```

Primero compilamos.

Después ejecutamos.

Resumen

./ indica que el programa se encuentra en la carpeta actual.

./programa ejecuta el archivo compilado.

Antes de ejecutarlo, debemos haber utilizado make.

La ejecución comienza en la función main().

¿Qué deberías haber entendido?

Al terminar este tema deberías poder responder:

¿Qué significa ./?

¿Por qué escribimos ./programa y no solamente programa?

¿Qué representa el punto (.)?

¿Qué ocurre cuando ejecutamos un programa?

¿Por qué es necesario compilar antes de ejecutar?

Nuestro primer ciclo de trabajo

Hasta hace unas páginas todos estos comandos parecían independientes.

Ahora podemos ver que forman parte de un mismo proceso.

Cuando desarrollamos un programa en C, normalmente seguimos estos pasos:

📁 workspaces

      │

      ▼

mkdir mi_proyecto

      │

      ▼

cd mi_proyecto

      │

      ▼

code .

      │

      ▼

Escribimos programa.c

      │

      ▼

```c
make programa
```

      │

      ▼

Se crea el ejecutable programa

      │

      ▼

```c
./programa
```

      │

      ▼

El programa se ejecuta

Fijate que cada comando resuelve un problema distinto:

Comando	¿Para qué lo usamos?

mkdir	Crear un proyecto nuevo.

cd	Entrar en el proyecto.

code	Escribir o editar el código.

```c
make	Compilar el programa.
```

./programa	Ejecutarlo.

A partir de este momento ya conocemos el flujo básico de trabajo que utilizaremos.

Con el tiempo iremos incorporando nuevas herramientas, pero este será el punto de partida de prácticamente todos nuestros programas.

¿Qué deberías haber entendido?

Al terminar esta sección deberías poder responder:

¿Cuál es el flujo básico para desarrollar un programa en C?

¿Qué función cumple cada comando?

¿En qué momento aparece el archivo ejecutable?

¿Por qué primero compilamos y después ejecutamos?

¿Qué diferencia existe entre el archivo programa.c y el ejecutable programa?

Octavo comando: cp

¿Qué problema resuelve?

Hasta ahora aprendimos a crear proyectos y escribir programas.

Pero imaginemos que queremos hacer una copia de un archivo antes de modificarlo.

O queremos duplicar un proyecto para probar una idea nueva sin arriesgar el original.

Entonces aparece una nueva pregunta:

¿Cómo copiamos un archivo o una carpeta?

Para resolver ese problema existe el comando cp.

¿Qué significa cp?

cp proviene de la palabra inglesa:

Copy

Que significa:

Copiar.

Su función consiste en crear una copia de un archivo o de una carpeta.

¿Cómo se usa?

Para copiar un archivo:

cp programa.c copia_programa.c

La computadora interpreta:

"Creá una copia del archivo programa.c y llamala copia_programa.c."

¿Qué ocurre cuando lo ejecutamos?

Antes:

📁 mi_proyecto

│

└── 📄 programa.c

Después de ejecutar:

cp programa.c copia_programa.c

La carpeta queda así:

📁 mi_proyecto

│

├── 📄 programa.c

│

└── 📄 copia_programa.c

Ahora existen dos archivos independientes.

Modificar uno no cambia el otro.

Resumen

cp significa Copy.

Crea una copia de un archivo o carpeta.

No modifica el archivo original.

¿Qué deberías haber entendido?

¿Qué significa cp?

¿Qué problema resuelve?

¿Qué diferencia hay entre copiar un archivo y moverlo?

Noveno comando: mv

¿Qué problema resuelve?

A veces un archivo ya existe, pero queremos:

cambiarle el nombre;

moverlo a otra carpeta.

¿Cómo lo hacemos?

Para resolver ese problema utilizamos mv.

¿Qué significa mv?

mv proviene de la palabra inglesa:

Move

Que significa:

Mover.

También permite cambiar el nombre de un archivo.

¿Cómo se usa?

Para cambiar el nombre de un archivo:

mv programa.c saludo.c

La computadora interpreta:

"El archivo ya no se llamará programa.c. Ahora se llamará saludo.c."

¿Qué ocurre cuando lo ejecutamos?

Antes:

📁 mi_proyecto

│

└── 📄 programa.c

Después:

📁 mi_proyecto

│

└── 📄 saludo.c

No se creó una copia.

Simplemente cambió el nombre del archivo.

Resumen

mv significa Move.

Permite mover archivos y carpetas.

También permite cambiarles el nombre.

No crea copias.

¿Qué deberías haber entendido?

¿Qué significa mv?

¿Qué diferencia hay entre copiar y mover?

¿Cómo podemos cambiar el nombre de un archivo?

Décimo comando: rm

¿Qué problema resuelve?

Con el tiempo iremos creando muchos archivos.

Algunos dejarán de ser útiles.

Entonces aparece una nueva pregunta:

¿Cómo eliminamos un archivo que ya no necesitamos?

Para resolver ese problema utilizamos rm.

¿Qué significa rm?

rm proviene de la palabra inglesa:

Remove

Que significa:

Eliminar.

Su función consiste en borrar archivos.

¿Cómo se usa?

Por ejemplo:

rm copia_programa.c

La computadora interpreta:

"Eliminá el archivo copia_programa.c."

¿Qué ocurre cuando lo ejecutamos?

Antes:

📁 mi_proyecto

│

├── 📄 programa.c

│

└── 📄 copia_programa.c

Después:

📁 mi_proyecto

│

└── 📄 programa.c

El archivo fue eliminado.

⚠️ Un detalle muy importante

A diferencia de cuando eliminamos un archivo desde el Explorador de Windows o el Finder de macOS, al utilizar rm normalmente el archivo no pasa por la Papelera de reciclaje.

Por eso debemos usar este comando con cuidado.

Resumen

rm significa Remove.

Elimina archivos.

No crea copias.

Debe utilizarse con cuidado porque normalmente la eliminación es definitiva.

¿Qué deberías haber entendido?

¿Qué significa rm?

¿Qué problema resuelve?

¿Qué ocurre con un archivo después de ejecutar rm?

¿Por qué debemos utilizar este comando con precaución?

Hemos completado nuestro primer conjunto de herramientas

Ahora conocemos los comandos fundamentales 

Comando	¿Para qué sirve?

pwd	Saber dónde estamos.

ls	Ver el contenido de una carpeta.

cd	Cambiar de carpeta.

mkdir	Crear una carpeta nueva.

code	Abrir un proyecto en VS Code.

```c
make	Compilar un programa.
```

./programa	Ejecutar un programa compilado.

cp	Copiar archivos o carpetas.

mv	Mover o cambiar el nombre de archivos y carpetas.

rm	Eliminar archivos.

Con estas herramientas ya podemos crear proyectos, organizarlos, escribir código, compilarlo y ejecutarlo.

## NUESTRO PRIMER PROGRAMA INTERACTIVO

¿Qué problema resuelve?

Hasta este momento, todos los programas que escribimos hacían exactamente lo mismo.

Por ejemplo:

```c
#include <stdio.h>
int main(void)
{
    printf("¡Hermosa mañana, ¿verdad?\n");
}
```

Cada vez que ejecutábamos el programa obteníamos el mismo resultado.

¡Hermosa mañana, ¿verdad?

No importaba quién lo utilizara ni cuántas veces lo ejecutáramos: la salida siempre era idéntica.

Pero pensemos en algunos programas que usamos todos los días.

Una calculadora espera que escribamos números.

Un navegador espera que escribamos una dirección web.

Un buscador espera que escribamos una consulta.

Un videojuego espera que presionemos teclas.

Todos tienen algo en común.

Esperan que el usuario les proporcione información.

Entonces surge una nueva pregunta:

¿Cómo puede un programa recibir información del usuario?

Entrada, procesamiento y salida

En la Semana 0 aprendimos que todo programa sigue el mismo esquema.

Entrada (Input)

        │

        ▼

 Procesamiento

        │

        ▼

Salida (Output)

Hasta ahora solo conocíamos la última parte.

Utilizábamos printf() para mostrar información en la pantalla.

Ahora aprenderemos cómo recibir información desde el teclado para que el programa pueda trabajar con ella.

La biblioteca CS50

Hasta ahora utilizamos una única biblioteca:

```c
#include <stdio.h>
```

Esta biblioteca nos permitió usar funciones como printf().

En este capítulo necesitaremos una función nueva llamada get_string(), pero esa función no pertenece a la biblioteca estándar de C.

Forma parte de una biblioteca creada especialmente para el curso CS50.

Para poder utilizarla debemos agregar una nueva línea al comienzo del programa.

```c
#include <cs50.h>
```

A partir de ese momento tendremos disponibles varias funciones que nos ayudarán a leer datos ingresados por el usuario.

Nuestra primera entrada de datos

La función que utilizaremos es:

```c
get_string()
```

Su trabajo consiste en mostrar un mensaje y esperar a que el usuario escriba una respuesta utilizando el teclado.

Cuando el usuario presiona Enter, el programa recibe esa información y puede continuar ejecutándose.

Nuestro primer programa interactivo

```c
#include <cs50.h>
#include <stdio.h>
int main(void)
{
    string nombre = get_string("¿Cómo te llamás? ");
    printf("Hola, %s\n", nombre);
}
```

¿Qué ocurre cuando ejecutamos este programa?

La computadora comienza ejecutando el programa.

Primero muestra la pregunta:

¿Cómo te llamás?

Ahora el programa se detiene momentáneamente.

No porque haya ocurrido un error, sino porque está esperando que el usuario escriba una respuesta.

Supongamos que el usuario escribe:

Mailen

y luego presiona Enter.

En ese momento el programa continúa su ejecución y muestra:

Hola, Mailen

Si otra persona ejecuta el mismo programa y escribe:

Juan

la salida será:

Hola, Juan

Por primera vez, el comportamiento del programa depende de la información que recibe del usuario.

Un detalle que todavía no vamos a explicar

Probablemente hayas notado esta línea:

```c
string nombre = get_string("¿Cómo te llamás? ");
```

Hay una palabra que todavía no conocemos:

string

No te preocupes si aún no entiendes qué significa.

Por ahora solo necesitamos saber que nos permite guardar el texto que escribe el usuario.

En el próximo capítulo descubriremos qué son los tipos de datos y por qué el programa necesita saber qué clase de información está almacenando.

Resumen

En este capítulo aprendimos que un programa no siempre produce la misma salida.

Gracias a la función get_string(), podemos pedir información al usuario y utilizarla durante la ejecución del programa.

También conocimos la biblioteca cs50.h, que incorpora funciones diseñadas para facilitar el aprendizaje del lenguaje C.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué significa que un programa sea interactivo?

¿Cuál es la diferencia entre entrada (input) y salida (output)?

¿Para qué sirve la función get_string()?

¿Por qué necesitamos incluir la biblioteca cs50.h?

¿Por qué el mismo programa puede producir resultados diferentes según lo que escriba el usuario?

Tipos de datos

¿Qué problema resuelve?

En el capítulo anterior escribimos nuestro primer programa interactivo.

```c
#include <cs50.h>
#include <stdio.h>
int main(void)
{
    string nombre = get_string("¿Cómo te llamás? ");
    printf("Hola, %s\n", nombre);
}
```

Probablemente haya una palabra que llamó tu atención.

string

Hasta ahora no explicamos qué significa ni por qué debemos escribirla.

Para entenderlo, pensemos en algunas preguntas que un programa podría hacer.

¿Cómo te llamás?

¿Cuántos años tenés?

¿Cuál es tu altura?

¿Aceptás los términos y condiciones?

Aunque todas son respuestas del usuario, no todas representan el mismo tipo de información.

Un nombre es un texto.

La edad es un número entero.

La altura puede tener decimales.

La respuesta a una pregunta como "¿Aceptás los términos?" solo puede ser sí o no.

Entonces surge una nueva pregunta.

¿Cómo sabe la computadora qué clase de información está recibiendo?

La computadora necesita contexto

Cuando una persona lee el número:

25

Normalmente entiende, gracias al contexto, qué representa.

Podría ser:

25 años.

25 kilómetros.

25 alumnos.

25 °C.

El número de una camiseta.

Las personas utilizamos el contexto constantemente.

La computadora no.

Para ella, toda la información son bits almacenados en memoria.

Si no le indicamos qué representan esos bits, no puede interpretarlos correctamente.

Por eso, cada vez que guardamos información, debemos decirle de qué tipo es.

Ese "apellido" que acompaña a un dato recibe el nombre de tipo de dato (data type).

¿Qué es un tipo de dato?

Un tipo de dato indica qué clase de información va a almacenar una variable.

Además, le dice a la computadora:

cuánto espacio debe reservar en memoria;

cómo interpretar esos bits;

qué operaciones puede realizar con ellos.

En otras palabras, el tipo de dato funciona como una etiqueta que describe el contenido.

Un ejemplo

Imaginemos que tenemos cuatro cajas.

📦 Textos

📦 Números enteros

📦 Números decimales

📦 Verdadero o falso

Si queremos guardar el nombre:

Mailen

No tendría sentido colocarlo en la caja de números.

Y si queremos guardar:

36

No tendría sentido almacenarlo como texto si vamos a realizar operaciones matemáticas con él.

Cada dato debe guardarse en la caja correcta.

Con la computadora ocurre exactamente lo mismo.

Los principales tipos de datos en C

A lo largo del libro iremos utilizando varios tipos de datos.

Los más importantes son:

Tipo	¿Qué almacena?	Ejemplo

int	Números enteros	25

float	Números con decimales	1.75

double	Decimales con mayor precisión	3.1415926535

char	Un único carácter	'A'

string	Texto	"Mailen"

bool	Verdadero o falso	true o false

void	Ausencia de valor	void

No te preocupes si todavía no conoces todos estos tipos.

En los próximos capítulos iremos estudiándolos uno por uno.

Volvamos al programa anterior

Ahora podemos entender mejor esta línea:

```c
string nombre = get_string("¿Cómo te llamás? ");
```

La palabra:

string

Le está diciendo a la computadora:

"Voy a guardar un texto."

Y como get_string() devuelve precisamente un texto, ambos son compatibles.

Resumen

En este capítulo aprendimos que la computadora necesita saber qué clase de información está manipulando.

Los tipos de datos permiten indicar si un valor representa un texto, un número entero, un número decimal, un carácter o cualquier otra clase de información.

Gracias a ellos, la computadora sabe cómo almacenar los datos en memoria y qué operaciones puede realizar con ellos.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué es un tipo de dato?

¿Por qué la computadora necesita conocer el tipo de un dato?

¿Qué información describe un tipo de dato?

¿Qué diferencia existe entre un número entero y un texto?

¿Qué tipos de datos veremos a lo largo del libro?

El tipo de dato int

¿Qué problema resuelve?

En el capítulo anterior aprendimos que la computadora necesita saber qué tipo de información va a almacenar.

Pero imaginemos que queremos guardar la edad de una persona.

36

O la cantidad de alumnos de un curso.

25

O los goles de un partido.

3

Todos estos valores tienen algo en común.

Son números enteros.

No tienen decimales.

Entonces surge una nueva pregunta.

¿Cómo le indicamos a la computadora que vamos a trabajar con números enteros?

¿Qué significa int?

La palabra int proviene del inglés integer, que significa número entero.

Este tipo de dato se utiliza para almacenar números sin parte decimal.

Por ejemplo:

-10

0

7

25

1500

Todos ellos pueden representarse mediante un int.

¿Cuándo utilizamos un int?

Siempre que necesitemos trabajar con cantidades enteras.

Algunos ejemplos son:

La edad de una persona.

La cantidad de libros de una biblioteca.

El número de jugadores de un equipo.

La cantidad de vidas en un videojuego.

El puntaje de un examen.

En todos estos casos no necesitamos decimales.

Nuestro primer ejemplo

Supongamos que queremos preguntarle la edad al usuario.

Podemos hacerlo así:

```c
#include <cs50.h>
#include <stdio.h>
int main(void)
{
    int edad = get_int("¿Cuántos años tenés? ");
    printf("Tenés %i años.\n", edad);
}
```

En este programa aparecen dos elementos nuevos.

int edad

Le indica a la computadora que edad almacenará un número entero.

Y la función:

```c
get_int()
```

Lee un número entero ingresado por el usuario.

Si el usuario escribe:

36

La salida será:

Tenés 36 años.

¿Por qué no usamos string?

Podríamos guardar la edad como texto, pero entonces la computadora no la trataría como un número.

Por ejemplo, no podría sumarle un año fácilmente ni realizar cálculos matemáticos de forma correcta.

Cuando un dato representa una cantidad numérica, lo más conveniente es almacenarlo como un número y no como un texto.

Resumen

El tipo de dato int se utiliza para almacenar números enteros.

Es ideal para representar cantidades que no necesitan decimales, como edades, puntajes o cantidades de objetos.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué significa int?

¿Qué tipo de información almacena?

¿Cuándo conviene utilizar un int?

¿Qué diferencia existe entre un int y un string?

¿Para qué sirve la función get_int()?

El tipo de dato float

¿Qué problema resuelve?

En el capítulo anterior aprendimos que el tipo de dato int permite almacenar números enteros.

Por ejemplo:

18

36

150

0

Pero no todos los números son enteros.

Pensemos en algunos ejemplos.

1.75

36.5

9.81

3.14

Todos ellos tienen una parte decimal.

Entonces surge una nueva pregunta.

¿Cómo le indicamos a la computadora que queremos trabajar con números decimales?

¿Qué significa float?

La palabra float proviene del inglés floating-point number, que significa número de punto flotante.

Aunque el nombre pueda parecer extraño, simplemente hace referencia a un número que puede tener una parte decimal.

Por ejemplo:

1.75

3.14

9.81

0.5

-12.8

Todos estos valores pueden almacenarse en un float.

¿Cuándo utilizamos un float?

Siempre que necesitemos representar valores que puedan contener decimales.

Algunos ejemplos son:

La altura de una persona.

La temperatura de una ciudad.

El peso de un objeto.

La velocidad de un automóvil.

El promedio de un examen.

En todos estos casos un número entero no sería suficiente.

Nuestro primer ejemplo

Supongamos que queremos preguntarle al usuario su altura.

```c
#include <cs50.h>
#include <stdio.h>
int main(void)
{
    float altura = get_float("¿Cuál es tu altura en metros? ");
    printf("Tu altura es %.2f metros.\n", altura);
}
```

Aquí aparecen dos elementos nuevos.

float altura

Le indica a la computadora que altura almacenará un número decimal.

Y la función:

```c
get_float()
```

permite leer un número decimal ingresado por el usuario.

Si el usuario escribe:

1.72

La salida será:

Tu altura es 1.72 metros.

¿Qué significa %.2f?

En el capítulo anterior utilizamos %i para mostrar números enteros.

Cuando trabajamos con números decimales utilizamos %f.

En este ejemplo escribimos:

%.2f

El .2 indica que queremos mostrar dos cifras después del punto decimal.

Por ejemplo:

Si el valor almacenado es:

1.723684

La salida será:

1.72

Si escribiéramos simplemente:

%f

podría mostrarse algo como:

1.723684

¿Por qué no usamos un int?

Si intentáramos guardar:

1.75

en un int, perderíamos la parte decimal.

Por eso, cuando un dato puede contener decimales, debemos utilizar un tipo de dato como float.

Resumen

El tipo de dato float permite almacenar números con parte decimal.

Es útil para representar medidas, temperaturas, promedios y cualquier otra cantidad que no siempre sea un número entero.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué significa float?

¿Qué tipo de información almacena?

¿Cuándo conviene utilizar un float?

¿Para qué sirve get_float()?

¿Qué significa %.2f en printf()?

El tipo de dato double

¿Qué problema resuelve?

En el capítulo anterior aprendimos que el tipo de dato float permite almacenar números con decimales.

Por ejemplo:

3.14

1.75

9.81

Entonces podría surgir una pregunta.

Si float ya almacena números decimales, ¿para qué existe también double?

La respuesta está en una palabra muy importante:

Precisión.

¿Qué significa double?

La palabra double proviene del inglés y significa doble.

Su nombre hace referencia a que este tipo de dato utiliza más espacio en memoria que un float, lo que le permite representar números decimales con una mayor precisión.

En otras palabras, puede almacenar más cifras significativas y reducir los errores de aproximación.

¿Por qué importa la precisión?

Imaginemos que queremos guardar el número π (pi).

Sabemos que su valor comienza así:

3.141592653589793...

Como tiene infinitas cifras decimales, ningún tipo de dato puede almacenarlo de forma exacta.

Lo único que puede hacer la computadora es guardar una aproximación.

Con un float esa aproximación será menos precisa.

Con un double será más precisa.

¿Cuándo utilizamos un double?

Elegiremos un double cuando necesitemos realizar cálculos donde la precisión sea importante.

Algunos ejemplos son:

Cálculos científicos.

Simulaciones físicas.

Coordenadas geográficas.

Aplicaciones de ingeniería.

Programas financieros.

En muchos programas sencillos un float es suficiente, pero en aplicaciones donde pequeños errores pueden acumularse, un double suele ser la mejor opción.

Nuestro primer ejemplo

```c
#include <stdio.h>
int main(void)
{
    double pi = 3.141592653589793;
    printf("%.15lf\n", pi);
}
```

La salida será similar a:

3.141592653589793

Aquí aparece un nuevo código de formato:

%lf

Se utiliza para mostrar valores de tipo double.

Más adelante dedicaremos un capítulo completo a los códigos de formato y veremos por qué existen distintos especificadores para cada tipo de dato.

¿Debo usar siempre double?

No necesariamente.

Aunque double ofrece mayor precisión, también ocupa más memoria que un float.

La elección depende del problema que queramos resolver.

Si estamos representando la altura de una persona o la temperatura ambiente, normalmente un float será suficiente.

Si estamos realizando cálculos científicos o financieros, un double suele ser una mejor elección.

Resumen

El tipo de dato double permite almacenar números decimales con mayor precisión que un float.

Utiliza más memoria, pero reduce los errores de aproximación cuando se trabaja con valores decimales.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué significa double?

¿Qué diferencia existe entre float y double?

¿Qué entendemos por precisión?

¿Cuándo conviene utilizar un double?

¿Por qué ningún tipo de dato puede almacenar exactamente el número π?

El tipo de dato char

¿Qué problema resuelve?

Hasta ahora aprendimos que existen distintos tipos de datos.

int para números enteros.

float y double para números con decimales.

Pero imaginemos que queremos almacenar una única letra.

Por ejemplo:

A

O un símbolo.

@

O un número como carácter.

7

Entonces surge una nueva pregunta.

¿Cómo le indicamos a la computadora que queremos almacenar un único carácter y no una palabra completa?

¿Qué significa char?

La palabra char proviene del inglés character, que significa carácter.

Este tipo de dato permite almacenar un único carácter.

Ese carácter puede ser:

una letra;

un número;

un signo de puntuación;

un símbolo especial.

Por ejemplo:

'A'

'b'

'7'

'?'

'@'

Todos ellos pueden almacenarse en un char.

¿Cuándo utilizamos un char?

Siempre que necesitemos trabajar con un solo carácter.

Algunos ejemplos son:

La inicial de un nombre.

La opción elegida en un menú (A, B o C).

Una calificación (A, B, C, D o F).

Un símbolo.

Nuestro primer ejemplo

```c
#include <stdio.h>
int main(void)
{
    char inicial = 'M';
    printf("La inicial es %c\n", inicial);
}
```

La salida será:

La inicial es M

Aquí aparece un nuevo código de formato:

%c

Se utiliza para mostrar un valor de tipo char.

Las comillas simples son importantes

Observemos esta línea:

```c
char inicial = 'M';
```

El carácter aparece entre comillas simples.

'M'

Eso le indica a la computadora que estamos almacenando un único carácter.

Más adelante veremos que los textos utilizan comillas dobles.

"Mailen"

Aunque ambos contienen letras, no representan el mismo tipo de información.

char no es lo mismo que string

Comparemos ambos tipos.

```c
char letra = 'M';
```

almacena un único carácter.

En cambio,

```c
string nombre = "Mailen";
```

almacena una secuencia de caracteres que forman un texto.

Podemos pensar que un string está formado por muchos char colocados uno detrás de otro.

Resumen

El tipo de dato char permite almacenar un único carácter.

Se utiliza cuando solo necesitamos guardar una letra, un número como carácter o un símbolo.

Para escribir un char utilizamos comillas simples, mientras que los textos utilizan comillas dobles.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué significa char?

¿Qué tipo de información almacena?

¿Qué diferencia existe entre un char y un string?

¿Por qué un char utiliza comillas simples?

¿Para qué sirve %c en printf()?

El tipo de dato string

¿Qué problema resuelve?

En el capítulo anterior aprendimos que el tipo de dato char permite almacenar un único carácter.

Por ejemplo:

```c
char inicial = 'M';
```

Pero imaginemos que queremos guardar un nombre completo.

Mailen

O una ciudad.

Buenos Aires

O una frase.

De Cero a IA

En todos estos casos un solo carácter no alcanza.

Entonces surge una nueva pregunta.

¿Cómo almacenamos un texto completo en la computadora?

¿Qué significa string?

La palabra string proviene del inglés y significa cadena o cadena de caracteres.

En programación, un string es una secuencia de caracteres colocados uno detrás del otro para formar un texto.

Por ejemplo:

"Hola"

"Mailen"

"Programación"

"De Cero a IA"

Todos ellos son ejemplos de string.

¿Cómo está formado un string?

Aunque cuando vemos una palabra parece una única unidad, para la computadora está formada por muchos caracteres individuales.

Por ejemplo:

"Hola"

H   o   l   a

Cada una de esas letras es un char.

El string simplemente las agrupa para formar un texto.

Podemos imaginarlo así:

char   char   char   char

 H       o      l      a

  └──────┴──────┴──────┘

          string

Por eso solemos decir que un string es una secuencia de caracteres.

¿Cuándo utilizamos un string?

Siempre que necesitemos almacenar texto.

Algunos ejemplos son:

El nombre de una persona.

Un apellido.

Una dirección de correo electrónico.

El nombre de una ciudad.

Una contraseña.

Un mensaje.

Nuestro primer ejemplo

```c
#include <cs50.h>
#include <stdio.h>
int main(void)
{
    string nombre = get_string("¿Cómo te llamás? ");
    printf("Hola, %s\n", nombre);
}
```

Si el usuario escribe:

Mailen

La salida será:

Hola, Mailen

Las comillas dobles

Cuando escribimos un string, utilizamos comillas dobles.

Por ejemplo:

"Hola"

o

"De Cero a IA"

Las comillas dobles indican que estamos trabajando con un texto.

Esto es diferente de un char, que utiliza comillas simples.

'A'

Compará ambos casos:

```c
char letra = 'A';
string palabra = "A";
```

Aunque ambos contienen la letra A, no representan lo mismo.

El primero almacena un único carácter.

El segundo almacena un texto, aunque ese texto tenga una sola letra.

Una aclaración importante

En este libro utilizamos el tipo de dato string porque forma parte de la biblioteca CS50.

En el lenguaje C estándar no existe un tipo llamado string.

Más adelante aprenderemos cómo representan realmente los textos los programas escritos en C.

Por ahora, string nos permitirá concentrarnos en aprender a programar sin preocuparnos por esos detalles.

Resumen

El tipo de dato string se utiliza para almacenar texto.

Un string está formado por una secuencia de caracteres (char) y se escribe entre comillas dobles.

Gracias a este tipo de dato podemos trabajar fácilmente con nombres, frases y cualquier otra información textual.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué significa string?

¿Qué tipo de información almacena?

¿Cuál es la diferencia entre un char y un string?

¿Por qué un string utiliza comillas dobles?

¿Por qué podemos usar string en CS50 aunque no exista en el lenguaje C estándar?

El tipo de dato bool

¿Qué problema resuelve?

Hasta ahora vimos distintos tipos de datos.

Podemos almacenar:

números enteros;

números decimales;

caracteres;

textos.

Pero imaginemos que queremos responder una pregunta como estas.

¿Está lloviendo?

¿El usuario aceptó los términos?

¿La contraseña es correcta?

¿El programa terminó?

En todos estos casos solo existen dos respuestas posibles.

Sí

No

Entonces surge una nueva pregunta.

¿Cómo almacena la computadora una respuesta que solo puede ser verdadera o falsa?

¿Qué significa bool?

La palabra bool proviene de Boolean, en honor al matemático inglés George Boole, quien desarrolló un sistema lógico basado en dos únicos valores.

El tipo de dato bool permite almacenar únicamente uno de estos valores:

true

false

Que significan:

Verdadero

Falso

No existen otros valores posibles para un bool.

¿Cuándo utilizamos un bool?

Siempre que una situación solo pueda tener dos estados.

Por ejemplo:

¿El usuario inició sesión?

¿La compra fue aprobada?

¿El archivo existe?

¿La luz está encendida?

¿El juego terminó?

En todos estos casos la respuesta es simplemente sí o no.

Nuestro primer ejemplo

```c
#include <stdbool.h>
#include <stdio.h>
int main(void)
{
    bool aprobado = true;
```

    if (aprobado)

```c
    {
        printf("Examen aprobado.\n");
    }
}
```

En este ejemplo, la variable aprobado almacena el valor true, indicando que el examen fue aprobado.

Nota: En los programas de CS50 normalmente utilizaremos bool gracias a las bibliotecas que estamos incluyendo. Más adelante veremos con más detalle cómo funciona en el lenguaje C estándar.

¿Por qué no usamos un string?

Podríamos escribir:

"Sí"

o

"No"

Pero esos son textos.

Cuando una respuesta solo puede tener dos estados, resulta más claro y eficiente utilizar un bool.

Pensemos en un interruptor

Podemos imaginar un interruptor de luz.

💡 Encendida

💡 Apagada

No existe un estado intermedio.

Con un bool ocurre exactamente lo mismo.

true  → Encendida

false → Apagada

Muchos programas toman decisiones utilizando este tipo de dato.

Resumen

El tipo de dato bool permite almacenar únicamente dos valores:

true

false

Se utiliza para representar situaciones que solo pueden ser verdaderas o falsas.

Más adelante veremos que este tipo de dato será fundamental para que nuestros programas puedan tomar decisiones.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué significa bool?

¿Qué valores puede almacenar?

¿Cuándo conviene utilizar un bool?

¿Por qué no es lo mismo utilizar un bool que un string con las palabras "Sí" y "No"?

¿Por qué bool será importante cuando aprendamos las estructuras condicionales?

Ya conocemos casi todos los tipos de datos que utilizaremos con frecuencia.

Solo nos queda uno más:

void

A diferencia de los anteriores, void no representa un tipo de información que podamos almacenar.

Entonces surge una última pregunta:

Si void no almacena datos, ¿por qué existe y para qué sirve?

El tipo de dato void

¿Qué problema resuelve?

Hasta ahora conocimos varios tipos de datos.

Aprendimos que podemos almacenar:

```c
números enteros (int);
números decimales (float y double);
caracteres (char);
textos (string);
```

valores verdaderos o falsos (bool).

Todos ellos tienen algo en común.

Sirven para almacenar información.

Sin embargo, desde el primer programa que escribimos apareció una palabra que todavía no explicamos.

```c
int main(void)
```

Entonces surge una nueva pregunta.

¿Qué significa void y por qué aparece si no almacena ningún dato?

¿Qué significa void?

La palabra void proviene del inglés y significa:

Vacío.

En programación, void indica que no existe ningún dato.

Es decir, representa la ausencia de un valor.

A diferencia de los demás tipos de datos, void no puede utilizarse para almacenar información.

¿Dónde vimos void por primera vez?

Desde el primer programa escribimos algo parecido a esto.

```c
int main(void)
{
    printf("¡Hola!\n");
}
```

La palabra:

void

aparece entre los paréntesis de main().

En este caso significa que la función no necesita recibir ningún dato para ejecutarse.

Más adelante aprenderemos qué son las funciones y entenderemos por qué esto es importante.

Por ahora basta con saber que void indica la ausencia de información.

¿Cuándo utilizamos void?

Generalmente veremos void en dos situaciones.

## 1. Cuando una función no recibe datos.

```c
int main(void)
```

En este ejemplo, main no necesita que el usuario le envíe información para comenzar a ejecutarse.

## 2. Cuando una función no devuelve ningún resultado.

Más adelante aprenderemos a crear nuestras propias funciones.

Algunas realizarán una tarea, pero no devolverán ningún valor.

Por ejemplo:

```c
void saludar(void)
{
    printf("¡Hola!\n");
}
```

No te preocupes si todavía no entiendes completamente este ejemplo.

Lo retomaremos cuando estudiemos las funciones.

¿Por qué no podemos crear una variable void?

Imaginemos que intentamos escribir:

```c
void dato;
```

¿Qué información debería almacenar?

La respuesta es sencilla.

Ninguna.

Y justamente por eso no tiene sentido crear una variable de tipo void.

Mientras que un int, un char o un string almacenan información, void representa que no hay ningún dato.

Resumen

El tipo void representa la ausencia de información.

No se utiliza para almacenar datos.

Lo veremos principalmente cuando trabajemos con funciones que no reciben parámetros o que no devuelven ningún valor.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué significa void?

¿Qué diferencia existe entre void y los demás tipos de datos?

¿Por qué void no puede utilizarse para crear una variable?

¿En qué situaciones aparece normalmente void?

¿Qué significa void en int main(void)?

Ya conocemos los principales tipos de datos del lenguaje C.

Pero todavía no hemos respondido una pregunta muy importante.

Sabemos qué tipo de información podemos almacenar, pero…

¿Dónde se guarda esa información mientras el programa se está ejecutando?

Para responder esa pregunta necesitaremos conocer uno de los conceptos más importantes de toda la programación:

Variables

Variables

¿Qué problema resuelve?

En los capítulos anteriores aprendimos que existen distintos tipos de datos.

Podemos trabajar con:

números enteros;

números decimales;

caracteres;

textos;

valores verdaderos o falsos.

Pero imaginemos el siguiente programa.

```c
printf("Hola, Mailen\n");
```

Funciona correctamente.

Sin embargo, ¿qué ocurriría si el usuario se llama Juan?

Tendríamos que modificar el código.

Y si se llama Sofía...

Tendríamos que volver a modificarlo.

Entonces surge una nueva pregunta.

¿Cómo puede un programa recordar información que cambia cada vez que se ejecuta?

¿Qué es una variable?

Una variable es un espacio reservado en la memoria de la computadora donde podemos guardar información para utilizarla más adelante.

Podemos imaginar una variable como una caja.

📦

Dentro de esa caja guardamos un dato.

Pero una computadora puede tener miles o incluso millones de cajas.

Entonces aparece otra pregunta.

¿Cómo sabe cuál debe utilizar?

La respuesta es sencilla.

Cada caja tiene una etiqueta con un nombre.

📦 nombre

📦 edad

📦 altura

Cuando el programa necesita un dato, simplemente busca la caja con la etiqueta correspondiente.

Una variable tiene tres partes

Cuando declaramos una variable, normalmente aparecen tres elementos.

```c
string nombre = "Mailen";
```

Analicemos cada uno.

El tipo de dato

string

Le indica a la computadora qué clase de información almacenará la variable.

El nombre

nombre

Es la etiqueta que utilizaremos para acceder al dato.

Elegir nombres claros hace que el código sea mucho más fácil de leer.

El valor

"Mailen"

Es la información que guardaremos dentro de la variable.

Podemos representarlo así:

Tipo      Nombre      Valor

 │           │          │

 ▼           ▼          ▼

string    nombre    "Mailen"

Un ejemplo completo

```c
#include <cs50.h>
#include <stdio.h>
int main(void)
{
    string nombre = get_string("¿Cómo te llamás? ");
    printf("Hola, %s\n", nombre);
}
```

Cuando el usuario escribe:

Mailen

La computadora hace algo parecido a esto.

┌─────────────────────┐

│ nombre              │

├─────────────────────┤

│ "Mailen"            │

└─────────────────────┘

Después, cuando encuentra:

```c
printf("Hola, %s\n", nombre);
```

busca el contenido de la variable nombre y lo reemplaza por el texto almacenado.

El resultado será:

Hola, Mailen

¿Por qué se llaman variables?

Porque su valor puede cambiar durante la ejecución del programa.

Por ejemplo:

```c
int vidas = 3;
```

Más adelante podría ocurrir:

```c
vidas = 2;
```

Y después:

```c
vidas = 1;
```

La caja sigue siendo la misma.

Lo único que cambia es el valor que contiene.

Por eso reciben el nombre de variables.

¿Cómo elegimos el nombre de una variable?

Una buena variable debe describir claramente la información que almacena.

Por ejemplo:

edad

es mucho más claro que:

x

Y:

temperatura

es mucho más descriptivo que:

dato

Cuanto más claro sea el nombre, más fácil será entender el programa.

Resumen

Una variable es un espacio reservado en memoria donde almacenamos información.

Cada variable tiene:

un tipo de dato;

un nombre;

un valor.

Las variables permiten que un programa recuerde información y trabaje con ella durante su ejecución.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué es una variable?

¿Por qué decimos que una variable es como una caja con una etiqueta?

¿Cuáles son las tres partes de una variable?

¿Por qué una variable recibe ese nombre?

¿Por qué es importante elegir nombres descriptivos?

Constantes

¿Qué problema resuelve?

En el capítulo anterior aprendimos que una variable puede cambiar su valor durante la ejecución de un programa.

Por ejemplo:

```c
int vidas = 3;
```

Más adelante podría ocurrir:

```c
vidas = 2;
```

Y después:

```c
vidas = 1;
```

Ese comportamiento es completamente normal.

Pero imaginemos ahora otros datos.

La velocidad de la luz.

El valor de π.

La cantidad de días de una semana.

La cantidad de meses de un año.

¿Tiene sentido que esos valores cambien durante la ejecución del programa?

La respuesta es no.

Entonces surge una nueva pregunta.

¿Cómo le indicamos a la computadora que un valor no debe modificarse?

¿Qué es una constante?

Una constante es un dato cuyo valor permanece igual durante toda la ejecución del programa.

A diferencia de una variable, una constante no puede modificarse una vez que ha sido definida.

Podemos pensar en ella como una caja sellada.

📦 Variable

Puede cambiar su contenido.

📦🔒 Constante

Su contenido permanece siempre igual.

¿Por qué necesitamos constantes?

Las constantes hacen que nuestros programas sean más seguros y fáciles de mantener.

Imaginemos que un programa necesita utilizar el valor de π en muchos cálculos.

Podríamos escribir:

3.14159265

cada vez que lo necesitemos.

Pero si un día decidimos utilizar una aproximación más precisa, tendríamos que modificar todas las apariciones de ese número.

En cambio, si definimos una constante:

```c
const double PI = 3.14159265;
```

solo deberemos cambiar el valor en un único lugar.

Además, evitamos modificarlo por accidente durante la ejecución del programa.

Nuestro primer ejemplo

```c
#include <stdio.h>
int main(void)
{
    const int DIAS_SEMANA = 7;
    printf("Una semana tiene %i días.\n", DIAS_SEMANA);
}
```

La salida será:

Una semana tiene 7 días.

¿Qué ocurre si intentamos modificar una constante?

Supongamos que escribimos:

```c
const int DIAS_SEMANA = 7;
DIAS_SEMANA = 8;
```

La computadora detectará un error durante la compilación.

¿Por qué?

Porque una constante no puede cambiar su valor después de haber sido creada.

Una convención muy utilizada

Es habitual escribir los nombres de las constantes completamente en mayúsculas.

Por ejemplo:

PI

DIAS_SEMANA

VELOCIDAD_LUZ

Esto no es una obligación del lenguaje C, pero ayuda a identificar rápidamente que se trata de un valor constante.

¿Variable o constante?

Podemos resumir la diferencia así:

Variable	Constante

Su valor puede cambiar.	Su valor permanece igual.

Se utiliza para datos que cambian durante la ejecución.	Se utiliza para datos que nunca deberían modificarse.

Resumen

Una constante es un dato cuyo valor no puede modificarse durante la ejecución del programa.

Utilizar constantes hace que el código sea más claro, más seguro y más fácil de mantener.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué es una constante?

¿En qué se diferencia de una variable?

¿Cuándo conviene utilizar una constante?

¿Qué ocurre si intentamos modificar una constante?

¿Por qué suele escribirse su nombre en mayúsculas?

Ya sabemos qué tipo de datos podemos utilizar, cómo almacenarlos en variables y cómo proteger aquellos que no deben cambiar.

Pero todavía no hemos hecho casi nada con esos datos.

Entonces surge una nueva pregunta:

¿Cómo puede un programa sumar, restar, comparar o combinar la información que almacena?

Para responderla conoceremos el siguiente tema:

Operadores

Aquí comenzaremos a realizar operaciones con los datos que hemos aprendido a almacenar.

Operadores

¿Qué problema resuelve?

Hasta este momento aprendimos a almacenar información en variables.

Por ejemplo:

```c
int edad = 36;
```

Pero guardar información no es suficiente.

Imaginemos que queremos:

sumar dos números;

calcular un promedio;

saber si una persona es mayor de edad;

aumentar el puntaje de un jugador;

disminuir la cantidad de vidas de un personaje.

En todos estos casos necesitamos realizar operaciones con los datos.

Entonces surge una nueva pregunta.

¿Cómo puede una computadora realizar operaciones con la información que almacena?

¿Qué es un operador?

Un operador es un símbolo que le indica a la computadora qué acción debe realizar sobre uno o más datos.

Por ejemplo, cuando escribimos:

5 + 3

el símbolo:

+

le dice a la computadora que debe realizar una suma.

De la misma manera, otros símbolos representan distintas operaciones.

Tipos de operadores

En C existen muchos operadores, pero los más utilizados pueden agruparse en cinco categorías.

Operadores aritméticos.

Operadores de asignación.

Operadores de incremento y decremento.

Operadores de comparación.

Operadores lógicos.

En los próximos apartados estudiaremos cada uno de ellos.

Operadores aritméticos

¿Qué problema resuelven?

Las matemáticas forman parte de muchísimos programas.

Una calculadora suma números.

Un videojuego calcula puntajes.

Una tienda calcula descuentos.

Un banco calcula intereses.

Entonces surge una nueva pregunta.

¿Cómo realiza la computadora operaciones matemáticas?

Los operadores aritméticos

Los operadores aritméticos permiten realizar operaciones matemáticas básicas.

Operador	Operación

+	Suma

-	Resta

*	Multiplicación

/	División

%	Resto de una división

Ejemplo

```c
#include <stdio.h>
int main(void)
{
    int a = 12;
    int b = 4;
    printf("Suma: %i\n", a + b);
    printf("Resta: %i\n", a - b);
    printf("Multiplicación: %i\n", a * b);
    printf("División: %i\n", a / b);
}
```

La salida será:

Suma: 16

Resta: 8

Multiplicación: 48

División: 3

El operador %

Existe un operador un poco diferente.

%

No calcula una división.

Calcula el resto de una división.

Por ejemplo:

10 % 3

La división da:

10 ÷ 3 = 3

Pero sobra:

1

Entonces:

10 % 3

produce:

1

Otro ejemplo.

20 % 5

Como la división es exacta, el resto es:

0

Este operador es muy útil para saber, por ejemplo, si un número es par o impar.

Resumen

Los operadores aritméticos permiten realizar operaciones matemáticas básicas sobre los datos almacenados en las variables.

Gracias a ellos podemos sumar, restar, multiplicar, dividir y calcular el resto de una división.

¿Qué deberías haber entendido?

Al finalizar esta sección deberías poder responder las siguientes preguntas:

¿Qué es un operador?

¿Qué hacen los operadores aritméticos?

¿Qué diferencia existe entre / y %?

¿Cuándo puede resultar útil el operador %?

Operadores de asignación

¿Qué problema resuelven?

Desde hace varios capítulos escribimos instrucciones como estas:

```c
int edad = 36;
string nombre = "Mailen";
float altura = 1.72;
```

Probablemente ya te hayas acostumbrado a ver el símbolo:

=

Pero...

¿Qué significa realmente?

¿Significa que ambos lados son iguales?

La respuesta es no.

En programación, el operador = tiene un significado diferente.

¿Qué es un operador de asignación?

El operador = sirve para guardar un valor dentro de una variable.

Podemos leer esta línea:

```c
int edad = 36;
```

como si dijera:

"Guardá el valor 36 dentro de la variable edad."

No significa:

"Edad es igual a 36."

Significa:

"Asignale el valor 36 a la variable edad."

Pensemos en una caja

Recordemos el ejemplo de las variables.

edad

┌──────────────┐

│              │

└──────────────┘

Cuando escribimos:

```c
edad = 36;
```

es como colocar el número 36 dentro de esa caja.

edad

┌──────────────┐

│      36      │

└──────────────┘

La variable no cambia.

Lo que cambia es el contenido de la caja.

Podemos cambiar el contenido

Más adelante podemos escribir:

```c
edad = 37;
```

Ahora la caja contiene otro valor.

edad

┌──────────────┐

│      37      │

└──────────────┘

El valor anterior desaparece y es reemplazado por el nuevo.

El lado izquierdo y el lado derecho

Observemos nuevamente la asignación.

```c
edad = 36;
```

Cada lado cumple una función distinta.

edad        =        36

```
 ↑                    ↑
Variable           Valor
```

A la izquierda siempre encontramos la variable que recibirá la información.

A la derecha encontramos el valor que queremos guardar.

También podemos asignar el resultado de una operación

El lado derecho no tiene por qué ser un número fijo.

También puede ser una expresión.

```c
int edad = 18 + 18;
```

La computadora primero realiza la suma.

18 + 18

Obtiene:

36

Y recién después guarda ese resultado dentro de la variable.

Incluso podemos usar otras variables

Supongamos que tenemos:

```c
int a = 10;
int b = 5;
```

Podemos escribir:

```c
int resultado = a + b;
```

La computadora hace lo siguiente:

Busca el valor de a.

Busca el valor de b.

Los suma.

Guarda el resultado en resultado.

Al finalizar, tendremos:

resultado

┌──────────────┐

│      15      │

└──────────────┘

Un error muy común

Muchas personas que comienzan a programar piensan que esta línea:

```c
edad = edad + 1;
```

no tiene sentido.

En matemáticas sería imposible.

Porque una cantidad no puede ser igual a sí misma más uno.

Pero en programación no estamos diciendo que ambos lados sean iguales.

Estamos diciendo:

"Tomá el valor actual de edad, sumale 1 y guardá nuevamente el resultado en edad."

Si edad valía:

36

Después de ejecutar esa instrucción pasará a valer:

37

Resumen

El operador = no compara valores.

Su función es asignar un valor a una variable.

Cada vez que utilizamos este operador, el contenido anterior de la variable es reemplazado por el nuevo valor.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué función cumple el operador =?

¿Por qué no significa "igual" como en matemáticas?

¿Qué ocurre cuando asignamos un nuevo valor a una variable?

¿Qué sucede en una instrucción como edad = edad + 1;?

¿Qué representa el lado izquierdo y el lado derecho de una asignación?

Ya sabemos cómo guardar información en una variable.

Pero muchas veces necesitaremos modificar ese valor de forma repetitiva.

Por ejemplo:

aumentar el puntaje de un jugador;

disminuir la cantidad de vidas;

sumar un producto al total de una compra.

Entonces surge una nueva pregunta:

¿Existe una forma más simple de escribir estas operaciones que repetir siempre variable = variable + ...?

En el próximo capítulo conoceremos los operadores de incremento y asignación abreviada, como:

+=

-=

++

--

que hacen el código más corto y fácil de leer.

Operadores de asignación abreviada

¿Qué problema resuelven?

En el capítulo anterior aprendimos que podemos modificar el valor de una variable.

Por ejemplo:

```c
puntaje = puntaje + 10;
```

La instrucción funciona correctamente.

Pero imaginemos un videojuego.

Cada vez que el jugador elimina un enemigo debemos sumar puntos.

Si esa operación se repite muchas veces, escribir siempre:

```c
puntaje = puntaje + 10;
```

resulta largo y repetitivo.

Entonces surge una nueva pregunta.

¿Existe una forma más corta de actualizar el valor de una variable?

La respuesta es sí

El lenguaje C incorpora los operadores de asignación abreviada.

Estos operadores permiten escribir la misma operación de forma más compacta.

Por ejemplo:

```c
puntaje += 10;
```

significa exactamente lo mismo que:

```c
puntaje = puntaje + 10;
```

La computadora obtiene el mismo resultado.

La diferencia es que el código es más corto y más fácil de leer.

Los operadores más utilizados

Operador	Equivale a

+=	x = x + valor

-=	x = x - valor

*=	x = x * valor

/=	x = x / valor

%=	x = x % valor

Algunos ejemplos

Si tenemos:

```c
int vidas = 5;
```

y escribimos:

```c
vidas -= 1;
```

es equivalente a:

```c
vidas = vidas - 1;
```

El resultado será:

4

Otro ejemplo.

```c
int dinero = 100;
```

Si ejecutamos:

```c
dinero += 50;
```

es equivalente a:

```c
dinero = dinero + 50;
```

Ahora la variable contiene:

150

También podemos multiplicar.

```c
int puntos = 20;
puntos *= 2;
```

equivale a:

```c
puntos = puntos * 2;
```

El resultado será:

40

¿Cuál conviene usar?

Ambas formas son correctas.

```c
puntaje = puntaje + 10;
```

y

```c
puntaje += 10;
```

producen exactamente el mismo resultado.

Sin embargo, la segunda suele ser más clara y más utilizada porque expresa de forma directa que estamos actualizando el valor de la variable.

Resumen

Los operadores de asignación abreviada permiten modificar el valor de una variable utilizando una sintaxis más corta.

No realizan operaciones nuevas.

Simplemente representan una forma más compacta de escribir una asignación.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué problema resuelven los operadores de asignación abreviada?

¿Qué significa +=?

¿Qué significa -=?

¿Qué diferencia existe entre x = x + 1 y x += 1?

¿Por qué muchos programadores prefieren utilizar esta sintaxis?

Existe una situación todavía más frecuente.

Muchas veces solo queremos aumentar o disminuir una variable en una unidad.

Por ejemplo:

```c
vidas += 1;
```

o

```c
vidas -= 1;
```

Entonces surge una nueva pregunta:

¿Existe una forma aún más simple de sumar o restar uno?

La respuesta es sí.

En el próximo capítulo conoceremos dos operadores muy utilizados:

++

--

que permiten incrementar o decrementar una variable de manera aún más sencilla.

Operadores de incremento y decremento

¿Qué problema resuelven?

En el capítulo anterior vimos que podíamos actualizar una variable de forma abreviada.

Por ejemplo:

```c
contador += 1;
```

o

```c
vidas -= 1;
```

Estas instrucciones son mucho más cortas que escribir la asignación completa.

Pero existe una situación todavía más común.

Muchas veces solo necesitamos aumentar o disminuir una variable en una única unidad.

Por ejemplo:

contar personas;

recorrer una lista;

aumentar el puntaje;

disminuir las vidas de un jugador;

contar los segundos de un cronómetro.

Entonces surge una nueva pregunta.

¿Existe una forma aún más simple de sumar o restar uno?

La respuesta es sí.

El operador de incremento

El operador:

++

aumenta una variable en una unidad.

Por ejemplo:

contador++;

es exactamente equivalente a escribir:

```c
contador += 1;
```

y también equivale a:

```c
contador = contador + 1;
```

Las tres instrucciones producen el mismo resultado.

La diferencia es únicamente la forma de escribirlas.

Un ejemplo

Supongamos que tenemos:

```c
int contador = 5;
```

Después ejecutamos:

contador++;

Ahora la variable contiene:

6

Si volvemos a ejecutar:

contador++;

el resultado será:

7

Cada ejecución aumenta el valor en uno.

El operador de decremento

El operador:

--

hace exactamente lo contrario.

Disminuye una variable en una unidad.

Por ejemplo:

vidas--;

equivale a:

```c
vidas -= 1;
```

y también a:

```c
vidas = vidas - 1;
```

Ejemplo

Supongamos:

```c
int vidas = 3;
```

Después ejecutamos:

vidas--;

Ahora tendremos:

2

Si volvemos a ejecutar:

vidas--;

obtendremos:

1

¿Cuándo conviene utilizarlos?

Siempre que únicamente queramos sumar o restar uno.

Por ejemplo, un contador.

contador++;

O las vidas de un videojuego.

vidas--;

O el número de intentos realizados.

intentos++;

Son operadores muy comunes porque contar elementos es una tarea muy frecuente en programación.

Una aclaración importante

Quizás encuentres código como este:

++contador;

o como este:

contador++;

En muchos casos ambos producen el mismo resultado.

Sin embargo, no siempre se comportan exactamente igual. La diferencia entre preincremento (++contador) y postincremento (contador++) aparece cuando el valor se utiliza dentro de una expresión más compleja.

Como todavía estamos aprendiendo los fundamentos, por ahora alcanza con saber que ambas formas incrementan la variable en uno. Más adelante, cuando trabajemos con expresiones y funciones, veremos esa diferencia con detalle.

Resumen

Los operadores ++ y -- permiten incrementar o decrementar una variable en una unidad.

Son una forma abreviada de escribir operaciones muy comunes y hacen que el código sea más claro cuando solo necesitamos sumar o restar uno.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué hace el operador ++?

¿Qué hace el operador --?

¿A qué instrucciones equivalen?

¿En qué situaciones conviene utilizarlos?

¿Qué diferencia existe entre usar += 1 y ++?

Ya sabemos cómo realizar operaciones matemáticas y cómo actualizar el valor de una variable.

Pero muchas veces necesitamos responder preguntas como:

¿Un número es mayor que otro?

¿Dos valores son iguales?

¿Una persona es mayor de edad?

¿Una contraseña coincide con la esperada?

Entonces surge una nueva pregunta:

¿Cómo puede una computadora comparar dos valores y decidir si una condición es verdadera o falsa?

Para responderla conoceremos los operadores de comparación, una herramienta fundamental para que los programas puedan tomar decisiones.

Operadores de comparación

¿Qué problema resuelven?

Hasta ahora aprendimos a guardar información y a realizar operaciones con ella.

Por ejemplo:

```c
int edad = 20;
```

Pero imaginemos que queremos responder preguntas como estas.

¿La persona es mayor de edad?

¿El jugador llegó a 100 puntos?

¿Dos números son iguales?

¿Una contraseña coincide con la esperada?

La computadora necesita comparar valores para poder responder estas preguntas.

Entonces surge una nueva pregunta.

¿Cómo sabe una computadora si dos valores son iguales, diferentes o cuál de ellos es mayor?

¿Qué es un operador de comparación?

Un operador de comparación compara dos valores.

El resultado de esa comparación siempre será uno de estos dos valores:

true

o

false

Es decir, la respuesta siempre será:

verdadero;

falso.

No existen otros resultados.

Los operadores de comparación

En C existen seis operadores principales.

Operador	Significado

==	Igual a

!=	Distinto de

>	Mayor que

<	Menor que

>=	Mayor o igual que

<=	Menor o igual que

Igual que (==)

Supongamos:

```c
int edad = 18;
```

Podemos preguntar:

edad == 18

La respuesta será:

true

Porque ambos valores son iguales.

En cambio:

edad == 20

produce:

false

Distinto de (!=)

Este operador verifica que los valores sean diferentes.

Por ejemplo:

edad != 20

Como la edad vale 18, el resultado será:

true

Porque 18 es distinto de 20.

Mayor que (>)

Supongamos:

```c
int temperatura = 28;
```

Si preguntamos:

temperatura > 20

La respuesta será:

true

Porque 28 es mayor que 20.

Menor que (<)

Ahora:

temperatura < 20

produce:

false

Porque 28 no es menor que 20.

Mayor o igual (>=)

Este operador acepta dos posibilidades.

Por ejemplo:

edad >= 18

Será verdadero cuando la edad sea:

18

o cualquier número mayor.

Menor o igual (<=)

De forma similar:

edad <= 18

será verdadero cuando la edad sea:

18;

17;

16;

cualquier número menor.

Un error muy común

Muchos principiantes escriben:

edad = 18

cuando quieren preguntar si la edad vale 18.

Pero ya sabemos que:

=

es el operador de asignación.

No sirve para comparar.

Para preguntar si dos valores son iguales debemos utilizar:

==

Esta es una de las confusiones más frecuentes al comenzar a programar.

Un ejemplo completo

```c
#include <stdio.h>
int main(void)
{
    int edad = 20;
    printf("%i\n", edad >= 18);
}
```

La salida será:

1

Quizás esto resulte extraño.

¿Por qué aparece un 1 en lugar de true?

En C, los valores booleanos se representan internamente mediante números.

true  → 1

false → 0

Más adelante, cuando estudiemos el tipo bool, veremos una forma más clara de trabajar con estos valores. Por ahora alcanza con saber que 1 representa verdadero y 0 representa falso.

¿Para qué sirven?

Por sí solos, los operadores de comparación únicamente responden una pregunta.

Su verdadero poder aparece cuando los utilizamos para tomar decisiones.

Por ejemplo:

¿edad >= 18?

La computadora obtiene:

true

Y con esa respuesta podrá decidir qué hacer después.

Eso es exactamente lo que aprenderemos en el capítulo de los condicionales.

Resumen

Los operadores de comparación permiten comparar dos valores.

El resultado siempre será:

true

false

Son la base de todas las decisiones que puede tomar un programa.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué hace un operador de comparación?

¿Qué diferencia existe entre = y ==?

¿Qué significa !=?

¿Qué representan >= y <=?

¿Por qué los operadores de comparación son fundamentales para los programas?

Ya sabemos comparar dos valores.

Pero muchas veces una sola comparación no alcanza.

Por ejemplo:

una persona debe ser mayor de 18 años y tener licencia;

un usuario puede ingresar si conoce la contraseña o tiene un código de recuperación;

una acción debe ejecutarse solo si una condición no se cumple.

Entonces surge una nueva pregunta:

¿Cómo podemos combinar varias condiciones para obtener una única respuesta?

Para resolver este problema conoceremos los operadores lógicos:

&&

||

!

Ellos permitirán construir condiciones mucho más complejas y prepararán el camino para el siguiente gran tema del libro: los condicionales (if, else if y else).

Overflow

¿Qué problema resuelve?

Hasta ahora aprendimos que una variable puede almacenar números.

Por ejemplo:

```c
int edad = 36;
```

También aprendimos que podemos realizar operaciones con ellos.

edad++;

o

```c
edad += 10;
```

Pero imaginemos que seguimos aumentando un número una y otra vez.

¿Puede crecer para siempre?

La respuesta es no.

Entonces surge una nueva pregunta.

¿Qué ocurre cuando intentamos guardar un número más grande de lo que una variable puede almacenar?

La memoria no es infinita

Recordemos que una variable ocupa un espacio en la memoria.

Ese espacio tiene un tamaño fijo.

Por ejemplo, un int utiliza una cantidad determinada de bits para guardar un número.

Eso significa que existe un número máximo y un número mínimo que puede representar.

Cuando intentamos superar ese límite ocurre un fenómeno llamado overflow.

¿Qué es un overflow?

Un overflow ocurre cuando el resultado de una operación supera la capacidad del tipo de dato.

Es como intentar llenar un vaso de 250 ml con un litro de agua.

El vaso simplemente no tiene espacio suficiente.

Con las variables ocurre exactamente lo mismo.

Un ejemplo sencillo

Supongamos que una caja solo pudiera almacenar números entre:

0 y 9

Si la caja contiene:

9

y le sumamos uno:

9 + 1

No existe espacio para guardar el número 10.

Dependiendo del tipo de dato y del lenguaje, el resultado puede "volver a empezar" o producir un comportamiento inesperado.

Eso es un overflow.

Un ejemplo en C

```c
#include <stdio.h>
#include <limits.h>
int main(void)
{
    int numero = INT_MAX;
    printf("%i\n", numero);
```

    numero++;

```c
    printf("%i\n", numero);
}
```

INT_MAX representa el mayor valor que puede almacenar un int.

Después de incrementarlo, el resultado ya no puede representarse correctamente y se produce un overflow.

¿Por qué es importante?

El overflow puede provocar resultados incorrectos sin que el programa muestre un error.

Por ejemplo:

cálculos financieros;

puntajes de un videojuego;

contadores;

sistemas científicos.

Si no conocemos los límites de los tipos de datos, nuestros programas pueden generar respuestas inesperadas.

Resumen

Cada tipo de dato tiene un límite.

Cuando una operación supera ese límite, ocurre un overflow.

Por eso es importante elegir el tipo de dato adecuado para cada situación.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué es un overflow?

¿Por qué ocurre?

¿Qué relación tiene con el tamaño de la memoria?

¿Por qué puede producir resultados inesperados?

¿Cómo podemos reducir el riesgo de que ocurra?

Format codes

¿Qué problema resuelven?

Hasta ahora aprendimos a mostrar información utilizando printf().

Por ejemplo:

```c
printf("Hola\n");
```

Pero imaginemos que queremos mostrar el valor de una variable.

Supongamos que tenemos:

```c
int edad = 36;
```

¿Cómo hacemos para que printf() escriba ese número?

¿Será suficiente escribir?

```c
printf("edad");
```

No.

La computadora imprimiría literalmente la palabra:

edad

Y si escribimos:

```c
printf(edad);
```

tampoco funcionará.

Entonces surge una nueva pregunta.

¿Cómo le indicamos a printf() qué tipo de dato queremos mostrar?

¿Qué es un format code?

Un format code (o código de formato) es una marca especial que colocamos dentro del texto de printf().

Cuando la computadora encuentra esa marca, sabe que allí debe reemplazarla por el valor de una variable.

Podemos imaginarlo como un espacio reservado.

"Hola, ____"

Cuando el programa conoce el nombre del usuario, simplemente completa ese espacio.

Por ejemplo:

"Hola, Mailen"

Los format codes funcionan exactamente de esa manera.

Nuestro primer format code

Supongamos:

```c
int edad = 36;
```

Podemos escribir:

```c
printf("Tengo %i años.\n", edad);
```

La salida será:

Tengo 36 años.

¿Qué ocurrió?

printf() encontró el símbolo:

%i

y lo reemplazó por el contenido de la variable:

edad

Cada tipo de dato tiene su código

Como ya aprendimos, una computadora distingue distintos tipos de datos.

Por eso cada uno tiene su propio format code.

Los más utilizados son:

Tipo	Format code

int	%i

float	%f

double	%lf

char	%c

string	%s

Ejemplos

Enteros

```c
int edad = 36;
printf("%i\n", edad);
```

Salida:

36

Decimales

```c
float altura = 1.72;
printf("%f\n", altura);
```

Salida:

1.720000

Quizás te sorprenda que aparezcan tantos ceros.

Más adelante veremos cómo controlar la cantidad de decimales que queremos mostrar.

Caracteres

```c
char inicial = 'M';
printf("%c\n", inicial);
```

Salida:

M

Texto

```c
string nombre = "Mailen";
printf("%s\n", nombre);
```

Salida:

Mailen

¿Qué ocurre si usamos el código incorrecto?

Supongamos que escribimos:

```c
int edad = 36;
printf("%s\n", edad);
```

Aquí estamos diciendo que un número entero es un texto.

La computadora intentará interpretar ese número como si fuera una dirección de memoria donde comienza una cadena de caracteres.

El resultado será incorrecto y, en muchos casos, el programa terminará con un error.

Por eso es importante utilizar siempre el format code que corresponde al tipo de dato.

¿Por qué el símbolo %?

El carácter % le indica a printf() que lo que sigue no forma parte del texto, sino que es una instrucción especial.

Por ejemplo:

```c
printf("Edad: %i");
```

Aquí %i no se imprimirá literalmente.

Será reemplazado por el valor que indiquemos después de la coma.

Resumen

Los format codes permiten insertar variables dentro del texto que muestra printf().

Cada tipo de dato tiene su propio código de formato, por lo que es importante utilizar el adecuado para evitar errores.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué es un format code?

¿Para qué sirve?

¿Qué format code utiliza un int?

¿Cuál corresponde a un string?

¿Qué puede ocurrir si usamos un format code incorrecto?

Hasta ahora aprendimos a mostrar información en pantalla.

Pero los programas realmente interesantes no solo muestran datos: también toman decisiones.

Entonces surge una nueva pregunta:

¿Cómo puede un programa ejecutar una acción cuando una condición se cumple y otra diferente cuando no se cumple?

Para responderla conoceremos los condicionales (if, else if y else), una de las herramientas más importantes de la programación.

Condicionales: if

¿Qué problema resuelven?

Hasta ahora, todos los programas que escribimos funcionaban de la misma manera.

Si ejecutábamos este código:

```c
printf("Hola.\n");
printf("Bienvenido.\n");
printf("Fin del programa.\n");
```

La computadora imprimía siempre los tres mensajes.

No importaba quién ejecutara el programa ni qué información hubiera ingresado.

Siempre seguía exactamente el mismo camino.

Pero imaginemos un programa que pregunta la edad de una persona.

Si tiene 18 años o más, queremos mostrar un mensaje.

Si es menor de edad, no queremos mostrar nada.

Ahora el programa ya no puede ejecutar todas las instrucciones de forma automática.

Necesita decidir.

Entonces surge una nueva pregunta.

¿Cómo puede una computadora ejecutar una instrucción solamente cuando se cumple una condición?

¿Qué es un if?

La instrucción if permite ejecutar un bloque de código únicamente cuando una condición es verdadera.

Podemos imaginarlo como un guardia en una puerta.

             ¿Se cumple la condición?

                   Sí

                   │

                   ▼

           Se abre la puerta

           y el programa entra

                   No

                   │

                   ▼

         La puerta permanece cerrada

         y el programa sigue su camino

El programa no siempre ejecuta ese bloque.

Primero pregunta.

Después decide.

La estructura de un if

La forma general es:

if (condición)

```c
{
```

    instrucciones;

```c
}
```

Podemos identificar tres partes.

if

Le indica a la computadora que comenzará una decisión.

(condición)

Aquí escribimos una expresión que produce:

true

false

```c
{
```

    ...

```c
}
```

Dentro de las llaves colocamos las instrucciones que se ejecutarán únicamente si la condición es verdadera.

Primer ejemplo

```c
#include <stdio.h>
int main(void)
{
    int edad = 20;
```

    if (edad >= 18)

```c
    {
        printf("Sos mayor de edad.\n");
    }
}
```

La computadora evalúa:

20 >= 18

Obtiene:

true

Como la respuesta es verdadera, ejecuta el bloque.

Resultado:

Sos mayor de edad.

¿Qué ocurre si la condición es falsa?

Ahora cambiemos el valor.

```c
int edad = 15;
```

La condición pasa a ser:

15 >= 18

Resultado:

false

¿Qué hace la computadora?

Simplemente salta todo el contenido del if.

Es decir, actúa como si ese bloque no existiera y continúa con la siguiente instrucción del programa.

El bloque puede tener varias instrucciones

No estamos limitados a una sola línea.

if (edad >= 18)

```c
{
    printf("Bienvenido.\n");
    printf("Podés ingresar.\n");
    printf("Disfrutá del evento.\n");
}
```

Si la condición es verdadera, la computadora ejecutará las tres instrucciones.

Si es falsa, omitirá las tres.

Un detalle importante

El if no obliga a que exista un caso alternativo.

Puede ocurrir perfectamente que una condición sea falsa y que el programa simplemente continúe.

Eso diferencia al if del else, que conoceremos en el próximo capítulo.

Resumen

La instrucción if permite que un programa tome su primera decisión.

Primero evalúa una condición.

Si el resultado es true, ejecuta el bloque de código.

Si el resultado es false, lo omite y continúa con el resto del programa.

¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

¿Qué problema resuelve la instrucción if?

¿Qué debe haber dentro de los paréntesis?

¿Qué función cumplen las llaves?

¿Qué ocurre cuando la condición es verdadera?

¿Qué ocurre cuando la condición es falsa?

Con if aprendimos a ejecutar código solo cuando una condición se cumple.

Pero muchas veces también necesitamos indicar qué debe hacer el programa cuando la condición no se cumple.

Por ejemplo:

Si la contraseña es correcta, permitir el acceso.

Si no es correcta, mostrar un mensaje de error.

Entonces surge una nueva pregunta:

¿Cómo puede un programa ejecutar un bloque de código cuando una condición es falsa?

La respuesta la encontraremos en el siguiente capítulo: else

# Condicionales: `else if`

## ¿Qué problema resuelve?

En los capítulos anteriores aprendimos que un programa puede elegir entre dos caminos utilizando `if` y `else`.

Por ejemplo:

```c id="3kj9pq"
if (edad >= 18)
{
    printf("Podés ingresar.\n");
}
else
{
    printf("No podés ingresar.\n");
}
```

Aquí solo existen dos posibilidades.

Pero imaginemos que un profesor quiere asignar una calificación.

- Si la nota es 9 o más, el resultado será **Excelente**.
- Si la nota es 7 o más, será **Aprobado**.
- Si es menor que 7, será **Desaprobado**.

Ahora ya no tenemos dos opciones.

Tenemos tres.

Entonces surge una nueva pregunta.

> **¿Cómo puede una computadora elegir entre varias posibilidades diferentes?**

---

# ¿Qué es `else if`?

La instrucción `else if` permite evaluar una nueva condición cuando la anterior resultó falsa.

Podemos imaginarlo como una serie de preguntas.

```text
¿Condición 1?

      Sí
      │
      ▼
 Acción 1

      No
      │
      ▼

¿Condición 2?

      Sí
      │
      ▼
 Acción 2

      No
      │
      ▼

 Acción final
```

La computadora irá revisando cada condición una por una hasta encontrar una que sea verdadera.

---

# La estructura

```c
if (condición1)
{
    ...
}
else if (condición2)
{
    ...
}
else
{
    ...
}
```

La computadora trabaja de la siguiente manera.

1. Evalúa la primera condición.
2. Si es verdadera, ejecuta ese bloque y termina.
3. Si es falsa, evalúa la siguiente condición.
4. Si ninguna condición resulta verdadera, ejecuta el bloque del `else`.

---

# Primer ejemplo

```c
#include <stdio.h>

int main(void)
{
    int nota = 8;

    if (nota >= 9)
    {
        printf("Excelente\n");
    }
    else if (nota >= 7)
    {
        printf("Aprobado\n");
    }
    else
    {
        printf("Desaprobado\n");
    }
}
```

La computadora comienza preguntando:

```text
¿8 es mayor o igual que 9?
```

Respuesta:

```text
false
```

Como la respuesta es falsa, continúa.

Ahora pregunta:

```text
¿8 es mayor o igual que 7?
```

Respuesta:

```text
true
```

En ese momento ejecuta:

```c
printf("Aprobado\n");
```

Y deja de evaluar el resto de las condiciones.

---

# ¿Qué ocurre si la primera condición es verdadera?

Supongamos ahora:

```c
int nota = 10;
```

La computadora evalúa:

```text
¿10 es mayor o igual que 9?
```

Respuesta:

```text
true
```

Como ya encontró una condición verdadera, ejecuta:

```c
printf("Excelente\n");
```

Y no revisa las demás condiciones.

Aunque la segunda condición también sería verdadera, ya no importa.

El programa ya tomó una decisión.

---

# El orden es importante

Observemos este ejemplo.

```c
if (nota >= 7)
{
    printf("Aprobado\n");
}
else if (nota >= 9)
{
    printf("Excelente\n");
}
```

Si la nota es:

```text
10
```

¿Qué ocurrirá?

La primera condición ya es verdadera.

Entonces el programa imprimirá:

```text
Aprobado
```

Y nunca llegará a comprobar si la nota era mayor o igual que 9.

Por eso, cuando trabajamos con varias condiciones, debemos escribir primero las más específicas y luego las más generales.

---

# ¿Cuántos `else if` podemos tener?

No existe un límite fijo.

Por ejemplo:

```c
if (...)
{
    ...
}
else if (...)
{
    ...
}
else if (...)
{
    ...
}
else if (...)
{
    ...
}
else
{
    ...
}
```

Podemos agregar tantos como necesitemos.

Sin embargo, si tenemos demasiados, el código puede volverse difícil de leer.

Más adelante conoceremos otras herramientas para resolver algunos de estos casos.

---

# Resumen

La instrucción `else if` permite evaluar varias condiciones de forma ordenada.

La computadora analiza cada una hasta encontrar la primera que sea verdadera.

Cuando eso ocurre, ejecuta ese bloque y deja de revisar las demás condiciones.

---

# ¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

- ¿Qué problema resuelve `else if`?
- ¿Qué ocurre cuando una condición resulta verdadera?
- ¿Por qué el orden de las condiciones es importante?
- ¿Es obligatorio terminar con un `else`?
- ¿Cuántos `else if` puede tener un programa?

---


Hasta ahora aprendimos a hacer que un programa **tome decisiones**.

Pero todavía hay una limitación importante.

Imaginemos que queremos mostrar un mensaje diez veces.

Podríamos escribir:

```c
printf("Hola\n");
printf("Hola\n");
printf("Hola\n");
```

...y repetir la misma instrucción una y otra vez.

¿Existe una forma de hacer que la computadora repita automáticamente una tarea sin escribir el mismo código muchas veces?

La respuesta la encontraremos en el siguiente capítulo:

# Bucles: `while`

Con `while` nuestros programas aprenderán a **repetir instrucciones**, dando un paso fundamental hacia la automatización.

¡Excelente! Ahora empieza uno de los capítulos que más cambia la forma de pensar al programar: **los bucles**.

Hasta ahora el programa **tomaba decisiones**. A partir de aquí, además de decidir, **podrá repetir tareas automáticamente**.

Yo dedicaría un capítulo completo únicamente a **`while`**.

---

# Bucles: `while`

## ¿Qué problema resuelven?

Hasta ahora aprendimos a escribir instrucciones como estas:

```c
printf("Hola\n");
```

La computadora ejecuta la instrucción una sola vez.

Si queremos mostrar el mismo mensaje cinco veces, podríamos escribir:

```c
printf("Hola\n");
printf("Hola\n");
printf("Hola\n");
printf("Hola\n");
printf("Hola\n");
```

El programa funciona.

Pero imaginemos que queremos mostrar el mensaje:

- 100 veces.
- 1.000 veces.
- 1.000.000 de veces.

Escribir la misma instrucción una y otra vez sería una pérdida de tiempo.

Entonces surge una nueva pregunta.

> **¿Cómo puede una computadora repetir automáticamente una misma tarea?**

---

# ¿Qué es un bucle?

Un **bucle** es una estructura que permite ejecutar un mismo bloque de código varias veces.

Podemos imaginarlo como una vuelta en una pista de atletismo.

```text
      Inicio
         │
         ▼
 ┌─────────────────┐
 │ Ejecutar código │
 └─────────────────┘
         │
         ▼
 ¿Se sigue cumpliendo
   la condición?
      │       │
     Sí       No
      │       │
      └──► Fin
```

Mientras la condición sea verdadera, el programa seguirá dando vueltas.

Cuando la condición deje de cumplirse, saldrá del bucle y continuará con el resto del programa.

---

# ¿Qué es `while`?

`while` significa **"mientras"**.

Su funcionamiento puede leerse casi como una frase en español.

```text
Mientras la condición sea verdadera,
seguí ejecutando este bloque.
```

---

# La estructura

```c
while (condición)
{
    instrucciones;
}
```

La computadora realiza siempre los mismos pasos.

1. Evalúa la condición.
2. Si es verdadera, ejecuta el bloque.
3. Vuelve a evaluar la condición.
4. Si sigue siendo verdadera, vuelve a ejecutar el bloque.
5. Repite este proceso hasta que la condición sea falsa.

---

# Primer ejemplo

```c
#include <stdio.h>

int main(void)
{
    int contador = 1;

    while (contador <= 5)
    {
        printf("Hola\n");
        contador++;
    }
}
```

Veamos qué ocurre.

Al comenzar:

```text
contador = 1
```

La computadora pregunta:

```text
¿1 <= 5?
```

Respuesta:

```text
true
```

Imprime:

```text
Hola
```

Luego ejecuta:

```c
contador++;
```

Ahora:

```text
contador = 2
```

La computadora vuelve a preguntar.

```text
¿2 <= 5?
```

Otra vez obtiene `true`.

El proceso se repite hasta que:

```text
contador = 6
```

Entonces pregunta:

```text
¿6 <= 5?
```

Respuesta:

```text
false
```

Y el bucle termina.

---

# ¿Cuántas veces se ejecutó?

El mensaje apareció:

```text
Hola
Hola
Hola
Hola
Hola
```

Exactamente cinco veces.

Y solo escribimos un `printf()`.

---

# La importancia del contador

Observemos esta línea.

```c
contador++;
```

Es una de las más importantes del programa.

¿Por qué?

Porque modifica la condición del `while`.

Cada vuelta aumenta el valor del contador.

Gracias a eso, en algún momento la condición deja de cumplirse.

Y el programa puede salir del bucle.

---

# ¿Qué ocurre si nunca cambia la condición?

Imaginemos este programa.

```c
int contador = 1;

while (contador <= 5)
{
    printf("Hola\n");
}
```

¿Qué ocurre?

La variable `contador` nunca cambia.

Siempre vale:

```text
1
```

La condición:

```text
1 <= 5
```

siempre será verdadera.

Entonces la computadora repetirá el mismo bloque una y otra vez.

Nunca saldrá del bucle.

Esto se conoce como un **bucle infinito**.

---

# Un ejemplo cotidiano

Imaginemos una botella que se llena automáticamente.

La regla es:

```text
Mientras la botella no esté llena,
seguí agregando agua.
```

Cuando finalmente se llena, dejamos de agregar agua.

Eso es exactamente lo que hace un `while`.

---

# Resumen

La instrucción `while` permite repetir un bloque de código mientras una condición sea verdadera.

En cada repetición, la condición vuelve a evaluarse.

Cuando deja de cumplirse, el bucle termina y el programa continúa con la siguiente instrucción.

---

# ¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

- ¿Qué problema resuelve un bucle?
- ¿Qué significa `while`?
- ¿Cuándo se ejecuta el bloque de un `while`?
- ¿Por qué suele utilizarse un contador?
- ¿Qué es un bucle infinito y cómo puede producirse?

---


Ya sabemos repetir instrucciones automáticamente.

Pero acabamos de descubrir un problema.

Si una condición nunca cambia, el programa puede quedar atrapado en un bucle infinito y no responder nunca.

Entonces surge una nueva pregunta:

> **¿Cómo podemos detener manualmente un programa que quedó ejecutándose sin fin?**

En el próximo capítulo aprenderemos a utilizar **`Ctrl + C`**, una combinación de teclas que permite interrumpir un programa en ejecución desde la terminal. Es una herramienta sencilla, pero muy útil durante el aprendizaje y el desarrollo de programas.

¡Vamos muy bien! Ahora sigue un capítulo muy corto, pero que evita muchísima frustración a quienes empiezan a programar. Muchos alumnos creen que, cuando un programa entra en un bucle infinito, "se rompió la computadora". Este capítulo les muestra que no es así y les da una herramienta para recuperar el control.

---

# Interrumpiendo un programa: `Ctrl + C`

## ¿Qué problema resuelve?

En el capítulo anterior aprendimos a utilizar `while` para repetir instrucciones.

También vimos que, si una condición nunca deja de cumplirse, el programa puede quedar atrapado en un **bucle infinito**.

Por ejemplo:

```c id="mdvq34"
#include <stdio.h>

int main(void)
{
    while (true)
    {
        printf("Hola\n");
    }
}
```

Este programa imprimirá el mensaje una y otra vez.

Nunca terminará por sí solo.

Entonces surge una nueva pregunta.

> **¿Cómo podemos detener un programa que no deja de ejecutarse?**

---

# ¿Qué es `Ctrl + C`?

`Ctrl + C` es una combinación de teclas que permite **interrumpir un programa que se está ejecutando en la terminal**.

Cuando la presionamos, enviamos una señal al programa para indicarle que debe finalizar.

Es importante aclarar que **no elimina el programa**, **no borra el código** y **no apaga la computadora**.

Simplemente detiene la ejecución.

---

# ¿Cuándo se utiliza?

La situación más común es cuando un programa entra en un bucle infinito.

Por ejemplo:

```c id="7ydpmt"
while (true)
{
    printf("Hola\n");
}
```

Como la condición siempre es verdadera, el programa nunca termina.

En ese momento podemos presionar:

```text id="1krh5t"
Ctrl + C
```

y la terminal recuperará el control.

---

# ¿Qué ocurre al presionarlo?

Imaginemos que el programa está ejecutándose.

```text id="z4s5ga"
Hola
Hola
Hola
Hola
Hola
Hola
Hola
Hola
...
```

Mientras el programa imprime mensajes, la terminal no acepta nuevos comandos porque el programa sigue en ejecución.

Cuando presionamos:

```text id="7hmvji"
Ctrl + C
```

el programa finaliza y vuelve a aparecer el cursor de la terminal.

```text id="6d7hyt"
$
```

Ahora podemos volver a escribir comandos como:

```text id="4m2af8"
ls
```

```text id="3vbvwy"
make
```

```text id="vpbqj0"
./programa
```

---

# ¿Siempre significa que hay un error?

No.

Muchas aplicaciones están diseñadas para ejecutarse de forma continua.

Por ejemplo:

- un servidor web;
- un programa que escucha conexiones de red;
- un reloj;
- un monitor del sistema.

En esos casos, es normal utilizar `Ctrl + C` para indicar que queremos finalizar la ejecución.

---

# Un consejo para quienes empiezan

Si ejecutás un programa y parece que no responde, no cierres la terminal inmediatamente.

Primero preguntate:

- ¿El programa está esperando que ingrese un dato?
- ¿Entró en un bucle infinito?
- ¿Simplemente sigue ejecutándose porque fue diseñado para hacerlo?

Muchas veces, la solución será tan sencilla como presionar:

```text id="4b5h0y"
Ctrl + C
```

---

# Resumen

`Ctrl + C` permite interrumpir un programa que se está ejecutando en la terminal.

Es especialmente útil cuando un programa entra en un bucle infinito o cuando queremos detener manualmente una aplicación.

No modifica el código ni elimina el programa; simplemente finaliza su ejecución.

---

# ¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

- ¿Qué hace `Ctrl + C`?
- ¿En qué situaciones resulta útil?
- ¿Qué ocurre cuando un programa entra en un bucle infinito?
- ¿`Ctrl + C` elimina el programa o solo detiene su ejecución?
- ¿Por qué la terminal vuelve a aceptar comandos después de usarlo?

---


Hasta ahora vimos un tipo de bucle que **revisa la condición antes de ejecutar el bloque**.

Pero existe otra situación muy común.

Imaginemos que queremos pedir una contraseña al usuario. Aunque la contraseña sea incorrecta, necesitamos preguntarla **al menos una vez**.

Entonces surge una nueva pregunta:

> **¿Existe un bucle que garantice que el bloque de código se ejecute al menos una vez antes de comprobar la condición?**

La respuesta la encontraremos en el siguiente capítulo: **`do...while`**. Allí conoceremos una variante de los bucles que primero ejecuta el código y recién después decide si debe repetirlo.

¡Excelente! Ahora seguimos con **`do...while`**.

Este capítulo suele generar confusión porque se parece mucho a `while`. La clave no es explicar la sintaxis primero, sino responder una pregunta muy simple:

> **¿Cuál es la diferencia con `while`?**

---

# Bucles: `do...while`

## ¿Qué problema resuelve?

En el capítulo anterior aprendimos que un `while` verifica la condición antes de ejecutar el bloque.

Por ejemplo:

```c
while (condición)
{
    instrucciones;
}
```

Si la condición es falsa desde el principio, el bloque nunca se ejecuta.

Pero imaginemos que queremos pedir una contraseña.

Aunque el usuario se equivoque, primero debemos darle la oportunidad de escribirla.

No tendría sentido comprobar si la contraseña es correcta antes de que el usuario la ingrese.

Entonces surge una nueva pregunta.

> **¿Existe un bucle que ejecute el código una vez antes de comprobar la condición?**

La respuesta es sí.

---

# ¿Qué es `do...while`?

`do...while` es un bucle que ejecuta el bloque de código **al menos una vez**.

Después de ejecutarlo, la computadora comprueba la condición.

Si la condición sigue siendo verdadera, repite el bloque.

Si es falsa, termina el bucle.

La diferencia con `while` está en el momento en que se evalúa la condición.

---

# La estructura

```c
do
{
    instrucciones;
}
while (condición);
```

Observá un detalle importante.

A diferencia de `while`, aquí aparece un punto y coma al final.

```c
while (condición);
```

Es parte de la sintaxis de `do...while`.

---

# ¿Cómo funciona?

La computadora realiza estos pasos.

1. Ejecuta el bloque.
2. Evalúa la condición.
3. Si la condición es verdadera, vuelve al principio.
4. Si es falsa, termina el bucle.

---

# Primer ejemplo

```c
#include <stdio.h>

int main(void)
{
    int contador = 1;

    do
    {
        printf("%i\n", contador);
        contador++;
    }
    while (contador <= 5);
}
```

¿Qué ocurre?

La computadora no pregunta primero.

Comienza ejecutando el bloque.

```text
1
```

Luego pregunta:

```text
¿2 <= 5?
```

Como la respuesta es verdadera, vuelve a ejecutar el bloque.

El proceso continúa hasta que:

```text
contador = 6
```

Entonces pregunta:

```text
¿6 <= 5?
```

Respuesta:

```text
false
```

Y el bucle termina.

---

# La diferencia con `while`

Supongamos este programa.

```c
int contador = 10;

while (contador <= 5)
{
    printf("Hola\n");
}
```

La condición es falsa desde el principio.

Resultado:

```text
(No imprime nada.)
```

Ahora observemos el mismo ejemplo con `do...while`.

```c
int contador = 10;

do
{
    printf("Hola\n");
}
while (contador <= 5);
```

Aunque la condición sea falsa, el programa imprimirá:

```text
Hola
```

¿Por qué?

Porque `do...while` ejecuta el bloque antes de comprobar la condición.

---

# ¿Cuándo conviene utilizarlo?

`do...while` es muy útil cuando una acción debe realizarse al menos una vez.

Por ejemplo:

- pedir una contraseña;
- solicitar un número válido;
- mostrar un menú de opciones;
- pedir una respuesta hasta que sea correcta.

En todos estos casos, primero necesitamos que el usuario interactúe con el programa y recién después podemos decidir si debemos repetir la acción.

---

# Un ejemplo cotidiano

Imaginemos una máquina expendedora.

No puede comprobar si una moneda es válida antes de que alguien la introduzca.

Primero recibe la moneda.

Después verifica si es correcta.

Si no lo es, vuelve a pedir otra.

Eso es exactamente lo que hace un `do...while`.

---

# Resumen

`do...while` es un bucle que ejecuta un bloque de código al menos una vez.

La condición se evalúa después de la primera ejecución.

Si la condición es verdadera, el bloque vuelve a ejecutarse.

Si es falsa, el bucle termina.

---

# ¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

- ¿Qué diferencia existe entre `while` y `do...while`?
- ¿Cuándo se evalúa la condición en cada uno?
- ¿Por qué `do...while` siempre ejecuta el bloque al menos una vez?
- ¿En qué situaciones resulta más conveniente utilizar `do...while`?
- ¿Qué detalle de sintaxis diferencia a `do...while` de `while`?

---


Hasta ahora escribimos programas donde **todo el código está dentro de `main()`**.

Esto funciona para programas pequeños.

Pero imaginemos que queremos calcular el promedio de varias listas de números.

Podríamos copiar el mismo código una y otra vez.

Sin embargo, eso haría que el programa fuera más largo y más difícil de mantener.

Entonces surge una nueva pregunta:

> **¿Existe una forma de escribir una tarea una sola vez y reutilizarla cada vez que la necesitemos?**

La respuesta la encontraremos en el siguiente capítulo: **Funciones**, una de las herramientas más poderosas para organizar y reutilizar código.

¡Excelente! Llegamos a uno de los capítulos más importantes de todo el libro. En mi opinión, **Funciones** marca el momento en que el lector deja de escribir programas "que funcionan" y empieza a escribir programas **bien organizados**.

No empezaría hablando de sintaxis. Empezaría hablando de un problema que todos conocemos: **repetir trabajo**.

---

# Funciones

## ¿Qué problema resuelven?

Hasta ahora, todo el código que escribimos estuvo dentro de una única función:

```c
int main(void)
{
    ...
}
```

Esto funciona perfectamente para programas pequeños.

Pero imaginemos que estamos desarrollando un programa para una escuela.

En varias partes del programa necesitamos mostrar el mismo mensaje de bienvenida.

Podríamos escribir:

```c
printf("Bienvenido al sistema.\n");
```

una vez.

Luego volver a escribirlo más abajo.

Y otra vez.

Y otra más.

El programa funcionará.

Pero si un día queremos cambiar el mensaje, tendremos que buscar todas las copias y modificarlas una por una.

Entonces surge una nueva pregunta.

> **¿Existe una forma de escribir una tarea una sola vez y reutilizarla todas las veces que sea necesario?**

La respuesta es sí.

---

# ¿Qué es una función?

Una **función** es un bloque de código que realiza una tarea específica.

En lugar de escribir el mismo código varias veces, lo escribimos una sola vez dentro de una función.

Después, cuando necesitamos realizar esa tarea nuevamente, simplemente llamamos a la función.

Podemos imaginar una función como una máquina.

```text
        Datos (opcional)
              │
              ▼
      ┌────────────────┐
      │    Función     │
      └────────────────┘
              │
              ▼
        Resultado (opcional)
```

Cada vez que utilizamos la máquina, realiza exactamente la misma tarea.

---

# Ya usamos funciones sin darnos cuenta

Aunque todavía no las habíamos estudiado, ya utilizamos varias funciones.

Por ejemplo:

```c
printf("Hola\n");
```

`printf()` es una función.

También lo son:

```c
get_int();
```

```c
get_string();
```

```c
get_float();
```

Hasta ahora simplemente las utilizábamos.

Ahora aprenderemos a crear nuestras propias funciones.

---

# Nuestra primera función

Supongamos que queremos mostrar siempre el mismo mensaje.

Podemos escribir:

```c
#include <stdio.h>

void saludar(void)
{
    printf("¡Bienvenido!\n");
}

int main(void)
{
    saludar();
}
```

¿Qué ocurre?

Cuando la computadora encuentra:

```c
saludar();
```

busca la función llamada `saludar` y ejecuta todas las instrucciones que contiene.

Después vuelve exactamente al lugar desde donde fue llamada y continúa con el resto del programa.

---

# ¿Qué significa `void`?

Observemos la primera línea.

```c
void saludar(void)
```

Aquí aparecen dos veces la palabra `void`.

Pero no significan exactamente lo mismo.

El primer `void` indica que la función **no devuelve ningún valor**.

El segundo `void` indica que la función **no recibe ningún dato**.

Por ahora alcanza con recordar que esta función simplemente realiza una tarea y termina.

Más adelante veremos funciones que reciben información y funciones que devuelven resultados.

---

# ¿Podemos llamar una función varias veces?

Sí.

Ese es justamente uno de sus mayores beneficios.

```c
int main(void)
{
    saludar();
    saludar();
    saludar();
}
```

La salida será:

```text
¡Bienvenido!
¡Bienvenido!
¡Bienvenido!
```

El código de la función fue escrito una sola vez.

Sin embargo, pudo utilizarse todas las veces que fue necesario.

---

# ¿Por qué son importantes?

Las funciones permiten:

- evitar repetir código;
- organizar mejor un programa;
- facilitar la lectura;
- corregir errores en un único lugar;
- reutilizar tareas siempre que las necesitemos.

A medida que los programas crecen, las funciones dejan de ser una comodidad y se convierten en una necesidad.

---

# Resumen

Una función es un bloque de código que realiza una tarea específica.

Podemos llamarla todas las veces que queramos sin necesidad de volver a escribir las mismas instrucciones.

Gracias a las funciones, los programas son más ordenados, más fáciles de leer y más sencillos de mantener.

---

# ¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

- ¿Qué es una función?
- ¿Qué problema resuelven las funciones?
- ¿Qué funciones utilizamos antes de crear las nuestras?
- ¿Qué ocurre cuando llamamos a una función?
- ¿Por qué las funciones ayudan a organizar un programa?

---


Ya sabemos crear una función y llamarla.

Pero todavía existe una limitación.

Nuestra función `saludar()` siempre muestra el mismo mensaje.

¿Y si queremos que salude a distintas personas?

Por ejemplo:

- "Hola, Mailen".
- "Hola, Juan".
- "Hola, Ana".

¿Tendremos que crear una función distinta para cada caso?

La respuesta es no.

Entonces surge una nueva pregunta:

> **¿Cómo puede una función recibir información para trabajar con datos diferentes cada vez que la llamamos?**

Para responderla conoceremos el concepto de **parámetros**, y junto con él comprenderemos uno de los temas más importantes de la programación: el **scope (alcance de las variables)**. Ese capítulo mostrará por qué algunas variables existen solo dentro de una función y por qué no pueden utilizarse desde cualquier parte del programa.

¡Excelente! Ahora llegamos a un capítulo que suele generar muchas dudas al principio, pero que, si se entiende bien desde el comienzo, hace mucho más fácil comprender programas grandes.

Yo lo llamaría simplemente **Scope (alcance de las variables)**, porque es el término que vas a encontrar en libros, documentación y cursos.

---

# Scope (alcance de las variables)

## ¿Qué problema resuelve?

En el capítulo anterior aprendimos a crear nuestras propias funciones.

Por ejemplo:

```c
void saludar(void)
{
    printf("¡Hola!\n");
}
```

También vimos que un programa puede tener varias funciones.

Pero imaginemos la siguiente situación.

Creamos una variable dentro de una función.

```c
void saludar(void)
{
    int edad = 20;
}
```

Luego intentamos utilizar esa misma variable desde `main()`.

```c
int main(void)
{
    printf("%i\n", edad);
}
```

¿Funcionará?

La respuesta es **no**.

Entonces surge una nueva pregunta.

> **¿Por qué una variable puede utilizarse en un lugar del programa, pero no en otro?**

---

# ¿Qué es el scope?

El **scope** (o **alcance**) es la parte del programa donde una variable existe y puede utilizarse.

Podemos imaginarlo como una habitación.

```text
┌──────────────────────────────┐
│ Función saludar()            │
│                              │
│   int edad = 20;             │
│                              │
└──────────────────────────────┘
```

La variable `edad` vive dentro de esa habitación.

Fuera de ella, la variable deja de existir.

---

# Variables locales

Las variables creadas dentro de una función se llaman **variables locales**.

Por ejemplo:

```c
void saludar(void)
{
    int edad = 20;

    printf("%i\n", edad);
}
```

Aquí la variable `edad` puede utilizarse sin problemas porque estamos dentro de la misma función donde fue creada.

---

# ¿Qué ocurre fuera de la función?

Observemos este ejemplo.

```c
#include <stdio.h>

void saludar(void)
{
    int edad = 20;
}

int main(void)
{
    printf("%i\n", edad);
}
```

La computadora mostrará un error.

¿Por qué?

Porque la variable `edad` solo existe dentro de `saludar()`.

Cuando `main()` intenta utilizarla, esa variable ya no está disponible.

---

# Cada función tiene sus propias variables

Supongamos el siguiente programa.

```c
#include <stdio.h>

void saludar(void)
{
    int numero = 10;

    printf("%i\n", numero);
}

int main(void)
{
    int numero = 20;

    printf("%i\n", numero);
}
```

Aunque ambas variables se llamen `numero`, no son la misma.

Cada función tiene su propio espacio.

La variable creada en `saludar()` no afecta a la variable creada en `main()`.

---

# Una analogía

Imaginemos dos aulas de una escuela.

En cada una hay un alumno llamado Juan.

```text
Aula A
Juan

Aula B
Juan
```

Aunque tengan el mismo nombre, son personas distintas porque están en aulas diferentes.

Con las variables ocurre lo mismo.

Pueden llamarse igual si pertenecen a scopes diferentes.

---

# ¿Por qué existe el scope?

El scope ayuda a mantener el programa organizado.

Cada función trabaja con sus propias variables y evita modificar accidentalmente información que pertenece a otra parte del programa.

Gracias a esto, los programas son más seguros y más fáciles de entender.

---

# Un vistazo a las variables globales

Hasta ahora todas nuestras variables fueron locales.

Existe otro tipo de variable que puede utilizarse desde varias funciones: las **variables globales**.

Por ejemplo:

```c
#include <stdio.h>

int contador = 0;

void aumentar(void)
{
    contador++;
}

int main(void)
{
    aumentar();
    printf("%i\n", contador);
}
```

En este caso, `contador` fue declarada fuera de cualquier función.

Por eso puede utilizarse tanto en `aumentar()` como en `main()`.

Sin embargo, las variables globales deben utilizarse con cuidado.

Si muchas funciones pueden modificar la misma variable, el programa puede volverse más difícil de entender y mantener.

Por eso, en la mayoría de los casos, es preferible trabajar con variables locales.

---

# Resumen

El **scope** define dónde una variable existe y puede utilizarse.

Las variables creadas dentro de una función son **locales** y solo pueden usarse dentro de esa función.

Las variables declaradas fuera de todas las funciones son **globales** y pueden compartirse entre distintas partes del programa.

Comprender el scope ayuda a escribir programas más organizados y a evitar errores.

---

# ¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas:

- ¿Qué es el scope?
- ¿Qué diferencia existe entre una variable local y una global?
- ¿Por qué una variable creada en una función no puede utilizarse desde otra?
- ¿Pueden existir dos variables con el mismo nombre?
- ¿Por qué conviene utilizar variables locales siempre que sea posible?

---


Ya sabemos que un programa puede tener varias funciones y que cada una trabaja con sus propias variables.

Pero todavía queda una pregunta importante.

Hasta ahora siempre escribimos nuestras funciones antes de `main()`.

¿Qué ocurre si queremos escribirlas después?

¿Cómo sabe la computadora que esa función existe?

Para resolver este problema conoceremos el último concepto de esta parte del libro: **los prototipos de funciones**. Después de ese capítulo, el lector tendrá todas las herramientas necesarias para empezar a construir programas mucho más grandes y organizados.

¡Excelente! 🎉 Llegamos al último capítulo de la primera parte del libro. Después de este, el lector ya tendrá una base muy sólida para comenzar con temas más avanzados, como arreglos, memoria, archivos, estructuras de datos, etc.

Como en los capítulos anteriores, empezaría por el problema y no por la sintaxis.

---

# Prototipos de funciones

## ¿Qué problema resuelven?

En el capítulo anterior aprendimos a crear nuestras propias funciones.

Por ejemplo:

```c
#include <stdio.h>

void saludar(void)
{
    printf("¡Hola!\n");
}

int main(void)
{
    saludar();
}
```

Este programa funciona correctamente.

Pero observemos un detalle.

La función `saludar()` aparece **antes** de `main()`.

¿Es obligatorio escribir las funciones en ese orden?

La respuesta es **no**.

Entonces surge una nueva pregunta.

> **¿Cómo puede la computadora ejecutar una función si todavía no la ha leído?**

---

# El problema

Imaginemos que escribimos el programa de esta manera.

```c
#include <stdio.h>

int main(void)
{
    saludar();
}

void saludar(void)
{
    printf("¡Hola!\n");
}
```

Cuando la computadora comienza a leer el programa encuentra:

```c
saludar();
```

Pero todavía no sabe qué es `saludar()`.

Todavía no llegó a esa parte del código.

Como consecuencia, el compilador mostrará un error.

---

# ¿Qué es un prototipo?

Un **prototipo** es una declaración que le informa al compilador que una función existe, aunque su implementación aparezca más adelante.

Podemos imaginarlo como el índice de un libro.

El índice nos dice que existe un capítulo llamado:

```text
Capítulo 5
```

Aunque todavía no lo hayamos leído.

Con los prototipos ocurre exactamente lo mismo.

Le dicen al compilador:

> "Más adelante encontrarás una función con este nombre."

---

# La estructura de un prototipo

Un prototipo tiene casi la misma forma que una función.

Por ejemplo:

```c
void saludar(void);
```

Observá el detalle.

Termina con un punto y coma.

No tiene llaves.

No contiene instrucciones.

Solo informa que esa función existe.

---

# Un ejemplo completo

```c
#include <stdio.h>

void saludar(void);

int main(void)
{
    saludar();
}

void saludar(void)
{
    printf("¡Hola!\n");
}
```

Ahora el compilador trabaja de esta manera.

1. Lee el prototipo.
2. Aprende que existe una función llamada `saludar()`.
3. Continúa leyendo el programa.
4. Cuando encuentra la implementación de la función, ya sabe exactamente de cuál se trata.

---

# ¿Por qué son útiles?

Los programas pequeños pueden escribirse sin demasiados problemas.

Pero imaginemos un proyecto con cientos o miles de líneas de código.

Muchas veces queremos que `main()` aparezca primero porque allí comienza el programa.

Las funciones auxiliares pueden escribirse después.

Los prototipos hacen posible esa organización.

---

# ¿Qué información contiene un prototipo?

Un prototipo indica tres cosas.

- El tipo de dato que devuelve la función.
- El nombre de la función.
- Los datos que recibe (si los hay).

Por ejemplo:

```c
int sumar(int a, int b);
```

Este prototipo nos dice que:

- la función se llama `sumar`;
- recibe dos números enteros;
- devuelve un número entero.

Todavía no sabemos cómo suma.

Solo sabemos que esa función existe.

---

# Una analogía

Imaginemos una película.

Al comienzo aparecen los nombres de los actores.

```text
Protagonistas

Ana Pérez
Juan Gómez
Laura Ruiz
```

Todavía no vimos actuar a ninguno.

Simplemente sabemos que participarán en la película.

Los prototipos cumplen exactamente esa función.

Presentan las funciones antes de que aparezcan.

---

# Resumen

Un prototipo es una declaración que informa al compilador que una función existe.

Gracias a los prototipos podemos escribir las funciones en el orden que resulte más conveniente, sin que el compilador pierda información.

---

# ¿Qué deberías haber entendido?

Al finalizar este capítulo deberías poder responder las siguientes preguntas?

- ¿Qué problema resuelven los prototipos?
- ¿Qué diferencia existe entre un prototipo y una función completa?
- ¿Por qué un prototipo termina con punto y coma?
- ¿Qué información proporciona un prototipo?
- ¿Por qué son útiles en programas grandes?

---

# Fin de la primera parte

¡Felicitaciones!

Si llegaste hasta aquí, ya dominás los fundamentos de la programación en C. A lo largo de esta primera parte aprendiste a comunicarte con la computadora, almacenar información, tomar decisiones, repetir tareas y organizar programas mediante funciones.

Todavía queda muchísimo por descubrir, pero ya contás con las herramientas necesarias para entender cómo piensa un programa y cómo transformar un problema en una secuencia de instrucciones.

A partir del próximo capítulo comenzaremos a explorar conceptos más avanzados, como la organización de datos en memoria, los arreglos y otras estructuras fundamentales que te permitirán construir programas cada vez más complejos.

---

# Lo que ya sabés hacer

Llegaste al final de la primera parte del libro. Puede que todavía no te sientas un programador experto, y eso es completamente normal. Sin embargo, ya adquiriste una base muy sólida: aprendiste cómo piensa una computadora y cómo darle instrucciones utilizando el lenguaje C.

Hasta este punto ya no escribís programas copiando código sin entenderlo. Ahora conocés las herramientas fundamentales que aparecen en prácticamente cualquier lenguaje de programación.

Todo lo que viene a continuación se construirá sobre estos conceptos.

---

## Resumen de la primera parte

| Tema | ¿Qué aprendiste? | Ejemplo |
|------|-------------------|---------|
| **Terminal** | Crear carpetas, navegar por el sistema y compilar programas. | `mkdir`, `cd`, `ls`, `make`, `./programa` |
| **Primer programa** | Crear un programa en C y ejecutarlo. | `printf("Hola");` |
| **Tipos de datos** | Elegir el tipo de dato adecuado para almacenar información. | `int`, `float`, `double`, `char`, `string`, `bool`, `void` |
| **Overflow** | Comprender que los tipos de datos tienen límites de almacenamiento. | `int` no puede representar números infinitamente grandes. |
| **Precisión de los flotantes** | Entender que algunos números decimales no pueden representarse exactamente. | `0.1 + 0.2` puede no dar exactamente `0.3`. |
| **Variables** | Guardar información en memoria para utilizarla más adelante. | `int edad = 20;` |
| **Constantes** | Crear valores que no deben modificarse durante la ejecución. | `const int DIAS = 7;` |
| **Operadores aritméticos** | Realizar cálculos matemáticos. | `+`, `-`, `*`, `/`, `%` |
| **Asignación** | Guardar un valor dentro de una variable. | `x = 5;` |
| **Asignación abreviada** | Actualizar variables de forma más sencilla. | `x += 3;` |
| **Incremento y decremento** | Aumentar o disminuir una variable en una unidad. | `x++;`, `x--;` |
| **Comparación** | Comparar valores. | `==`, `!=`, `<`, `>`, `<=`, `>=` |
| **Operadores lógicos** | Combinar varias condiciones. | `&&`, `||`, `!` |
| **Format codes** | Mostrar correctamente distintos tipos de datos con `printf()`. | `%i`, `%f`, `%c`, `%s` |
| **Condicionales** | Ejecutar diferentes bloques según una condición. | `if`, `else if`, `else` |
| **While** | Repetir instrucciones mientras una condición sea verdadera. | `while (x < 10)` |
| **Ctrl + C** | Interrumpir un programa que continúa ejecutándose. | Bucle infinito. |
| **Do...while** | Ejecutar un bloque al menos una vez antes de comprobar la condición. | `do { } while (...);` |
| **Funciones** | Agrupar instrucciones para reutilizar código. | `void saludar(void)` |
| **Scope** | Comprender dónde existe una variable y dónde puede utilizarse. | Variables locales y globales. |
| **Prototipos** | Declarar funciones antes de implementarlas para organizar mejor el código. | `void saludar(void);` |

---

# En este momento ya sos capaz de...

✅ Crear un programa desde cero.

✅ Compilarlo y ejecutarlo desde la terminal.

✅ Declarar variables de distintos tipos.

✅ Guardar y modificar información.

✅ Realizar operaciones matemáticas.

✅ Comparar valores y combinar condiciones.

✅ Tomar decisiones con `if`.

✅ Repetir tareas utilizando bucles.

✅ Detener programas cuando sea necesario.

✅ Dividir un programa en funciones reutilizables.

✅ Comprender el alcance de las variables.

✅ Organizar programas utilizando prototipos.

---
