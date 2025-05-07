# Módulo 3 - Ejercicio 2 (Dificultad 2)

## Enunciado
Escribe un algoritmo que pida un número de día de la semana (1 para Lunes, ..., 7 para Domingo) e indique si es un día laboral (Lunes a Viernes) o fin de semana (Sábado o Domingo), usando estructuras `Si`/`Sino Si`/`Sino`.

## Código con Errores
```pseudocode
Proceso DiaLaboralSi

    Definir dia Como Entero;

    Escribir "Ingrese número de día (1-7):";
    Leer dia;

    Si dia >= 1 Y dia =< 5 Entonces // Pista 1: Revisa el operador "menor o igual".
        Escribir "Es un día laboral.";
    Sino Si dia == 6 O dia == 7 Entonces // Pista 2: Revisa el operador de igualdad para comparación.
        Escribir "Es fin de semana."
    Sino // Pista 3: ¿Qué pasa si el número no está entre 1 y 7? ¿Falta manejar ese caso?
        // No hay mensaje para día inválido
    FinSi

FinProceso
```

## Solución Correcta
```pseudocode
Proceso DiaLaboralSi_Solucion

    Definir dia Como Entero;

    Escribir "Ingrese número de día (1-7):";
    Leer dia;

    Si dia >= 1 Y dia <= 5 Entonces // Corregido: Operador correcto es '<='.
        Escribir "Es un día laboral.";
    Sino Si dia = 6 O dia = 7 Entonces // Corregido: Operador de igualdad es '='.
        Escribir "Es fin de semana.";
    Sino // Añadido: Manejo del caso inválido.
        Escribir "Número de día inválido.";
    FinSi

FinProceso
```

## Explicación de la Solución
1.  El operador relacional para "menor o igual que" es `<=`, no `=<`. Se corrigió en la primera condición.
2.  El operador para comparar si dos valores son iguales en PSeInt es un solo signo de igual (`=`), no doble (`==`) como en otros lenguajes. Se corrigió en la segunda condición.
3.  El código original no manejaba el caso en que el usuario ingresara un número fuera del rango 1-7 (ej: 0, 8, -2). Se añadió un mensaje en el último `Sino` para indicar que el número de día es inválido.
