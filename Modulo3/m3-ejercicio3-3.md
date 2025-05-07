# Módulo 3 - Ejercicio 3 (Dificultad 3)

## Enunciado
Resuelve el mismo problema del ejercicio anterior (día laboral o fin de semana según el número 1-7), pero esta vez utilizando la estructura `Segun`.

## Código con Errores
```pseudocode
Proceso DiaLaboralSegun

    Definir dia Como Caracter; // Pista 1: El número del día es entero, ¿es 'Caracter' el tipo correcto?

    Escribir "Ingrese número de día (1-7):";
    Leer dia;

    Segun dia Hacer
        1, 2, 3, 4, 5: // Pista 2: ¿Necesitan comillas los números en las opciones si la variable es numérica?
            Escribir "Es un día laboral.";
        "6", "7":
            Escribir "Es fin de semana.";
        De Otro Modo
            Escribir "Número de día inválido.";
    FinSegun // Pista 3: ¿Falta algo en la línea 'De Otro Modo'?

FinProceso
```

<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso DiaLaboralSegun_Solucion

    Definir dia Como Entero; // Corregido: El día es un número Entero.

    Escribir "Ingrese número de día (1-7):";
    Leer dia;

    Segun dia Hacer
        1, 2, 3, 4, 5: // Corregido: Sin comillas para opciones numéricas.
            Escribir "Es un día laboral.";
        6, 7: // Corregido: Sin comillas para opciones numéricas.
            Escribir "Es fin de semana.";
        De Otro Modo: // Corregido: Añadir dos puntos ':' al final.
            Escribir "Número de día inválido.";
    FinSegun

FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

# Explicación de la Solución
1.  La variable `dia` almacena un número entero (1 a 7), por lo que su tipo debe ser `Entero`, no `Caracter`.
2.  Cuando la variable evaluada en `Segun` es numérica (`Entero` o `Real`), las opciones (`1, 2, 3...`) también deben ser valores numéricos literales, sin comillas. Las comillas se usan si la variable fuera `Caracter` y las opciones fueran texto.
3.  La cláusula `De Otro Modo` dentro de un `Segun` debe terminar con dos puntos (`:`), igual que las otras opciones. Faltaban los dos puntos.

</details>
