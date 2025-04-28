<!--
Meta Description: # La Palabra Clave "private" en Swift: Controlando el Acceso a las Propiedades y Métodos ## Sinopsis En Swift, la palabra clave `private` se utiliza p...
Meta Keywords: private, clase, que, una, acceso
-->

# La Palabra Clave "private" en Swift: Controlando el Acceso a las Propiedades y Métodos

## Sinopsis
En Swift, la palabra clave `private` se utiliza para restringir el acceso a propiedades y métodos dentro de la definición de una clase, estructura o extensión. Esto permite encapsular la lógica y proteger la integridad de los datos, lo que mejora la seguridad y mantenibilidad del código.

## Documentación
### Propósito
La palabra clave `private` se utiliza en Swift para controlar el acceso a los miembros de una clase o estructura. Al declarar una propiedad o método como `private`, se limita su uso solo al contexto de la misma clase o estructura, evitando que el código externo pueda acceder a ellos.

### Uso
Para declarar una propiedad o método como privado, se antepone la palabra clave `private` a la declaración. Esto significa que solo el código dentro de la misma clase o estructura puede acceder a estos miembros.

### Detalles
- **Acceso Restringido**: Los miembros declarados como `private` no son accesibles desde fuera de la clase o estructura en la que están definidos.
- **Alcance**: La palabra clave `private` aplica solo al contexto inmediato, lo que significa que los subtipos (subclases) no tienen acceso a los miembros privados de la clase padre.
- **Organización del Código**: Usar `private` ayuda a evitar conflictos de nombres y a mantener el código más organizado, al ocultar la implementación interna.

## Ejemplos

### Ejemplo Básico
```swift
class CuentaBancaria {
    private var saldo: Double = 0.0
    
    func depositar(cantidad: Double) {
        saldo += cantidad
    }
    
    func obtenerSaldo() -> Double {
        return saldo
    }
}

let cuenta = CuentaBancaria()
cuenta.depositar(cantidad: 100.0)
print(cuenta.obtenerSaldo()) // Imprime: 100.0
// print(cuenta.saldo) // Error: 'saldo' es privado y no se puede acceder desde fuera de la clase.
```

### Ejemplo con Métodos Privados
```swift
class Calculadora {
    private func sumar(a: Int, b: Int) -> Int {
        return a + b
    }
    
    func calcularSuma(a: Int, b: Int) -> Int {
        return sumar(a: a, b: b)
    }
}

let calculadora = Calculadora()
print(calculadora.calcularSuma(a: 3, b: 5)) // Imprime: 8
// calculadora.sumar(a: 3, b: 5) // Error: 'sumar' es privado y no se puede acceder desde fuera de la clase.
```

## Explicación
Un error común al utilizar `private` es intentar acceder a propiedades o métodos privados desde una subclase. Dado que los miembros privados no son accesibles fuera de la clase donde están definidos, esto generará un error de compilación. Para compartir miembros entre una clase y sus subclases, se puede utilizar `fileprivate` o `internal`, dependiendo de las necesidades de acceso.

Otro punto a tener en cuenta es que `private` mejora la encapsulación, pero debe usarse con cuidado. Un uso excesivo puede complicar la reutilización del código, por lo que es importante encontrar un equilibrio adecuado entre privacidad y accesibilidad.

## Resumen en Una Frase
La palabra clave `private` en Swift permite restringir el acceso a propiedades y métodos dentro de una clase o estructura, mejorando la encapsulación y la mantenibilidad del código.