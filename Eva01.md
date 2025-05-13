# Evaluación: PSeInt - Módulos 1, 2 y 3

**Instrucciones:** Resuelve los siguientes 10 problemas utilizando pseudocódigo en PSeInt. Asegúrate de definir adecuadamente las variables, utilizar los operadores correctos y aplicar las estructuras condicionales necesarias para cumplir con los requisitos de cada enunciado. Todos los ejercicios tienen una **Dificultad: 10/10** (considerando solo los temas de los Módulos 1-3).

---

## Ejercicio 1: Calculadora de Tarifa Eléctrica

**Enunciado:** Escribe un algoritmo que calcule el monto a pagar por el consumo de energía eléctrica. Se debe pedir al usuario la cantidad de KWh consumidos (puede ser real). La tarifa se calcula de la siguiente manera:
*   Los primeros 100 KWh tienen un costo de $1.5 por KWh.
*   Los siguientes 150 KWh (es decir, de 101 KWh a 250 KWh) tienen un costo de $2.0 por KWh.
*   El consumo excedente por encima de 250 KWh tiene un costo de $3.0 por KWh.
Además, si el consumo total supera los 400 KWh, se aplica un cargo adicional fijo de $50 por "alto consumo". Muestra el monto total a pagar.

**Conceptos Clave:** Variables Reales, Operadores Aritméticos, Operadores Relacionales, `Si`/`Sino Si`/`Sino` anidados o secuenciales.

```markdown
### Ejercicio 1: Calculadora de Tarifa Eléctrica (Dificultad 10)

**Enunciado:** Escribe un algoritmo que calcule el monto a pagar por el consumo de energía eléctrica. Se debe pedir al usuario la cantidad de KWh consumidos (puede ser real). La tarifa se calcula de la siguiente manera:
*   Los primeros 100 KWh tienen un costo de $1.5 por KWh.
*   Los siguientes 150 KWh (es decir, de 101 KWh a 250 KWh) tienen un costo de $2.0 por KWh.
*   El consumo excedente por encima de 250 KWh tiene un costo de $3.0 por KWh.
Además, si el consumo total supera los 400 KWh, se aplica un cargo adicional fijo de $50 por "alto consumo". Muestra el monto total a pagar.

**Salida Esperada:** Un mensaje claro indicando el total a pagar. Ej: "El total a pagar es: $XXX.XX"
```

---

## Ejercicio 2: Clasificación Completa de Triángulos

**Enunciado:** Pide al usuario las longitudes de los tres lados de un triángulo (l1, l2, l3 - pueden ser reales). Primero, verifica si esas longitudes pueden formar un triángulo válido (la suma de dos lados cualesquiera debe ser mayor que el tercer lado). Si no es válido, muestra un mensaje de error. Si es válido, clasifícalo y muestra *todas* las clasificaciones que apliquen:
*   Según sus lados: Equilátero (3 lados iguales), Isósceles (2 lados iguales), Escaleno (ningún lado igual).
*   Según sus ángulos (usando el Teorema de Pitágoras generalizado: `c^2 = a^2 + b^2 - 2ab*cos(C)` implica `cos(C) = (a^2 + b^2 - c^2) / (2ab)`. Si `cos(C) > 0` -> ángulo agudo, `cos(C) = 0` -> ángulo recto, `cos(C) < 0` -> ángulo obtuso. Debes encontrar el ángulo opuesto al lado más largo para clasificar el triángulo): Rectángulo (un ángulo recto), Acutángulo (todos los ángulos agudos), Obtusángulo (un ángulo obtuso).

**Conceptos Clave:** Variables Reales, Op. Aritméticos (`^`), Op. Relacionales, Op. Lógicos (`Y`), `Si`/`Sino Si`/`Sino` anidados, Validación compleja.

