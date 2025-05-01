## Módulo 2: Operadores y Expresiones Condicionales Simples

**Archivo: `Modulo2/Modulo2.md`**

```markdown
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

**¡A aplicar los operadores y condicionales!**

---
**Archivos de Ejercicios del Módulo 2:**
*(Generaré los 10 archivos .md ahora)*

**Archivo: `Modulo2/m2-ejercicio1-1.md`**
```markdown
# Módulo 2 - Ejercicio 1 (Dificultad 1)

## Enunciado
Escribe un algoritmo que pida al usuario dos números enteros y muestre el resultado de restar el segundo número al primero.

## Código con Errores
```pseudocode
Proceso RestaBasica

    Definir num1, num2, resultado Como Real; // Pista 1: Si pides enteros y restas enteros, ¿necesitas 'Real'?

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número:";
    Leer num2;

    resultado <- num1 - num_2; // Pista 2: Revisa el nombre de la segunda variable en la resta.

    Escribir "La resta es: ", resultado; // Pista 3: ¿Hay alguna palabra clave mal escrita?

Fin Proseso // Pista 3: Revisa la palabra clave final.
```

## Solución Correcta
```pseudocode
Proceso RestaBasica_Solucion

    Definir num1, num2, resultado Como Entero; // Corregido: Usar Entero si la entrada es entera.

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número:";
    Leer num2;

    resultado <- num1 - num2; // Corregido: Nombre correcto de la variable 'num2'.

    Escribir "La resta es: ", resultado;

FinProceso // Corregido: Palabra clave correcta.
```

## Explicación de la Solución
1.  Dado que se piden números enteros y la resta de enteros es un entero, es más apropiado definir las variables como `Entero` en lugar de `Real`.
2.  En la operación de resta, se escribió `num_2` en lugar de `num2`. Los nombres de variables deben coincidir exactamente con su definición.
3.  La palabra clave para finalizar un algoritmo es `FinProceso`, no `FinProseso`.
```

---
**Archivo: `Modulo2/m2-ejercicio2-2.md`**
```markdown
# Módulo 2 - Ejercicio 2 (Dificultad 2)

## Enunciado
Escribe un algoritmo que pida un número al usuario e indique si es positivo o no (considera el cero como no positivo en este caso).

## Código con Errores
```pseudocode
Proceso EsPositivo

    Definir numero Como Real;

    Escribir "Ingrese un número:";
    Leer num; // Pista 1: ¿Se está leyendo en la variable definida?

    Si numero < 0 Entonces // Pista 2: ¿La condición `numero < 0` identifica a los números positivos?
        Escribir "El número es positivo.";
    FinSi

    // Pista 3: ¿Qué pasa si el número no es menor que 0? ¿Debería mostrarse algo más? (Falta estructura)

FinProceso
```

## Solución Correcta
```pseudocode
Proceso EsPositivo_Solucion

    Definir numero Como Real;

    Escribir "Ingrese un número:";
    Leer numero; // Corregido: Leer en la variable 'numero'.

    Si numero > 0 Entonces // Corregido: Condición correcta para positivo (mayor que 0).
        Escribir "El número es positivo.";
    Sino // Añadido: Estructura 'Sino' para el caso contrario.
        Escribir "El número no es positivo (es cero o negativo).";
    FinSi

FinProceso
```

## Explicación de la Solución
1.  La variable definida fue `numero`, pero se intentó leer en `num`. Se corrigió a `Leer numero;`.
2.  La condición para que un número sea positivo es que sea `> 0`. La condición original `numero < 0` identifica a los negativos. Se cambió a `numero > 0`.
3.  El código original solo mostraba mensaje si el número era negativo (según la condición errónea). Faltaba la estructura `Sino` para manejar el caso en que la condición no se cumple (cuando el número es 0 o positivo, o en la versión corregida, cuando es 0 o negativo) y mostrar el mensaje apropiado.
```

---
**Archivo: `Modulo2/m2-ejercicio3-3.md`**
```markdown
# Módulo 2 - Ejercicio 3 (Dificultad 3)

