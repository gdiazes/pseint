# Módulo 1 - Ejercicio 8 (Dificultad 8)

## Enunciado

Escribe un algoritmo que pida al usuario su edad (un número entero) y determine si es mayor de edad (18 años o más). Guarda el resultado (Verdadero o Falso) en una variable lógica y muéstrala.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso VerificarMayoriaEdad

    Definir edad Como Entero;
    Definir es_mayor Como Logico; // Pista 1: Revisa si el nombre de la variable 'es_mayor' sigue las convenciones (o si hay caracteres inválidos).

    Escribir "Ingrese su edad:";
    Leer edad;

    // Asignar el resultado de la comparación a la variable lógica
    esMayor <- edad > 18; // Pista 2: ¿La condición "mayor de 18" incluye exactamente los 18 años?

    Escribir "Es mayor de edad?: ", es_Mayor; // Pista 3: PSeInt distingue entre mayúsculas y minúsculas en los nombres de variables. ¿Coincide con la definición?

FinProceso
```
<details>
<summary>Mostrar Solución Correcta</summary>
## Solución Correcta

```pseudocode
Proceso VerificarMayoriaEdad_Solucion

    Definir edad Como Entero;
    Definir esMayor Como Logico; // Corregido: Nombre de variable válido (sin guion bajo, o usando uno consistentemente).

    Escribir "Ingrese su edad:";
    Leer edad;

    // Asignar el resultado de la comparación a la variable lógica
    esMayor <- edad >= 18; // Corregido: Usar '>=' (mayor o igual) para incluir los 18 años.

    Escribir "Es mayor de edad?: ", esMayor; // Corregido: Usar el nombre exacto 'esMayor'.

FinProceso
```
</details>
<details>
<summary>Mostrar Explicación de la Solución</summary>
## Explicación de la Solución

1.  Aunque PSeInt puede ser flexible, los nombres de variables estándar no suelen usar guiones (`-`) y pueden tener problemas con guiones bajos (`_`) dependiendo de la configuración. Es más seguro usar `camelCase` como `esMayor`. Se cambió `es_mayor` por `esMayor`. (Si se usara `es_mayor` consistentemente estaría bien, pero el error 3 mostraba inconsistencia).
2.  El enunciado pide verificar si es "18 años o más". La condición `edad > 18` solo sería verdadera para edades de 19 en adelante. Para incluir los 18 años, la comparación correcta es `edad >= 18` (mayor o igual a 18).
3.  PSeInt, por defecto (o en modo estricto), distingue entre mayúsculas y minúsculas (es *case-sensitive*). La variable se definió como `esMayor` (o `es_mayor`) pero se intentó mostrar como `es_Mayor` (con M mayúscula). Se debe usar exactamente el mismo nombre que en la definición: `esMayor`.
</details>
