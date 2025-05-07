# Módulo 3 - Ejercicio 8 (Dificultad 8)

## Enunciado
Un estacionamiento cobra $15 por la primera hora o fracción. Después de la primera hora, cobra $10 por cada hora o fracción adicional. Escribe un algoritmo que pida el número de horas que estuvo el vehículo (puede ser real, ej: 2.5 horas) y calcule el total a pagar.

## Código con Errores
```pseudocode
Proceso TarifaEstacionamiento

    Definir horasEstacionado, totalPagar Como Real;
    Definir horasEnteras Como Entero; // Pista 1: ¿Necesitas esta variable? Considera la función Techo o Trunc.

    tarifaInicial <- 15.0;
    tarifaAdicional <- 10.0;

    Escribir "Ingrese el número de horas estacionado:";
    Leer horasEstacionado;

    Si horasEstacionado <= 1 Entonces
        totalPagar = tarifaInicial; // Pista 2: Operador de asignación.
    Sino
        // Calcular horas adicionales (la parte entera *después* de la primera hora)
        horasAdicionales <- Techo(horasEstacionado - 1); // Techo redondea hacia arriba
        totalPagar <- tarifaInicial + horasAdicionales * tarifaAdicional;
    FinSi

    Escribir "Total a pagar: $", TotalPagar; // Pista 3: ¿Coincide el nombre de la variable con su definición (mayúsculas/minúsculas)?

FinProceso
```

<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso TarifaEstacionamiento_Solucion_Alternativa
	
    Definir horasEstacionado, totalPagar Como Real;
    Definir horasEnterasTotales Como Entero;
	
    Definir tarifaInicial, tarifaAdicional Como Real;
    tarifaInicial <- 15.0;
    tarifaAdicional <- 10.0;
	
    Escribir "Ingrese el número de horas estacionado:";
    Leer horasEstacionado;
	
    // Validar entrada no negativa
    Si horasEstacionado > 0 Entonces
        Si horasEstacionado <= 1 Entonces
            totalPagar <- tarifaInicial;
        Sino
          
            horasEnterasTotales <- Trunc(horasEstacionado); // Obtiene la parte entera
			
            // Si horasEstacionado tiene una parte decimal (es decir, no es un entero exacto),
            // entonces necesitamos sumar 1 a la parte entera para redondear hacia arriba.
            // Ej: horasEstacionado = 2.3 -> Trunc(2.3) = 2. Como 2.3 > 2, sumamos 1 -> 3.
            // Ej: horasEstacionado = 2.0 -> Trunc(2.0) = 2. Como 2.0 no es > 2, no sumamos 1 -> 2.
            Si horasEstacionado > horasEnterasTotales Entonces
                horasEnterasTotales <- horasEnterasTotales + 1;
            FinSi
			
            totalPagar <- tarifaInicial + (horasEnterasTotales - 1) * tarifaAdicional;
        FinSi
        Escribir "Total a pagar: $", totalPagar;
    Sino
        Escribir "Número de horas debe ser positivo.";
    FinSi
	
FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  La variable `horasEnteras` no se usaba en el código original con errores. La lógica correcta (ver punto 3) sí puede beneficiarse de una variable para las horas redondeadas, como `horasAdicionalesEnteras` o `horasEnterasTotales` en la solución.
2.  En el bloque `Si horasEstacionado <= 1`, se usó `=` en lugar del operador de asignación `<-`.
3.  Había un error lógico sutil en el cálculo original `horasAdicionales <- Techo(horasEstacionado - 1)`. Por ejemplo, para 2.0 horas, esto daría `Techo(1.0) = 1` hora adicional, total $15 + 1*$10 = $25. Para 2.1 horas, daría `Techo(1.1) = 2` horas adicionales, total $15 + 2*$10 = $35. La forma correcta es redondear el total de horas hacia arriba (`Techo(horasEstacionado)`) y luego calcular el costo: `tarifaInicial + (horasEnterasTotales - 1) * tarifaAdicional`. Además, al mostrar el resultado, se usó `TotalPagar` (con mayúscula) en lugar de `totalPagar` (definido con minúscula). Se corrigió la lógica y el nombre de la variable. Se añadió también validación para horas positivas.
</details>