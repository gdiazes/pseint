# Módulo 4 - Ejercicio 6 (Dificultad 6)

## Enunciado
Escribe un algoritmo que calcule el factorial de un número entero no negativo `N` ingresado por el usuario. El factorial (N!) es el producto de todos los enteros positivos desde 1 hasta N (ej: 5! = 5 * 4 * 3 * 2 * 1 = 120). Por definición, 0! = 1. Usa un bucle `Para`.

## Código con Errores
```pseudocode
Proceso FactorialPara

    Definir n, i Como Entero;
    Definir factorial Como Real; // Pista 1: El factorial de un entero es siempre entero, ¿es 'Real' necesario? (Aunque podría crecer mucho)

    Escribir "Ingrese un número entero no negativo N:";
    Leer n;

    Si n >= 0 Entonces
        factorial <- 0; // Pista 2: ¿Cuál es el valor inicial correcto para un acumulador de producto (factorial)?
        Si n = 0 Entonces
            factorial <- 1;
        Else // Pista 3: Palabra clave incorrecta.
            Para i <- 1 Hasta n Hacer
                factorial <- factorial * i;
            FinPara
        FinSi
        Escribir n, "! = ", factorial;
    Sino
        Escribir "N debe ser no negativo.";
    FinSi

FinProceso
```
