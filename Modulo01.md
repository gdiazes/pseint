¡Perfecto! Comencemos con la creación del **Módulo 1**.

Primero, el archivo principal del módulo que contendrá la teoría y los enlaces a los ejercicios.

---

**Archivo: `Modulo1/Modulo1.md`**

```markdown
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
```

### 5. Comentarios

Los comentarios son líneas que PSeInt ignora al ejecutar el algoritmo. Se usan para explicar partes del código, hacerlo más legible o dejar notas. Se escriben usando doble barra `//`.

```pseudocode
Proceso EjemploComentarios
    // Esto es un comentario de una sola línea.
    Escribir "Hola"; // Esto también es un comentario, al final de una instrucción.
FinProceso
```

### 6. Instrucciones Básicas: `Escribir` y `Leer`

*   **`Escribir`:** Muestra mensajes o el valor de las variables en la pantalla (en el área de salida de PSeInt). Puedes mostrar texto fijo (entre comillas) o el contenido de variables. Para mostrar varios elementos, sepáralos con comas.

    ```pseudocode
    Proceso EjemploEscribir
        Definir saludo Como Caracter;
        saludo <- "Mundo";
        Escribir "Hola ", saludo, "!"; // Muestra: Hola Mundo!
        Escribir 123; // Muestra: 123
    FinProceso
    ```
*   **`Leer`:** Detiene la ejecución del algoritmo y espera a que el usuario ingrese un dato por teclado y presione Enter. Ese dato se guarda en la variable especificada.

    ```pseudocode
    Proceso EjemploLeer
        Definir nombreUsuario Como Caracter;
        Escribir "Por favor, introduce tu nombre:";
        Leer nombreUsuario; // Espera a que el usuario escriba algo y lo guarda en nombreUsuario
        Escribir "Bienvenido/a, ", nombreUsuario;
    FinProceso
    ```

### 7. Variables y Tipos de Datos

Una **variable** es como una caja con una etiqueta donde podemos guardar información (datos) que puede cambiar durante la ejecución del algoritmo.

*   **Declaración:** En PSeInt (especialmente en modo estricto), es buena práctica declarar las variables antes de usarlas, indicando su nombre y qué tipo de dato guardarán. Se usa la palabra clave `Definir`.

    ```pseudocode
    Definir edad Como Entero;
    Definir precio Como Real;
    Definir letraInicial Como Caracter;
    Definir estaActivo Como Logico;
    ```
*   **Tipos de Datos Fundamentales:**
    *   `Entero`: Números enteros (sin decimales), ej: `-5`, `0`, `25`.
    *   `Real`: Números con decimales, ej: `3.14`, `-0.5`, `10.0`.
    *   `Caracter`: Un solo carácter o una cadena de texto, ej: `"a"`, `"Hola Mundo"`.
    *   `Logico`: Solo puede contener dos valores: `Verdadero` o `Falso`.

### 8. Operador de Asignación (`<-`)

Se utiliza para guardar un valor en una variable. La flecha `<-` indica que el valor de la derecha se almacena en la variable de la izquierda.

```pseudocode
Proceso EjemploAsignacion
    Definir contador Como Entero;
    Definir mensaje Como Caracter;

    contador <- 0; // Guarda 0 en contador
    mensaje <- "Inicio"; // Guarda "Inicio" en mensaje

    Escribir mensaje, ": ", contador; // Muestra: Inicio: 0

    contador <- contador + 1; // Actualiza el valor de contador
    mensaje <- "Actualizado";

    Escribir mensaje, ": ", contador; // Muestra: Actualizado: 1
FinProceso
```

---

## Ejercicios del Módulo 1

A continuación, encontrarás los enlaces a los ejercicios prácticos de este módulo. Cada uno incrementa ligeramente la dificultad e incluye errores comunes para que aprendas a identificarlos y corregirlos.

