<!--
Meta Description: # Uso de "super" en Swift: Comprendiendo la Herencia y el Acceso a Métodos ## Sinopsis El uso de la palabra clave "super" en Swift es fundamental para...
Meta Keywords: super, clase, método, base, tipo
-->

# Uso de "super" en Swift: Comprendiendo la Herencia y el Acceso a Métodos

## Sinopsis
El uso de la palabra clave "super" en Swift es fundamental para acceder a métodos, propiedades y subscripts de una clase base desde una clase derivada. Esta característica es esencial para implementar correctamente la herencia en Swift.

## Documentación
La palabra clave "super" se utiliza dentro de una clase derivada para referirse a la implementación de su clase base. Permite invocar métodos y acceder a propiedades que se han heredado, garantizando que la lógica de la clase base se pueda reutilizar y extender en la clase derivada.

### Propósito
El propósito de "super" es facilitar la extensión y personalización del comportamiento de las clases en un modelo de herencia. Al utilizar "super", los desarrolladores pueden llamar a inicializadores y métodos de la clase base, asegurando que se ejecuten las configuraciones o comportamientos necesarios definidos en la clase padre.

### Uso
Para usar "super", simplemente se antepone a la llamada del método o propiedad que se desea acceder. Por ejemplo, al sobrescribir un método en una subclase, puedes llamar al método de la clase base usando "super":

```swift
class ClaseBase {
    func metodo() {
        print("Método de ClaseBase")
    }
}

class ClaseDerivada: ClaseBase {
    override func metodo() {
        super.metodo() // Llama al método de ClaseBase
        print("Método de ClaseDerivada")
    }
}
```

## Ejemplos

### Ejemplo 1: Llamando a un Método de la Clase Base
```swift
class Animal {
    func hacerSonido() {
        print("El animal hace un sonido")
    }
}

class Perro: Animal {
    override func hacerSonido() {
        super.hacerSonido() // Llama al método de Animal
        print("El perro ladra")
    }
}

let miPerro = Perro()
miPerro.hacerSonido()
// Salida:
// El animal hace un sonido
// El perro ladra
```

### Ejemplo 2: Usando "super" con Inicializadores
```swift
class Vehiculo {
    var tipo: String
    
    init(tipo: String) {
        self.tipo = tipo
    }
}

class Coche: Vehiculo {
    var modelo: String
    
    init(tipo: String, modelo: String) {
        self.modelo = modelo
        super.init(tipo: tipo) // Llama al inicializador de Vehiculo
    }
}

let miCoche = Coche(tipo: "Sedán", modelo: "Toyota")
print("\(miCoche.tipo) - \(miCoche.modelo)")
// Salida: Sedán - Toyota
```

## Explicación
Al utilizar "super", es importante recordar que:
- "super" solo puede usarse dentro del contexto de una clase derivada.
- No se puede llamar a métodos de la clase base desde fuera de la clase derivada utilizando "super".
- Si no se llama al método de la clase base en un método sobrescrito, se puede perder la lógica definida en la clase base.

Un error común es olvidar llamar a "super" en un inicializador o un método sobrescrito, lo que puede resultar en un comportamiento inesperado o en la omisión de configuraciones importantes.

## Resumen en una línea
La palabra clave "super" en Swift permite a las clases derivadas acceder y reutilizar métodos y propiedades de su clase base, facilitando la herencia y la extensión de comportamientos.