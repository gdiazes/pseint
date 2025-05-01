# Módulo 2 - Ejercicio 9 (Dificultad 9)

## Enunciado
Escribe un algoritmo que pida un número (puede ser positivo, negativo o cero) y muestre su valor absoluto. El valor absoluto de un número es el número sin signo (ej: |-5| = 5, |7| = 7, |0| = 0).

## Código con Errores
```pseudocode
Proceso ValorAbsoluto

    Definir numero, valorAbs Como Real;

    Escribir "Ingrese un número:";
    Leer numero;

    Si numero >= 0 Entonces
        valorAbs = numero; // Pista 1: Revisa el operador de asignación.
    Sino
        valorAbs <- -numero; // Si es negativo, lo convierte a positivo
    // Pista 2: ¿Falta cerrar la estructura condicional?

    Escribir "El valor absoluto de ", numero, " es : ", valorAbs; // Pista 3: Revisa la sintaxis de esta línea Escribir. ¿Hay algún error tipográfico?

FinProceso
```

<details> 
  <summary>Mostrar Solución Correcta</summary> 

## Solución Correcta
```pseudocode
Proceso ValorAbsoluto_Solucion

    Definir numero, valorAbs Como Real;

    Escribir "Ingrese un número:";
    Leer numero;

    Si numero >= 0 Entonces
        valorAbs <- numero; // Corregido: Usar '<-'.
    Sino
        valorAbs <- -numero; // Si es negativo, lo convierte a positivo
    FinSi // Corregido: Añadir 'FinSi'.

    Escribir "El valor absoluto de ", numero, " es: ", valorAbs; // Corregido: Quitar espacio antes de ':'.

FinProceso
```

</details><details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  En el bloque `Entonces`, se usó `=` en lugar del operador de asignación correcto `<-`.
2.  Faltaba la palabra clave `FinSi` para cerrar la estructura `Si/Sino`.
3.  En la línea `Escribir` final, había un espacio extra antes de los dos puntos (`es : `). Aunque no es un error de ejecución grave, es un error de formato/tipeo. Se corrigió a `es: `.

</details>
