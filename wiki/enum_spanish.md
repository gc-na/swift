<!--
Meta Description: # Enum en Swift: Definición y Uso Efectivo ## Sinopsis Los `enum` (enumeraciones) en Swift son una poderosa característica que permite agrupar un conj...
Meta Keywords: enum, case, que, valores, swift
-->

# Enum en Swift: Definición y Uso Efectivo

## Sinopsis
Los `enum` (enumeraciones) en Swift son una poderosa característica que permite agrupar un conjunto de valores relacionados bajo un mismo tipo, facilitando la gestión y el uso de estos valores en el código.

## Documentación
En Swift, un `enum` es un tipo de dato que define un conjunto de valores relacionados. Los `enum` pueden tener métodos asociados y propiedades, lo que los convierte en una herramienta versátil para organizar y estructurar el código. Son especialmente útiles para representar estados, opciones o categorías.

### Propósito
Los `enum` permiten crear tipos de datos personalizados que pueden mejorar la legibilidad y la seguridad del código. Al agrupar valores relacionados, se evita el uso de múltiples constantes o variables sueltas.

### Uso
Para definir un `enum`, se utiliza la palabra clave `enum`, seguida del nombre del enumerado y sus posibles valores. Los valores de un `enum` pueden ser de diferentes tipos, incluidos tipos asociados.

### Ejemplo básico de definición
```swift
enum Direccion {
    case norte
    case sur
    case este
    case oeste
}
```

## Ejemplos
Aquí hay algunos ejemplos que ilustran el uso de `enum` en Swift:

### Ejemplo 1: Uso básico de `enum`
```swift
enum Color {
    case rojo
    case verde
    case azul
}

let colorFavorito = Color.rojo
```

### Ejemplo 2: `enum` con valores asociados
```swift
enum Resultado {
    case exito(String)
    case fallo(String)
}

let resultado = Resultado.exito("La operación fue exitosa.")
```

### Ejemplo 3: Uso de métodos en `enum`
```swift
enum Estado {
    case activo
    case inactivo
    
    func descripcion() -> String {
        switch self {
        case .activo:
            return "El estado es activo."
        case .inactivo:
            return "El estado es inactivo."
        }
    }
}

let estadoActual = Estado.activo
print(estadoActual.descripcion()) // "El estado es activo."
```

## Explicación
Al usar `enum`, es importante tener en cuenta algunos aspectos:

1. **Mutabilidad**: Las instancias de `enum` son inmutables por defecto. Para cambiar su valor, es necesario asignar una nueva instancia.
   
2. **Switch**: El uso de la declaración `switch` es común para manejar diferentes casos de un `enum`, lo que garantiza que todos los casos sean tratados.

3. **Valores no asociados**: Los `enum` también pueden tener valores asociados, lo que permite almacenar información adicional sobre cada caso.

4. **Raw Values**: Los `enum` pueden tener valores predeterminados (raw values), como cadenas o enteros, lo que facilita su uso en ciertas situaciones.

5. **Limitaciones**: Los `enum` en Swift no pueden heredar de otros tipos, lo que puede ser un inconveniente en algunos casos de diseño.

## Resumen en una línea
Los `enum` en Swift son tipos de datos que agrupan valores relacionados, mejorando la claridad y la seguridad del código.