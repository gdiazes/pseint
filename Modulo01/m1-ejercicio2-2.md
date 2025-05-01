# Módulo 1 - Ejercicio 2 (Dificultad 2)

## Enunciado

Escribe un algoritmo que pida al usuario ingresar un número entero y luego muestre en pantalla el número ingresado.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso EcoNumero

    Definir numero Como Caracter; // Pista 1: Se pide un número entero, ¿es 'Caracter' el tipo correcto?

    Escribir "Ingrese un número entero:";
    Leer numeroUsuario; // Pista 2: La variable donde se guarda el dato debe coincidir con la definida.

    Escribir "El número ingresado es: ", numero; // Pista 3: ¿Se está mostrando la variable correcta?

FinProceso
```

<details>
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta

```pseudocode
Proceso EcoNumero_Solucion

    Definir numero Como Entero; // Corregido: El tipo para números enteros es 'Entero'.

    Escribir "Ingrese un número entero:";
    Leer numero; // Corregido: Usar la variable 'numero' que fue definida.

    Escribir "El número ingresado es: ", numero; // Correcto, ahora muestra la variable correcta.

FinProceso
```

</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución

1.  Se pidió un número entero, por lo tanto, el tipo de dato correcto al `Definir` la variable es `Entero`, no `Caracter` (que es para texto).
2.  La instrucción `Leer` debe usar el nombre de la variable que se definió previamente para guardar el dato. Se cambió `Leer numeroUsuario` por `Leer numero`.
3.  Aunque la línea `Escribir` estaba sintácticamente bien, mostraba la variable `numero`. El error conceptual estaba en el punto 2, al intentar leer en una variable no definida (`numeroUsuario`). Al corregir el `Leer`, esta línea ahora funciona como se espera.

</details>