1.  [Ejercicio 1 (Dificultad 1): Hola Mundo](./m1-ejercicio1-1.md)
2.  [Ejercicio 2 (Dificultad 2): Eco de Entrada](./m1-ejercicio2-2.md)
3.  [Ejercicio 3 (Dificultad 3): Suma de Constantes](./m1-ejercicio3-3.md)
4.  [Ejercicio 4 (Dificultad 4): Área de un Rectángulo](./m1-ejercicio4-4.md)
5.  [Ejercicio 5 (Dificultad 5): Saludo Personalizado](./m1-ejercicio5-5.md)
6.  [Ejercicio 6 (Dificultad 6): Intercambio de Variables](./m1-ejercicio6-6.md)
7.  [Ejercicio 7 (Dificultad 7): Promedio de Dos Números](./m1-ejercicio7-7.md)
8.  [Ejercicio 8 (Dificultad 8): Variable Lógica (Mayor de Edad)](./m1-ejercicio8-8.md)
9.  [Ejercicio 9 (Dificultad 9): Concatenar Nombre y Apellido](./m1-ejercicio9-9.md)
10. [Ejercicio 10 (Dificultad 10): Cálculo Simple de Venta](./m1-ejercicio10-10.md)

**¡Mucha suerte y a practicar!**
```

---

Ahora, crearé los archivos de los ejercicios uno por uno, siguiendo la estructura acordada. Empezando por el primero.

**Archivo: `Modulo1/m1-ejercicio1-1.md`**

```markdown
# Módulo 1 - Ejercicio 1 (Dificultad 1)

## Enunciado

Escribe un algoritmo que simplemente muestre el mensaje "Hola Mundo!" en la pantalla.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso SaludoBasico

    // Mostrar el mensaje
    Escribo "Hola Mundo!"; // Pista 1: Revisa cómo se escribe la instrucción para mostrar mensajes.

FinProceso SaludoBasico // Pista 2: ¿Es necesario repetir el nombre al finalizar el proceso?

// Pista 3: Falta algo fundamental al inicio del mensaje para que sea considerado texto.
```

## Solución Correcta

```pseudocode
Proceso SaludoBasico_Solucion

    // Mostrar el mensaje
    Escribir "Hola Mundo!"; // Corregido: La instrucción es 'Escribir' y el texto va entre comillas.

FinProceso // Corregido: Solo se necesita 'FinProceso'.
```

## Explicación de la Solución

1.  La instrucción para mostrar mensajes en PSeInt es `Escribir`, no `Escribo`.
2.  La línea final del algoritmo debe ser simplemente `FinProceso`, sin repetir el nombre del algoritmo.
3.  El texto literal que se quiere mostrar con `Escribir` debe ir encerrado entre comillas dobles (`"`). Se añadieron las comillas alrededor de `Hola Mundo!`.
```

---

**Archivo: `Modulo1/m1-ejercicio2-2.md`**

```markdown
# Módulo 1 - Ejercicio 2 (Dificultad 2)

## Enunciado

Escribe un algoritmo que pida al usuario ingresar un número entero y luego muestre en pantalla el número ingresado.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso EcoNumero

    Definir numero Como Caracter; // Pista 1: Se pide un número entero, ¿es 'Caracter' el tipo correcto?

    Escribir "Ingrese un número entero:";
    Leer numeroUsuario; // Pista 2: La variable donde se guarda el dato debe coincidir con la definida.

    Escribir "El número ingresado es: ", numero; // Pista 3: ¿Se está mostrando la variable correcta?

FinProceso
```

## Solución Correcta

```pseudocode
Proceso EcoNumero_Solucion

    Definir numero Como Entero; // Corregido: El tipo para números enteros es 'Entero'.

    Escribir "Ingrese un número entero:";
    Leer numero; // Corregido: Usar la variable 'numero' que fue definida.

    Escribir "El número ingresado es: ", numero; // Correcto, ahora muestra la variable correcta.

