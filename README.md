**Nombre del Curso:** De Cero a Experto en Pseudocódigo con PSeInt

**Objetivo General:** Que el estudiante domine la lógica de programación y la escritura de algoritmos utilizando pseudocódigo estricto en PSeInt, resolviendo problemas de dificultad creciente.

**Formato:** Archivos Markdown para GitHub.

**Desglose de Módulos:**

**Módulo 1: Introducción a los Algoritmos y PSeInt**

*   **Teoría:**
    *   ¿Qué es un algoritmo? (Concepto, características: preciso, definido, finito).
    *   ¿Qué es el pseudocódigo? (Ventajas, relación con lenguajes de programación).
    *   Introducción a la interfaz de PSeInt (Editor, ejecución paso a paso, panel de variables).
    *   Estructura básica de un algoritmo en PSeInt (`Proceso`/`FinProceso`).
    *   Comentarios (`//`).
    *   Instrucciones básicas: `Escribir` (mostrar mensajes y variables), `Leer` (capturar datos del usuario).
    *   Variables: Concepto, declaración implícita/explícita (uso de `Definir`).
    *   Tipos de datos fundamentales: `Entero`, `Real`, `Caracter`, `Logico`.
    *   Operador de asignación (`<-`).
  
**Módulo 2: Operadores y Expresiones Condicionales Simples**

*   **Teoría:**
    *   Operadores Aritméticos (`+`, `-`, `*`, `/`, `^`, `%` o `MOD`).
    *   Operadores Relacionales (`>`, `<`, `=`, `>=`, `<=`, `<>`).
    *   Operadores Lógicos (`Y`, `O`, `NO` o `&`, `|`, `~`).
    *   Jerarquía de operadores.
    *   Expresiones: Combinación de variables, constantes y operadores.
    *   Estructura condicional simple: `Si ... Entonces ... FinSi`.
    *   Estructura condicional doble: `Si ... Entonces ... Sino ... FinSi`.

**Módulo 3: Estructuras Condicionales Anidadas y Múltiples**

*   **Teoría:**
    *   Condicionales anidados (`Si` dentro de otro `Si` o `Sino`).
    *   Buenas prácticas para evitar complejidad excesiva en anidamientos.
    *   Estructura condicional múltiple: `Segun ... Hacer ... De Otro Modo ... FinSegun`.
    *   Comparación entre `Si` anidados y `Segun`. Cuándo usar cada uno.


**Módulo 4: Estructuras Repetitivas (Bucles)**

*   **Teoría:**
    *   Necesidad de repetir instrucciones.
    *   Bucle `Mientras ... Hacer ... FinMientras` (condición al inicio).
    *   Bucle `Repetir ... Hasta Que ...` (condición al final, se ejecuta al menos una vez).
    *   Bucle `Para variable <- valor_inicial Hasta valor_final Con Paso paso Hacer ... FinPara` (controlado por contador).
    *   Contadores y Acumuladores dentro de bucles.
    *   Bucles anidados.
    *   Cómo elegir el bucle adecuado.


**Módulo 5: Arreglos Unidimensionales (Vectores)**

*   **Teoría:**
    *   ¿Qué es un arreglo? Concepto de colección de datos del mismo tipo.
    *   Vectores (arreglos de una dimensión).
    *   Declaración de vectores: `Dimension nombre_vector[tamaño]`.
    *   Acceso a elementos: Índices (PSeInt usualmente empieza en 1).
    *   Recorrer vectores con bucles (`Para` es ideal).
    *   Operaciones comunes: Cargar, mostrar, buscar elementos, sumar elementos, encontrar el mayor/menor.


**Módulo 6: Arreglos Bidimensionales (Matrices)**

*   **Teoría:**
    *   Matrices (arreglos de dos dimensiones - filas y columnas).
    *   Declaración de matrices: `Dimension nombre_matriz[filas, columnas]`.
    *   Acceso a elementos: Índices (fila, columna).
    *   Recorrer matrices con bucles anidados (`Para`).
    *   Operaciones comunes: Cargar, mostrar por filas/columnas, sumar filas/columnas, buscar elementos, sumar la diagonal principal/secundaria (si es cuadrada).

**Módulo 7: Subprocesos (Funciones y Procedimientos)**

*   **Teoría:**
    *   Necesidad de modularidad: Reutilización de código, claridad, división de problemas.
    *   Concepto de Subproceso (equivalente a funciones/procedimientos).
    *   Definición de un Subproceso: `SubProceso [retorno] <- Nombre ( [argumentos] ) ... FinSubProceso`.
    *   Llamada a un Subproceso.
    *   Paso de parámetros: Por valor y por referencia (cómo PSeInt maneja esto).
    *   Variables locales y globales (ámbito/alcance).
    *   Diferencia conceptual entre funciones (devuelven un valor) y procedimientos (realizan una tarea). Cómo simular ambos en PSeInt.
