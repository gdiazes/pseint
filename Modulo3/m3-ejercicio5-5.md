# Módulo 3 - Ejercicio 5 (Dificultad 5)

## Enunciado
Escribe un algoritmo que pida la medida de un ángulo en grados (número real) y lo clasifique en: Agudo (< 90), Recto (= 90), Obtuso (> 90 y < 180), Llano (= 180). Considera solo ángulos entre 0 y 180 grados.

## Código con Errores
```pseudocode
Proceso TipoDeAngulo

    Definir angulo Como Real;

    Escribir "Ingrese la medida del ángulo (0-180 grados):";
    Leer angulo;

    Si angulo > 0 Y angulo < 90 // Pista 1: ¿Qué pasa con el ángulo 0? ¿Y falta el 'Entonces'?
        Escribir "Ángulo Agudo";
    Sino Si angulo = 90 Entonces
        Escribir "Ángulo Recto";
    Sino Si angulo > 90 O angulo < 180 Entonces // Pista 2: Para ser obtuso, ¿ambas condiciones deben cumplirse ('Y') o basta con una ('O')?
        Escribir "Ángulo Obtuso";
    Sino Si angulo = 180 Entonces
        Escribir "Ángulo Llano";
    Sino
        Escribir "Ángulo fuera de rango (0-180) o inválido."; // Pista 3: ¿Se consideran ángulos negativos o mayores a 180 según el 'Si' inicial?
    FinSi

FinProceso
```

<details><summary>Mostrar Solución Correcta</summary>

## Solución Correcta
```pseudocode
Proceso TipoDeAngulo_Solucion

    Definir angulo Como Real;

    Escribir "Ingrese la medida del ángulo (0-180 grados):";
    Leer angulo;

    Si angulo >= 0 Y angulo <= 180 Entonces // Validar rango primero
        Si angulo < 90 Entonces // Corregido: Incluye 0, y ya sabemos que es >= 0.
            Escribir "Ángulo Agudo";
        Sino Si angulo = 90 Entonces
            Escribir "Ángulo Recto";
        Sino Si angulo < 180 Entonces // Corregido: Ya sabemos que es > 90. Condición 'Y' implícita.
            Escribir "Ángulo Obtuso";
        Sino // Si no es < 180, y está en rango, solo puede ser 180
            Escribir "Ángulo Llano";
        FinSi
    Sino
        Escribir "Ángulo fuera de rango (0-180)."; // Corregido: Mensaje para fuera de rango.
    FinSi

FinProceso
```

</details><details><summary>Mostrar Explicación de la Solución</summary>

## Explicación de la Solución
1.  En la primera condición `Si angulo > 0 Y angulo < 90`, faltaba la palabra clave `Entonces`. Además, no consideraba el ángulo 0 como agudo (aunque estrictamente no lo sea, en clasificaciones simples a veces se incluye o se maneja aparte). La solución reestructura validando el rango 0-180 primero.
2.  Para que un ángulo sea obtuso, debe ser *simultáneamente* mayor que 90 **Y** menor que 180. El operador lógico correcto es `Y` (o `&`), no `O` (o `|`). Usar `O` haría que cualquier ángulo menor a 180 (incluidos agudos y rectos) o mayor a 90 sea clasificado como obtuso incorrectamente. La solución simplifica esto gracias a la estructura `Sino Si`.
3.  El `Sino` final del código original intentaba capturar ángulos fuera de rango, pero la lógica de las condiciones anteriores no garantizaba que solo esos casos llegaran allí. Al reestructurar con una validación de rango inicial (`Si angulo >= 0 Y angulo <= 180`), el `Sino` externo maneja correctamente los ángulos fuera de ese rango específico.

</details>