<!--
Meta Description: # inout en Swift: Referencias a Variables en Funciones ## Sinopsis El modificador `inout` en Swift permite pasar variables a funciones por referencia,...
Meta Keywords: inout, que, variable, funciones, valor
-->

# inout en Swift: Referencias a Variables en Funciones

## Sinopsis
El modificador `inout` en Swift permite pasar variables a funciones por referencia, lo que permite que estas funciones modifiquen el valor original de la variable.

## Documentación
El modificador `inout` se utiliza en la declaración de parámetros de funciones para indicar que el argumento puede ser modificado dentro de la función. Al usar `inout`, cualquier cambio realizado en el parámetro dentro de la función se reflejará en la variable original que fue pasada como argumento.

### Propósito
La principal intención de `inout` es facilitar la modificación de variables sin necesidad de retornar un nuevo valor. Esto es especialmente útil para realizar múltiples modificaciones en un único argumento.

### Uso
Para utilizar `inout`, sigue estos pasos:
1. Declara el parámetro de la función con el modificador `inout`.
2. Al llamar a la función, utiliza el operador `&` delante de la variable que deseas modificar.

### Ejemplo de declaración de función
```swift
func incrementarValor(_ numero: inout Int) {
    numero += 1
}
```

## Ejemplos
### Ejemplo Básico
A continuación se presenta un ejemplo básico de uso de `inout` en una función:

```swift
var contador = 0

func aumentarContador(_ valor: inout Int) {
    valor += 5
}

aumentarContador(&contador)
print(contador) // Salida: 5
```

### Ejemplo con múltiples parámetros
También puedes usar `inout` con múltiples parámetros:

```swift
func intercambiarValores(_ a: inout Int, _ b: inout Int) {
    let temp = a
    a = b
    b = temp
}

var x = 10
var y = 20

intercambiarValores(&x, &y)
print(x) // Salida: 20
print(y) // Salida: 10
```

## Explicación
### Errores Comunes
- **No usar `&`:** Si olvidas usar el operador `&` al pasar la variable, recibirás un error de compilación. Es necesario para indicar que estás pasando la variable por referencia.
- **Pasar constantes:** No puedes pasar constantes como argumentos a funciones que utilizan `inout`, ya que no se pueden modificar.

### Notas Adicionales
- `inout` se puede utilizar con cualquier tipo de variable, incluyendo tipos de valor y tipos de referencia.
- Es importante recordar que `inout` no es el mismo que la mutabilidad. Un parámetro `inout` puede ser un tipo de valor que se modifica, pero una variable de tipo referencia no necesariamente cambia su identidad.

## Resumen en una Línea
El modificador `inout` en Swift permite pasar variables a funciones por referencia, permitiendo que estas funciones modifiquen el valor original de la variable.