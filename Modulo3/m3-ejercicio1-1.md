# Módulo 3 - Ejercicio 1 (Dificultad 1)

## Enunciado
Escribe un algoritmo que pida un número y determine si es positivo, negativo o cero, usando estructuras `Si`/`Sino Si`/`Sino`.

## Código con Errores
```pseudocode
Proceso PositivoNegativoCero

    Definir num Como Real;

    Escribir "Ingrese un número:";
    Leer num;

    Si num > 0 Entonces
        Escribir "El número es positivo."
    Sino Si num < 0 Entonces // Pista 1: Revisa la sintaxis de esta línea, ¿falta algo al final?
        Escribir "El número es negativo.";
    Sino // Pista 2: Si no es positivo ni negativo, ¿qué es? ¿Está bien el mensaje?
        Escribir "El número es positivo o negativo.";
    FinSi // Pista 3: ¿Esta estructura cierra todos los 'Si' abiertos?

FinProceso
```
<details>
<summary>Mostrar Solución Correcta</summary>
    
## Solución Correcta
```pseudocode
Proceso PositivoNegativoCero_Solucion

    Definir num Como Real;

    Escribir "Ingrese un número:";
    Leer num;

    Si num > 0 Entonces
        Escribir "El número es positivo."; // Corregido: Añadir punto y coma si es necesario.
    Sino Si num < 0 Entonces // Correcto (asumiendo ;)
        Escribir "El número es negativo."; // Corregido: Añadir punto y coma si es necesario.
    Sino // Lógica: Si no es > 0 ni < 0, entonces es 0.
        Escribir "El número es cero."; // Corregido: Mensaje correcto para el caso restante.
    FinSi // Correcto: Cierra la estructura Si/Sino Si/Sino.

FinProceso
```
</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  Aunque PSeInt puede ser flexible, a menudo se requiere un punto y coma (`;`) al final de cada instrucción. Faltaban en los `Escribir`. (Considerado error menor si el perfil es flexible). La sintaxis `Sino Si` es correcta.
2.  Si un número no es mayor que cero (`num > 0` es falso) y tampoco es menor que cero (`num < 0` es falso), la única posibilidad restante es que sea exactamente cero. El mensaje en el último `Sino` era incorrecto; debe indicar que es cero.
3.  La estructura `Si ... Sino Si ... Sino ... FinSi` está correctamente cerrada con un único `FinSi`. El error no estaba aquí, sino en la lógica del último `Sino`.

</details>
