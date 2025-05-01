# Módulo 1 - Ejercicio 10 (Dificultad 10)

## Enunciado

Escribe un algoritmo para una tienda simple. Debe pedir el nombre de un producto (texto), su precio unitario (real) y la cantidad de unidades compradas (entero). Luego, debe calcular el precio total (precio unitario * cantidad) y mostrar un mensaje como: "El total por [cantidad] unidades de [producto] es: $[total]".

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso CalculoVentaSimple

    Definir producto Como Caracter;
    Definir precioUnitario Como Real;
    Definir cantidad Como Entero;
    Definir total // Pista 1: Falta algo importante al definir la variable 'total'.

    Escribir "Ingrese nombre del producto:";
    Leer producto;
    Escribir "Ingrese precio unitario:";
    Leer precio_Unitario; // Pista 2: ¿Coincide este nombre de variable con el definido?
    Escribir "Ingrese cantidad comprada:";
    Leer cantidad;

    // Calcular total
    total = precioUnitario * cantidad; // Pista 3: Revisa el operador de asignación.

    // Mostrar resultado
    Escribir "El total por ", cantidad, " unidades de ", producto, " es: $", total;

FinProceso
```
<details>
<summary>Mostrar Solución Correcta</summary>
## Solución Correcta

```pseudocode
Proceso CalculoVentaSimple_Solucion

    Definir producto Como Caracter;
    Definir precioUnitario, total Como Real; // Corregido: Definir 'total' y su tipo (Real, ya que puede tener decimales).
    Definir cantidad Como Entero;

    Escribir "Ingrese nombre del producto:";
    Leer producto;
    Escribir "Ingrese precio unitario:";
    Leer precioUnitario; // Corregido: Usar el nombre exacto 'precioUnitario'.
    Escribir "Ingrese cantidad comprada:";
    Leer cantidad;

    // Calcular total
    total <- precioUnitario * cantidad; // Corregido: Usar '<-' para asignar.

    // Mostrar resultado
    Escribir "El total por ", cantidad, " unidades de ", producto, " es: $", total;

FinProceso
```
</details>
<details>
<summary>Mostrar Explicación de la Solución</summary> 
## Explicación de la Solución

1.  Al definir la variable `total`, faltaba especificar su tipo de dato (`Como Real`, ya que la multiplicación de un `Real` por un `Entero` puede dar `Real`). Se añadió `Como Real` a la definición (o se incluyó `total` en la definición de `precioUnitario`).
2.  Al leer el precio, se usó el nombre de variable `precio_Unitario` (con guion bajo), pero se había definido como `precioUnitario` (camelCase). Se debe usar el nombre exacto de la definición. Se corrigió `Leer precio_Unitario` a `Leer precioUnitario`.
3.  Nuevamente, se usó el operador `=` para la asignación en lugar del correcto `<-`. Se corrigió `total = precioUnitario * cantidad` a `total <- precioUnitario * cantidad`.
</details>
