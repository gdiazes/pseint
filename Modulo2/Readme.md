# Módulo 2: Operadores y Expresiones Condicionales Simples

## Teoría

En este módulo, aprenderemos a realizar cálculos y a tomar decisiones básicas en nuestros algoritmos.

### 1. Operadores Aritméticos

Son los símbolos que nos permiten realizar operaciones matemáticas:

*   `+` : Suma
*   `-` : Resta
*   `*` : Multiplicación
*   `/` : División
*   `^` : Potencia
*   `%` o `MOD` : Módulo (resto de la división entera)

**Ejemplo:**

```pseudocode
Proceso EjemploAritmeticos
    Definir a, b, suma, resto Como Entero;
    a <- 10;
    b <- 3;
    suma <- a + b;  // suma valdrá 13
    resto <- a MOD b; // resto valdrá 1 (10 dividido 3 es 3 con resto 1)
    Escribir "Suma: ", suma, ", Resto: ", resto;
FinProceso
```

### 2. Operadores Relacionales

Se usan para comparar dos valores. El resultado de una comparación es siempre un valor lógico (`Verdadero` o `Falso`).

*   `>` : Mayor que
*   `<` : Menor que
*   `=` : Igual que (*Ojo: en PSeInt es un solo igual para comparación*)
*   `>=` : Mayor o igual que
*   `<=` : Menor o igual que
*   `<>` : Distinto que

**Ejemplo:**

```pseudocode
Proceso EjemploRelacionales
    Definir edad Como Entero;
    Definir esMayor, esIgual Como Logico;
    edad <- 20;
    esMayor <- edad >= 18; // esMayor valdrá Verdadero
    esIgual <- edad = 25;  // esIgual valdrá Falso
    Escribir "Mayor de edad?: ", esMayor, ", Tiene 25?: ", esIgual;
FinProceso
```

### 3. Operadores Lógicos

Permiten combinar varias condiciones (expresiones lógicas).

*   `Y` (o `&`): Devuelve `Verdadero` si **ambas** condiciones son verdaderas.
*   `O` (o `|`): Devuelve `Verdadero` si **al menos una** de las condiciones es verdadera.
*   `NO` (o `~`): Invierte el valor lógico de una condición (Verdadero se vuelve Falso, y viceversa).

**Ejemplo:**

```pseudocode
Proceso EjemploLogicos
    Definir nota Como Real;
    Definir estaAprobado, esExcelente Como Logico;
    nota <- 7.5;
    estaAprobado <- nota >= 4;           // Verdadero
    esExcelente <- nota >= 9;            // Falso
    // ¿Está aprobado Y es excelente?
    Escribir "Aprobado y excelente?: ", estaAprobado Y esExcelente; // Falso
    // ¿Está aprobado O es excelente?
    Escribir "Aprobado o excelente?: ", estaAprobado O esExcelente; // Verdadero
    // ¿NO está aprobado?
    Escribir "No está aprobado?: ", NO estaAprobado; // Falso
FinProceso
```

### 4. Jerarquía de Operadores

PSeInt (como la mayoría de los lenguajes) evalúa las expresiones en un orden específico:

1.  Paréntesis `()`
2.  Potencia `^`
3.  Multiplicación `*`, División `/`, Módulo `MOD` (de izquierda a derecha)
4.  Suma `+`, Resta `-` (de izquierda a derecha)
5.  Relacionales `>`, `<`, `=`, `>=`, `<=`, `<>`
6.  Negación `NO`
7.  Conjunción `Y`
8.  Disyunción `O`

*¡Usa paréntesis `()` para asegurar el orden deseado cuando tengas dudas!*

### 5. Estructura Condicional Simple: `Si ... Entonces ... FinSi`

Permite ejecutar un bloque de instrucciones **solo si** una condición es `Verdadero`.

```pseudocode
Si <condición> Entonces
    // Instrucciones a ejecutar si la condición es Verdadera
FinSi
```

**Ejemplo:**

```pseudocode
Proceso EjemploSiSimple
    Definir temperatura Como Real;
    Escribir "Ingrese la temperatura actual:";
    Leer temperatura;
    Si temperatura > 30 Entonces
        Escribir "Hace mucho calor!";
    FinSi
    Escribir "Fin del programa.";
FinProceso
```

### 6. Estructura Condicional Doble: `Si ... Entonces ... Sino ... FinSi`

Permite elegir entre **dos** bloques de instrucciones: uno si la condición es `Verdadero` y otro si es `Falso`.

```pseudocode
Si <condición> Entonces
    // Instrucciones si la condición es Verdadera
Sino
    // Instrucciones si la condición es Falsa
FinSi
```

**Ejemplo:**

```pseudocode
Proceso EjemploSiSino
    Definir edad Como Entero;
    Escribir "Ingrese su edad:";
    Leer edad;
    Si edad >= 18 Entonces
        Escribir "Eres mayor de edad.";
    Sino
        Escribir "Eres menor de edad.";
    FinSi
FinProceso
```

---

## Ejercicios del Módulo 2

1.  [Ejercicio 1 (Dificultad 1): Resta Simple](./m2-ejercicio1-1.md)
2.  [Ejercicio 2 (Dificultad 2): ¿Es Positivo?](./m2-ejercicio2-2.md)
3.  [Ejercicio 3 (Dificultad 3): División y Módulo](./m2-ejercicio3-3.md)
4.  [Ejercicio 4 (Dificultad 4): Par o Impar](./m2-ejercicio4-4.md)
5.  [Ejercicio 5 (Dificultad 5): Comparar Dos Números](./m2-ejercicio5-5.md)
6.  [Ejercicio 6 (Dificultad 6): Descuento por Compra](./m2-ejercicio6-6.md)
7.  [Ejercicio 7 (Dificultad 7): ¿Vocal o Consonante? (Simple)](./m2-ejercicio7-7.md)
8.  [Ejercicio 8 (Dificultad 8): Login Básico](./m2-ejercicio8-8.md)
9.  [Ejercicio 9 (Dificultad 9): Calcular Valor Absoluto](./m2-ejercicio9-9.md)
10. [Ejercicio 10 (Dificultad 10): ¿Triángulo Válido?](./m2-ejercicio10-10.md)

