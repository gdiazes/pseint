# Módulo 1: Introducción a los Algoritmos y PSeInt

## Teoría

¡Bienvenido/a al mundo de la programación con PSeInt! Antes de escribir código complejo, debemos entender los fundamentos: qué es un algoritmo y cómo PSeInt nos ayuda a crearlos.

### 1. ¿Qué es un Algoritmo?

Piensa en un algoritmo como una **receta de cocina** o un **manual de instrucciones**. Es una secuencia de pasos **lógicos, ordenados y finitos** que describen exactamente cómo resolver un problema o realizar una tarea.

Características clave de un algoritmo:

*   **Preciso:** Cada paso debe estar claramente definido, sin ambigüedad.
*   **Definido:** Si sigues el algoritmo varias veces con los mismos datos de entrada, siempre obtendrás el mismo resultado.
*   **Finito:** El algoritmo debe terminar después de un número finito de pasos. No puede quedarse en un bucle infinito.

### 2. ¿Qué es el Pseudocódigo?

El pseudocódigo es una forma de describir los pasos de un algoritmo utilizando un lenguaje **intermedio** entre el lenguaje humano natural y un lenguaje de programación real (como Java, Python, C++, etc.).

**Ventajas:**

*   Se enfoca en la **lógica** del problema, no en la sintaxis estricta de un lenguaje específico.
*   Es más fácil de leer y entender que el código de programación real para los principiantes.
*   Facilita la posterior traducción a cualquier lenguaje de programación.

### 3. Introducción a PSeInt

PSeInt es una herramienta fantástica diseñada para **aprender los fundamentos de la programación y el desarrollo de la lógica**. Nos permite escribir algoritmos en pseudocódigo (en español) y ejecutarlos para ver cómo funcionan.

**Interfaz Principal:**

*   **Área de Edición:** Donde escribes tu pseudocódigo.
*   **Botones de Ejecución:** El botón verde (▶️) ejecuta el algoritmo completo. El botón con los "pies" permite la ejecución **paso a paso**, lo cual es ¡muy útil! para entender el flujo.
*   **Panel de Variables (opcional):** Puede mostrar el valor de las variables mientras el algoritmo se ejecuta.
*   **Área de Salida:** Donde ves los mensajes que tu algoritmo muestra (`Escribir`) y donde ingresas datos cuando el algoritmo los pide (`Leer`).

### 4. Estructura Básica en PSeInt

Todo algoritmo en PSeInt comienza con la palabra clave `Proceso` (o `Algoritmo`, según la configuración) seguida de un nombre descriptivo, y termina con `FinProceso` (o `FinAlgoritmo`).

```pseudocode
Proceso MiPrimerAlgoritmo
    // Aquí van las instrucciones
FinProceso
