<!--
Meta Description: # `fileprivate` en Swift: Control de Acceso a Nivel de Archivo ## Sinopsis `fileprivate` es un modificador de acceso en Swift que permite restringir l...
Meta Keywords: fileprivate, archivo, que, swift, acceso
-->

# `fileprivate` en Swift: Control de Acceso a Nivel de Archivo

## Sinopsis
`fileprivate` es un modificador de acceso en Swift que permite restringir la visibilidad de propiedades, métodos y tipos a un único archivo fuente. Es especialmente útil para encapsular la lógica y asegurar que ciertos componentes no sean accesibles desde otros archivos.

## Documentación
El modificador de acceso `fileprivate` se utiliza para definir el alcance de las entidades dentro de un archivo Swift. A diferencia de `private`, que limita el acceso a la misma clase o estructura, `fileprivate` permite que cualquier entidad dentro del mismo archivo pueda acceder a las propiedades y métodos marcados con este modificador.

### Propósito
- Proteger datos sensibles y evitar el acceso no autorizado desde otros archivos.
- Facilitar la colaboración entre diferentes entidades dentro del mismo archivo sin exponerlas globalmente.

### Uso
Para utilizar `fileprivate`, simplemente precede la declaración de una propiedad, método o tipo con la palabra clave `fileprivate`. A continuación se muestra un ejemplo de su uso:

```swift
fileprivate class MiClase {
    fileprivate var propiedad: Int = 0
    
    fileprivate func metodo() {
        print("Método de MiClase.")
    }
}
```

## Ejemplos
Aquí tienes algunos ejemplos básicos de cómo se usa `fileprivate` en Swift:

### Ejemplo 1: Uso de `fileprivate` con una clase
```swift
fileprivate class MiClase {
    fileprivate var contador: Int = 0
    
    fileprivate func incrementar() {
        contador += 1
    }
}

let instancia = MiClase()
instancia.incrementar() // Funciona, ya que se accede dentro del mismo archivo.
```

### Ejemplo 2: `fileprivate` en una estructura
```swift
fileprivate struct MiEstructura {
    fileprivate var mensaje: String = "Hola"
    
    fileprivate func mostrarMensaje() {
        print(mensaje)
    }
}

let estructura = MiEstructura()
estructura.mostrarMensaje() // Funciona, ya que se accede dentro del mismo archivo.
```

## Explicación
### Errores Comunes
- Intentar acceder a una propiedad o método `fileprivate` desde un archivo diferente resultará en un error de compilación. Este es un comportamiento esperado, pero puede ser confuso si no se entiende el alcance del modificador.
- `fileprivate` no es la opción más restrictiva. Si necesitas que ciertas entidades sean accesibles solo dentro de una clase o estructura específica, considera utilizar `private`.

### Notas Adicionales
- `fileprivate` es útil en proyectos grandes donde el encapsulamiento es esencial para mantener el código organizado y evitar conflictos de nombres.
- Recuerda que a pesar de que `fileprivate` permite un mayor acceso dentro del mismo archivo, no es una panacea para el diseño de software. Un buen diseño de clases y estructuras sigue siendo fundamental.

## Resumen en Una Línea
El modificador de acceso `fileprivate` en Swift permite restringir la visibilidad de propiedades y métodos a un único archivo, facilitando la encapsulación y el manejo del acceso a los datos.