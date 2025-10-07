# Módulo 4 - Ejercicio 5 (Dificultad 5)

## Enunciado
Escribe un algoritmo que pida al usuario ingresar un número entero entre 1 y 100. Debe seguir pidiendo el número hasta que el usuario ingrese uno que esté dentro de ese rango. Usa un bucle `Repetir`.

## Código con Errores
```pseudocode
Proceso ValidarEntradaRepetir

    Definir numIngresado Como Entero;

    Repetir
        Escribir "Ingrese un número entero entre 1 y 100:";
        Leer numIngresado;
        Si numIngresado < 1 O numIngresado > 100 Entonces
            Escribir "Número fuera de rango. Intente de nuevo.";
        FinSi
    Mientras numIngresado < 1 O numIngresado > 100; // Pista 1: ¿Es 'Mientras' la palabra clave correcta para la condición del 'Repetir'?

    // Pista 2: ¿La condición de parada está bien formulada? El bucle termina cuando la condición es Verdadera.

    Escribir "Número válido ingresado: ", numIngresado;

FinProceso // Pista 3: ¿Hay algún error en la definición de variables o estructura general? (Revisión general)
```