```markdown
### Ejercicio 2: Clasificación Completa de Triángulos (Dificultad 10)

**Enunciado:** Pide al usuario las longitudes de los tres lados de un triángulo (l1, l2, l3 - pueden ser reales). Primero, verifica si esas longitudes pueden formar un triángulo válido (la suma de dos lados cualesquiera debe ser mayor que el tercer lado). Si no es válido, muestra un mensaje de error. Si es válido, clasifícalo y muestra *todas* las clasificaciones que apliquen:
*   Según sus lados: Equilátero, Isósceles o Escaleno.
*   Según sus ángulos (usando el Teorema de Pitágoras o su generalización): Rectángulo, Acutángulo u Obtusángulo. (Pista: compara el cuadrado del lado más largo con la suma de los cuadrados de los otros dos).

**Salida Esperada:** "No es un triángulo válido." o "Clasificación: [Tipo Lados], [Tipo Ángulos]". Ej: "Clasificación: Isósceles, Acutángulo".
```

---

## Ejercicio 3: Descuento Avanzado en Tienda

**Enunciado:** Una tienda aplica descuentos basados en el monto de la compra y si el cliente es miembro VIP o no. Pide al usuario el monto total de la compra (real) y si es miembro VIP (Lógico: Verdadero/Falso, o Caracter: 'S'/'N'). Las reglas son:
*   Compras menores a $500: Sin descuento.
*   Compras de $500 a $1500 (inclusive): 5% de descuento para no-VIP, 10% para VIP.
*   Compras mayores a $1500: 10% de descuento para no-VIP, 15% para VIP.
Calcula y muestra el monto final a pagar.

**Conceptos Clave:** Variables Reales/Lógicas/Caracteres, Op. Aritméticos, Op. Relacionales, Op. Lógicos (`Y`), `Si`/`Sino Si`/`Sino` anidados.

```markdown
### Ejercicio 3: Descuento Avanzado en Tienda (Dificultad 10)

**Enunciado:** Una tienda aplica descuentos basados en el monto de la compra y si el cliente es miembro VIP o no. Pide al usuario el monto total de la compra (real) y si es miembro VIP (Lógico: Verdadero/Falso, o puedes usar Caracter: 'S'/'N' y convertirlo a Lógico). Las reglas son:
*   Compras menores a $500: Sin descuento.
*   Compras de $500 a $1500 (inclusive): 5% de descuento para no-VIP, 10% para VIP.
*   Compras mayores a $1500: 10% de descuento para no-VIP, 15% para VIP.
Calcula y muestra el monto final a pagar después del descuento.

**Salida Esperada:** "El monto final a pagar es: $XXX.XX"
```

---

## Ejercicio 4: Mini Menú de Conversiones

**Enunciado:** Crea un programa que muestre un menú con 3 opciones de conversión de temperatura:
1.  Celsius a Fahrenheit (F = C * 9/5 + 32)
2.  Fahrenheit a Celsius (C = (F - 32) * 5/9)
3.  Celsius a Kelvin (K = C + 273.15)
Pide al usuario que elija una opción (1, 2 o 3). Luego, pide la temperatura en la unidad original (real). Realiza la conversión seleccionada usando la estructura `Segun` y muestra el resultado. Si la opción no es válida, muestra un mensaje de error.

**Conceptos Clave:** Variables Reales/Enteras, `Escribir`/`Leer`, `Segun`, Op. Aritméticos.

```markdown
### Ejercicio 4: Mini Menú de Conversiones (Dificultad 10)

**Enunciado:** Crea un programa que muestre un menú con 3 opciones de conversión de temperatura:
1.  Celsius a Fahrenheit (F = C * 9/5 + 32)
2.  Fahrenheit a Celsius (C = (F - 32) * 5/9)
3.  Celsius a Kelvin (K = C + 273.15)
Pide al usuario que elija una opción (1, 2 o 3). Luego, pide la temperatura en la unidad original (real). Realiza la conversión seleccionada usando la estructura `Segun` y muestra el resultado formateado. Ej: "XX.X °C equivalen a YY.Y °F". Si la opción no es válida, muestra "Opción inválida.".

**Salida Esperada:** El resultado de la conversión o un mensaje de error.
```

---

## Ejercicio 5: Clasificación de Notas con Múltiples Criterios

