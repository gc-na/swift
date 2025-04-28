<!--
Meta Description: # Uso del bucle "for" en Swift: Guía Completa ## Sinopsis El bucle "for" en Swift permite iterar sobre una secuencia de elementos, como arrays, diccio...
Meta Keywords: swift, bucle, iterar, sobre, una
-->

# Uso del bucle "for" en Swift: Guía Completa

## Sinopsis
El bucle "for" en Swift permite iterar sobre una secuencia de elementos, como arrays, diccionarios, o rangos numéricos, facilitando la repetición de código de manera eficiente y legible.

## Documentación
El bucle "for" es una de las estructuras de control más utilizadas en Swift. Su propósito principal es ejecutar un bloque de código un número determinado de veces o recorrer colecciones de datos. Swift proporciona varias formas de utilizar "for", lo que lo hace versátil para diferentes tipos de iteraciones.

### Tipos de bucles "for":
1. **for-in**: Utilizado para iterar sobre elementos en una colección.
2. **for**: Permite iterar un número específico de veces utilizando un rango.

### Sintaxis
1. **for-in**:
   ```swift
   for elemento in colección {
       // Código a ejecutar
   }
   ```

2. **for**:
   ```swift
   for i in 0..<n {
       // Código a ejecutar
   }
   ```
   Donde `n` es el número de iteraciones.

## Ejemplos

### Ejemplo 1: Uso de for-in con un array
```swift
let frutas = ["manzana", "banana", "cereza"]
for fruta in frutas {
    print(fruta)
}
```

### Ejemplo 2: Uso de for con un rango
```swift
for i in 1...5 {
    print("Iteración número \(i)")
}
```

### Ejemplo 3: Iterar sobre un diccionario
```swift
let edades = ["Juan": 25, "Ana": 30, "Pedro": 22]
for (nombre, edad) in edades {
    print("\(nombre) tiene \(edad) años.")
}
```

## Explicación
Al utilizar el bucle "for", es importante tener en cuenta algunas consideraciones:

- **Rango cerrado vs. rango abierto**: Al usar `0..<n`, se incluye desde 0 hasta `n-1`. Si se desea incluir `n`, se debe usar `0...n`.
- **Mutabilidad de los elementos**: Al iterar sobre colecciones, los elementos son constantes a menos que se declare explícitamente como variables dentro del bucle.
- **Evitar errores comunes**: Asegúrate de no modificar la colección que estás iterando, ya que esto puede llevar a errores en tiempo de ejecución.

## Resumen en una línea
El bucle "for" en Swift es una herramienta fundamental para iterar sobre colecciones y realizar tareas repetitivas de manera eficiente y legible.