# Módulo 3 - Ejercicio 9 (Dificultad 9)

## Enunciado
Escribe un algoritmo que calcule el Índice de Masa Corporal (IMC = peso / altura^2). Pide al usuario su peso en kg (real) y su altura en metros (real). Luego, clasifica el resultado según la OMS:
*   < 18.5: Bajo peso
*   18.5 a 24.9: Peso normal
*   25.0 a 29.9: Sobrepeso
*   >= 30.0: Obesidad

## Código con Errores
```pseudocode
Proceso CalcularIMC

    Definir peso, altura, imc Como Real;

    Escribir "Ingrese su peso en kg:";
    Leer peso;
    Escribir "Ingrese su altura en metros:";
    Leer altura;

    // Calcular IMC si la altura es válida
    Si altura >= 0 Entonces // Pista 1: ¿Puede la altura ser exactamente 0 para calcular IMC?
        imc <- peso / (altura ^ 2);

        Escribir "Su IMC es: ", imc;

        // Clasificar
        Si imc < 18.5 Entonces
            Escribir "Clasificación: Bajo peso";
        Sino Si imc >= 18.5 O imc <= 24.9 Entonces // Pista 2: ¿Debe cumplirse una condición ('O') o ambas ('Y') para estar en este rango?
            Escribir "Clasificación: Peso normal";
        Sino Si imc >= 25.0 Y imc <= 29.9 Entonces
            Escribir "Clasificación: Sobrepeso";
        Sino // Si no es ninguno de los anteriores, y es >= 30
            Escribir "Clasificación: Obeso"; // Pista 3: Falta cerrar la estructura interna.
        // FinSi faltante
    Sino
        Escribir "Altura inválida.";
    FinSi

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

1.  Para calcular el IMC, la altura no puede ser cero (división por cero) y tanto altura como peso deben ser valores positivos. La condición inicial `altura >= 0` era insuficiente. Se cambió a `altura > 0 Y peso > 0`.
2.  Para estar en el rango de "Peso normal" (18.5 a 24.9), el IMC debe cumplir *ambas* condiciones: ser mayor o igual a 18.5 **Y** ser menor o igual a 24.9. El operador `O` era incorrecto. Sin embargo, en una estructura `Si/Sino Si`, si llegamos a `Sino Si imc <= 24.9`, ya sabemos que la condición anterior (`imc < 18.5`) fue falsa, lo que implica que `imc >= 18.5`. Por lo tanto, solo necesitamos verificar el límite superior (`imc <= 24.9`). Lo mismo aplica para el sobrepeso.
3.  Faltaba un `FinSi` para cerrar la estructura condicional anidada que realizaba la clasificación del IMC.
</details>