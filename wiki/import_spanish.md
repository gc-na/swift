<!--
Meta Description: # Importar en Swift: Uso y Ejemplos del Comando `import` ## Sinopsis El comando `import` en Swift se utiliza para incluir módulos y bibliotecas en un ...
Meta Keywords: swift, import, importar, módulos, que
-->

# Importar en Swift: Uso y Ejemplos del Comando `import`

## Sinopsis
El comando `import` en Swift se utiliza para incluir módulos y bibliotecas en un archivo de código, permitiendo el acceso a sus funcionalidades y tipos definidos. Esto facilita la reutilización de código y la organización de proyectos.

## Documentación
El comando `import` es fundamental en Swift, ya que permite al programador acceder a bibliotecas estándar y personalizadas. Swift tiene una serie de módulos que contienen funciones, clases y estructuras útiles. Al importar un módulo, se puede utilizar directamente su contenido sin necesidad de redefinirlo.

### Propósito
El propósito principal de `import` es facilitar la modularización del código y el uso de bibliotecas externas, mejorando la legibilidad y mantenibilidad del código.

### Uso
La sintaxis básica para importar un módulo es:

```swift
import NombreDelModulo
```

Por ejemplo, para importar la biblioteca estándar de Swift, se puede utilizar:

```swift
import Foundation
```

### Detalles
- **Módulos**: Un módulo es un conjunto de funcionalidades agrupadas. La biblioteca estándar de Swift es un módulo, al igual que cualquier biblioteca que se pueda descargar o crear.
- **Importación selectiva**: Swift permite importar solo partes específicas de un módulo utilizando `@_exported import`.
- **Importaciones múltiples**: Se pueden importar varios módulos en un solo archivo, cada uno en una línea separada.

## Ejemplos
### Ejemplo básico de importación
```swift
import UIKit

let label = UILabel()
label.text = "Hola, mundo!"
```

### Importar múltiples módulos
```swift
import Foundation
import CoreGraphics

let fechaActual = Date()
let tamañoRectangulo = CGSize(width: 100, height: 50)
```

### Importación selectiva
```swift
@_exported import MyCustomModule

// Ahora se puede utilizar todo el contenido de MyCustomModule directamente
```

## Explicación
Es importante tener en cuenta los siguientes puntos al usar el comando `import` en Swift:

- **Conflictos de nombres**: Si dos módulos importados contienen tipos o funciones con el mismo nombre, puede generar conflictos. Se puede utilizar alias para resolver esto.
- **Importaciones innecesarias**: Importar módulos que no se utilizan puede hacer que el código sea más pesado y menos eficiente. Siempre es recomendable importar solo lo necesario.
- **Acceso a funciones**: Las funciones y tipos de un módulo se pueden acceder directamente una vez que el módulo ha sido importado, lo que ahorra tiempo y esfuerzo al escribir código.

## Resumen en una línea
El comando `import` en Swift permite incluir módulos y bibliotecas en el código para acceder a sus funcionalidades de manera eficiente y organizada.