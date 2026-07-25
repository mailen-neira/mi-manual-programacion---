# mi-manual-programacion---
# 📖 De Cero a IA

## Mi Manual de Programación

Este repositorio documenta todo lo que voy aprendiendo durante mi camino desde cero en programación hasta especializarme en IA.

Semana 0 - Pensamiento Computacional
¿Qué es el pensamiento computacional?

Antes de aprender un lenguaje de programación, hay que aprender a pensar como una computadora.

La computadora no "adivina" lo que queremos hacer. Necesita que el problema esté definido de manera clara y ordenada.

Programar consiste, primero, en aprender a resolver problemas paso a paso.

TODO PROGRAMA REQUIERE 3 PASOS

INPUT
   ↓
PROCESO
   ↓
OUTPUT

Input: los datos que ingresan al programa.
Proceso: las instrucciones que transforman esos datos.
Output: el resultado que obtiene el usuario.

Ejemplo

Quiero saber cuál es el doble de un número.

INPUT
Número: 5

↓

PROCESO
Multiplicar por 2

↓

OUTPUT
10

Como calcular la edad de una persona?

INPUT
Año de nacimiento

↓

PROCESO
Año actual - Año de nacimiento

↓

OUTPUT
Edad

COMO ENTIENDE LA COMPUTADORA LA INFORMACION?

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

DEL ALGORITMO AL CODIGO

Primero pensamos la solución.
Después la escribimos

Problema

↓

Algoritmo

↓

Pseudocódigo

↓

Código

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

#include <stdio.h>

int main(void)
{
    printf("Hello, world!\n");
}

Si observamos este programa por primera vez, probablemente veamos un conjunto de palabras y símbolos difíciles de entender.
Sin embargo, un programa no es una sola pieza.
Está formado por distintos elementos que cumplen funciones específicas.
Comprender cada uno de ellos nos permitirá entender cómo funciona cualquier programa, sin importar el lenguaje en el que esté escrito.

1. FUNCIONES
Una función es un bloque de código diseñado para realizar una tarea específica.
Podemos pensar en una función como un verbo.

Ejemplos:

printf() → mostrar información.
scanf() → leer información.
sqrt() → calcular una raíz cuadrada.

En el programa anterior:

printf("Hello, world!");

printf() es una función.

Dónde lo veo en un programa?
En la instrucción:

printf("Hello, world!");

printf() es una función. Su trabajo es mostrar información en la pantalla.

2. PARAMETROS (Argumentos)
Las funciones muchas veces necesitan información para poder trabajar.
Esa información se llama parámetro o argumento.

Ejemplo:

printf("Hello, world!");

El parametro es: 

"Hello, world!"

Si canbiamos el parametro:

printf("Hola Mailen");

La funcion sigue siendo la misma. 
Lo unico que cambia es la informacion que recibe.
Una función puede comportarse de distintas maneras según los parámetros que reciba.

¿Dónde lo veo en un programa?
En la misma instrucción:

printf("Hello, world!");

"Hello, world!" es el parámetro que recibe la función. Es la información que utilizará para realizar su tarea.

3. SIDE EFFECT (efecto secundario)
Al ejecutar una función pueden ocurrir cambios visibles.
Eso se conoce como efecto secundario.

Ejemplo:

printf("Hola");

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

printf("Hello, world!");

aparece el texto en la pantalla.
Ese cambio visible es el efecto secundario de ejecutar la función

4. RETURN VALUE (valor retorno)
No todas las funciones solo realizan acciones.
Muchas también devuelven un resultado.
Ese resultado se llama valor de retorno.

Por ejemplo:

sqrt(25)

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

5. EXPRESIONES BOOLEANAS 

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

6. CONDICIONALES
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

7. LOOPS (bucles)
En lugar de escribir la misma instrucción muchas veces, utilizamos un bucle.

Ejemplo:

Repetir 10 veces

↓

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


CURSO DE REFERENCIA 

Este manual está basado en mi recorrido de aprendizaje a través del curso CS50x: Introduction to Computer Science, desarrollado por la Universidad de Harvard y dictado por el profesor David J. Malan.

CS50 es un curso introductorio de Ciencias de la Computación que enseña los fundamentos de la programación y del pensamiento computacional. A lo largo del curso se trabajan conceptos fundamentales utilizando diferentes lenguajes y herramientas, entre ellos Scratch, C, Python, SQL, HTML, CSS y JavaScript.

El objetivo de este manual no es reemplazar el contenido del curso, sino documentar mi proceso de aprendizaje con mis propias palabras, complementándolo con ejemplos, explicaciones y notas personales que me ayuden a comprender mejor cada tema.

🔗 Curso oficial de CS50: https://cs50.harvard.edu/x/


CS50x – Semana 1
Introducción al lenguaje C

¿Qué es un lenguaje de programación?
Un lenguaje de programación es un idioma que utilizamos para comunicarnos con la computadora.
Nos permite escribir instrucciones que la computadora ejecutará para realizar una determinada tarea.
En la Semana 1 comenzamos a trabajar con C, uno de los lenguajes de programación más importantes e influyentes de la historia.

Código fuente (Source Code)

El código que escribimos los programadores se llama código fuente.
Está pensado para que los humanos podamos leerlo, escribirlo y entenderlo.

Ejemplo:

printf("¡Hermosa mañana, ¿verdad?\n");

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

Proceso completo

Programador
      ↓
Escribe código fuente (C)
      ↓
Compilador
      ↓
Traduce a código máquina (0 y 1)
      ↓
Genera un programa ejecutable
      ↓
Computadora ejecuta el programa

En CS50 normalmente utilizaremos:
make hello
Este comando compila el programa.
Luego:
./hello
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
make hello
./hello

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

#include <stdio.h>

int main(void)
{
    printf("¡Hermosa mañana, ¿verdad?\n");
}

El funcionamiento es exactamente el mismo.
Simplemente cambiamos el texto que se imprime.

Analizando el programa

#include <stdio.h>

Incluye la biblioteca estándar de entrada y salida.
Gracias a ella podemos utilizar funciones como:
printf()

int main(void)

Es la función principal del programa.
Todo programa en C comienza ejecutándose aquí.

printf()

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
printf("¡Hermosa mañana, ¿verdad?\n");
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

#include <stdio.h>

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

string nombre = get_string("¿Cómo te llamás? ");

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

Comparación con Scratch
En Scratch hacíamos:

Preguntar

↓

Esperar respuesta

↓

Unir "Hola"

↓

Mostrar

En C hacemos exactamente lo mismo escribiendo:

string answer = get_string("Como te llamas? ");

printf("Hola, %s\n", answer);
