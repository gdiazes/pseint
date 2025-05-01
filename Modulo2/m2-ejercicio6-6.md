# Módulo 2 - Ejercicio 6 (Dificultad 6)

## Enunciado
Una tienda ofrece un 10% de descuento si el monto total de la compra es superior a $1000. Escribe un algoritmo que pida el monto total de la compra y calcule el precio final a pagar (aplicando el descuento si corresponde).

## Código con Errores
```pseudocode
Proceso CalcularDescuento

    Definir montoCompra, precioFinal Como Real;
    Definir descuento Como Real;
    descuento <- 0.10; // 10%

    Escribir "Ingrese el monto total de la compra:";
    Leer monto_Compra; // Pista 1: Verifica la consistencia del nombre de la variable.

    precioFinal <- montoCompra; // Inicializar precio final

    Si montoCompra < 1000 Entonces // Pista 2: ¿Cuál es la condición para aplicar el descuento? (superior a 1000)
        montoDescontado = montoCompra * descuento; // Pista 3: Revisa el operador de asignación y si esta variable fue definida.
        precioFinal <- montoCompra - montoDescontado;
    FinSi

    Escribir "El precio final a pagar es: $", precioFinal;

FinProceso
```

<details> 
    <summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso CalcularDescuento_Solucion

    Definir montoCompra, precioFinal, montoDescontado Como Real; // Corregido: Definir montoDescontado.
    Definir descuento Como Real;
    descuento <- 0.10; // 10%

    Escribir "Ingrese el monto total de la compra:";
    Leer montoCompra; // Corregido: Nombre de variable consistente.

    precioFinal <- montoCompra; // Inicializar precio final

    Si montoCompra > 1000 Entonces // Corregido: Condición correcta para aplicar descuento (> 1000).
        montoDescontado <- montoCompra * descuento; // Corregido: Usar '<-' y variable definida.
        precioFinal <- montoCompra - montoDescontado;
    FinSi
    // Si no se cumple la condición, precioFinal mantiene el valor original de montoCompra.

    Escribir "El precio final a pagar es: $", precioFinal;

FinProceso
```

</details>

<details>
    <summary>Mostrar Explicación de la Solución</summary>
    
## Explicación de la Solución
1.  Se definió la variable como `montoCompra` pero se intentó leer en `monto_Compra`. Se corrigió `Leer` para usar el nombre definido.
2.  La condición para aplicar el descuento es que la compra sea *superior* a $1000, es decir, `montoCompra > 1000`. La condición original era `montoCompra < 1000`, que haría lo contrario.
3.  Dentro del `Si`, se usó `=` en lugar de `<-` para la asignación. Además, la variable `montoDescontado` no había sido definida. Se añadió `montoDescontado` a la lista de `Definir` y se corrigió el operador a `<-`.

</details>
