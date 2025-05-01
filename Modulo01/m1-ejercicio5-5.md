# Módulo 1 - Ejercicio 5 (Dificultad 5)

## Enunciado

Escribe un algoritmo que pida al usuario su nombre y luego lo salude mostrando el mensaje "Hola, [nombre ingresado]!".

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso SaludoPersonalizado

    // Declarar la variable para el nombre
    Definir nombre Como Real; // Pista 1: ¿Es 'Real' el tipo de dato adecuado para un nombre?

    // Pedir el nombre al usuario
    Escribir "Introduce tu nombre: ";
    nombre <- Leer; // Pista 2: La función Leer() necesita ser usada correctamente para asignar el valor a la variable 'nombre'.

    // Mostrar el saludo
    Escribir "Hola, " + nombre + "!"; // Pista 3: Revisa la sintaxis para unir texto y variables al mostrar con 'Escribir'.

FinProceso
```

<details>
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta

```pseudocode
Proceso SaludoPersonalizado_Solucion

    // Declarar la variable para el nombre
    Definir nombre Como Caracter; // Corregido: El tipo debe ser Caracter (o Cadena).

    // Pedir el nombre al usuario
    Escribir "Introduce tu nombre: ";
    Leer nombre; // Corregido: Leer asigna directamente a la variable.

    // Mostrar el saludo
    Escribir "Hola, ", nombre, "!"; // Corregido: Usar comas para concatenar en Escribir.

FinProceso
```

</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución

1.  La variable `nombre` debe ser de tipo `Caracter` (o `Cadena`, según el perfil de PSeInt) para almacenar texto, no `Real` que es para números con decimales.
2.  La instrucción `Leer` se usa directamente con la variable donde se guardará el dato: `Leer nombre;`. No se usa como una función que devuelve un valor para asignar con `<-` en este contexto básico.
3.  La instrucción `Escribir` en PSeInt permite mostrar múltiples elementos separados por comas (`,`). El uso del signo `+` para concatenar cadenas es común en otros lenguajes, pero en PSeInt estándar se usan comas dentro de `Escribir`. Se cambió `+` por `,`.

</details>