FinProceso
```

## Explicación de la Solución

1.  Se pidió un número entero, por lo tanto, el tipo de dato correcto al `Definir` la variable es `Entero`, no `Caracter` (que es para texto).
2.  La instrucción `Leer` debe usar el nombre de la variable que se definió previamente para guardar el dato. Se cambió `Leer numeroUsuario` por `Leer numero`.
3.  Aunque la línea `Escribir` estaba sintácticamente bien, mostraba la variable `numero`. El error conceptual estaba en el punto 2, al intentar leer en una variable no definida (`numeroUsuario`). Al corregir el `Leer`, esta línea ahora funciona como se espera.
```

---

**Archivo: `Modulo1/m1-ejercicio3-3.md`**

```markdown
# Módulo 1 - Ejercicio 3 (Dificultad 3)

## Enunciado

Escribe un algoritmo que sume dos números enteros definidos directamente en el código (constantes, por ejemplo, 5 y 7) y muestre el resultado.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso SumaConstantes

    Definir num1, num2 Como Entero;
    Definir resultado Como Real; // Pista 1: Si sumas dos enteros, ¿el resultado siempre necesita ser 'Real'?

    num1 = 5; // Pista 2: ¿Es '=' el operador correcto para asignar valores en PSeInt?
    num2 <- 7;

    resultado <- num1 + num 2; // Pista 3: Revisa si hay algún espacio inesperado en los nombres de variables.

    Escribir "La suma de ", num1, " y ", num2, " es: ", resultado;

FinProceso
```

## Solución Correcta

```pseudocode
Proceso SumaConstantes_Solucion

    Definir num1, num2, resultado Como Entero; // Corregido: El resultado también puede ser Entero.

    num1 <- 5; // Corregido: Usar el operador de asignación '<-'.
    num2 <- 7;

    resultado <- num1 + num2; // Corregido: Sin espacio en 'num2'.

    Escribir "La suma de ", num1, " y ", num2, " es: ", resultado;

FinProceso
```

## Explicación de la Solución

1.  La suma de dos números enteros siempre da como resultado otro número entero. Por lo tanto, la variable `resultado` puede (y es preferible en este caso) definirse como `Entero`, no `Real`. Se cambió `Definir resultado Como Real` a `Definir resultado Como Entero` (o se añadió a la definición existente).
2.  El operador para asignar un valor a una variable en PSeInt es `<-` (flecha), no `=` (signo de igual). Se corrigió `num1 = 5` a `num1 <- 5`.
3.  En la línea del cálculo `resultado <- num1 + num 2;`, había un espacio entre `num` y `2`, haciendo que PSeInt lo interprete como una variable inexistente `num`. Se corrigió a `num2`.
```

---

**Archivo: `Modulo1/m1-ejercicio4-4.md`**

```markdown
# Módulo 1 - Ejercicio 4 (Dificultad 4)

## Enunciado

Escribe un algoritmo que calcule el área de un rectángulo. Debe pedir al usuario la longitud de la base y la altura (pueden tener decimales) y luego mostrar el área calculada. Fórmula: Área = Base * Altura.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso AreaRectangulo

    Definir base, altura, area Como Entero; // Pista 1: Si la base y altura pueden tener decimales, ¿'Entero' es adecuado para ellas y para el área?

    Escribir "Ingrese la base del rectángulo:";
    Leer base

    Escribir "Ingrese la altura del rectángulo:";
    Leer altura; // Pista 2: Revisa si falta algo al final de la instrucción 'Leer base'.

    area = base * altura; // Pista 3: Revisa el operador de asignación y la fórmula.

    Escribir "El área del rectángulo es: ", area;