## Enunciado
Escribe un algoritmo que pida dos números enteros, dividendo y divisor. Calcule y muestre el cociente (división real) y el resto (módulo) de la división entera.

## Código con Errores
```pseudocode
Proceso DivisionYModulo

    Definir dividendo, divisor, resto Como Entero;
    Definir cociente Como Entero; // Pista 1: El cociente de una división, ¿es siempre entero?

    Escribir "Ingrese el dividendo (entero):";
    Leer dividendo;
    Escribir "Ingrese el divisor (entero):";
    Leer divisor;

    cociente <- dividendo / divisor;
    resto <- dividendo % divisor; // Pista 2: Revisa si '%' es el operador de módulo estándar en PSeInt.

    Escribir "Cociente: ", cociente;
    Escribir "Resto: ", resto // Pista 3: Falta algo al final de esta línea.

FinProceso
```

## Solución Correcta
```pseudocode
Proceso DivisionYModulo_Solucion

    Definir dividendo, divisor, resto Como Entero;
    Definir cociente Como Real; // Corregido: El cociente puede tener decimales.

    Escribir "Ingrese el dividendo (entero):";
    Leer dividendo;
    Escribir "Ingrese el divisor (entero):";
    Leer divisor;

    cociente <- dividendo / divisor;
    resto <- dividendo MOD divisor; // Corregido: Usar 'MOD' para el módulo.

    Escribir "Cociente: ", cociente;
    Escribir "Resto: ", resto; // Corregido: Añadir punto y coma final (si es necesario).

FinProceso
```

## Explicación de la Solución
1.  El resultado de una división (`/`), incluso entre enteros, puede ser un número con decimales (ej: 7 / 2 = 3.5). Por lo tanto, la variable `cociente` debe ser de tipo `Real`.
2.  El operador estándar para calcular el módulo (resto de la división entera) en PSeInt es `MOD`, no el símbolo `%` (aunque algunos perfiles flexibles podrían aceptarlo).
3.  Faltaba el punto y coma (`;`) al final de la última instrucción `Escribir`. Aunque PSeInt puede ser permisivo, en modo estricto es necesario.
```

---
**Archivo: `Modulo2/m2-ejercicio4-4.md`**
```markdown
# Módulo 2 - Ejercicio 4 (Dificultad 4)

## Enunciado
Escribe un algoritmo que pida un número entero e indique si es par o impar. (Un número es par si el resto de dividirlo por 2 es 0).

## Código con Errores
```pseudocode
Proceso ParOImpar

    Definir num Como Entero;

    Escribir "Ingrese un número entero:";
    Leer num;

    resultado <- num MOD 2; // Pista 1: Falta definir la variable 'resultado'.

    Si resultado = 0 Entonces
        Escribir "El número es impar."; // Pista 2: Si el resto es 0, ¿el número es par o impar?
    Sino
        Escribir "El número es par."; // Pista 3: Revisa la lógica, este mensaje debería estar en el 'Entonces'.
    FinSi

FinProceso
```

## Solución Correcta
```pseudocode
Proceso ParOImpar_Solucion

    Definir num, resultado Como Entero; // Corregido: Definir la variable 'resultado'.

    Escribir "Ingrese un número entero:";
    Leer num;

    resultado <- num MOD 2;

    Si resultado = 0 Entonces
        Escribir "El número es par."; // Corregido: Mensaje correcto para resto 0.
    Sino
        Escribir "El número es impar."; // Corregido: Mensaje correcto para resto distinto de 0.
    FinSi

FinProceso
```

