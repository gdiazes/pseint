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
	
    // Calcular IMC si la altura Y EL PESO son válidos
    // Pista 1 Corregida: La altura debe ser mayor que 0 para evitar división por cero.
    // Adicionalmente, el peso también debe ser mayor que 0 para un IMC con sentido.
    Si altura > 0 Y peso > 0 Entonces // Si EXTERNO (Inicio en línea 11)
        imc <- peso / (altura ^ 2);
		
        Escribir "Su IMC es: ", imc;
		
        // Clasificar CON ANIDACIÓN EXPLÍCITA Y ESTRICTA
        Si imc < 18.5 Entonces // Si Interno Nivel 1
            Escribir "Clasificación: Bajo peso";
        Sino // Sino de Si Interno Nivel 1
            // Pista 2 Corregida: Para estar en el rango de "Peso normal", ambas condiciones deben cumplirse (Y lógico).
            // Ya sabemos que imc no es < 18.5 por el flujo.
            Si imc <= 24.9 Entonces // Si Interno Nivel 2 (Condición simplificada: ya sabemos >=18.5)
                Escribir "Clasificación: Peso normal";
            Sino // Sino de Si Interno Nivel 2
                // Ya sabemos que imc no es <= 24.9 por el flujo.
                Si imc <= 29.9 Entonces // Si Interno Nivel 3 (Condición simplificada: ya sabemos >=25.0)
                    Escribir "Clasificación: Sobrepeso";
                Sino // Sino de Si Interno Nivel 3 (Si no es ninguno de los anteriores, es >= 30)
                    Escribir "Clasificación: Obeso";
                FinSi // Cierra Si Interno Nivel 3 (imc <= 29.9)
            FinSi     // Cierra Si Interno Nivel 2 (imc <= 24.9)
        FinSi         // Cierra Si Interno Nivel 1 (imc < 18.5)
        // Fin de la clasificación anidada
		
    Sino // Este Sino pertenece al Si EXTERNO (altura > 0 Y peso > 0)
        // Mensaje de error mejorado para cubrir ambas validaciones.
        Escribir "Altura o peso inválidos. Ambos deben ser mayores que cero."; // Esta sería aproximadamente tu línea problemática
    FinSi // ESTE FinSi CIERRA el Si EXTERNO. (Aproximadamente tu línea 33)

FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución

1.  Para calcular el IMC, la altura no puede ser cero (división por cero) y tanto altura como peso deben ser valores positivos. La condición inicial `altura >= 0` era insuficiente. Se cambió a `altura > 0 Y peso > 0`.
2.  Para estar en el rango de "Peso normal" (18.5 a 24.9), el IMC debe cumplir *ambas* condiciones: ser mayor o igual a 18.5 **Y** ser menor o igual a 24.9. El operador `O` era incorrecto. Sin embargo, en una estructura `Si/Sino Si`, si llegamos a `Sino Si imc <= 24.9`, ya sabemos que la condición anterior (`imc < 18.5`) fue falsa, lo que implica que `imc >= 18.5`. Por lo tanto, solo necesitamos verificar el límite superior (`imc <= 24.9`). Lo mismo aplica para el sobrepeso.
3.  Faltaba un `FinSi` para cerrar la estructura condicional anidada que realizaba la clasificación del IMC.
</details>