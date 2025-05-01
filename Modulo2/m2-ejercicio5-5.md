# Módulo 2 - Ejercicio 5 (Dificultad 5)

## Enunciado
Escribe un algoritmo que pida dos números diferentes al usuario y muestre cuál de los dos es mayor.

## Código con Errores
```pseudocode
Proceso CompararNumeros

    Definir num1, num2 Como Real;

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número (diferente al primero):";
    Leer num2;

    Si num1 > num2 // Pista 1: ¿Es esta la palabra clave correcta para iniciar la condición?
        Escribir num1, " es mayor que ", num2;
    Sino // Pista 2: Si num1 no es mayor que num2, y sabemos que son diferentes, ¿qué podemos concluir?
        Escribir num2, " es menor que ", num1; // Pista 3: El mensaje está bien, pero ¿es la única posibilidad si num1 NO es mayor que num2? (considerando la Pista 2)
    FinSi

FinProceso
```
<details>
  
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso CompararNumeros_Solucion

    Definir num1, num2 Como Real;

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número (diferente al primero):";
    Leer num2;

    Si num1 > num2 Entonces // Corregido: Añadir 'Entonces' después de la condición.
        Escribir num1, " es mayor que ", num2;
    Sino// Lógica: Si no es mayor, y son diferentes, debe ser menor.
        Escribir num2, " es mayor que ", num1; // Corregido: Mensaje lógico para el caso 'Sino'.
    FinSi

FinProceso
```

</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>
  
## Explicación de la Solución
1.  La estructura condicional requiere la palabra clave `Entonces` después de la condición y antes del bloque de instrucciones a ejecutar si es verdadera. Faltaba `Entonces`.
2.  El enunciado indica que los números son diferentes. Si la condición `num1 > num2` es falsa, la única posibilidad restante es que `num1 < num2` (o sea, `num2 > num1`).
3.  Dado el punto 2, si entramos en el bloque `Sino`, significa que `num2` es el mayor. El mensaje original (`num2, " es menor que ", num1;`) era incorrecto en este contexto. Se corrigió para indicar que `num2` es mayor que `num1`.

</details>
