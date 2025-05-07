# Módulo 3 - Ejercicio 7 (Dificultad 7)

## Enunciado
Escribe un algoritmo que pida dos números diferentes y los muestre ordenados de menor a mayor.

## Código con Errores
```pseudocode
Proceso OrdenarDosNumeros

    Definir n1, n2, menor, mayor Como Real;

    Escribir "Ingrese el primer número:";
    Leer n1;
    Escribir "Ingrese el segundo número (diferente):";
    Leer n2;

    Si n1 < n2 Entonces // Pista 1: ¿Está completa la estructura Si/Sino?
        menor <- n1
        mayor <- n2; // Pista 2: Faltan puntos y comas.
    Sino
        menor <- n2;
        mayor <- n1;

    // Pista 3: Falta cerrar el 'Si' inicial.

    Escribir "Números ordenados: ", menor, ", ", mayor;

FinProceso
```

<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso OrdenarDosNumeros_Solucion

    Definir n1, n2, menor, mayor Como Real;

    Escribir "Ingrese el primer número:";
    Leer n1;
    Escribir "Ingrese el segundo número (diferente):";
    Leer n2;

    Si n1 < n2 Entonces
        menor <- n1; // Corregido: Añadir punto y coma (si es necesario).
        mayor <- n2;
    Sino
        menor <- n2;
        mayor <- n1;
    FinSi // Corregido: Añadir 'FinSi'.

    Escribir "Números ordenados: ", menor, ", ", mayor;

FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  La estructura `Si n1 < n2 Entonces ... Sino ...` estaba incompleta porque le faltaba la palabra clave `FinSi` al final para cerrarla.
2.  Faltaban los puntos y comas (`;`) al final de las instrucciones de asignación dentro del bloque `Entonces` (y potencialmente en las del `Sino`, dependiendo de la configuración de PSeInt).
3.  Relacionado con el punto 1, el error fundamental era la ausencia del `FinSi` para delimitar correctamente la estructura condicional.
</details>