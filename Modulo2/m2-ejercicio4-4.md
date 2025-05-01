# Módulo 2 - Ejercicio 4 (Dificultad 4)

## Enunciado
Escribe un algoritmo que pida un número entero e indique si es par o impar. (Un número es par si el resto de dividirlo por 2 es 0).

## Código con Errores
```pseudocode
Proceso ParOImpar

    Definir num Como Entero;

    Escribir "Ingrese un número entero:";
    Leer num;

    resultado <- num MOD 2; // Pista 1: Falta definir la variable 'resultado'.

    Si resultado = 0 Entonces
        Escribir "El número es impar."; // Pista 2: Si el resto es 0, ¿el número es par o impar?
    Sino
        Escribir "El número es par."; // Pista 3: Revisa la lógica, este mensaje debería estar en el 'Entonces'.
    FinSi

FinProceso
```
<details>
  
<summary>Mostrar Solución Correcta</summary>
  
## Solución Correcta
```pseudocode
Proceso ParOImpar_Solucion

    Definir num, resultado Como Entero; // Corregido: Definir la variable 'resultado'.

    Escribir "Ingrese un número entero:";
    Leer num;

    resultado <- num MOD 2;

    Si resultado = 0 Entonces
        Escribir "El número es par."; // Corregido: Mensaje correcto para resto 0.
    Sino
        Escribir "El número es impar."; // Corregido: Mensaje correcto para resto distinto de 0.
    FinSi

FinProceso
```
</details>

<details>
<summary>Mostrar Explicación de la Solución</summary>
  
## Explicación de la Solución
1.  La variable `resultado` se usó para almacenar el módulo, pero no se definió previamente con `Definir`. Se añadió `resultado` a la definición de variables enteras.
2.  Si el resto de dividir por 2 (`resultado`) es 0, significa que el número es par. El mensaje original decía "impar". Se corrigió el mensaje dentro del `Entonces`.
3.  Consecuentemente, si el resto no es 0 (bloque `Sino`), el número es impar. El mensaje original decía "par". Se corrigió el mensaje dentro del `Sino`. Los mensajes estaban intercambiados.

</details>
