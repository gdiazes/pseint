# Módulo 4 - Ejercicio 7 (Dificultad 7)

## Enunciado
Crea un juego simple de "Adivina el número". El algoritmo debe generar un número secreto aleatorio entre 1 y 100 (puedes usar `azar(100) + 1`). Luego, debe pedir al usuario que adivine el número. Si el usuario no acierta, el algoritmo debe decirle si el número secreto es mayor o menor que el intento, y seguir pidiendo números hasta que acierte. Usa un bucle `Mientras`.

## Código con Errores
```pseudocode
Proceso AdivinaNumeroMientras

    Definir secreto, intento, numIntentos Como Entero;
    numIntentos <- 0;
    secreto <- azar(100) + 1;

    Escribir "¡Adivina el número secreto (entre 1 y 100)!";
    Leer intento; // Pista 1: La primera lectura está fuera del bucle. ¿Qué pasa si acierta al primer intento?

    Mientras intento = secreto Hacer // Pista 2: ¿Cuál es la condición para CONTINUAR el bucle (no haber acertado)?
        numIntentos <- numIntentos + 1;
        Si intento < secreto Entonces
            Escribir "El número secreto es MAYOR. Intenta de nuevo:";
        Sino
            Escribir "El número secreto es MENOR. Intenta de nuevo:";
        FinSi
        Leer intento; // Pide el siguiente intento
    FinMientras

    Escribir "¡Correcto! El número era ", secreto;
    Escribir "Lo adivinaste en ", numIntentos, " intentos."; // Pista 3: ¿Se cuenta el último intento (el correcto)?

FinProceso
```
