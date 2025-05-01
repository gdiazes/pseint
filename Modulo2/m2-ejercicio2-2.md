# Módulo 2 - Ejercicio 2 (Dificultad 2)

## Enunciado
Escribe un algoritmo que pida un número al usuario e indique si es positivo o no (considera el cero como no positivo en este caso).

## Código con Errores
```pseudocode
Proceso EsPositivo

    Definir numero Como Real;

    Escribir "Ingrese un número:";
    Leer num; // Pista 1: ¿Se está leyendo en la variable definida?

    Si numero < 0 Entonces // Pista 2: ¿La condición `numero < 0` identifica a los números positivos?
        Escribir "El número es positivo.";
    FinSi

    // Pista 3: ¿Qué pasa si el número no es menor que 0? ¿Debería mostrarse algo más? (Falta estructura)

FinProceso
```
<details>
<summary>Mostrar Solución Correcta</summary>
  
## Solución Correcta
```pseudocode
Proceso EsPositivo_Solucion

    Definir numero Como Real;

    Escribir "Ingrese un número:";
    Leer numero; // Corregido: Leer en la variable 'numero'.

    Si numero > 0 Entonces // Corregido: Condición correcta para positivo (mayor que 0).
        Escribir "El número es positivo.";
    Sino // Añadido: Estructura 'Sino' para el caso contrario.
        Escribir "El número no es positivo (es cero o negativo).";
    FinSi

FinProceso
```
</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  La variable definida fue `numero`, pero se intentó leer en `num`. Se corrigió a `Leer numero;`.
2.  La condición para que un número sea positivo es que sea `> 0`. La condición original `numero < 0` identifica a los negativos. Se cambió a `numero > 0`.
3.  El código original solo mostraba mensaje si el número era negativo (según la condición errónea). Faltaba la estructura `Sino` para manejar el caso en que la condición no se cumple (cuando el número es 0 o positivo, o en la versión corregida, cuando es 0 o negativo) y mostrar el mensaje apropiado.

</details>
