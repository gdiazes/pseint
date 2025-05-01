# Módulo 1 - Ejercicio 6 (Dificultad 6)

## Enunciado

Escribe un algoritmo que pida al usuario dos números enteros, los guarde en variables `a` y `b`, intercambie sus valores (que `a` tenga el valor de `b` y `b` el valor de `a`) y finalmente muestre los valores intercambiados.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso IntercambioVariables

    Definir a, b, aux Como Entero;

    Escribir "Ingrese el primer número (a):";
    Leer a;
    Escribir "Ingrese el segundo número (b):";
    Leer b;

    Escribir "Valores originales: a=", a, ", b=", b;

    // Intentar intercambiar valores
    a <- b;
    b <- a; // Pista 1: Si 'a' ya tiene el valor de 'b', ¿qué valor estás asignando aquí a 'b'? Piensa si necesitas algo más.

    aux <- a; // Pista 2: La variable 'aux' se usa para guardar temporalmente un valor. ¿Se está usando en el momento correcto?

    Escribir "Valores intercambiados: a=", a, ", b="; b; // Pista 3: Revisa la sintaxis al final de esta línea de 'Escribir'.

FinProceso
```

<details>
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta

```pseudocode
Proceso IntercambioVariables_Solucion

    Definir a, b, aux Como Entero;

    Escribir "Ingrese el primer número (a):";
    Leer a;
    Escribir "Ingrese el segundo número (b):";
    Leer b;

    Escribir "Valores originales: a=", a, ", b=", b;

    // Intercambiar valores usando una variable auxiliar
    aux <- a; // Guarda el valor original de 'a'
    a <- b;   // 'a' ahora tiene el valor de 'b'
    b <- aux; // 'b' toma el valor original de 'a' que estaba en 'aux'

    Escribir "Valores intercambiados: a=", a, ", b=", b; // Corregido: Sin punto y coma extra en medio.

FinProceso
```

</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución

1.  El error lógico principal está en el intento de intercambio. Al hacer `a <- b`, el valor original de `a` se pierde. Luego, al hacer `b <- a`, se le asigna a `b` el valor que `a` acaba de recibir (que es el valor original de `b`), por lo que ambas variables terminan con el valor original de `b`. La solución correcta requiere una variable auxiliar (`aux`) para guardar temporalmente uno de los valores antes de sobrescribirlo.
2.  La variable `aux` se usaba *después* de que el valor original de `a` ya se había perdido. Debe usarse *antes* de la primera asignación (`a <- b`) para guardar el valor original de `a`. El orden correcto es: `aux <- a`, luego `a <- b`, y finalmente `b <- aux`.
3.  En la última línea `Escribir`, había un punto y coma (`;`) después de `"b="`, separando incorrectamente la variable `b` del resto de la instrucción. Se eliminó ese punto y coma.

</details>
