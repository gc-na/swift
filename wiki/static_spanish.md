<!--
Meta Description: # El uso de "static" en Swift: Definición y Ejemplos ## Sinopsis El modificador `static` en Swift permite definir propiedades y métodos que pertenecen...
Meta Keywords: static, que, propiedades, swift, métodos
-->

# El uso de "static" en Swift: Definición y Ejemplos

## Sinopsis
El modificador `static` en Swift permite definir propiedades y métodos que pertenecen a la clase o estructura en lugar de a instancias individuales. Esto proporciona una forma eficiente de manejar datos y comportamientos que son comunes a todas las instancias.

## Documentación
El modificador `static` se utiliza en Swift para declarar propiedades y métodos que están asociados a la clase o estructura en sí, y no a instancias específicas de estas. Hay dos contextos importantes donde se puede aplicar `static`: en clases y en estructuras.

### Propiedades Estáticas
Las propiedades estáticas se definen utilizando el prefijo `static` y son compartidas por todas las instancias de la clase o estructura. Esto es útil para almacenar valores que son constantes o que se deben compartir entre todas las instancias.

### Métodos Estáticos
Los métodos estáticos son funciones que se pueden llamar en la propia clase o estructura, sin necesidad de crear una instancia. Esto es útil para operaciones que no dependen del estado de una instancia.

### Uso
Para definir una propiedad o método estático, simplemente se coloca la palabra clave `static` antes de la declaración. A continuación se muestra la sintaxis:

```swift
class NombreDeClase {
    static var propiedadEstatica: Tipo = valor
    static func metodoEstatico() {
        // código
    }
}
```

## Ejemplos

### Ejemplo de Propiedad Estática
```swift
class Contador {
    static var totalContadores = 0
    
    init() {
        Contador.totalContadores += 1
    }
}

let contador1 = Contador()
let contador2 = Contador()
print(Contador.totalContadores) // Imprime: 2
```

### Ejemplo de Método Estático
```swift
class Matemáticas {
    static func sumar(a: Int, b: Int) -> Int {
        return a + b
    }
}

let resultado = Matemáticas.sumar(a: 5, b: 10)
print(resultado) // Imprime: 15
```

## Explicación
Al usar `static`, es importante tener en cuenta que:

1. **No se puede acceder a propiedades de instancia**: Dentro de un método estático, no se puede acceder a propiedades de instancia, ya que no hay una instancia disponible.
2. **No se pueden sobreescribir en subclases**: A diferencia de los métodos de instancia, los métodos y propiedades estáticas no se pueden sobreescribir en las subclases.
3. **Uso adecuado de memoria**: Usar `static` puede ayudar a conservar memoria al evitar la creación de múltiples instancias para acceder a datos compartidos.

## Resumen en una línea
El modificador `static` en Swift permite definir propiedades y métodos que son comunes a todas las instancias de una clase o estructura, facilitando la gestión de datos compartidos.