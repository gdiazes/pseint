# Módulo 4 - Ejercicio 2 (Dificultad 2)

## Enunciado
Escribe un algoritmo que muestre los números pares entre 2 y 20 (inclusive), usando un bucle `Mientras`.

## Código con Errores
```pseudocode
Proceso ParesMientras

    Definir num Como Entero;
    num <- 2;

    Mientras num < 20 Hacer // Pista 1: ¿La condición '< 20' incluye el número 20?
        Escribir num;
        num <- num + 1; // Pista 2: Si sumas 1 cada vez, ¿mostrarás solo pares?
    // Pista 3: ¿Falta cerrar la estructura del bucle?

FinProceso
```
<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso ParesMientras_Solucion

    Definir num Como Entero;
    num <- 2; // Inicia en el primer par

    Mientras num <= 20 Hacer // Corregido: Usar '<=' para incluir el 20.
        Escribir num;
        num <- num + 2; // Corregido: Incrementar de 2 en 2 para obtener el siguiente par.
    FinMientras // Corregido: Añadir 'FinMientras'.

FinProceso
```
</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  La condición `num < 20` haría que el bucle se detenga cuando `num` sea 20, sin llegar a mostrarlo. Para incluir el 20, la condición debe ser `num <= 20`.
2.  Al incrementar `num` de 1 en 1 (`num <- num + 1`), se mostrarían todos los números (2, 3, 4,...). Para mostrar solo los pares, y partiendo de un par (2), se debe incrementar de 2 en 2 (`num <- num + 2`).
3.  Faltaba la palabra clave `FinMientras` para cerrar correctamente la estructura del bucle.
```
</details>