**Enunciado:** Pide al usuario una calificación numérica (0-100, real). Clasifícala según el siguiente sistema y muestra *solo una* categoría:
*   90-100: "A - Excelente"
*   80-89.9: "B - Bueno"
*   70-79.9: "C - Satisfactorio"
*   60-69.9: "D - Suficiente"
*   0-59.9: "F - No aprobado"
Además, si la nota está fuera del rango 0-100, muestra "Nota inválida". Usa `Si`/`Sino Si`/`Sino`.

**Conceptos Clave:** Variables Reales, Op. Relacionales, Op. Lógicos (`Y`), `Si`/`Sino Si`/`Sino`.

```markdown
### Ejercicio 5: Clasificación de Notas con Múltiples Criterios (Dificultad 10)

**Enunciado:** Pide al usuario una calificación numérica (0-100, real). Clasifícala según el siguiente sistema y muestra *solo una* categoría:
*   90-100: "A - Excelente"
*   80-89.9: "B - Bueno"
*   70-79.9: "C - Satisfactorio"
*   60-69.9: "D - Suficiente"
*   0-59.9: "F - No aprobado"
Asegúrate de manejar primero el caso de que la nota esté fuera del rango 0-100, mostrando "Nota inválida.". Utiliza una estructura `Si`/`Sino Si`/`Sino` eficiente.

**Salida Esperada:** La categoría correspondiente o "Nota inválida.".
```

---

## Ejercicio 6: Validación de Fecha Compleja (Simplificada)

**Enunciado:** Pide al usuario día, mes y año (números enteros). Valida si la fecha es "básicamente correcta" según estas reglas (sin considerar años bisiestos):
*   Año debe ser positivo.
*   Mes debe estar entre 1 y 12.
*   Día debe estar entre 1 y 31 para meses 1, 3, 5, 7, 8, 10, 12.
*   Día debe estar entre 1 y 30 para meses 4, 6, 9, 11.
*   Día debe estar entre 1 y 28 para mes 2 (Febrero).
Muestra "Fecha válida" o "Fecha inválida".

**Conceptos Clave:** Variables Enteras, Op. Relacionales, Op. Lógicos (`Y`, `O`), `Si`/`Sino Si`/`Sino` anidados o `Segun` combinado con `Si`.

```markdown
### Ejercicio 6: Validación de Fecha Compleja (Simplificada) (Dificultad 10)

**Enunciado:** Pide al usuario día, mes y año (números enteros). Valida si la fecha es "básicamente correcta" según estas reglas (sin considerar años bisiestos por ahora):
*   Año > 0
*   Mes entre 1 y 12
*   Día entre 1 y 31 para meses con 31 días (1, 3, 5, 7, 8, 10, 12).
*   Día entre 1 y 30 para meses con 30 días (4, 6, 9, 11).
*   Día entre 1 y 28 para mes 2.
Si todas las condiciones se cumplen, muestra "Fecha válida". En cualquier otro caso, muestra "Fecha inválida".

**Salida Esperada:** "Fecha válida" o "Fecha inválida".
```

---

## Ejercicio 7: Identificador de Tipo de Carácter

**Enunciado:** Pide al usuario que ingrese un solo carácter. Determina y muestra si el carácter es:
*   Una vocal minúscula ('a', 'e', 'i', 'o', 'u')
*   Una vocal mayúscula ('A', 'E', 'I', 'O', 'U')
*   Una consonante minúscula (cualquier otra letra de 'a' a 'z')
*   Una consonante mayúscula (cualquier otra letra de 'A' a 'Z')
*   Un dígito ('0' a '9')
*   Otro símbolo (cualquier otro carácter)
Usa condicionales anidados o `Si`/`Sino Si`. (Pista: puedes comparar caracteres directamente, ej: `car >= 'a' Y car <= 'z'`).

**Conceptos Clave:** Variables Caracter, Op. Relacionales con caracteres, Op. Lógicos (`Y`, `O`), `Si`/`Sino Si`/`Sino` anidados.

