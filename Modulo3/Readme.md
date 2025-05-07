## Módulo 3: Estructuras Condicionales Anidadas y Múltiples

**Archivo: `Modulo3/Modulo3.md`**

# Módulo 3: Estructuras Condicionales Anidadas y Múltiples

## Teoría

Ahora que manejamos las decisiones simples, vamos a explorar cómo tomar decisiones más complejas, ya sea evaluando condiciones dentro de otras o eligiendo entre múltiples opciones posibles.

### 1. Condicionales Anidados

Un condicional anidado ocurre cuando colocamos una estructura `Si...Entonces...Sino...FinSi` **dentro** de otra. Esto nos permite refinar las decisiones.

```pseudocode
Proceso EjemploAnidado
    Definir edad Como Entero;
    Definir tieneLicencia Como Logico;

    Escribir "Ingrese su edad:";
    Leer edad;

    Si edad >= 18 Entonces
        Escribir "Ingrese si tiene licencia (Verdadero/Falso):";
        Leer tieneLicencia;
        Si tieneLicencia Entonces // Condicional anidado
            Escribir "Puede conducir.";
        Sino
            Escribir "Es mayor de edad, pero necesita licencia para conducir.";
        FinSi
    Sino
        Escribir "Es menor de edad, no puede conducir.";
    FinSi
FinProceso
```

**Buenas Prácticas:**

*   **Indentación:** Usa sangría (espacios al inicio de la línea) para mostrar claramente qué bloque de código pertenece a cada `Si` o `Sino`. PSeInt suele hacerlo automáticamente.
*   **Evitar Complejidad Excesiva:** Demasiados niveles de anidamiento pueden hacer el código difícil de leer y entender. Si se vuelve muy complejo, considera si hay una forma más simple de estructurar la lógica o si necesitas usar subprocesos (Módulo 7).

### 2. Estructura Condicional Múltiple: `Segun`

Cuando necesitas elegir entre **múltiples valores posibles** para una **única variable o expresión**, la estructura `Segun` (similar al `switch` en otros lenguajes) es más clara y eficiente que usar muchos `Si` anidados o encadenados (`Si... Sino Si... Sino Si...`).

```pseudocode
Segun <expresion_numerica_o_caracter> Hacer
    <opcion_1>:
        // Instrucciones si la expresión coincide con opcion_1
    <opcion_2>, <opcion_3>: // Se pueden agrupar opciones
        // Instrucciones si la expresión coincide con opcion_2 u opcion_3
    ...
    <opcion_N>:
        // Instrucciones si la expresión coincide con opcion_N
    De Otro Modo: // Opcional: se ejecuta si no coincide con ninguna opción anterior
        // Instrucciones por defecto
FinSegun
```

**Características Clave:**

*   La `<expresion_numerica_o_caracter>` se evalúa una sola vez.
*   Las `<opcion_i>` deben ser valores constantes (números o cadenas de texto).
*   El bloque `De Otro Modo` captura todos los casos no especificados.

**Ejemplo:**

```pseudocode
Proceso EjemploSegun
    Definir dia Como Entero;

    Escribir "Ingrese un número de día (1=Lunes, ..., 7=Domingo):";
    Leer dia;

    Segun dia Hacer
        1:
            Escribir "Lunes";
        2:
            Escribir "Martes";
        3:
            Escribir "Miércoles";
        4:
            Escribir "Jueves";
        5:
            Escribir "Viernes";
        6, 7: // Opciones agrupadas
            Escribir "Fin de semana";
        De Otro Modo:
            Escribir "Número de día inválido.";
    FinSegun
FinProceso
```

### 3. Comparación: `Si` Anidados vs. `Segun`

*   Usa `Segun` cuando la decisión depende del valor específico de **una sola variable** o expresión (generalmente entera o de carácter). Es más legible para menús o clasificaciones basadas en códigos.
*   Usa `Si` anidados (o `Si... Sino Si...`) cuando las decisiones dependen de **diferentes condiciones** o **rangos de valores** que no se pueden listar fácilmente como opciones discretas.

---

## Ejercicios del Módulo 3

1.  [Ejercicio 1 (Dificultad 1): Positivo, Negativo o Cero](./m3-ejercicio1-1.md)
2.  [Ejercicio 2 (Dificultad 2): ¿Fin de Semana? (con Si)](./m3-ejercicio2-2.md)
3.  [Ejercicio 3 (Dificultad 3): ¿Fin de Semana? (con Segun)](./m3-ejercicio3-3.md)
4.  [Ejercicio 4 (Dificultad 4): Calificación Literal](./m3-ejercicio4-4.md)
5.  [Ejercicio 5 (Dificultad 5): Tipo de Ángulo](./m3-ejercicio5-5.md)
6.  [Ejercicio 6 (Dificultad 6): Calculadora Simple (Segun)](./m3-ejercicio6-6.md)
7.  [Ejercicio 7 (Dificultad 7): Ordenar Dos Números](./m3-ejercicio7-7.md)
8.  [Ejercicio 8 (Dificultad 8): Tarifa de Estacionamiento](./m3-ejercicio8-8.md)
9.  [Ejercicio 9 (Dificultad 9): Clasificación IMC](./m3-ejercicio9-9.md)
10. [Ejercicio 10 (Dificultad 10): Menú Cajero Básico](./m3-ejercicio10-10.md)

**¡A dominar las decisiones complejas!**
```
