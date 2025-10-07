# Módulo 4 - Ejercicio 1 (Dificultad 1)

## Enunciado
Escribe un algoritmo que muestre los números del 1 al 10 en la pantalla, uno debajo del otro, usando un bucle `Para`.

## Código con Errores
```pseudocode
Proceso Numeros1a10Para

    Definir i Como Entero;

    Para i <- 1 Hasta 10 Hacer Con Paso 1 // Pista 1: ¿Es necesaria la cláusula 'Con Paso 1'? (No es error, pero puede simplificarse)
        Escribir i;
    Fin Para // Pista 2: Revisa la sintaxis para finalizar el bucle 'Para'.

    // Pista 3: ¿Se definió correctamente la variable 'i'? Revisa la primera línea.

FinProceso
```
<details><summary>Mostrar Solución Correcta</summary>
## Solución Correcta
```pseudocode
Proceso Numeros1a10Para_Solucion

    Definir i Como Entero; // Correcto.

    Para i <- 1 Hasta 10 Hacer // Corregido: 'Con Paso 1' es opcional si el paso es 1.
        Escribir i;
    FinPara // Corregido: Sintaxis correcta 'FinPara'.

FinProceso
```
</details><details><summary>Mostrar Explicación de la Solución</summary>
## Explicación de la Solución
1.  La cláusula `Con Paso 1` en un bucle `Para` es opcional. Si el paso es 1 (el valor por defecto), puede omitirse para simplificar el código. No era un error de ejecución, pero sí una posible mejora/simplificación.
2.  La palabra clave para finalizar un bucle `Para` es `FinPara` (todo junto), no `Fin Para` (separado).
3.  La definición `Definir i Como Entero;` era correcta. El comentario de la Pista 3 era para asegurar la revisión completa, pero no había error allí.
```
</details>
