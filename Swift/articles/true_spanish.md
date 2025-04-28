<!--
Meta Description: # Verdadero en Swift: Uso y Funcionalidad del Valor Booleano ## Sinopsis En Swift, el valor booleano `true` es fundamental para las estructuras de con...
Meta Keywords: true, swift, que, valor, condiciones
-->

# Verdadero en Swift: Uso y Funcionalidad del Valor Booleano

## Sinopsis
En Swift, el valor booleano `true` es fundamental para las estructuras de control y la lógica de programación. Se utiliza para representar la verdad en condiciones, sentencias if y bucles, siendo esencial para la toma de decisiones en el código.

## Documentación
El tipo de dato `Bool` en Swift puede contener uno de dos valores: `true` o `false`. El valor `true` indica una condición afirmativa. A diferencia de otros lenguajes de programación, Swift no permite la coerción automática de otros tipos de datos a booleanos, lo que significa que debes utilizar expresiones booleanas explícitas al evaluar condiciones.

### Propósito
`true` se utiliza en operaciones lógicas y condiciones, permitiendo que los desarrolladores controlen el flujo de ejecución del programa. Por ejemplo, se usa en condiciones `if`, bucles `while`, y en expresiones booleanas.

### Uso
Para utilizar `true`, simplemente se puede asignar a una variable de tipo `Bool` o utilizarlo directamente en condiciones. Ejemplo:

```swift
let esVerdadero: Bool = true
if esVerdadero {
    print("La condición es verdadera.")
}
```

## Ejemplos
### Ejemplo 1: Uso básico de `true`
```swift
let esAdulto: Bool = true

if esAdulto {
    print("Eres un adulto.")
} else {
    print("Eres un menor.")
}
```

### Ejemplo 2: Bucle `while` con `true`
```swift
var contador = 0
while true {
    contador += 1
    if contador == 5 {
        break
    }
}
print("El bucle se detuvo después de \(contador) iteraciones.")
```

## Explicación
Uno de los errores comunes al trabajar con booleanos en Swift es intentar usar valores que no sean explícitamente `true` o `false` en condiciones. A diferencia de otros lenguajes como JavaScript, donde cualquier valor puede ser evaluado como verdadero o falso, en Swift debes asegurarte de que estás utilizando un valor de tipo `Bool`. 

Además, es importante recordar que `true` y `false` son sensibles a mayúsculas y minúsculas, por lo que `True` o `FALSE` no son válidos y generarán errores de compilación.

## Resumen en una línea
El valor `true` en Swift es un tipo booleano que representa una condición afirmativa, esencial para las estructuras de control y la lógica de programación.