## Explicación de la Solución
1.  La variable `resultado` se usó para almacenar el módulo, pero no se definió previamente con `Definir`. Se añadió `resultado` a la definición de variables enteras.
2.  Si el resto de dividir por 2 (`resultado`) es 0, significa que el número es par. El mensaje original decía "impar". Se corrigió el mensaje dentro del `Entonces`.
3.  Consecuentemente, si el resto no es 0 (bloque `Sino`), el número es impar. El mensaje original decía "par". Se corrigió el mensaje dentro del `Sino`. Los mensajes estaban intercambiados.
```

---
**Archivo: `Modulo2/m2-ejercicio5-5.md`**
```markdown
# Módulo 2 - Ejercicio 5 (Dificultad 5)

## Enunciado
Escribe un algoritmo que pida dos números diferentes al usuario y muestre cuál de los dos es mayor.

## Código con Errores
```pseudocode
Proceso CompararNumeros

    Definir num1, num2 Como Real;

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número (diferente al primero):";
    Leer num2;

    Si num1 > num2 // Pista 1: ¿Es esta la palabra clave correcta para iniciar la condición?
        Escribir num1, " es mayor que ", num2;
    Sino // Pista 2: Si num1 no es mayor que num2, y sabemos que son diferentes, ¿qué podemos concluir?
        Escribir num2, " es menor que ", num1; // Pista 3: El mensaje está bien, pero ¿es la única posibilidad si num1 NO es mayor que num2? (considerando la Pista 2)
    FinSi

FinProceso
```

## Solución Correcta
```pseudocode
Proceso CompararNumeros_Solucion

    Definir num1, num2 Como Real;

    Escribir "Ingrese el primer número:";
    Leer num1;
    Escribir "Ingrese el segundo número (diferente al primero):";
    Leer num2;

    Si num1 > num2 Entonces // Corregido: Añadir 'Entonces' después de la condición.
        Escribir num1, " es mayor que ", num2;
    Sino // Lógica: Si no es mayor, y son diferentes, debe ser menor.
        Escribir num2, " es mayor que ", num1; // Corregido: Mensaje lógico para el caso 'Sino'.
    FinSi

FinProceso
```

## Explicación de la Solución
1.  La estructura condicional requiere la palabra clave `Entonces` después de la condición y antes del bloque de instrucciones a ejecutar si es verdadera. Faltaba `Entonces`.
2.  El enunciado indica que los números son diferentes. Si la condición `num1 > num2` es falsa, la única posibilidad restante es que `num1 < num2` (o sea, `num2 > num1`).
3.  Dado el punto 2, si entramos en el bloque `Sino`, significa que `num2` es el mayor. El mensaje original (`num2, " es menor que ", num1;`) era incorrecto en este contexto. Se corrigió para indicar que `num2` es mayor que `num1`.
```

---
**Archivo: `Modulo2/m2-ejercicio6-6.md`**
```markdown
# Módulo 2 - Ejercicio 6 (Dificultad 6)

## Enunciado
Una tienda ofrece un 10% de descuento si el monto total de la compra es superior a $1000. Escribe un algoritmo que pida el monto total de la compra y calcule el precio final a pagar (aplicando el descuento si corresponde).

## Código con Errores
```pseudocode
Proceso CalcularDescuento

    Definir montoCompra, precioFinal Como Real;
    Definir descuento Como Real;
    descuento <- 0.10; // 10%

    Escribir "Ingrese el monto total de la compra:";
    Leer monto_Compra; // Pista 1: Verifica la consistencia del nombre de la variable.

    precioFinal <- montoCompra; // Inicializar precio final

    Si montoCompra < 1000 Entonces // Pista 2: ¿Cuál es la condición para aplicar el descuento? (superior a 1000)
        montoDescontado = montoCompra * descuento; // Pista 3: Revisa el operador de asignación y si esta variable fue definida.
        precioFinal <- montoCompra - montoDescontado;
    FinSi

    Escribir "El precio final a pagar es: $", precioFinal;

FinProceso
```

