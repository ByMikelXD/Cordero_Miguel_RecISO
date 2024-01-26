# Pila LEMP de 3/4 Capas - Miguel Cordero González

# Índice

1. [Introducción](#introducción)
2. [Programación Python](#Programación-Python)
    * [Código 1](#Código1)
    * [Servidor NFS](#nfs-server)
    * [Servidores WEB](#servidores-web1-y-web2)
    * [Servidor BBDD](#ddbb)

Introducción

# Programación Python
Descripción de lo que hace el algoritmo 1

El programa solicitara tres números al usuario, determina cuál es el mayor de ellos y luego pregunta si el usuario desea finalizar el proceso. Este bucle se repite hasta que el usuario ingresa 0 para finalizar el programa.

## Código1

![](FOTOS/)

Descripción de lo que hace el algoritmo 2

El programa solicitara al usuario si desea ejecutarse, y si la respuesta es "s", solicita 10 números al usuario, determina si cada número es par o impar, y finalmente imprime un mensaje indicando si el número fue seleccionado o no, junto con el resto de la división por 2.

Código2

![](FOTOS/)

Descripción de lo que hace el algoritmo 3

El programa solicitara al usuario que ingrese un número y luego imprime la tabla de multiplicar correspondiente a ese número hasta el 10. El proceso se repite hasta que el usuario ingresa 0.

Código3

![](FOTOS/)

# Desarrollo de algoritmos en Python

Enunciado 1
Desarrolla un algoritmo que pida al usuario las calificaciones de 5 módulos de un alumno.
El algoritmo mostrará en pantalla la calificación mayor, la calificación menor, y la media de
las calificaciones.

```
Proceso CalificacionesAlumno
    // Definir variables
    Definir calificacion, suma, maxima, minima Como Real
    suma = 0

    // Inicializar valores de máxima y mínima con valores extremos
    maxima = -1
    minima = 101

    // Solicitar calificaciones al usuario
    Para i = 1 Hasta 5 Hacer
        Escribir "Ingrese la calificación del módulo ", i, ": "
        Leer calificacion

        // Validar que la calificación esté en el rango [0, 100]
        Mientras calificacion < 0 o calificacion > 100 Hacer
            Escribir "La calificación debe estar en el rango de 0 a 100. Intente nuevamente: "
            Leer calificacion
        Fin Mientras

        // Actualizar suma
        suma = suma + calificacion

        // Actualizar máxima y mínima
        Si calificacion > maxima Entonces
            maxima = calificacion
        Fin Si

        Si calificacion < minima Entonces
            minima = calificacion
        Fin Si
    Fin Para

    // Calcular media
    media = suma / 5

    // Mostrar resultados
    Escribir "La calificación mayor es: ", maxima
    Escribir "La calificación menor es: ", minima
    Escribir "La media de las calificaciones es: ", media
Fin Proceso
```

Enunciado 2
Escribe un algoritmo que, dado un número introducido por el usuario, indique si el número
es capicua o no.

```
Proceso VerificarCapicua
    // Definir variables
    Definir numero, original, invertido Como Entero
    Definir esCapicua Como Booleano

    // Solicitar al usuario que ingrese un número
    Escribir "Ingrese un número: "
    Leer numero

    // Almacenar el número original antes de invertirlo
    original = numero

    // Inicializar el número invertido
    invertido = 0

    // Invertir el número
    Mientras numero > 0 Hacer
        invertido = invertido * 10 + (numero MOD 10)
        numero = numero / 10
    Fin Mientras

    // Verificar si el número original es igual al invertido
    Si original = invertido Entonces
        esCapicua = Verdadero
    Sino
        esCapicua = Falso
    Fin Si

    // Mostrar el resultado
    Si esCapicua Entonces
        Escribir "El número ingresado es capicúa."
    Sino
        Escribir "El número ingresado no es capicúa."
    Fin Si
Fin Proceso
```

Enunciado 3
Implementa un algoritmo que busque el nombre de una ciudad entre un conjunto de diez ciudades
predefinidas. Al inicio se creará el conjunto con el nombre de las diez ciudades. Posteriormente se
pedirá el nombre de una ciudad al usuario. El programa indicará si la ciudad se encuentra en el
conjunto o no. Deberá dar por válidas entradas en minúsculas, mayúsculas. Por ejemplo, Si
tenemos almacenada “Mérida”, se dará por válido “mérida”, “Mérida”, “MÉRIDA”, “MériDa”,
etc.

Enunciado 4
Desarrolla un programa que pida al usuario un número del 1 al 50 y que muestre la representación
de dicho número en binario, octal y hexadecimal.

Enunciado 5
Implementa un programa que pida al usuario una cantidad de dinero hasta que dicha cantidad sea
múltiplo de 5 y, como máximo 3000. Una vez que se cumplan estas condiciones se tiene que
mostrar al usuario el número de billetes de 100, 50, 20, 10 y 5 que se necesitan para obtener la
cantidad de dinero indicada.
