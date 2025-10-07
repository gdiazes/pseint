# Módulo 4 - Ejercicio 8 (Dificultad 8)

## Enunciado
Escribe un algoritmo que pida al usuario cuántas notas desea ingresar (`N`). Luego, debe pedirle que ingrese esas `N` notas (reales) una por una, calcular la suma total y finalmente mostrar el promedio de las notas. Usa un bucle `Para` y un acumulador.

## Código con Errores
```pseudocode
Proceso PromedioNNotas

    Definir n, i Como Entero;
    Definir nota, suma, promedio Como Real;
    suma <- 0.0;

    Escribir "¿Cuántas notas ingresará?";
    Leer n;

    // Pedir y sumar las notas
    Para i <- 1 Hasta n Hacer
        Escribir "Ingrese la nota ", i, ":";
        Leer nota;
        suma = nota; // Pista 1: ¿Se está acumulando la suma correctamente? Revisa asignación y operación.
    FinPara

    // Calcular promedio
    Si n > 0 // Pista 2: ¿Está bien la condición para evitar división por cero?
        promedio <- suma / n;
        Escribir "El promedio de las ", n, " notas es: ", promedio;
    Sino
        Escribir "No se ingresaron notas."; // Pista 3: ¿Se definió la variable 'promedio'? (Revisión general)
    FinSi

FinProceso
```