## Solución Correcta
```pseudocode
Proceso CalcularDescuento_Solucion

    Definir montoCompra, precioFinal, montoDescontado Como Real; // Corregido: Definir montoDescontado.
    Definir descuento Como Real;
    descuento <- 0.10; // 10%

    Escribir "Ingrese el monto total de la compra:";
    Leer montoCompra; // Corregido: Nombre de variable consistente.

    precioFinal <- montoCompra; // Inicializar precio final

    Si montoCompra > 1000 Entonces // Corregido: Condición correcta para aplicar descuento (> 1000).
        montoDescontado <- montoCompra * descuento; // Corregido: Usar '<-' y variable definida.
        precioFinal <- montoCompra - montoDescontado;
    FinSi
    // Si no se cumple la condición, precioFinal mantiene el valor original de montoCompra.

    Escribir "El precio final a pagar es: $", precioFinal;

FinProceso
```

## Explicación de la Solución
1.  Se definió la variable como `montoCompra` pero se intentó leer en `monto_Compra`. Se corrigió `Leer` para usar el nombre definido.
2.  La condición para aplicar el descuento es que la compra sea *superior* a $1000, es decir, `montoCompra > 1000`. La condición original era `montoCompra < 1000`, que haría lo contrario.
3.  Dentro del `Si`, se usó `=` en lugar de `<-` para la asignación. Además, la variable `montoDescontado` no había sido definida. Se añadió `montoDescontado` a la lista de `Definir` y se corrigió el operador a `<-`.
```

---
**Archivo: `Modulo2/m2-ejercicio7-7.md`**
```markdown
# Módulo 2 - Ejercicio 7 (Dificultad 7)

## Enunciado
Escribe un algoritmo que pida al usuario ingresar una letra y determine si es una vocal (a, e, i, o, u). Considera solo letras minúsculas.

## Código con Errores
```pseudocode
Proceso EsVocalSimple

    Definir letra Como Entero; // Pista 1: ¿Es 'Entero' el tipo correcto para guardar una letra?

    Escribir "Ingrese una letra (minúscula):";
    Leer letra;

    // Comprobar si es una vocal
    Si letra = "a" O letra = "e" O letra = "i" O letra = "o" U letra = "u" Entonces // Pista 2: Revisa el operador lógico para la última vocal.
        Escribir "La letra ingresada es una vocal.";
    Sino
        Escribir "La letra ingresada no es una vocal."; // Pista 3: ¿Está bien escrito 'Escribir'?
    FinSi

FinProceso
```

## Solución Correcta
```pseudocode
Proceso EsVocalSimple_Solucion

    Definir letra Como Caracter; // Corregido: Usar 'Caracter' para letras.

    Escribir "Ingrese una letra (minúscula):";
    Leer letra;

    // Comprobar si es una vocal
    Si letra = "a" O letra = "e" O letra = "i" O letra = "o" O letra = "u" Entonces // Corregido: Usar 'O' (o '|') para todas las comparaciones.
        Escribir "La letra ingresada es una vocal.";
    Sino
        Escribir "La letra ingresada no es una vocal."; // Corregido: Palabra clave 'Escribir'.
    FinSi

FinProceso
```

## Explicación de la Solución
1.  Una variable que almacena una letra debe ser de tipo `Caracter`, no `Entero`.
2.  El operador lógico para unir condiciones con "o" es `O` (o `|`). Se usó una `U` por error al final de la condición compuesta. Se reemplazó `U` por `O`.
3.  En el bloque `Sino`, la instrucción para mostrar el mensaje estaba mal escrita como `Escribir` (faltaba la 'r'). Se corrigió a `Escribir`.
```

---
**Archivo: `Modulo2/m2-ejercicio8-8.md`**
```markdown
# Módulo 2 - Ejercicio 8 (Dificultad 8)

## Enunciado
Simula un inicio de sesión muy básico. Define un nombre de usuario y una contraseña correctos dentro del algoritmo. Pide al usuario que ingrese su usuario y contraseña. Muestra "Acceso concedido" si ambos coinciden con los correctos, y "Acceso denegado" en caso contrario.

