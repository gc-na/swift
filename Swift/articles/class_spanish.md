<!--
Meta Description: # Clases en Swift: Definición, Uso y Ejemplos ## Sinopsis Las clases en Swift son plantillas para crear objetos que encapsulan datos y funcionalidad. ...
Meta Keywords: que, clases, nombre, las, edad
-->

# Clases en Swift: Definición, Uso y Ejemplos

## Sinopsis
Las clases en Swift son plantillas para crear objetos que encapsulan datos y funcionalidad. Permiten la creación de estructuras complejas y son fundamentales para la programación orientada a objetos.

## Documentación
Las clases en Swift son un tipo de constructo que permite definir un nuevo tipo de objeto. Una clase puede contener propiedades (variables) y métodos (funciones) que operan sobre esas propiedades. Swift también soporta la herencia, lo que permite que una clase derive de otra, reutilizando y extendiendo su funcionalidad.

### Propósito
El propósito de las clases es proporcionar una forma de organizar y estructurar el código de manera que se pueda modelar el mundo real en aplicaciones de software, facilitando la reutilización y el mantenimiento del código.

### Uso
Para definir una clase en Swift, se utiliza la palabra clave `class`, seguida del nombre de la clase. Se pueden definir propiedades y métodos dentro de la clase. También se pueden crear inicializadores para establecer el estado inicial de un objeto.

### Detalles
- **Herencia**: Las clases pueden heredar de otras clases, permitiendo la creación de jerarquías de clases.
- **Referencia**: Las instancias de clases son tipos de referencia, lo que significa que cuando se asignan a una nueva variable, ambas variables apuntan al mismo objeto.
- **Desinicializadores**: Las clases pueden incluir desinicializadores, que se ejecutan cuando un objeto es deallocated.

## Ejemplos

### Ejemplo Básico de Clase
```swift
class Persona {
    var nombre: String
    var edad: Int

    init(nombre: String, edad: Int) {
        self.nombre = nombre
        self.edad = edad
    }

    func describir() -> String {
        return "Soy \(nombre) y tengo \(edad) años."
    }
}

let persona1 = Persona(nombre: "Juan", edad: 30)
print(persona1.describir()) // Salida: Soy Juan y tengo 30 años.
```

### Ejemplo de Herencia
```swift
class Estudiante: Persona {
    var materia: String

    init(nombre: String, edad: Int, materia: String) {
        self.materia = materia
        super.init(nombre: nombre, edad: edad)
    }

    override func describir() -> String {
        return "Soy \(nombre), tengo \(edad) años y estudio \(materia)."
    }
}

let estudiante1 = Estudiante(nombre: "Ana", edad: 22, materia: "Matemáticas")
print(estudiante1.describir()) // Salida: Soy Ana, tengo 22 años y estudio Matemáticas.
```

## Explicación
Un error común al trabajar con clases en Swift es olvidar inicializar todas las propiedades antes de usar el objeto. Swift requiere que todas las propiedades tengan un valor antes de que se complete la inicialización. Además, dado que las clases son tipos de referencia, es importante tener cuidado al modificar un objeto a través de múltiples variables, ya que los cambios se reflejarán en todas las referencias.

## Resumen en Una Línea
Las clases en Swift son constructos que permiten crear objetos con propiedades y métodos, facilitando la programación orientada a objetos.