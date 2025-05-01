# Módulo 2 - Ejercicio 7 (Dificultad 7)

## Enunciado
Escribe un algoritmo que pida al usuario ingresar una letra y determine si es una vocal (a, e, i, o, u). Considera solo letras minúsculas.

## Código con Errores
```pseudocode
Proceso EsVocalSimple

    Definir letra Como Entero; // Pista 1: ¿Es 'Entero' el tipo correcto para guardar una letra?

    Escribir "Ingrese una letra (minúscula):";
    Leer letra;

    // Comprobar si es una vocal
    Si letra = "a" O letra = "e" O letra = "i" O letra = "o" U letra = "u" Entonces // Pista 2: Revisa el operador lógico para la última vocal.
        Escribir "La letra ingresada es una vocal.";
    Sino
        Escribir "La letra ingresada no es una vocal."; // Pista 3: ¿Está bien escrito 'Escribir'?
    FinSi

FinProceso
```

<details> 
    <summary>Mostrar Solución Correcta</summary> 

## Solución Correcta
```pseudocode
Proceso EsVocalSimple_Solucion

    Definir letra Como Caracter; // Corregido: Usar 'Caracter' para letras.

    Escribir "Ingrese una letra (minúscula):";
    Leer letra;

    // Comprobar si es una vocal
    Si letra = "a" O letra = "e" O letra = "i" O letra = "o" O letra = "u" Entonces // Corregido: Usar 'O' (o '|') para todas las comparaciones.
        Escribir "La letra ingresada es una vocal.";
    Sino
        Escribir "La letra ingresada no es una vocal."; // Corregido: Palabra clave 'Escribir'.
    FinSi

FinProceso
```

</details>

<details>
    <summary>Mostrar Explicación de la Solución</summary>
    
## Explicación de la Solución
1.  Una variable que almacena una letra debe ser de tipo `Caracter`, no `Entero`.
2.  El operador lógico para unir condiciones con "o" es `O` (o `|`). Se usó una `U` por error al final de la condición compuesta. Se reemplazó `U` por `O`.
3.  En el bloque `Sino`, la instrucción para mostrar el mensaje estaba mal escrita como `Escribir` (faltaba la 'r'). Se corrigió a `Escribir`.

</details>

