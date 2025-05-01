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

<details> <summary>Mostrar Solución Correcta</summary> ## Solución Correcta
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

</details><details><summary>Mostrar Explicación de la Solución</summary>## Explicación de la Solución
1.  Una variable que almacena una letra debe ser de tipo `Caracter`, no `Entero`.
2.  El operador lógico para unir condiciones con "o" es `O` (o `|`). Se usó una `U` por error al final de la condición compuesta. Se reemplazó `U` por `O`.
3.  En el bloque `Sino`, la instrucción para mostrar el mensaje estaba mal escrita como `Escribir` (faltaba la 'r'). Se corrigió a `Escribir`.
</details>
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

<details> 
  <summary>Mostrar Solución Correcta</summary> 
  
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

</details>
<details><summary>Mostrar Explicación de la Solución</summary>
  
## Explicación de la Solución
1.  Faltaba el punto y coma (`;`) al final de la línea `usrCorrecto <- "admin"`.
2.  La estructura condicional `Si ... Entonces ... Sino ...` debe terminar obligatoriamente con `FinSi`. Faltaba esta palabra clave al final.
3.  Faltaba el punto y coma (`;`) al final de la instrucción `Escribir "Acceso denegado"`.

</details>
