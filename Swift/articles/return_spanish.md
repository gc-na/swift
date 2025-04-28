<!--
Meta Description: # El Comando "return" en Swift: Utilidad y Ejemplos ## Sinopsis El comando `return` en Swift es fundamental para finalizar la ejecución de una función...
Meta Keywords: return, función, que, una, valor
-->

# El Comando "return" en Swift: Utilidad y Ejemplos

## Sinopsis
El comando `return` en Swift es fundamental para finalizar la ejecución de una función y devolver un valor al llamador, permitiendo así que los resultados de cálculos o procesos sean utilizados en otras partes del código.

## Documentación
El comando `return` se utiliza en funciones de Swift para indicar el final de su ejecución y para devolver un valor específico al contexto donde fue llamada la función. Esto es crucial en la programación funcional y orientada a objetos, ya que permite que las funciones sean reutilizables y modulares.

### Propósito
El propósito del `return` es:
- Finalizar la ejecución de una función.
- Pasar un valor de regreso al llamador, permitiendo el uso de resultados calculados.

### Uso
El uso básico de `return` se presenta dentro de una función, seguido del valor que se desea devolver. En funciones que no devuelven un valor (funciones `Void`), el `return` es opcional.

### Detalles
- Si una función tiene un tipo de retorno, debe utilizar `return` para devolver un valor de ese tipo.
- Si no se incluye un `return` donde se espera uno, el compilador generará un error.
- El `return` puede estar en cualquier parte de la función, pero una vez ejecutado, la función termina inmediatamente.

## Ejemplos

### Ejemplo 1: Función que retorna un entero
```swift
func sumar(a: Int, b: Int) -> Int {
    return a + b
}

let resultado = sumar(a: 5, b: 3) // resultado será 8
```

### Ejemplo 2: Función que retorna un booleano
```swift
func esPar(numero: Int) -> Bool {
    return numero % 2 == 0
}

let esNumeroPar = esPar(numero: 4) // esNumeroPar será true
```

### Ejemplo 3: Función sin retorno
```swift
func imprimirMensaje(mensaje: String) {
    print(mensaje)
    // No se necesita return aquí
}

imprimirMensaje(mensaje: "Hola, Swift!")
```

## Explicación
Un error común es intentar usar `return` en funciones que no tienen un tipo de retorno definido. Esto generará un error de compilación. Además, es importante recordar que el `return` puede aparecer varias veces en una función, permitiendo salidas tempranas en condiciones específicas. Sin embargo, el `return` debe corresponder al tipo de dato especificado en la declaración de la función.

### Errores comunes
1. **Olvidar el tipo de retorno**: Si se declara una función que espera devolver un valor y no se usa `return`, el compilador indicará un error.
2. **Confusión con funciones de tipo `Void`**: En funciones que no devuelven un valor, el uso de `return` es opcional y puede omitirse, lo que a veces puede llevar a confusiones.

## Resumen en una línea
El comando `return` en Swift finaliza la ejecución de una función y devuelve un valor al llamador, siendo esencial para la modularidad y reutilización del código.