FinProceso
```

## Solución Correcta

```pseudocode
Proceso AreaRectangulo_Solucion

    Definir base, altura, area Como Real; // Corregido: Usar 'Real' para permitir decimales.

    Escribir "Ingrese la base del rectángulo:";
    Leer base; // Corregido: Añadir punto y coma al final (requerido en algunas configuraciones/modo estricto).

    Escribir "Ingrese la altura del rectángulo:";
    Leer altura;

    area <- base * altura; // Corregido: Usar '<-' para asignar. La fórmula está bien.

    Escribir "El área del rectángulo es: ", area;

FinProceso
```

## Explicación de la Solución

1.  Dado que la base y la altura pueden tener decimales (ej: 5.5 cm), y el resultado de multiplicarlos también puede tenerlos, el tipo de dato adecuado para las tres variables (`base`, `altura`, `area`) es `Real`. Se cambió `Entero` por `Real`.
2.  En configuraciones más estrictas de PSeInt, cada instrucción debe terminar con punto y coma (`;`). Faltaba en la línea `Leer base`. Se añadió.
3.  El operador de asignación correcto es `<-`, no `=`. Se corrigió `area = base * altura` a `area <- base * altura`. La fórmula matemática (multiplicación) era correcta.
```

---

**Archivo: `Modulo1/m1-ejercicio5-5.md`**

```markdown
# Módulo 1 - Ejercicio 5 (Dificultad 5)

## Enunciado

Escribe un algoritmo que pida al usuario su nombre y luego lo salude mostrando el mensaje "Hola, [nombre ingresado]!".

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso SaludoPersonalizado

    // Declarar la variable para el nombre
    Definir nombre Como Real; // Pista 1: ¿Es 'Real' el tipo de dato adecuado para un nombre?

    // Pedir el nombre al usuario
    Escribir "Introduce tu nombre: ";
    nombre <- Leer; // Pista 2: La función Leer() necesita ser usada correctamente para asignar el valor a la variable 'nombre'.

    // Mostrar el saludo
    Escribir "Hola, " + nombre + "!"; // Pista 3: Revisa la sintaxis para unir texto y variables al mostrar con 'Escribir'.

FinProceso
```

## Solución Correcta

```pseudocode
Proceso SaludoPersonalizado_Solucion

    // Declarar la variable para el nombre
    Definir nombre Como Caracter; // Corregido: El tipo debe ser Caracter (o Cadena).

    // Pedir el nombre al usuario
    Escribir "Introduce tu nombre: ";
    Leer nombre; // Corregido: Leer asigna directamente a la variable.

    // Mostrar el saludo
    Escribir "Hola, ", nombre, "!"; // Corregido: Usar comas para concatenar en Escribir.

FinProceso
```

## Explicación de la Solución

1.  La variable `nombre` debe ser de tipo `Caracter` (o `Cadena`, según el perfil de PSeInt) para almacenar texto, no `Real` que es para números con decimales.
2.  La instrucción `Leer` se usa directamente con la variable donde se guardará el dato: `Leer nombre;`. No se usa como una función que devuelve un valor para asignar con `<-` en este contexto básico.
3.  La instrucción `Escribir` en PSeInt permite mostrar múltiples elementos separados por comas (`,`). El uso del signo `+` para concatenar cadenas es común en otros lenguajes, pero en PSeInt estándar se usan comas dentro de `Escribir`. Se cambió `+` por `,`.
```

---

**Archivo: `Modulo1/m1-ejercicio6-6.md`**

```markdown
# Módulo 1 - Ejercicio 6 (Dificultad 6)

## Enunciado

