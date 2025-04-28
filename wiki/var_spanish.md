<!--
Meta Description: # Uso de "var" en Swift: Declaración de Variables ## Sinopsis La palabra clave `var` en Swift se utiliza para declarar variables que pueden cambiar su...
Meta Keywords: que, var, swift, variables, variable
-->

# Uso de "var" en Swift: Declaración de Variables

## Sinopsis
La palabra clave `var` en Swift se utiliza para declarar variables que pueden cambiar su valor a lo largo del tiempo. Es una de las formas más fundamentales de manejar datos en el lenguaje.

## Documentación
En Swift, `var` es una palabra clave que permite crear variables. Las variables son contenedores que almacenan información que puede ser modificada durante la ejecución del programa. A diferencia de las constantes, que se declaran con la palabra clave `let`, las variables pueden ser reasignadas.

### Propósito
El propósito de `var` es permitir a los desarrolladores almacenar y manipular datos que pueden cambiar. Esto es útil en situaciones donde los valores no son fijos, como contadores, entradas del usuario o resultados de cálculos.

### Uso
Para declarar una variable en Swift, se utiliza la sintaxis:

```swift
var nombreVariable: Tipo = valorInicial
```

- `nombreVariable`: el nombre que le das a la variable.
- `Tipo`: el tipo de dato que almacenará la variable (opcional, Swift puede inferir el tipo).
- `valorInicial`: el valor con el que se inicia la variable.

### Ejemplo
Aquí hay algunos ejemplos simples de cómo usar `var` en Swift:

```swift
var contador: Int = 0
contador += 1  // contador ahora es 1

var nombre: String = "Juan"
nombre = "Pedro"  // nombre ahora es "Pedro"

var temperatura = 25.0  // Inferencia de tipo a Double
temperatura += 5.0  // temperatura ahora es 30.0
```

## Explicación
Algunos errores comunes al usar `var` incluyen:

- **No inicializar una variable**: En Swift, todas las variables deben ser inicializadas antes de ser utilizadas. Intentar acceder a una variable sin un valor inicial generará un error de compilación.
  
- **Confusión entre `var` y `let`**: Recuerda que `var` es para variables mutables, mientras que `let` es para constantes inmutables. Usar `let` cuando necesitas cambiar el valor posteriormente causará errores.

- **Tipos de dato**: Asegúrate de asignar un valor que coincida con el tipo de dato de la variable, o deja que Swift infiera el tipo adecuadamente.

## Resumen en una línea
La palabra clave `var` en Swift se utiliza para declarar variables mutables que pueden cambiar de valor a lo largo del tiempo.