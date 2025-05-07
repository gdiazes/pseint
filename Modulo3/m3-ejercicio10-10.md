# Módulo 3 - Ejercicio 10 (Dificultad 10)

## Enunciado
Simula un menú básico de cajero automático. Define un saldo inicial. Muestra las opciones: 1. Consultar Saldo, 2. Depositar, 3. Retirar, 4. Salir. Pide al usuario elegir una opción (usando `Segun`).
*   Si elige 1, muestra el saldo.
*   Si elige 2, pide una cantidad a depositar (positiva), la suma al saldo y muestra el nuevo saldo.
*   Si elige 3, pide una cantidad a retirar (positiva), verifica si hay saldo suficiente, la resta (si es posible) y muestra el nuevo saldo o un mensaje de error.
*   Si elige 4, muestra "Gracias por usar el cajero."
*   Si elige otra opción, muestra "Opción no válida."

## Código con Errores
```pseudocode
Proceso MenuCajero

    Definir saldoInicial, saldoActual, deposito, retiro Como Real;
    Definir opcion Como Entero;

    saldoInicial <- 1000.0;
    saldoActual <- saldoInicial;

    Escribir "Bienvenido al Cajero Automático";
    Escribir "1. Consultar Saldo";
    Escribir "2. Depositar";
    Escribir "3. Retirar";
    Escribir "4. Salir";
    Escribir "Elija una opción:";
    Leer opcion;

    Segun (opcion) Hacer // Pista 1: ¿Son necesarios los paréntesis alrededor de 'opcion'?
        1:
            Escribir "Su saldo actual es: $", saldoActual;
        2:
            Escribir "Ingrese cantidad a depositar:";
            Leer deposito;
            Si deposito > 0 Entonces
                saldoActual <- saldoActual + deposito;
                Escribir "Depósito exitoso. Nuevo saldo: $", saldoActual;
            Sino
                Escribir "Cantidad a depositar debe ser positiva.";
            FinSi
        3:
            Escribir "Ingrese cantidad a retirar:";
            Leer retiro;
            Si retiro > 0 Entonces
                Si retiro <= saldoActual // Verifica fondos
                    saldoActual <- saldoActual - retiro;
                    Escribir "Retiro exitoso. Nuevo saldo: $", saldoActual;
                Sino
                    Escribir "Saldo insuficiente.";
                FinSi // Pista 2: ¿Está bien indentado/cerrado este FinSi respecto al Si de retiro > 0? (Es correcto, pero revisa la lógica completa)
            Else // Pista 3: ¿Es 'Else' la palabra clave correcta para el 'Sino'?
                Escribir "Cantidad a retirar debe ser positiva.";
            FinSi
        4:
            Escribir "Gracias por usar el cajero.";
        De Otro Modo:
            Escribir "Opción no válida.";
    FinSegun

FinProceso
```

<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso MenuCajero_Solucion

    Definir saldoInicial, saldoActual, deposito, retiro Como Real;
    Definir opcion Como Entero;

    saldoInicial <- 1000.0;
    saldoActual <- saldoInicial;

    Escribir "Bienvenido al Cajero Automático";
    Escribir "1. Consultar Saldo";
    Escribir "2. Depositar";
    Escribir "3. Retirar";
    Escribir "4. Salir";
    Escribir "Elija una opción:";
    Leer opcion;

    Segun opcion Hacer // Corregido: Paréntesis no necesarios (aunque PSeInt flexible puede aceptarlos).
        1:
            Escribir "Su saldo actual es: $", saldoActual;
        2:
            Escribir "Ingrese cantidad a depositar:";
            Leer deposito;
            Si deposito > 0 Entonces
                saldoActual <- saldoActual + deposito;
                Escribir "Depósito exitoso. Nuevo saldo: $", saldoActual;
            Sino
                Escribir "Cantidad a depositar debe ser positiva.";
            FinSi
        3:
            Escribir "Ingrese cantidad a retirar:";
            Leer retiro;
            Si retiro > 0 Entonces
                Si retiro <= saldoActual Entonces // Verifica fondos
                    saldoActual <- saldoActual - retiro;
                    Escribir "Retiro exitoso. Nuevo saldo: $", saldoActual;
                Sino
                    Escribir "Saldo insuficiente.";
                FinSi // Este FinSi cierra el Si de verificación de fondos.
            Sino // Corregido: Palabra clave 'Sino'.
                Escribir "Cantidad a retirar debe ser positiva.";
            FinSi // Este FinSi cierra el Si de retiro > 0.
        4:
            Escribir "Gracias por usar el cajero.";
        De Otro Modo:
            Escribir "Opción no válida.";
    FinSegun

FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  Los paréntesis alrededor de la variable en la instrucción `Segun (opcion) Hacer` no son necesarios en la sintaxis estándar de PSeInt, aunque algunos perfiles flexibles podrían permitirlos. Se quitaron para seguir la sintaxis común: `Segun opcion Hacer`.
2.  La indentación y el `FinSi` interno (el que cierra la comprobación de `retiro <= saldoActual`) estaban correctos. El problema estaba en el `Else` (ver punto 3).
3.  La palabra clave para la alternativa en una estructura condicional es `Sino`, no `Else` (que es común en otros lenguajes). Se corrigió `Else` a `Sino`. Además, faltaba un `FinSi` para cerrar la condición externa `Si retiro > 0`. La solución lo incluye correctamente.
</details>