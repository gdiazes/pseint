# Curso de Introducción a la Programación con PseInt

¡Bienvenido/a al curso de introducción a la programación utilizando PseInt! Este curso está diseñado para principiantes absolutos, sin necesidad de experiencia previa en programación. Aprenderemos los fundamentos de la lógica de programación y cómo expresarla mediante pseudocódigo.

## Formato del Curso

*   **Plataforma:** GitHub (usando Markdown).
*   **Metodología:** Aprendizaje basado en ejercicios prácticos.
*   **Estructura:** El curso se divide en módulos temáticos.
*   **Ejercicios:**
    *   Cada módulo contendrá 10 ejercicios.
    *   Los ejercicios tendrán un nivel de dificultad progresivo, del 1 (más fácil) al 10 (más difícil dentro del módulo).
    *   Cada ejercicio presentará un código con **3 errores intencionales**.
    *   Junto a cada error (o cerca de la línea) habrá un comentario (`// Pista X: ...`) que te dará una pequeña ayuda para identificarlo y corregirlo.
    *   Tu tarea será encontrar los errores, entender por qué son errores y corregir el código para que funcione como se espera.

## ¿Cómo usar este material?

1.  Lee la introducción de cada módulo para entender los conceptos que se practicarán.
2.  Aborda los ejercicios en orden de dificultad.
3.  Copia el código del ejercicio en tu PseInt.
4.  Intenta ejecutarlo. Observa los mensajes de error o el comportamiento incorrecto.
5.  Usa las pistas para localizar y corregir los 3 errores.
6.  Una vez corregido, ejecuta el código para asegurarte de que funciona correctamente y produce el resultado esperado.
7.  ¡Experimenta! Modifica el código corregido para ver qué pasa.

¡Empecemos!

---

## Módulo 1: Introducción, Entrada y Salida Básica

**Conceptos:** Estructura básica de un algoritmo (`Proceso`/`FinProceso`), comentarios (`//`), escribir mensajes en pantalla (`Escribir`), leer datos del teclado (`Leer`), definir variables (`Definir Como`), tipos de datos básicos (`Entero`, `Caracter`, `Real`).

---

### Ejercicio 1.1 (Dificultad: 1/10)

**Objetivo:** Mostrar un simple mensaje de "Hola Mundo" en la pantalla.

```Pseint
Proceso SaludoBasico
    // Este proceso deberia mostrar un saludo
    Escribir Hola Mundo"; // Pista 1: Los mensajes de texto necesitan algo especial alrededor.
Fin Proceso // Pista 2: Revisa la palabra clave para finalizar el proceso.
// Pista 3: Falta la instrucción principal para iniciar el algoritmo.
