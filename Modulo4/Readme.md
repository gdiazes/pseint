# Módulo 4: Estructuras Repetitivas (Bucles)

## Teoría

Los bucles son herramientas esenciales en programación que nos permiten **ejecutar un bloque de código múltiples veces** sin tener que escribirlo repetidamente. Son fundamentales para procesar listas de datos, realizar cálculos iterativos y controlar el flujo del programa.

### 1. Necesidad de Repetir Instrucciones

Imagina que necesitas mostrar los números del 1 al 5. Podrías escribir:

```pseudocode
Escribir 1;
Escribir 2;
Escribir 3;
Escribir 4;
Escribir 5;
```

Pero ¿y si fueran 100 números? Sería muy tedioso. Los bucles resuelven esto.

### 2. Bucle `Mientras ... Hacer ... FinMientras`

Este bucle ejecuta un bloque de código **mientras** una condición sea `Verdadero`. La condición se evalúa **antes** de cada iteración (vuelta). Si la condición es falsa desde el principio, el bloque de código nunca se ejecuta.

```pseudocode
Mientras <condición> Hacer
    // Instrucciones a repetir mientras la condición sea Verdadera
    // ¡Importante: Algo dentro del bucle debe eventualmente hacer que la condición sea Falsa!
FinMientras
```

**Ejemplo (Números 1 a 5):**

```pseudocode
Proceso EjemploMientras
    Definir contador Como Entero;
    contador <- 1; // Inicialización

    Mientras contador <= 5 Hacer // Condición
        Escribir contador;
        contador <- contador + 1; // Actualización (para evitar bucle infinito)
    FinMientras
FinProceso
```

### 3. Bucle `Repetir ... Hasta Que ...`

Este bucle ejecuta un bloque de código **al menos una vez** y luego evalúa una condición. Si la condición es `Falso`, repite el bloque; si es `Verdadero`, el bucle termina. La condición se evalúa **después** de cada iteración.

```pseudocode
Repetir
    // Instrucciones a repetir
    // Algo aquí debería eventualmente hacer que la condición sea Verdadera
Hasta Que <condición> // Se repite mientras la condición sea Falsa
```

**Ejemplo (Pedir contraseña hasta que sea correcta):**

```pseudocode
Proceso EjemploRepetir
    Definir pwdIngresada, pwdCorrecta Como Caracter;
    pwdCorrecta <- "1234";

    Repetir
        Escribir "Ingrese la contraseña:";
        Leer pwdIngresada;
        Si pwdIngresada <> pwdCorrecta Entonces
            Escribir "Contraseña incorrecta. Intente de nuevo.";
        FinSi
    Hasta Que pwdIngresada = pwdCorrecta; // Termina cuando la contraseña es correcta

    Escribir "Acceso concedido.";
FinProceso
```

### 4. Bucle `Para ... Hacer ... FinPara`

Este bucle es ideal cuando sabes **exactamente cuántas veces** quieres repetir un bloque de código. Utiliza una variable contador que se incrementa (o decrementa) automáticamente en cada iteración.

```pseudocode
Para <variable> <- <valor_inicial> Hasta <valor_final> Con Paso <paso> Hacer
    // Instrucciones a repetir
FinPara
```

*   `<variable>`: Variable numérica que actúa como contador.
*   `<valor_inicial>`: Valor inicial del contador.
*   `<valor_final>`: El bucle continúa mientras el contador sea menor o igual (o mayor o igual si el paso es negativo) que este valor.
*   `Con Paso <paso>`: (Opcional) Cuánto se suma (o resta si es negativo) al contador en cada iteración. Si se omite, el paso es `1`.

**Ejemplo (Números 1 a 5):**

```pseudocode
Proceso EjemploPara
    Definir i Como Entero;

    Para i <- 1 Hasta 5 Con Paso 1 Hacer // 'Con Paso 1' es opcional aquí
        Escribir i;
    FinPara
FinProceso
```

**Ejemplo (Números Pares del 10 al 2, descendente):**

