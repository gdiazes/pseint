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
<details>
  <summary>Mostrar Explicación de la Solución</summary>
  
## Explicación de la Solución
1.  Faltaba el punto y coma (`;`) al final de la línea `usrCorrecto <- "admin"`.
2.  La estructura condicional `Si ... Entonces ... Sino ...` debe terminar obligatoriamente con `FinSi`. Faltaba esta palabra clave al final.
3.  Faltaba el punto y coma (`;`) al final de la instrucción `Escribir "Acceso denegado"`.

</details>
