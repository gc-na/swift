<!--
Meta Description: # Subscript en Swift: Acceso Eficiente a Colecciones y Objetos ## Sinopsis El subscript en Swift es una característica que permite acceder a los eleme...
Meta Keywords: subscript, que, una, swift, los
-->

# Subscript en Swift: Acceso Eficiente a Colecciones y Objetos

## Sinopsis
El subscript en Swift es una característica que permite acceder a los elementos de una colección, como arreglos o diccionarios, de manera concisa y legible. Ofrece una sintaxis similar a la de los arrays, facilitando la interacción con estructuras de datos personalizadas.

## Documentación
El subscript es una forma de acceder a los elementos dentro de una colección, mediante una sintaxis que utiliza corchetes `[]`. En Swift, puedes definir subscripts en tus propias clases y estructuras, permitiendo un acceso intuitivo a las propiedades de tus objetos.

### Propósito
El propósito principal del subscript es proporcionar una forma rápida y fácil de acceder a los elementos de una colección o estructura de datos. Esto mejora la legibilidad del código y reduce la necesidad de métodos adicionales para realizar accesos simples.

### Uso
Para definir un subscript, utilizas la palabra clave `subscript`, seguida de parámetros que indican qué tipo de acceso necesitas. Un subscript puede ser de lectura, de escritura, o ambos.

```swift
struct Puntos {
    var puntos: [Int]
    
    subscript(index: Int) -> Int {
        get {
            return puntos[index]
        }
        set {
            puntos[index] = newValue
        }
    }
}
```

En este ejemplo, la estructura `Puntos` tiene un subscript que permite acceder a los elementos del arreglo `puntos` de forma simple.

## Ejemplos

### Ejemplo Básico de Subscript
```swift
struct Matriz {
    var valores: [[Int]]

    subscript(fila: Int, columna: Int) -> Int {
        get {
            return valores[fila][columna]
        }
        set {
            valores[fila][columna] = newValue
        }
    }
}

var matriz = Matriz(valores: [[1, 2, 3], [4, 5, 6]])
print(matriz[0, 1]) // Imprime 2
matriz[0, 1] = 10
print(matriz[0, 1]) // Imprime 10
```

### Subscript de Solo Lectura
```swift
struct Dias {
    var nombres: [String]

    subscript(index: Int) -> String {
        return nombres[index]
    }
}

let dias = Dias(nombres: ["Lunes", "Martes", "Miércoles"])
print(dias[1]) // Imprime "Martes"
```

## Explicación
Al implementar subscripts en Swift, es importante tener en cuenta lo siguiente:

- **Índices Fuera de Rango**: Asegúrate de manejar adecuadamente los índices, ya que acceder a un índice fuera de los límites de la colección resultará en un error de ejecución.
  
- **Tipo de Retorno**: Puedes definir subscripts que devuelvan tipos diferentes o que acepten múltiples parámetros, lo cual puede ser útil para estructuras más complejas.

- **Sobrecarga**: Puedes sobrecargar subscripts, lo que significa que puedes definir varios subscripts en la misma estructura o clase, siempre que tengan diferentes tipos o números de parámetros.

## Resumen en Una Línea
El subscript en Swift permite un acceso eficiente y legible a los elementos de colecciones y objetos personalizados.