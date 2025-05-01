# Módulo 1 - Ejercicio 3 (Dificultad 3)

## Enunciado

Escribe un algoritmo que sume dos números enteros definidos directamente en el código (constantes, por ejemplo, 5 y 7) y muestre el resultado.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso SumaConstantes

    Definir num1, num2 Como Entero;
    Definir resultado Como Real; // Pista 1: Si sumas dos enteros, ¿el resultado siempre necesita ser 'Real'?

    num1 = 5; // Pista 2: ¿Es '=' el operador correcto para asignar valores en PSeInt?
    num2 <- 7;

    resultado <- num1 + num 2; // Pista 3: Revisa si hay algún espacio inesperado en los nombres de variables.

    Escribir "La suma de ", num1, " y ", num2, " es: ", resultado;

FinProceso
```

<details>
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta

```pseudocode
Proceso SumaConstantes_Solucion

    Definir num1, num2, resultado Como Entero; // Corregido: El resultado también puede ser Entero.

    num1 <- 5; // Corregido: Usar el operador de asignación '<-'.
    num2 <- 7;

    resultado <- num1 + num2; // Corregido: Sin espacio en 'num2'.

    Escribir "La suma de ", num1, " y ", num2, " es: ", resultado;

FinProceso
```

</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución

1.  La suma de dos números enteros siempre da como resultado otro número entero. Por lo tanto, la variable `resultado` puede (y es preferible en este caso) definirse como `Entero`, no `Real`. Se cambió `Definir resultado Como Real` a `Definir resultado Como Entero` (o se añadió a la definición existente).
2.  El operador para asignar un valor a una variable en PSeInt es `<-` (flecha), no `=` (signo de igual). Se corrigió `num1 = 5` a `num1 <- 5`.
3.  En la línea del cálculo `resultado <- num1 + num 2;`, había un espacio entre `num` y `2`, haciendo que PSeInt lo interprete como una variable inexistente `num`. Se corrigió a `num2`.

</details>
