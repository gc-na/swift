<!--
Meta Description: # La Instrucción "continue" en Swift: Controlando el Flujo de Bucles ## Sinopsis La instrucción `continue` en Swift se utiliza dentro de bucles para o...
Meta Keywords: continue, iteración, bucle, del, código
-->

# La Instrucción "continue" en Swift: Controlando el Flujo de Bucles

## Sinopsis
La instrucción `continue` en Swift se utiliza dentro de bucles para omitir la ejecución del resto del código en la iteración actual y continuar con la siguiente iteración.

## Documentación
La instrucción `continue` es una herramienta esencial para el control de flujo en bucles, como `for`, `while` y `repeat-while`. Al utilizar `continue`, puedes saltarte determinadas condiciones en la iteración actual sin romper el bucle completo.

### Propósito
El propósito principal de `continue` es mejorar la legibilidad del código y permitir una gestión más eficiente de las condiciones dentro de los bucles.

### Uso
La instrucción `continue` se coloca dentro de un bloque de código de un bucle y se activa bajo ciertas condiciones. Cuando se ejecuta, el bucle ignora el resto del código en la iteración actual y pasa directamente a la siguiente.

### Detalles
- `continue` solo se puede utilizar dentro de bucles.
- Al ser invocada, `continue` no interrumpe el bucle, sino que lo hace continuar.
- Es útil para evitar la ejecución de código innecesario o para filtrar elementos en una colección.

## Ejemplos

### Ejemplo 1: Usando `continue` en un bucle `for`

```swift
for i in 1...5 {
    if i == 3 {
        continue // Salta a la siguiente iteración cuando i es 3
    }
    print(i) // Imprimirá 1, 2, 4, 5
}
```

### Ejemplo 2: Usando `continue` en un bucle `while`

```swift
var number = 0

while number < 5 {
    number += 1
    if number == 3 {
        continue // Salta la impresión cuando number es 3
    }
    print(number) // Imprimirá 1, 2, 4, 5
}
```

## Explicación
Un error común al usar `continue` es no tener en cuenta que, al saltar una iteración, el flujo de ejecución puede llevar a resultados no deseados, especialmente si se omiten condiciones importantes que afectan el comportamiento del bucle. Además, su uso excesivo puede hacer que el código sea más difícil de seguir. Es recomendable usar `continue` con moderación y asegurarse de que su propósito sea claro.

## Resumen en una línea
La instrucción `continue` en Swift permite omitir el resto del código en la iteración actual de un bucle y continuar con la siguiente iteración, mejorando el control del flujo de ejecución.