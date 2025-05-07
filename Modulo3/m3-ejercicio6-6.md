# Módulo 3 - Ejercicio 6 (Dificultad 6)

## Enunciado
Crea una calculadora simple que pida dos números reales y luego pregunte qué operación realizar (1:Suma, 2:Resta, 3:Multiplicación, 4:División). Debe mostrar el resultado de la operación seleccionada usando `Segun`.

## Código con Errores
```pseudocode
Proceso CalculadoraSegun

    Definir num1, num2, resultado Como Real;
    Definir opcion Como Caracter; // Pista 1: La opción es un número (1-4), ¿es 'Caracter' adecuado?

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número:";
    Leer num2;

    Escribir "Elija operación: 1.Suma 2.Resta 3.Multiplicación 4.División";
    Leer opcion;

    Segun opcion Hacer
        "1": resultado <- num1 + num2; // Pista 2: Si opcion es numérica, ¿las opciones necesitan comillas?
        "2": resultado <- num1 - num2;
        "3": resultado <- num1 * num2;
        "4": Si num2 <> 0 Entonces
                 resultado <- num1 / num2;
             Sino
                 Escribir "Error: División por cero.";
                 // Falta asignar algo a resultado o manejar la salida
             FinSi
        De Otro Modo:
            Escribir "Opción inválida.";
            // Falta asignar algo a resultado o manejar la salida
    Fin Segun // Pista 3: Revisa la palabra clave para finalizar 'Segun'.

    // Mostrar resultado siempre, incluso si hubo error?
    Escribir "El resultado es: ", resultado;

FinProceso
```

<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso CalculadoraSegun_Solucion

    Definir num1, num2, resultado Como Real;
    Definir opcion Como Entero; // Corregido: La opción es un número Entero.
    Definir operacionValida Como Logico; // Para controlar si mostrar resultado

    operacionValida <- Verdadero; // Asumir que es válida inicialmente

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número:";
    Leer num2;

    Escribir "Elija operación: 1.Suma 2.Resta 3.Multiplicación 4.División";
    Leer opcion;

    Segun opcion Hacer
        1: // Corregido: Sin comillas
            resultado <- num1 + num2;
        2: // Corregido: Sin comillas
            resultado <- num1 - num2;
        3: // Corregido: Sin comillas
            resultado <- num1 * num2;
        4:
            Si num2 <> 0 Entonces
                resultado <- num1 / num2;
            Sino
                Escribir "Error: División por cero.";
                operacionValida <- Falso; // Marcar como inválida
            FinSi
        De Otro Modo:
            Escribir "Opción inválida.";
            operacionValida <- Falso; // Marcar como inválida
    FinSegun // Corregido: Palabra clave 'FinSegun'.

    // Mostrar resultado solo si la operación fue válida
    Si operacionValida Entonces
        Escribir "El resultado es: ", resultado;
    FinSi

FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  La variable `opcion` almacena un número entero (1, 2, 3 o 4), por lo que su tipo debe ser `Entero`, no `Caracter`.
2.  Como `opcion` es `Entero`, las claves dentro del `Segun` deben ser los números literales `1`, `2`, `3`, `4`, sin comillas. Las comillas se usarían si `opcion` fuera `Caracter`.
3.  La palabra clave para finalizar la estructura `Segun` es `FinSegun`, no `Fin Segun` (separado). Adicionalmente, el código original tenía un problema lógico: mostraba la variable `resultado` incluso si había ocurrido un error (división por cero u opción inválida), lo que podría mostrar un valor incorrecto o no inicializado. La solución introduce una variable lógica `operacionValida` para controlar si se debe mostrar el resultado final.
</details>