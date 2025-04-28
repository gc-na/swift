<!--
Meta Description: # Extensiones en Swift: Ampliando Funcionalidades de Tipos ## Sinopsis Las extensiones en Swift permiten agregar nuevas funcionalidades a clases, estr...
Meta Keywords: extensiones, swift, agregar, una, que
-->

# Extensiones en Swift: Ampliando Funcionalidades de Tipos

## Sinopsis
Las extensiones en Swift permiten agregar nuevas funcionalidades a clases, estructuras, enumeraciones y protocolos existentes, sin necesidad de modificar el código original. Esto facilita la organización y la reutilización del código.

## Documentación
Las extensiones son una característica poderosa de Swift que permite a los desarrolladores ampliar la funcionalidad de tipos predefinidos o personalizados. Las extensiones pueden incluir métodos, propiedades, inicializadores, subíndices y conformidad a protocolos. Esto es especialmente útil para agregar funcionalidades adicionales sin heredar de una clase.

### Propósito
El propósito principal de las extensiones es mejorar la modularidad y la legibilidad del código, permitiendo a los desarrolladores organizar funcionalidades relacionadas en un solo lugar.

### Uso
Para definir una extensión, se utiliza la palabra clave `extension`, seguida del nombre del tipo que se desea extender. A continuación, se pueden agregar nuevas propiedades o métodos.

#### Sintaxis básica:
```swift
extension NombreDelTipo {
    // Nuevas propiedades o métodos
}
```

## Ejemplos

### Ejemplo 1: Agregar un método a una estructura
```swift
struct Rectángulo {
    var ancho: Double
    var alto: Double
}

extension Rectángulo {
    func área() -> Double {
        return ancho * alto
    }
}

let rect = Rectángulo(ancho: 5, alto: 10)
print(rect.área()) // Salida: 50.0
```

### Ejemplo 2: Agregar una propiedad calculada
```swift
extension Int {
    var esPar: Bool {
        return self % 2 == 0
    }
}

let número = 4
print(número.esPar) // Salida: true
```

### Ejemplo 3: Conformidad a un protocolo
```swift
protocol Describible {
    func descripción() -> String
}

extension String: Describible {
    func descripción() -> String {
        return "La cadena es: \(self)"
    }
}

let cadena = "Hola, mundo"
print(cadena.descripción()) // Salida: La cadena es: Hola, mundo
```

## Explicación
### Problemas Comunes y Notas
- **Confusión con la Herencia**: Las extensiones no permiten agregar almacenamiento de propiedades, solo se pueden agregar propiedades calculadas.
- **Métodos que Ocultan**: Si un método en una extensión tiene el mismo nombre que un método existente en el tipo, el método de la extensión puede ocultar el original, lo que puede llevar a confusiones.
- **Extensiones y Inicializadores**: No se pueden agregar inicializadores a clases que no se definieron en la extensión, aunque se pueden definir inicializadores en tipos que sí se han definido.

## Resumen en una línea
Las extensiones en Swift permiten añadir nuevas funcionalidades a tipos existentes de manera modular y organizada, mejorando la reutilización del código.