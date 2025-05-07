# Módulo 3 - Ejercicio 9 (Dificultad 9)

## Enunciado
Escribe un algoritmo que calcule el Índice de Masa Corporal (IMC = peso / altura^2). Pide al usuario su peso en kg (real) y su altura en metros (real). Luego, clasifica el resultado según la OMS:
*   < 18.5: Bajo peso
*   18.5 a 24.9: Peso normal
*   25.0 a 29.9: Sobrepeso
*   >= 30.0: Obesidad

## Código con Errores
```pseudocode
Proceso CalcularIMC

    Definir peso, altura, imc Como Real;

    Escribir "Ingrese su peso en kg:";
    Leer peso;
    Escribir "Ingrese su altura en metros:";
    Leer altura;

    // Calcular IMC si la altura es válida
    Si altura >= 0 Entonces // Pista 1: ¿Puede la altura ser exactamente 0 para calcular IMC?
        imc <- peso / (altura ^ 2);

        Escribir "Su IMC es: ", imc;

        // Clasificar
        Si imc < 18.5 Entonces
            Escribir "Clasificación: Bajo peso";
        Sino Si imc >= 18.5 O imc <= 24.9 Entonces // Pista 2: ¿Debe cumplirse una condición ('O') o ambas ('Y') para estar en este rango?
            Escribir "Clasificación: Peso normal";
        Sino Si imc >= 25.0 Y imc <= 29.9 Entonces
            Escribir "Clasificación: Sobrepeso";
        Sino // Si no es ninguno de los anteriores, y es >= 30
            Escribir "Clasificación: Obeso"; // Pista 3: Falta cerrar la estructura interna.
        // FinSi faltante
    Sino
        Escribir "Altura inválida.";
    FinSi

FinProceso
```

<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso CalcularIMC_Solucion

    Definir peso, altura, imc Como Real;

    Escribir "Ingrese su peso en kg:";
    Leer peso;
    Escribir "Ingrese su altura en metros:";
    Leer altura;

    // Calcular IMC si peso y altura son válidos
    Si altura > 0 Y peso > 0 Entonces // Corregido: Altura y peso deben ser > 0.
        imc <- peso / (altura ^ 2);

        Escribir "Su IMC es: ", imc;

        // Clasificar (aprovechando el flujo del Si/Sino Si)
        Si imc < 18.5 Entonces
            Escribir "Clasificación: Bajo peso";
        Sino Si imc <= 24.9 Entonces // Corregido: Si llega aquí, ya es >= 18.5. Solo falta comprobar el límite superior. Operador 'Y' es implícito.
            Escribir "Clasificación: Peso normal";
        Sino Si imc <= 29.9 Entonces // Corregido: Si llega aquí, ya es >= 25.0.
            Escribir "Clasificación: Sobrepeso";
        Sino // Si no es ninguno de los anteriores, es >= 30.0
            Escribir "Clasificación: Obesidad";
        FinSi // Corregido: Añadir FinSi para la clasificación.
    Sino
        Escribir "Peso o altura inválidos (deben ser mayores que cero).";
    FinSi

FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución

1.  Para calcular el IMC, la altura no puede ser cero (división por cero) y tanto altura como peso deben ser valores positivos. La condición inicial `altura >= 0` era insuficiente. Se cambió a `altura > 0 Y peso > 0`.
2.  Para estar en el rango de "Peso normal" (18.5 a 24.9), el IMC debe cumplir *ambas* condiciones: ser mayor o igual a 18.5 **Y** ser menor o igual a 24.9. El operador `O` era incorrecto. Sin embargo, en una estructura `Si/Sino Si`, si llegamos a `Sino Si imc <= 24.9`, ya sabemos que la condición anterior (`imc < 18.5`) fue falsa, lo que implica que `imc >= 18.5`. Por lo tanto, solo necesitamos verificar el límite superior (`imc <= 24.9`). Lo mismo aplica para el sobrepeso.
3.  Faltaba un `FinSi` para cerrar la estructura condicional anidada que realizaba la clasificación del IMC.
</details>