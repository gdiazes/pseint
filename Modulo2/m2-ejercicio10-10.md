# Módulo 2 - Ejercicio 10 (Dificultad 10)

## Enunciado
Para que tres longitudes (l1, l2, l3) puedan formar un triángulo, se debe cumplir la "desigualdad triangular": la suma de las longitudes de dos lados cualesquiera debe ser mayor que la longitud del tercer lado. Escribe un algoritmo que pida las tres longitudes (reales) y determine si pueden formar un triángulo válido.

## Código con Errores
```pseudocode
Proceso TrianguloValido

    Definir l1, l2, l3 Como Real;
    Definir esValido Como Caracter; // Pista 1: ¿Es 'Caracter' el tipo adecuado para guardar un resultado Verdadero/Falso?

    Escribir "Ingrese la longitud del lado 1:";
    Leer l1;
    Escribir "Ingrese la longitud del lado 2:";
    Leer l2;
    Escribir "Ingrese la longitud del lado 3:";
    Leer l3;

    // Verificar desigualdad triangular
    cond1 <- (l1 + l2) > l3;
    cond2 <- (l1 + l3) > l2;
    cond3 <- (l2 + l3) > l1;

    esValido = cond1 Y cond2 Y cond3; // Pista 2: Revisa el operador de asignación.

    Si (esValido) Entonces // Pista 3: En PSeInt, ¿se compara directamente una variable lógica con Verdadero/Falso o se usa su valor?
        Escribir "Las longitudes pueden formar un triángulo.";
    Sino
        Escribir "Las longitudes NO pueden formar un triángulo.";
    FinSi

FinProceso
```

<details> 
  <summary>Mostrar Solución Correcta</summary> 
  
## Solución Correcta
```pseudocode
Proceso TrianguloValido_Solucion

    Definir l1, l2, l3 Como Real;
    Definir cond1, cond2, cond3, esValido Como Logico; // Corregido: Usar 'Logico' para Verdadero/Falso.

    Escribir "Ingrese la longitud del lado 1:";
    Leer l1;
    Escribir "Ingrese la longitud del lado 2:";
    Leer l2;
    Escribir "Ingrese la longitud del lado 3:";
    Leer l3;

    // Verificar desigualdad triangular
    cond1 <- (l1 + l2) > l3;
    cond2 <- (l1 + l3) > l2;
    cond3 <- (l2 + l3) > l1;

    esValido <- cond1 Y cond2 Y cond3; // Corregido: Usar '<-'.

    Si esValido Entonces // Corregido: Se usa directamente la variable lógica en la condición.
        Escribir "Las longitudes pueden formar un triángulo.";
    Sino
        Escribir "Las longitudes NO pueden formar un triángulo.";
    FinSi

FinProceso
```

</details>
<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  La variable `esValido` (y las condiciones `cond1`, `cond2`, `cond3`) almacenan un resultado lógico (Verdadero o Falso), por lo que su tipo debe ser `Logico`, no `Caracter`.
2.  Se usó `=` en lugar de `<-` para asignar el resultado de la combinación lógica a `esValido`.
3.  En PSeInt, una variable de tipo `Logico` ya contiene `Verdadero` o `Falso`. No es necesario (y generalmente es redundante) compararla explícitamente con `Verdadero` (ej: `Si esValido = Verdadero Entonces`). Se puede usar directamente `Si esValido Entonces`. El código original con `Si (esValido) Entonces` es aceptable en PSeInt flexible, pero usarla directamente es más común y limpio. El "error" estaba más relacionado con la definición incorrecta del tipo en el punto 1. Al corregir el tipo, la condición `Si esValido Entonces` funciona perfectamente.
</details>
