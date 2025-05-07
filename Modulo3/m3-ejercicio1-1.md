# Módulo 3 - Ejercicio 1 (Dificultad 1)

## Enunciado
Escribe un algoritmo que pida un número y determine si es positivo, negativo o cero, usando estructuras `Si`/`Sino Si`/`Sino`.

## Código con Errores
```pseudocode
Proceso PositivoNegativoCero

    Definir num Como Real;

    Escribir "Ingrese un número:";
    Leer num;

    Si num > 0 Entonces
        Escribir "El número es positivo."
    Sino Si num < 0 Entonces // Pista 1: Revisa la sintaxis de esta línea, ¿falta algo al final?
        Escribir "El número es negativo.";
    Sino // Pista 2: Si no es positivo ni negativo, ¿qué es? ¿Está bien el mensaje?
        Escribir "El número es positivo o negativo.";
    FinSi // Pista 3: ¿Esta estructura cierra todos los 'Si' abiertos?

FinProceso
```

## Solución Correcta
```pseudocode
Proceso PositivoNegativoCero_Solucion

    Definir num Como Real;

    Escribir "Ingrese un número:";
    Leer num;

    Si num > 0 Entonces
        Escribir "El número es positivo."; // Corregido: Añadir punto y coma si es necesario.
    Sino Si num < 0 Entonces // Correcto (asumiendo ;)
        Escribir "El número es negativo."; // Corregido: Añadir punto y coma si es necesario.
    Sino // Lógica: Si no es > 0 ni < 0, entonces es 0.
        Escribir "El número es cero."; // Corregido: Mensaje correcto para el caso restante.
    FinSi // Correcto: Cierra la estructura Si/Sino Si/Sino.

FinProceso
```

## Explicación de la Solución
1.  Aunque PSeInt puede ser flexible, a menudo se requiere un punto y coma (`;`) al final de cada instrucción. Faltaban en los `Escribir`. (Considerado error menor si el perfil es flexible). La sintaxis `Sino Si` es correcta.
2.  Si un número no es mayor que cero (`num > 0` es falso) y tampoco es menor que cero (`num < 0` es falso), la única posibilidad restante es que sea exactamente cero. El mensaje en el último `Sino` era incorrecto; debe indicar que es cero.
3.  La estructura `Si ... Sino Si ... Sino ... FinSi` está correctamente cerrada con un único `FinSi`. El error no estaba aquí, sino en la lógica del último `Sino`.
```

---
**Archivo: `Modulo3/m3-ejercicio2-2.md`**
```markdown
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
