# Pila LEMP de 3/4 Capas - Miguel Cordero González

# Índice

1. [Introducción](#introducción)
2. [Programación Python](#Programación-Python)
    * [Código 1](#Descripción-de-lo-que-hace-el-algoritmo-1)
    * [Código 2](#Descripción-de-lo-que-hace-el-algoritmo-2)
    * [Código 3](#Descripción-de-lo-que-hace-el-algoritmo-3)


Introducción

# Programación Python

### Descripción de lo que hace el algoritmo 1

El programa solicitara tres números al usuario, determina cuál es el mayor de ellos y luego pregunta si el usuario desea finalizar el proceso. Este bucle se repite hasta que el usuario ingresa 0 para finalizar el programa.

Código1

![](FOTOS/)

### Descripción de lo que hace el algoritmo 2

El programa solicitara al usuario si desea ejecutarse, y si la respuesta es "s", solicita 10 números al usuario, determina si cada número es par o impar, y finalmente imprime un mensaje indicando si el número fue seleccionado o no, junto con el resto de la división por 2.

Código2

![](FOTOS/)

### Descripción de lo que hace el algoritmo 3

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
predefinidas. Al inicio se creará el conjunto con el nombre de las diez ciudades. Posteriormente se pedirá el nombre de una ciudad al usuario. El programa indicará si la ciudad se encuentra en el conjunto o no. Deberá dar por válidas entradas en minúsculas, mayúsculas. Por ejemplo, Si tenemos almacenada “Mérida”, se dará por válido “mérida”, “Mérida”, “MÉRIDA”, “MériDa”, etc.

```
Proceso BuscarCiudad
    // Definir el conjunto de diez ciudades predefinidas
    Definir ciudades[10] Como Caracter
    ciudades[1] = "Mérida"
    ciudades[2] = "Barcelona"
    ciudades[3] = "Madrid"
    ciudades[4] = "Londres"
    ciudades[5] = "París"
    ciudades[6] = "Nueva York"
    ciudades[7] = "Roma"
    ciudades[8] = "Sídney"
    ciudades[9] = "Tokio"
    ciudades[10] = "Berlín"

    // Solicitar al usuario que ingrese el nombre de una ciudad
    Escribir "Ingrese el nombre de una ciudad: "
    Leer ciudad_ingresada

    // Convertir la ciudad ingresada a minúsculas para hacer la comparación
    ciudad_ingresada = ConvertirAMinúsculas(ciudad_ingresada)

    // Buscar la ciudad en el conjunto
    Encontrada = Falso
    Para i = 1 Hasta 10 Hacer
        // Convertir la ciudad actual a minúsculas para la comparación
        ciudad_actual = ConvertirAMinúsculas(ciudades[i])

        Si ciudad_actual = ciudad_ingresada Entonces
            Encontrada = Verdadero
            Romper // Salir del bucle si la ciudad se encuentra
        Fin Si
    Fin Para

    // Mostrar el resultado
    Si Encontrada Entonces
        Escribir "La ciudad se encuentra en el conjunto."
    Sino
        Escribir "La ciudad no se encuentra en el conjunto."
    Fin Si
Fin Proceso

Proceso ConvertirAMinúsculas(caracter)
    // Función auxiliar para convertir un string a minúsculas
    // Puedes utilizar funciones proporcionadas por el lenguaje de programación específico
    // o implementar tu propia lógica para convertir a minúsculas.
    // La implementación específica dependerá del lenguaje que estés utilizando.
Fin Proceso
```

Enunciado 4
Desarrolla un programa que pida al usuario un número del 1 al 50 y que muestre la representación de dicho número en binario, octal y hexadecimal.

```
Proceso MostrarRepresentaciones
    // Definir variables
    Definir numero, binario, octal, hexadecimal Como Entero

    // Solicitar al usuario un número del 1 al 50
    Mientras Verdadero
        Escribir "Ingrese un número del 1 al 50: "
        Leer numero

        Si numero >= 1 y numero <= 50 Entonces
            Salir del Mientras
        Fin Si

        Escribir "El número debe estar en el rango del 1 al 50. Intente nuevamente."
    Fin Mientras

    // Calcular representaciones binaria, octal y hexadecimal
    binario <- ConvertirABinario(numero)
    octal <- ConvertirAOctal(numero)
    hexadecimal <- ConvertirAHexadecimal(numero)

    // Mostrar resultados
    Escribir "Representación binaria: ", binario
    Escribir "Representación octal: ", octal
    Escribir "Representación hexadecimal: ", hexadecimal

Fin Proceso

Proceso ConvertirABinario(numero)
    // Función para convertir a representación binaria
    Cadena binario
    binario <- ""
    
    Mientras numero > 0 Hacer
        binario <- (numero MOD 2) Concatenar binario
        numero <- numero / 2
    Fin Mientras
    
    Devolver binario
Fin Proceso

Proceso ConvertirAOctal(numero)
    // Función para convertir a representación octal
    Cadena octal
    octal <- ""
    
    Mientras numero > 0 Hacer
        octal <- (numero MOD 8) Concatenar octal
        numero <- numero / 8
    Fin Mientras
    
    Devolver octal
Fin Proceso

Proceso ConvertirAHexadecimal(numero)
    // Función para convertir a representación hexadecimal
    Cadena hexadecimal
    hexadecimal <- ""
    
    Mientras numero > 0 Hacer
        Resto <- numero MOD 16
        Si Resto < 10 Entonces
            hexadecimal <- Resto Concatenar hexadecimal
        Sino
            hexadecimal <- ConvertirAHexadecimalLetra(Resto) Concatenar hexadecimal
        Fin Si
        numero <- numero / 16
    Fin Mientras
    
    Devolver hexadecimal
Fin Proceso

Proceso ConvertirAHexadecimalLetra(valor)
    // Función auxiliar para convertir a letra en representación hexadecimal
    Caracter letrasHexadecimales[6]
    letrasHexadecimales[10] <- "A"
    letrasHexadecimales[11] <- "B"
    letrasHexadecimales[12] <- "C"
    letrasHexadecimales[13] <- "D"
    letrasHexadecimales[14] <- "E"
    letrasHexadecimales[15] <- "F"

    Devolver letrasHexadecimales[valor]
Fin Proceso

// Llamar al proceso para ejecutar el programa
MostrarRepresentaciones()
```

Enunciado 5
Implementa un programa que pida al usuario una cantidad de dinero hasta que dicha cantidad sea
múltiplo de 5 y, como máximo 3000. Una vez que se cumplan estas condiciones se tiene que
mostrar al usuario el número de billetes de 100, 50, 20, 10 y 5 que se necesitan para obtener la cantidad de dinero indicada.

```
Proceso DesgloseBilletes
    // Definir variables
    Definir cantidad, billetes_100, billetes_50, billetes_20, billetes_10, billetes_5 Como Entero

    // Solicitar al usuario una cantidad de dinero
    Mientras Verdadero
        Escribir "Ingrese una cantidad de dinero (máximo 3000, múltiplo de 5): "
        Leer cantidad

        Si cantidad > 0 y cantidad <= 3000 y (cantidad MOD 5 = 0) Entonces
            Salir del Mientras // Salir del bucle si la cantidad es válida
        Fin Si

        Escribir "La cantidad debe ser un múltiplo de 5 y no puede superar los 3000."
    Fin Mientras

    // Inicializar variables para contar billetes
    billetes_100 <- 0
    billetes_50 <- 0
    billetes_20 <- 0
    billetes_10 <- 0
    billetes_5 <- 0

    // Desglose de billetes
    Mientras cantidad >= 100 Hacer
        billetes_100 <- billetes_100 + 1
        cantidad <- cantidad - 100
    Fin Mientras

    Mientras cantidad >= 50 Hacer
        billetes_50 <- billetes_50 + 1
        cantidad <- cantidad - 50
    Fin Mientras

    Mientras cantidad >= 20 Hacer
        billetes_20 <- billetes_20 + 1
        cantidad <- cantidad - 20
    Fin Mientras

    Mientras cantidad >= 10 Hacer
        billetes_10 <- billetes_10 + 1
        cantidad <- cantidad - 10
    Fin Mientras

    Mientras cantidad >= 5 Hacer
        billetes_5 <- billetes_5 + 1
        cantidad <- cantidad - 5
    Fin Mientras

    // Mostrar resultados
    Escribir "Billetes de 100:", billetes_100
    Escribir "Billetes de 50:", billetes_50
    Escribir "Billetes de 20:", billetes_20
    Escribir "Billetes de 10:", billetes_10
    Escribir "Billetes de 5:", billetes_5
Fin Proceso

// Llamar al proceso para ejecutar el programa
DesgloseBilletes()
```
