<!--
Meta Description: # Protocolo en Swift: Definición, Uso y Ejemplos ## Sinopsis Un protocolo en Swift es un conjunto de métodos y propiedades que define una interfaz que...
Meta Keywords: que, protocolos, protocolo, swift, los
-->

# Protocolo en Swift: Definición, Uso y Ejemplos

## Sinopsis
Un protocolo en Swift es un conjunto de métodos y propiedades que define una interfaz que las clases, estructuras y enumeraciones pueden adoptar y cumplir. Los protocolos son fundamentales en la programación orientada a objetos y permiten la creación de código más modular y reutilizable.

## Documentación
En Swift, un protocolo es una forma de definir un conjunto de funcionalidades que se espera que las clases, estructuras o enumeraciones implementen. Los protocolos declaran propiedades y métodos, pero no proporcionan la implementación. Esto permite que diferentes tipos adopten el mismo protocolo y ofrezcan diversas implementaciones.

### Propósito
Los protocolos son útiles para:
- Definir un contrato que debe ser cumplido por cualquier tipo que lo adopte.
- Permitir la programación orientada a protocolos, que promueve la separación de responsabilidades y la reutilización de código.
- Facilitar la interoperabilidad entre diferentes tipos mediante la implementación de un mismo protocolo.

### Uso
Para declarar un protocolo en Swift, se utiliza la palabra clave `protocol`, seguida del nombre del protocolo y sus requisitos. Se puede adoptar un protocolo mediante la lista de conformidad en la declaración de una clase, estructura o enumeración.

```swift
protocol NombreDelProtocolo {
    var propiedad: Tipo { get set }
    func metodo()
}
```

## Ejemplos
### Ejemplo 1: Definición y Conformidad Básica
```swift
protocol Vehiculo {
    var velocidad: Double { get set }
    func acelerar()
}

class Coche: Vehiculo {
    var velocidad: Double = 0.0
    
    func acelerar() {
        velocidad += 10.0
        print("La velocidad del coche es ahora \(velocidad) km/h.")
    }
}

let miCoche = Coche()
miCoche.acelerar()
```

### Ejemplo 2: Uso de Protocolos con Extensiones
```swift
protocol Describible {
    var descripcion: String { get }
}

extension Describible {
    func descripcionCompleta() -> String {
        return "Descripción: \(descripcion)"
    }
}

struct Producto: Describible {
    var descripcion: String
}

let producto = Producto(descripcion: "Un producto increíble.")
print(producto.descripcionCompleta())
```

## Explicación
Al trabajar con protocolos en Swift, es importante tener en cuenta algunos aspectos:

- **Conformidad opcional**: Un tipo puede adoptar múltiples protocolos, lo que permite una gran flexibilidad en el diseño. Sin embargo, es esencial implementar todos los métodos y propiedades requeridos por el protocolo.
  
- **Protocolos y herencia**: Los protocolos pueden heredar de otros protocolos, lo que permite la creación de jerarquías de protocolos y la adición de nuevos requisitos.

- **Protocolos de tipo**: Swift permite que los protocolos sean utilizados como tipos, lo que significa que puedes declarar variables, parámetros y tipos de retorno como un protocolo específico.

### Errores comunes
- No implementar todos los requisitos del protocolo resultará en un error de compilación.
- Asumir que los protocolos son lo mismo que las clases: los protocolos no contienen implementación, solo definen un contrato.

## Resumen en una línea
Un protocolo en Swift es un contrato que define métodos y propiedades que los tipos adoptantes deben implementar, promoviendo la modularidad y reutilización del código.