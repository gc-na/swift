<!--
Meta Description: # init en Swift: Inicializadores en el Lenguaje de Programación Swift ## Sinopsis El modificador `init` en Swift es un mecanismo fundamental que permi...
Meta Keywords: init, nombre, swift, string, propiedades
-->

# init en Swift: Inicializadores en el Lenguaje de Programación Swift

## Sinopsis
El modificador `init` en Swift es un mecanismo fundamental que permite inicializar instancias de tipos, ya sean estructuras o clases. Este artículo explora su uso, estructura y ejemplos prácticos.

## Documentación
El inicializador `init` en Swift es un método especial que se invoca cuando se crea una nueva instancia de una clase o estructura. Su propósito principal es establecer el estado inicial de un objeto al asignar valores a sus propiedades.

### Propósito
- Proporcionar un punto de entrada para la creación de instancias de tipos personalizados.
- Asegurarse de que todas las propiedades del tipo tengan un valor válido antes de que la instancia sea utilizada.

### Uso
Para definir un inicializador, se utiliza la palabra reservada `init` seguida de la definición de parámetros. Los inicializadores pueden ser de dos tipos: Designados y de Conveniencia.

- **Inicializadores designados:** Son los principales inicializadores de una clase. Se encargan de asignar valores a las propiedades y pueden llamar a otros inicializadores de la misma clase.
  
- **Inicializadores de conveniencia:** Son secundarios y se utilizan para simplificar la creación de instancias. Llaman a un inicializador designado de la misma clase.

### Sintaxis
```swift
class NombreClase {
    var propiedad: Tipo
    
    init(propiedad: Tipo) {
        self.propiedad = propiedad
    }
}
```

## Ejemplos

### Ejemplo 1: Inicializador Simple
```swift
class Persona {
    var nombre: String
    var edad: Int
    
    init(nombre: String, edad: Int) {
        self.nombre = nombre
        self.edad = edad
    }
}

let persona = Persona(nombre: "Juan", edad: 30)
```

### Ejemplo 2: Inicializador con Valor Predeterminado
```swift
class Vehiculo {
    var marca: String
    var modelo: String
    
    init(marca: String, modelo: String = "Desconocido") {
        self.marca = marca
        self.modelo = modelo
    }
}

let vehiculo = Vehiculo(marca: "Toyota")
```

### Ejemplo 3: Inicializador de Conveniencia
```swift
class Estudiante {
    var nombre: String
    var grado: Int
    
    init(nombre: String, grado: Int) {
        self.nombre = nombre
        self.grado = grado
    }
    
    convenience init(nombre: String) {
        self.init(nombre: nombre, grado: 1)
    }
}

let estudiante = Estudiante(nombre: "Ana")
```

## Explicación
El uso del inicializador `init` puede presentar algunos desafíos para los desarrolladores, especialmente al trabajar con propiedades opcionales y valores predeterminados. Es crucial asegurarse de que todas las propiedades obligatorias estén inicializadas, ya que Swift no permite instancias con propiedades no establecidas. 

**Errores comunes:**
- Intentar acceder a propiedades no inicializadas.
- Olvidar llamar a `super.init()` en los inicializadores de subclases.

## Resumen en una línea
El `init` en Swift es un mecanismo esencial para inicializar instancias de clases y estructuras, garantizando que todas las propiedades tengan valores válidos al momento de su creación.