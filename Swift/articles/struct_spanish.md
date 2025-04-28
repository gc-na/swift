<!--
Meta Description: # Estructuras en Swift: Guía Completa sobre el Uso de `struct` ## Sinopsis Las estructuras (`struct`) en Swift son tipos de datos flexibles y versátil...
Meta Keywords: estructuras, swift, que, las, datos
-->

# Estructuras en Swift: Guía Completa sobre el Uso de `struct`

## Sinopsis
Las estructuras (`struct`) en Swift son tipos de datos flexibles y versátiles que permiten agrupar datos y comportamientos relacionados. Son fundamentales en Swift para la creación de modelos de datos y representan una manera eficiente de organizar y encapsular información.

## Documentación
### ¿Qué es una estructura en Swift?
Una estructura en Swift es un tipo de dato que permite crear objetos que pueden contener propiedades y métodos. A diferencia de las clases, las estructuras son tipos por valor, lo que significa que se copian cuando se asignan o pasan a funciones. Esto proporciona una forma segura y predecible de manejar datos.

### Uso de estructuras
Las estructuras se utilizan comúnmente para representar datos simples y complejos, como coordenadas en un sistema, información de usuarios, o cualquier otro conjunto de datos que necesite ser agrupado. Se declaran utilizando la palabra clave `struct`, seguida por el nombre de la estructura y un bloque que contiene sus propiedades y métodos.

### Sintaxis básica
```swift
struct NombreDeLaEstructura {
    // Propiedades
    var propiedad1: Tipo
    var propiedad2: Tipo
    
    // Métodos
    func metodoEjemplo() {
        // Implementación del método
    }
}
```

### Ejemplo de uso:
```swift
struct Persona {
    var nombre: String
    var edad: Int
    
    func saludar() {
        print("Hola, mi nombre es \(nombre) y tengo \(edad) años.")
    }
}

let persona1 = Persona(nombre: "Juan", edad: 30)
persona1.saludar() // Salida: Hola, mi nombre es Juan y tengo 30 años.
```

## Explicación
### Errores comunes y consideraciones
1. **Copia de valores**: Al trabajar con estructuras, es importante recordar que se crean copias de los valores. Cambiar una propiedad de una instancia no afectará a otras instancias.
2. **Inicializadores**: Swift genera automáticamente un inicializador para las estructuras, pero si se definen propiedades sin valores predeterminados, se debe proporcionar un inicializador explícito.
3. **Mutabilidad**: Para modificar las propiedades de una estructura, la instancia debe ser declarada como `var`. Si se declara como `let`, será inmutable.
4. **Equidad**: Las estructuras adoptan el protocolo `Equatable` automáticamente si todas sus propiedades son comparables, permitiendo comparaciones directas entre instancias.

## Resumen en una línea
Las estructuras en Swift son tipos de datos por valor que permiten agrupar propiedades y métodos, facilitando la organización y el manejo de datos de manera efectiva.