Escribe un algoritmo que pida al usuario dos números enteros, los guarde en variables `a` y `b`, intercambie sus valores (que `a` tenga el valor de `b` y `b` el valor de `a`) y finalmente muestre los valores intercambiados.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso IntercambioVariables

    Definir a, b, aux Como Entero;

    Escribir "Ingrese el primer número (a):";
    Leer a;
    Escribir "Ingrese el segundo número (b):";
    Leer b;

    Escribir "Valores originales: a=", a, ", b=", b;

    // Intentar intercambiar valores
    a <- b;
    b <- a; // Pista 1: Si 'a' ya tiene el valor de 'b', ¿qué valor estás asignando aquí a 'b'? Piensa si necesitas algo más.

    aux <- a; // Pista 2: La variable 'aux' se usa para guardar temporalmente un valor. ¿Se está usando en el momento correcto?

    Escribir "Valores intercambiados: a=", a, ", b="; b; // Pista 3: Revisa la sintaxis al final de esta línea de 'Escribir'.

FinProceso
```

## Solución Correcta

```pseudocode
Proceso IntercambioVariables_Solucion

    Definir a, b, aux Como Entero;

    Escribir "Ingrese el primer número (a):";
    Leer a;
    Escribir "Ingrese el segundo número (b):";
    Leer b;

    Escribir "Valores originales: a=", a, ", b=", b;

    // Intercambiar valores usando una variable auxiliar
    aux <- a; // Guarda el valor original de 'a'
    a <- b;   // 'a' ahora tiene el valor de 'b'
    b <- aux; // 'b' toma el valor original de 'a' que estaba en 'aux'

    Escribir "Valores intercambiados: a=", a, ", b=", b; // Corregido: Sin punto y coma extra en medio.

FinProceso
```

## Explicación de la Solución

1.  El error lógico principal está en el intento de intercambio. Al hacer `a <- b`, el valor original de `a` se pierde. Luego, al hacer `b <- a`, se le asigna a `b` el valor que `a` acaba de recibir (que es el valor original de `b`), por lo que ambas variables terminan con el valor original de `b`. La solución correcta requiere una variable auxiliar (`aux`) para guardar temporalmente uno de los valores antes de sobrescribirlo.
2.  La variable `aux` se usaba *después* de que el valor original de `a` ya se había perdido. Debe usarse *antes* de la primera asignación (`a <- b`) para guardar el valor original de `a`. El orden correcto es: `aux <- a`, luego `a <- b`, y finalmente `b <- aux`.
3.  En la última línea `Escribir`, había un punto y coma (`;`) después de `"b="`, separando incorrectamente la variable `b` del resto de la instrucción. Se eliminó ese punto y coma.
```

---

**Archivo: `Modulo1/m1-ejercicio7-7.md`**

```markdown
# Módulo 1 - Ejercicio 7 (Dificultad 7)

## Enunciado

Escribe un algoritmo que pida al usuario dos números (pueden tener decimales), calcule su promedio y muestre el resultado. Fórmula: Promedio = (Numero1 + Numero2) / 2.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso CalcularPromedio

    Define n1, n2, promedio Como Real; // Pista 1: Revisa la palabra clave para definir variables.

    Escribir "Ingrese el primer número:";
    Leer n1;
    Escribir "Ingrese el segundo número:";
    Leer n2;

    promedio <- n1 + n2 / 2; // Pista 2: Considera la jerarquía de operadores. ¿Qué se calcula primero aquí? ¿Necesitas agrupar algo?

    Escribir "El promedio es: " promedio; // Pista 3: Falta algo al final de la variable 'promedio' al mostrarla.

FinProceso
```

## Solución Correcta

```pseudocode
Proceso CalcularPromedio_Solucion

    Definir n1, n2, promedio Como Real; // Corregido: La palabra clave es 'Definir'.

    Escribir "Ingrese el primer número:";
    Leer n1;
    Escribir "Ingrese el segundo número:";
    Leer n2;

    promedio <- (n1 + n2) / 2; // Corregido: Añadir paréntesis para asegurar que la suma se haga antes de la división.

    Escribir "El promedio es: ", promedio; // Corregido: Usar coma para separar el texto de la variable.

FinProceso
```

## Explicación de la Solución