```markdown
### Ejercicio 7: Identificador de Tipo de Carácter (Dificultad 10)

**Enunciado:** Pide al usuario que ingrese un solo carácter. Determina y muestra a cuál de las siguientes categorías pertenece:
*   "Vocal Minúscula"
*   "Vocal Mayúscula"
*   "Consonante Minúscula"
*   "Consonante Mayúscula"
*   "Dígito"
*   "Otro Símbolo"
(Pista: El orden de las comprobaciones importa. Verifica primero vocales, luego consonantes, luego dígitos).

**Salida Esperada:** Una de las categorías listadas.
```

---

## Ejercicio 8: Cálculo de Salario con Bonificación

**Enunciado:** Pide al usuario las horas trabajadas en la semana (entero) y la tarifa por hora (real). Calcula el salario semanal. Las horas normales (hasta 40) se pagan a la tarifa normal. Las horas extra (más de 40) se pagan al doble de la tarifa normal. Además, si el salario total calculado (incluyendo extras) supera los $2000, se añade una bonificación fija de $100. Muestra el salario final (con bonificación si aplica).

**Conceptos Clave:** Variables Enteras/Reales, Op. Aritméticos, Op. Relacionales, `Si`/`Sino`, Condicional anidado o secuencial.

```markdown
### Ejercicio 8: Cálculo de Salario con Bonificación (Dificultad 10)

**Enunciado:** Pide al usuario las horas trabajadas en la semana (entero) y la tarifa por hora (real). Calcula el salario semanal según estas reglas:
*   Las primeras 40 horas se pagan a la tarifa normal.
*   Las horas que excedan las 40 se pagan al doble de la tarifa normal.
*   Si el salario total calculado (normal + extra) supera los $2000, se añade una bonificación fija de $100 al total.
Muestra el salario final a percibir.

**Salida Esperada:** "El salario final es: $XXX.XX"
```

---

## Ejercicio 9: Juego de Dados Simple (Mayor Puntaje)

**Enunciado:** Simula el lanzamiento de dos dados (números aleatorios del 1 al 6) para dos jugadores (Jugador 1 y Jugador 2). Calcula la suma de los dos dados para cada jugador. Determina quién ganó (el que tenga la suma mayor) o si hubo empate. Muestra los resultados de los dados de cada jugador, su suma y quién ganó. (Usa la función `azar(6) + 1` para simular cada dado).

**Conceptos Clave:** Variables Enteras, `azar()`, Op. Aritméticos, Op. Relacionales, `Si`/`Sino Si`/`Sino`.

```markdown
### Ejercicio 9: Juego de Dados Simple (Mayor Puntaje) (Dificultad 10)

**Enunciado:** Simula el lanzamiento de dos dados para el Jugador 1 y dos dados para el Jugador 2 (cuatro números aleatorios entre 1 y 6 usando `azar(6) + 1`). Calcula la suma de los puntos para cada jugador. Muestra los dados lanzados por cada uno, su suma total, y finalmente indica quién ganó (el de mayor suma) o si fue un empate.

**Salida Esperada:** Mensajes como:
"Jugador 1 lanzó: D1 y D2 -> Suma: S1"
"Jugador 2 lanzó: D3 y D4 -> Suma: S2"
"Resultado: [Jugador 1 gana / Jugador 2 gana / Empate]"
```

---

## Ejercicio 10: Verificación de Acceso con Doble Factor (Simplificado)

**Enunciado:** Define un usuario (`usrCorrecto`) y una contraseña (`pwdCorrecta`) fijos en el código. Pide al usuario que ingrese su usuario y contraseña. Si ambos coinciden, pide un código de verificación de 3 dígitos (entero) que también está fijo en el código (`codigoCorrecto`). Si el código ingresado también coincide, muestra "Acceso Concedido". En cualquier otro caso (usuario incorrecto, contraseña incorrecta, o código incorrecto), muestra "Acceso Denegado". Usa condicionales anidados.

**Conceptos Clave:** Variables Caracter/Entero, Op. Relacionales (`=`), Op. Lógicos (`Y`), `Si`/`Sino` anidados.



¡Mucha suerte con la evaluación! Estos ejercicios pondrán a prueba la comprensión integrada de los primeros tres módulos.
