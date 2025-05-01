# Módulo 1 - Ejercicio 7 (Dificultad 7)

## Enunciado

Escribe un algoritmo que pida al usuario dos números (pueden tener decimales), calcule su promedio y muestre el resultado. Fórmula: Promedio = (Numero1 + Numero2) / 2.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso CalcularPromedio

    Define n1, n2, promedio Como Real; // Pista 1: Revisa la palabra clave para definir variables.

    Escribir "Ingrese el primer número:";
    Leer n1;
    Escribir "Ingrese el segundo número:";
    Leer n2;

    promedio <- n1 + n2 / 2; // Pista 2: Considera la jerarquía de operadores. ¿Qué se calcula primero aquí? ¿Necesitas agrupar algo?

    Escribir "El promedio es: " promedio; // Pista 3: Falta algo al final de la variable 'promedio' al mostrarla.

FinProceso
```

<details>
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta

```pseudocode
Proceso CalcularPromedio_Solucion

    Definir n1, n2, promedio Como Real; // Corregido: La palabra clave es 'Definir'.

    Escribir "Ingrese el primer número:";
    Leer n1;
    Escribir "Ingrese el segundo número:";
    Leer n2;

    promedio <- (n1 + n2) / 2; // Corregido: Añadir paréntesis para asegurar que la suma se haga antes de la división.

    Escribir "El promedio es: ", promedio; // Corregido: Usar coma para separar el texto de la variable.

FinProceso
```

</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución

1.  La palabra clave para declarar variables en PSeInt es `Definir`, no `Define`. Se corrigió la primera línea.
2.  Debido a la jerarquía de operadores, la división (`/`) tiene mayor precedencia que la suma (`+`). En la línea `promedio <- n1 + n2 / 2`, primero se calcularía `n2 / 2` y luego se sumaría `n1` a ese resultado, lo cual es incorrecto para el promedio. Para calcular la suma primero, es necesario agrupar `n1 + n2` usando paréntesis: `promedio <- (n1 + n2) / 2`.
3.  En la instrucción `Escribir`, para mostrar múltiples elementos (el texto "El promedio es: " y el valor de la variable `promedio`), estos deben separarse por una coma (`,`). Faltaba la coma antes de `promedio`.

</details>