1.  La palabra clave para declarar variables en PSeInt es `Definir`, no `Define`. Se corrigió la primera línea.
2.  Debido a la jerarquía de operadores, la división (`/`) tiene mayor precedencia que la suma (`+`). En la línea `promedio <- n1 + n2 / 2`, primero se calcularía `n2 / 2` y luego se sumaría `n1` a ese resultado, lo cual es incorrecto para el promedio. Para calcular la suma primero, es necesario agrupar `n1 + n2` usando paréntesis: `promedio <- (n1 + n2) / 2`.
3.  En la instrucción `Escribir`, para mostrar múltiples elementos (el texto "El promedio es: " y el valor de la variable `promedio`), estos deben separarse por una coma (`,`). Faltaba la coma antes de `promedio`.
```

---

**Archivo: `Modulo1/m1-ejercicio8-8.md`**

```markdown
# Módulo 1 - Ejercicio 8 (Dificultad 8)

## Enunciado

Escribe un algoritmo que pida al usuario su edad (un número entero) y determine si es mayor de edad (18 años o más). Guarda el resultado (Verdadero o Falso) en una variable lógica y muéstrala.

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso VerificarMayoriaEdad

    Definir edad Como Entero;
    Definir es_mayor Como Logico; // Pista 1: Revisa si el nombre de la variable 'es_mayor' sigue las convenciones (o si hay caracteres inválidos).

    Escribir "Ingrese su edad:";
    Leer edad;

    // Asignar el resultado de la comparación a la variable lógica
    esMayor <- edad > 18; // Pista 2: ¿La condición "mayor de 18" incluye exactamente los 18 años?

    Escribir "Es mayor de edad?: ", es_Mayor; // Pista 3: PSeInt distingue entre mayúsculas y minúsculas en los nombres de variables. ¿Coincide con la definición?

FinProceso
```

## Solución Correcta

```pseudocode
Proceso VerificarMayoriaEdad_Solucion

    Definir edad Como Entero;
    Definir esMayor Como Logico; // Corregido: Nombre de variable válido (sin guion bajo, o usando uno consistentemente).

    Escribir "Ingrese su edad:";
    Leer edad;

    // Asignar el resultado de la comparación a la variable lógica
    esMayor <- edad >= 18; // Corregido: Usar '>=' (mayor o igual) para incluir los 18 años.

    Escribir "Es mayor de edad?: ", esMayor; // Corregido: Usar el nombre exacto 'esMayor'.

FinProceso
```

## Explicación de la Solución

1.  Aunque PSeInt puede ser flexible, los nombres de variables estándar no suelen usar guiones (`-`) y pueden tener problemas con guiones bajos (`_`) dependiendo de la configuración. Es más seguro usar `camelCase` como `esMayor`. Se cambió `es_mayor` por `esMayor`. (Si se usara `es_mayor` consistentemente estaría bien, pero el error 3 mostraba inconsistencia).
2.  El enunciado pide verificar si es "18 años o más". La condición `edad > 18` solo sería verdadera para edades de 19 en adelante. Para incluir los 18 años, la comparación correcta es `edad >= 18` (mayor o igual a 18).
3.  PSeInt, por defecto (o en modo estricto), distingue entre mayúsculas y minúsculas (es *case-sensitive*). La variable se definió como `esMayor` (o `es_mayor`) pero se intentó mostrar como `es_Mayor` (con M mayúscula). Se debe usar exactamente el mismo nombre que en la definición: `esMayor`.
```

---

**Archivo: `Modulo1/m1-ejercicio9-9.md`**

