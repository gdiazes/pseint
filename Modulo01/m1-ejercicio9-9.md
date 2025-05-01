# Módulo 1 - Ejercicio 9 (Dificultad 9)

## Enunciado

Escribe un algoritmo que pida al usuario su nombre y su apellido por separado, los una (concatene) en una sola variable llamada `nombreCompleto` (asegúrate de que haya un espacio entre nombre y apellido) y muestre el nombre completo.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso ConcatenarNombres

    Definir nombre, apellido Como Caracter;
    Definir nombreCompleto Como Entero; // Pista 1: Si vas a unir texto (nombre y apellido), ¿'Entero' es el tipo correcto para 'nombreCompleto'?

    Escribir "Ingrese su nombre:";
    Leer nombre;
    Escribir "Ingrese su apellido:";
    Leer apellido;

    // Intentar concatenar nombre y apellido
    nombreCompleto = nombre + " " + apellido; // Pista 2: Revisa el operador de asignación. Además, ¿funciona el '+' para unir cadenas en PSeInt estándar? (Relacionado con Pista 3)

    Escribir "Su nombre completo es: ", nombre Completo; // Pista 3: Revisa cómo se muestra la variable y si hay espacios donde no debería.

FinProceso
```
<details>
<summary>Mostrar Solución Correcta</summary>

## Solución Correcta

```pseudocode
Proceso ConcatenarNombres_Solucion

    Definir nombre, apellido, nombreCompleto Como Caracter; // Corregido: 'nombreCompleto' debe ser Caracter/Cadena.

    Escribir "Ingrese su nombre:";
    Leer nombre;
    Escribir "Ingrese su apellido:";
    Leer apellido;

    // Concatenar nombre y apellido (forma común en PSeInt)
    // Nota: La forma exacta puede depender del perfil, pero asignar funciona.
    // A menudo se usa la función CONCATENAR o se unen al Escribir.
    // Asignaremos para este ejemplo, asumiendo que el perfil lo permite o es flexible.
    // Si no, la alternativa es mostrarlo directamente en Escribir.

    nombreCompleto <- Concatenar(Concatenar(nombre, " "), apellido); // Usando función explícita si '+' no funciona
    // Alternativa si '+' funciona en el perfil usado:
    // nombreCompleto <- nombre + " " + apellido;
    // Alternativa más simple (sin variable extra, solo mostrar):
    // (No aplica si el requisito es guardar en 'nombreCompleto')

    Escribir "Su nombre completo es: ", nombreCompleto; // Corregido: Nombre de variable sin espacio y operador '<-'.

FinProceso

// Solución Alternativa (más universal en PSeInt, sin variable extra)
Proceso ConcatenarNombres_Alternativa

    Definir nombre, apellido Como Caracter;

    Escribir "Ingrese su nombre:";
    Leer nombre;
    Escribir "Ingrese su apellido:";
    Leer apellido;

    // Mostrar directamente concatenando con comas en Escribir
    Escribir "Su nombre completo es: ", nombre, " ", apellido; // Une las partes al mostrar

FinProceso
```
</details>
<details>
<summary>Mostrar Explicación de la Solución</summary> 
  
## Explicación de la Solución

1.  La variable `nombreCompleto` almacenará la unión de dos cadenas de texto (nombre y apellido), por lo que su tipo de dato debe ser `Caracter` (o `Cadena`), no `Entero`.
2.  Se usó `=` en lugar del operador de asignación `<-`. Además, la concatenación de cadenas con el operador `+` no es estándar en todos los perfiles de PSeInt (aunque algunos lo permiten). Una forma más segura es usar la función `Concatenar()` o, si solo se necesita mostrar, hacerlo directamente en la instrucción `Escribir` usando comas. Se corrigió la asignación a `<-` y se usó `Concatenar()` como ejemplo robusto (ver alternativas en la solución).
3.  En la línea `Escribir`, había un espacio en el nombre de la variable (`nombre Completo` en lugar de `nombreCompleto`). Los nombres de variables no pueden contener espacios. Se corrigió a `nombreCompleto`.
</details>