```pseudocode
Proceso EjemploParaDescendente
    Definir num Como Entero;

    Para num <- 10 Hasta 2 Con Paso -2 Hacer
        Escribir num;
    FinPara // Muestra: 10, 8, 6, 4, 2
FinProceso
```

### 5. Contadores y Acumuladores

Son variables que se usan comúnmente dentro de los bucles:

*   **Contador:** Variable (generalmente entera) que se incrementa (o decrementa) en una cantidad fija (usualmente 1) en cada iteración para llevar la cuenta de cuántas veces se ha ejecutado el bucle o cuántos elementos cumplen una condición.
    `contador <- contador + 1`
*   **Acumulador:** Variable (puede ser entera o real) que va sumando (o multiplicando, etc.) valores variables en cada iteración para obtener un total.
    `suma <- suma + valorActual`

**Ejemplo (Sumar los primeros 5 números):**

```pseudocode
Proceso SumaConAcumulador
    Definir i, suma Como Entero;
    suma <- 0; // Inicializar acumulador

    Para i <- 1 Hasta 5 Hacer
        suma <- suma + i; // Acumula el valor de 'i'
    FinPara

    Escribir "La suma de 1 a 5 es: ", suma; // Muestra 15
FinProceso
```

### 6. Bucles Anidados

Puedes colocar un bucle dentro de otro. Esto es útil para trabajar con estructuras bidimensionales (como matrices, que veremos más adelante) o para realizar tareas repetitivas complejas.

**Ejemplo (Tabla de multiplicar básica del 1 al 3):**

```pseudocode
Proceso TablaMultiplicarAnidada
    Definir i, j, resultado Como Entero;

    Para i <- 1 Hasta 3 Hacer // Bucle externo (para cada tabla)
        Escribir "Tabla del ", i, ":";
        Para j <- 1 Hasta 10 Hacer // Bucle interno (para cada multiplicación)
            resultado <- i * j;
            Escribir i, " x ", j, " = ", resultado;
        FinPara
        Escribir ""; // Línea en blanco para separar tablas
    FinPara
FinProceso
```

### 7. Cómo Elegir el Bucle Adecuado

*   **`Para`:** Cuando sabes de antemano el número de repeticiones o quieres iterar sobre un rango definido.
*   **`Mientras`:** Cuando la repetición depende de una condición que puede ser falsa desde el inicio y no sabes cuántas veces se ejecutará.
*   **`Repetir`:** Cuando necesitas que el bloque se ejecute al menos una vez y la condición de parada se verifica al final.

---

## Ejercicios del Módulo 4

1.  [Ejercicio 1 (Dificultad 1): Números del 1 al 10 (Para)](./m4-ejercicio1-1.md)
2.  [Ejercicio 2 (Dificultad 2): Números Pares del 2 al 20 (Mientras)](./m4-ejercicio2-2.md)
3.  [Ejercicio 3 (Dificultad 3): Suma de los Primeros N Números (Para)](./m4-ejercicio3-3.md)
4.  [Ejercicio 4 (Dificultad 4): Tabla de Multiplicar de un Número (Para)](./m4-ejercicio4-4.md)
5.  [Ejercicio 5 (Dificultad 5): Validar Entrada (Repetir)](./m4-ejercicio5-5.md)
6.  [Ejercicio 6 (Dificultad 6): Factorial de un Número (Para)](./m4-ejercicio6-6.md)
7.  [Ejercicio 7 (Dificultad 7): Adivina el Número (Mientras)](./m4-ejercicio7-7.md)
8.  [Ejercicio 8 (Dificultad 8): Promedio de N Notas (Para/Acumulador)](./m4-ejercicio8-8.md)
9.  [Ejercicio 9 (Dificultad 9): Contador de Positivos, Negativos y Ceros (Mientras/Contador)](./m4-ejercicio9-9.md)
10. [Ejercicio 10 (Dificultad 10): Dibujar Cuadrado con Asteriscos (Anidados)](./m4-ejercicio10-10.md)
