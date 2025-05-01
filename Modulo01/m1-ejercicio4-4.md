# Módulo 1 - Ejercicio 4 (Dificultad 4)

## Enunciado

Escribe un algoritmo que calcule el área de un rectángulo. Debe pedir al usuario la longitud de la base y la altura (pueden tener decimales) y luego mostrar el área calculada. Fórmula: Área = Base * Altura.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso AreaRectangulo

    Definir base, altura, area Como Entero; // Pista 1: Si la base y altura pueden tener decimales, ¿'Entero' es adecuado para ellas y para el área?

    Escribir "Ingrese la base del rectángulo:";
    Leer base

    Escribir "Ingrese la altura del rectángulo:";
    Leer altura; // Pista 2: Revisa si falta algo al final de la instrucción 'Leer base'.

    area = base * altura; // Pista 3: Revisa el operador de asignación y la fórmula.

    Escribir "El área del rectángulo es: ", area;

FinProceso
```

<details>
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta

```pseudocode
Proceso AreaRectangulo_Solucion

    Definir base, altura, area Como Real; // Corregido: Usar 'Real' para permitir decimales.

    Escribir "Ingrese la base del rectángulo:";
    Leer base; // Corregido: Añadir punto y coma al final (requerido en algunas configuraciones/modo estricto).

    Escribir "Ingrese la altura del rectángulo:";
    Leer altura;

    area <- base * altura; // Corregido: Usar '<-' para asignar. La fórmula está bien.

    Escribir "El área del rectángulo es: ", area;

FinProceso
```

</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución

1.  Dado que la base y la altura pueden tener decimales (ej: 5.5 cm), y el resultado de multiplicarlos también puede tenerlos, el tipo de dato adecuado para las tres variables (`base`, `altura`, `area`) es `Real`. Se cambió `Entero` por `Real`.
2.  En configuraciones más estrictas de PSeInt, cada instrucción debe terminar con punto y coma (`;`). Faltaba en la línea `Leer base`. Se añadió.
3.  El operador de asignación correcto es `<-`, no `=`. Se corrigió `area = base * altura` a `area <- base * altura`. La fórmula matemática (multiplicación) era correcta.

</details>