```markdown
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

## Explicación de la Solución

1.  La variable `nombreCompleto` almacenará la unión de dos cadenas de texto (nombre y apellido), por lo que su tipo de dato debe ser `Caracter` (o `Cadena`), no `Entero`.
2.  Se usó `=` en lugar del operador de asignación `<-`. Además, la concatenación de cadenas con el operador `+` no es estándar en todos los perfiles de PSeInt (aunque algunos lo permiten). Una forma más segura es usar la función `Concatenar()` o, si solo se necesita mostrar, hacerlo directamente en la instrucción `Escribir` usando comas. Se corrigió la asignación a `<-` y se usó `Concatenar()` como ejemplo robusto (ver alternativas en la solución).
3.  En la línea `Escribir`, había un espacio en el nombre de la variable (`nombre Completo` en lugar de `nombreCompleto`). Los nombres de variables no pueden contener espacios. Se corrigió a `nombreCompleto`.
```

---

**Archivo: `Modulo1/m1-ejercicio10-10.md`**

```markdown
# Módulo 1 - Ejercicio 10 (Dificultad 10)

## Enunciado

Escribe un algoritmo para una tienda simple. Debe pedir el nombre de un producto (texto), su precio unitario (real) y la cantidad de unidades compradas (entero). Luego, debe calcular el precio total (precio unitario * cantidad) y mostrar un mensaje como: "El total por [cantidad] unidades de [producto] es: $[total]".

## Código con Errores

**Instrucciones:** El siguiente código tiene 3 errores. Intenta encontrarlos y corregirlos basándote en las pistas proporcionadas como comentarios.

```pseudocode
Proceso CalculoVentaSimple

    Definir producto Como Caracter;
    Definir precioUnitario Como Real;
    Definir cantidad Como Entero;
    Definir total // Pista 1: Falta algo importante al definir la variable 'total'.

    Escribir "Ingrese nombre del producto:";
    Leer producto;
    Escribir "Ingrese precio unitario:";
    Leer precio_Unitario; // Pista 2: ¿Coincide este nombre de variable con el definido?
    Escribir "Ingrese cantidad comprada:";
    Leer cantidad;

    // Calcular total
    total = precioUnitario * cantidad; // Pista 3: Revisa el operador de asignación.

    // Mostrar resultado
    Escribir "El total por ", cantidad, " unidades de ", producto, " es: $", total;

FinProceso
```

## Solución Correcta

```pseudocode
Proceso CalculoVentaSimple_Solucion

    Definir producto Como Caracter;
    Definir precioUnitario, total Como Real; // Corregido: Definir 'total' y su tipo (Real, ya que puede tener decimales).
    Definir cantidad Como Entero;

    Escribir "Ingrese nombre del producto:";
    Leer producto;
    Escribir "Ingrese precio unitario:";
    Leer precioUnitario; // Corregido: Usar el nombre exacto 'precioUnitario'.
    Escribir "Ingrese cantidad comprada:";
    Leer cantidad;

    // Calcular total
    total <- precioUnitario * cantidad; // Corregido: Usar '<-' para asignar.

    // Mostrar resultado
    Escribir "El total por ", cantidad, " unidades de ", producto, " es: $", total;

FinProceso
```

## Explicación de la Solución

1.  Al definir la variable `total`, faltaba especificar su tipo de dato (`Como Real`, ya que la multiplicación de un `Real` por un `Entero` puede dar `Real`). Se añadió `Como Real` a la definición (o se incluyó `total` en la definición de `precioUnitario`).
2.  Al leer el precio, se usó el nombre de variable `precio_Unitario` (con guion bajo), pero se había definido como `precioUnitario` (camelCase). Se debe usar el nombre exacto de la definición. Se corrigió `Leer precio_Unitario` a `Leer precioUnitario`.
3.  Nuevamente, se usó el operador `=` para la asignación en lugar del correcto `<-`. Se corrigió `total = precioUnitario * cantidad` a `total <- precioUnitario * cantidad`.
```

---

¡Listo! Hemos creado el archivo `Modulo1.md` con la teoría y los enlaces, y los 10 archivos `.md` para cada ejercicio del Módulo 1, cada uno con su enunciado, código con errores y pistas, solución correcta y explicación.

¿Revisamos algo o procedemos con la estructura del Módulo 2?