## Código con Errores
```pseudocode
Proceso LoginBasico

    Definir usrCorrecto, pwdCorrecta, usrIngresado, pwdIngresada Como Caracter;

    usrCorrecto <- "admin"
    pwdCorrecta <- "1234"; // Pista 1: Revisa si falta algo al final de la asignación anterior.

    Escribir "Usuario:";
    Leer usrIngresado;
    Escribir "Contraseña:";
    Leer pwdIngresada;

    // Verificar credenciales
    Si usrIngresado = usrCorrecto Y pwdIngresada = pwdCorrecta Entonces // Pista 2: ¿Está completa la estructura del 'Si'?
        Escribir "Acceso concedido.";
    Sino
        Escribir "Acceso denegado"; // Pista 3: Falta algo al final de esta línea.

FinProceso // Pista 2: (Relacionado) ¿Dónde termina el bloque 'Sino'?
```

## Solución Correcta
```pseudocode
Proceso LoginBasico_Solucion

    Definir usrCorrecto, pwdCorrecta, usrIngresado, pwdIngresada Como Caracter;

    usrCorrecto <- "admin"; // Corregido: Añadir punto y coma.
    pwdCorrecta <- "1234";

    Escribir "Usuario:";
    Leer usrIngresado;
    Escribir "Contraseña:";
    Leer pwdIngresada;

    // Verificar credenciales
    Si usrIngresado = usrCorrecto Y pwdIngresada = pwdCorrecta Entonces
        Escribir "Acceso concedido.";
    Sino
        Escribir "Acceso denegado."; // Corregido: Añadir punto y coma.
    FinSi // Corregido: Añadir 'FinSi' para cerrar la estructura condicional.

FinProceso
```

## Explicación de la Solución
1.  Faltaba el punto y coma (`;`) al final de la línea `usrCorrecto <- "admin"`.
2.  La estructura condicional `Si ... Entonces ... Sino ...` debe terminar obligatoriamente con `FinSi`. Faltaba esta palabra clave al final.
3.  Faltaba el punto y coma (`;`) al final de la instrucción `Escribir "Acceso denegado"`.
```

---
**Archivo: `Modulo2/m2-ejercicio9-9.md`**
```markdown
# Módulo 2 - Ejercicio 9 (Dificultad 9)

## Enunciado
Escribe un algoritmo que pida un número (puede ser positivo, negativo o cero) y muestre su valor absoluto. El valor absoluto de un número es el número sin signo (ej: |-5| = 5, |7| = 7, |0| = 0).

## Código con Errores
```pseudocode
Proceso ValorAbsoluto

    Definir numero, valorAbs Como Real;

    Escribir "Ingrese un número:";
    Leer numero;

    Si numero >= 0 Entonces
        valorAbs = numero; // Pista 1: Revisa el operador de asignación.
    Sino
        valorAbs <- -numero; // Si es negativo, lo convierte a positivo
    // Pista 2: ¿Falta cerrar la estructura condicional?

    Escribir "El valor absoluto de ", numero, " es : ", valorAbs; // Pista 3: Revisa la sintaxis de esta línea Escribir. ¿Hay algún error tipográfico?

FinProceso
```

## Solución Correcta
```pseudocode
Proceso ValorAbsoluto_Solucion

    Definir numero, valorAbs Como Real;

    Escribir "Ingrese un número:";
    Leer numero;

    Si numero >= 0 Entonces
        valorAbs <- numero; // Corregido: Usar '<-'.
    Sino
        valorAbs <- -numero; // Si es negativo, lo convierte a positivo
    FinSi // Corregido: Añadir 'FinSi'.

    Escribir "El valor absoluto de ", numero, " es: ", valorAbs; // Corregido: Quitar espacio antes de ':'.

FinProceso
```

