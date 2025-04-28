<!--
Meta Description: # Funciones en Swift: Guía Completa sobre el Uso de la Palabra Clave "func" ## Sinopsis La palabra clave `func` en Swift se utiliza para definir funci...
Meta Keywords: funciones, swift, func, función, que
-->

# Funciones en Swift: Guía Completa sobre el Uso de la Palabra Clave "func"

## Sinopsis
La palabra clave `func` en Swift se utiliza para definir funciones, que son bloques de código reutilizables que realizan una tarea específica y pueden aceptar parámetros y devolver valores. Esta característica es fundamental en la programación en Swift, ya que permite organizar y estructurar el código de manera eficiente.

## Documentación
En Swift, `func` es la forma en que se declaran las funciones. Las funciones son esenciales para dividir el código en partes más manejables y legibles. Una función puede recibir cero o más parámetros y puede devolver un valor de cualquier tipo.

### Sintaxis
```swift
func nombreDeLaFuncion(parametro1: Tipo, parametro2: Tipo) -> TipoDeRetorno {
    // Cuerpo de la función
}
```

### Componentes
- **nombreDeLaFuncion**: Un identificador que se utiliza para llamar a la función.
- **parametros**: Opcionales, se definen con un nombre y un tipo.
- **TipoDeRetorno**: Especifica el tipo de dato que la función devolverá. Si no se devuelve ningún valor, se utiliza `Void`.

### Propósito
Las funciones en Swift permiten:
- Reutilizar código.
- Mejorar la legibilidad y mantenimiento del código.
- Facilitar la programación modular.

## Ejemplos
### Ejemplo 1: Función Simple
```swift
func saludar(nombre: String) -> String {
    return "Hola, \(nombre)!"
}

let mensaje = saludar(nombre: "Juan")
print(mensaje) // Salida: Hola, Juan!
```

### Ejemplo 2: Función Sin Parámetros
```swift
func obtenerFechaActual() -> String {
    let fecha = Date()
    let formatter = DateFormatter()
    formatter.dateStyle = .medium
    return formatter.string(from: fecha)
}

print(obtenerFechaActual()) // Salida: fecha actual en formato medio
```

### Ejemplo 3: Función con Parámetros Opcionales
```swift
func multiplicar(a: Int, b: Int = 2) -> Int {
    return a * b
}

print(multiplicar(a: 4)) // Salida: 8
print(multiplicar(a: 4, b: 3)) // Salida: 12
```

## Explicación
Al usar `func`, es importante tener en cuenta:
- **Nombres de Función**: Deben ser descriptivos para mejorar la legibilidad del código.
- **Tipos de Parámetros**: Asegúrate de especificar correctamente los tipos para evitar errores.
- **Funciones Anidadas**: Puedes definir funciones dentro de otras funciones, pero ten cuidado con el alcance de las variables.

### Errores Comunes
- Olvidar el tipo de retorno si es necesario.
- No proporcionar argumentos requeridos al llamar a la función.
- Usar nombres de funciones que colisionen con palabras reservadas.

## Resumen en Una Línea
La palabra clave `func` en Swift se utiliza para definir funciones, que permiten organizar y reutilizar el código de manera eficiente.