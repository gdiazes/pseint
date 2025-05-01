# Módulo 2 - Ejercicio 1 (Dificultad 1)

## Enunciado
Escribe un algoritmo que pida al usuario dos números enteros y muestre el resultado de restar el segundo número al primero.

## Código con Errores
```pseudocode
Proceso RestaBasica

    Definir num1, num2, resultado Como Real; // Pista 1: Si pides enteros y restas enteros, ¿necesitas 'Real'?

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número:";
    Leer num2;

    resultado <- num1 - num_2; // Pista 2: Revisa el nombre de la segunda variable en la resta.

    Escribir "La resta es: ", resultado; // Pista 3: ¿Hay alguna palabra clave mal escrita?

Fin Proseso // Pista 3: Revisa la palabra clave final.
```
<details>
<summary>Mostrar Solución Correcta</summary>
## Solución Correcta
```pseudocode
Proceso RestaBasica_Solucion

    Definir num1, num2, resultado Como Entero; // Corregido: Usar Entero si la entrada es entera.

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número:";
    Leer num2;

    resultado <- num1 - num2; // Corregido: Nombre correcto de la variable 'num2'.

    Escribir "La resta es: ", resultado;

FinProceso // Corregido: Palabra clave correcta.
```
</details>
<details>
<summary>Mostrar Explicación de la Solución</summary>
## Explicación de la Solución
1.  Dado que se piden números enteros y la resta de enteros es un entero, es más apropiado definir las variables como `Entero` en lugar de `Real`.
2.  En la operación de resta, se escribió `num_2` en lugar de `num2`. Los nombres de variables deben coincidir exactamente con su definición.
3.  La palabra clave para finalizar un algoritmo es `FinProceso`, no `FinProseso`.
</details>