## Explicación de la Solución
1.  En el bloque `Entonces`, se usó `=` en lugar del operador de asignación correcto `<-`.
2.  Faltaba la palabra clave `FinSi` para cerrar la estructura `Si/Sino`.
3.  En la línea `Escribir` final, había un espacio extra antes de los dos puntos (`es : `). Aunque no es un error de ejecución grave, es un error de formato/tipeo. Se corrigió a `es: `.
```

---
**Archivo: `Modulo2/m2-ejercicio10-10.md`**
```markdown
# Módulo 2 - Ejercicio 10 (Dificultad 10)

## Enunciado
Para que tres longitudes (l1, l2, l3) puedan formar un triángulo, se debe cumplir la "desigualdad triangular": la suma de las longitudes de dos lados cualesquiera debe ser mayor que la longitud del tercer lado. Escribe un algoritmo que pida las tres longitudes (reales) y determine si pueden formar un triángulo válido.

## Código con Errores
```pseudocode
Proceso TrianguloValido

    Definir l1, l2, l3 Como Real;
    Definir esValido Como Caracter; // Pista 1: ¿Es 'Caracter' el tipo adecuado para guardar un resultado Verdadero/Falso?

    Escribir "Ingrese la longitud del lado 1:";
    Leer l1;
    Escribir "Ingrese la longitud del lado 2:";
    Leer l2;
    Escribir "Ingrese la longitud del lado 3:";
    Leer l3;

    // Verificar desigualdad triangular
    cond1 <- (l1 + l2) > l3;
    cond2 <- (l1 + l3) > l2;
    cond3 <- (l2 + l3) > l1;

    esValido = cond1 Y cond2 Y cond3; // Pista 2: Revisa el operador de asignación.

    Si (esValido) Entonces // Pista 3: En PSeInt, ¿se compara directamente una variable lógica con Verdadero/Falso o se usa su valor?
        Escribir "Las longitudes pueden formar un triángulo.";
    Sino
        Escribir "Las longitudes NO pueden formar un triángulo.";
    FinSi

FinProceso
```

## Solución Correcta
```pseudocode
Proceso TrianguloValido_Solucion

    Definir l1, l2, l3 Como Real;
    Definir cond1, cond2, cond3, esValido Como Logico; // Corregido: Usar 'Logico' para Verdadero/Falso.

    Escribir "Ingrese la longitud del lado 1:";
    Leer l1;
    Escribir "Ingrese la longitud del lado 2:";
    Leer l2;
    Escribir "Ingrese la longitud del lado 3:";
    Leer l3;

    // Verificar desigualdad triangular
    cond1 <- (l1 + l2) > l3;
    cond2 <- (l1 + l3) > l2;
    cond3 <- (l2 + l3) > l1;

    esValido <- cond1 Y cond2 Y cond3; // Corregido: Usar '<-'.

    Si esValido Entonces // Corregido: Se usa directamente la variable lógica en la condición.
        Escribir "Las longitudes pueden formar un triángulo.";
    Sino
        Escribir "Las longitudes NO pueden formar un triángulo.";
    FinSi

FinProceso
```

## Explicación de la Solución
1.  La variable `esValido` (y las condiciones `cond1`, `cond2`, `cond3`) almacenan un resultado lógico (Verdadero o Falso), por lo que su tipo debe ser `Logico`, no `Caracter`.
2.  Se usó `=` en lugar de `<-` para asignar el resultado de la combinación lógica a `esValido`.
3.  En PSeInt, una variable de tipo `Logico` ya contiene `Verdadero` o `Falso`. No es necesario (y generalmente es redundante) compararla explícitamente con `Verdadero` (ej: `Si esValido = Verdadero Entonces`). Se puede usar directamente `Si esValido Entonces`. El código original con `Si (esValido) Entonces` es aceptable en PSeInt flexible, pero usarla directamente es más común y limpio. El "error" estaba más relacionado con la definición incorrecta del tipo en el punto 1. Al corregir el tipo, la condición `Si esValido Entonces` funciona perfectamente.
```

---

¡Módulo 2 completo! Continuaré con el Módulo 3.
