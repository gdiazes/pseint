# Módulo 2 - Ejercicio 3 (Dificultad 3)

## Enunciado
Escribe un algoritmo que pida dos números enteros, dividendo y divisor. Calcule y muestre el cociente (división real) y el resto (módulo) de la división entera.

## Código con Errores
```pseudocode
Proceso DivisionYModulo

    Definir dividendo, divisor, resto Como Entero;
    Definir cociente Como Entero; // Pista 1: El cociente de una división, ¿es siempre entero?

    Escribir "Ingrese el dividendo (entero):";
    Leer dividendo;
    Escribir "Ingrese el divisor (entero):";
    Leer divisor;

    cociente <- dividendo / divisor;
    resto <- dividendo % divisor; // Pista 2: Revisa si '%' es el operador de módulo estándar en PSeInt.

    Escribir "Cociente: ", cociente;
    Escribir "Resto: ", resto // Pista 3: Falta algo al final de esta línea.

FinProceso
```
<details>
  
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso DivisionYModulo_Solucion

    Definir dividendo, divisor, resto Como Entero;
    Definir cociente Como Real; // Corregido: El cociente puede tener decimales.

    Escribir "Ingrese el dividendo (entero):";
    Leer dividendo;
    Escribir "Ingrese el divisor (entero):";
    Leer divisor;

    cociente <- dividendo / divisor;
    resto <- dividendo MOD divisor; // Corregido: Usar 'MOD' para el módulo.

    Escribir "Cociente: ", cociente;
    Escribir "Resto: ", resto; // Corregido: Añadir punto y coma final (si es necesario).

FinProceso
```
</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>
  
## Explicación de la Solución
1.  El resultado de una división (`/`), incluso entre enteros, puede ser un número con decimales (ej: 7 / 2 = 3.5). Por lo tanto, la variable `cociente` debe ser de tipo `Real`.
2.  El operador estándar para calcular el módulo (resto de la división entera) en PSeInt es `MOD`, no el símbolo `%` (aunque algunos perfiles flexibles podrían aceptarlo).
3.  Faltaba el punto y coma (`;`) al final de la última instrucción `Escribir`. Aunque PSeInt puede ser permisivo, en modo estricto es necesario.
</details>
