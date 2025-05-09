# Módulo 3 - Ejercicio 4 (Dificultad 4)

## Enunciado
Escribe un algoritmo que pida una calificación numérica (0 a 10) y muestre su equivalente literal: Sobresaliente (9-10), Notable (7-8), Aprobado (5-6), Suspenso (0-4). Usa `Si`/`Sino Si`/`Sino`.

## Código con Errores
```pseudocode
Proceso CalificacionLiteral

    Definir nota Como Entero; // Pista 1: Una calificación puede ser 7.5, ¿es 'Entero' siempre adecuado?

    Escribir "Ingrese la calificación (0-10):";
    Leer nota;

    Si nota >= 9 Y nota <= 10 Entonces
        Escribir "Sobresaliente";
    Sino Si nota >= 7 Y nota < 9 Entonces // Nota 9 ya está cubierta arriba.
        Escribir "Notable";
    Sino Si nota >= 5 // Pista 2: Si llega aquí, ya sabemos que es < 7. ¿Es suficiente esta condición?
        Escribir "Aprobado";
    Sino // Pista 3: Si no es >= 5, ¿qué rango queda? ¿Está bien la condición implícita?
        Escribir "Suspenso";
    FinSi
    // Falta manejar notas fuera de 0-10

FinProceso
```

<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso CalificacionLiteral_Solucion_Corregido
	
    Definir nota Como Real;
	
    Escribir "Ingrese la calificación (0-10):";
    Leer nota;
	
    Si nota >= 0 Y nota <= 10 Entonces // Si Principal (externo)
        Si nota >= 9 Entonces           // Si Anidado Nivel 1
            Escribir "Sobresaliente";
        Sino                           // Sino del Si Anidado Nivel 1
            Si nota >= 7 Entonces      // Si Anidado Nivel 2
                Escribir "Notable";
            Sino                       // Sino del Si Anidado Nivel 2
                Si nota >= 5 Entonces  // Si Anidado Nivel 3
                    Escribir "Aprobado";
                Sino                   // Sino del Si Anidado Nivel 3
                    Escribir "Suspenso";
                FinSi                  // Cierra Si Anidado Nivel 3
            FinSi                      // Cierra Si Anidado Nivel 2
        FinSi                          // Cierra Si Anidado Nivel 1
    Sino                               // Sino del Si Principal
        Escribir "Calificación fuera de rango (0-10).";
    FinSi                              // Cierra Si Principal
	
FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  Las calificaciones pueden tener decimales (ej. 7.5), por lo que `Real` es un tipo más adecuado que `Entero`.
2.  En la estructura `Si/Sino Si`, cuando se llega a una condición, ya se sabe que las anteriores fueron falsas. Por ejemplo, en `Sino Si nota >= 5`, ya sabemos que `nota` es menor que 7 (porque no entró en `nota >= 7`). La condición original era suficiente *dentro de esa lógica*, pero el problema principal era la falta de validación del rango 0-10 y la redundancia en las condiciones. La solución reestructura para validar primero el rango 0-10 y luego simplifica las condiciones internas.
3.  El código original no validaba si la nota estaba dentro del rango esperado (0-10). Si se ingresaba -5 o 15, podía dar un resultado incorrecto o no esperado. La solución añade una validación inicial `Si nota >= 0 Y nota <= 10` y un `Sino` para manejar las notas fuera de rango.
</details>
