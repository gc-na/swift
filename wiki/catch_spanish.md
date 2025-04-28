<!--
Meta Description: # Uso de "catch" en Swift: Manejo de Errores ## Sinopsis El comando "catch" en Swift se utiliza para manejar errores en bloques de código que pueden l...
Meta Keywords: error, catch, errores, swift, para
-->

# Uso de "catch" en Swift: Manejo de Errores

## Sinopsis
El comando "catch" en Swift se utiliza para manejar errores en bloques de código que pueden lanzar excepciones. Permite capturar y gestionar errores de manera controlada, mejorando la robustez y la confiabilidad de las aplicaciones.

## Documentación
En Swift, el manejo de errores se realiza mediante el uso de `do`, `try` y `catch`. La palabra clave `catch` se emplea para capturar errores lanzados en el bloque `do`. Un error puede ser cualquier tipo que conforme al protocolo `Error`. La estructura básica para utilizar `catch` es la siguiente:

```swift
do {
    // Código que puede lanzar un error
    try funciónQuePuedeLanzarError()
} catch {
    // Manejo del error
    print("Se produjo un error: \(error)")
}
```

### Propósito
El propósito del bloque `catch` es proporcionar un mecanismo para manejar errores de forma segura. Al capturar errores, los desarrolladores pueden ofrecer respuestas adecuadas, como mostrar un mensaje al usuario o realizar una acción alternativa.

### Uso
Para usar `catch`, primero es necesario tener un bloque `do` donde se ejecute el código que podría fallar. Si un error es lanzado, el control del flujo se transfiere al bloque `catch`, donde se puede manejar el error de manera apropiada.

## Ejemplos

### Ejemplo Básico
A continuación se muestra un ejemplo simple donde se lanza un error si la entrada es negativa:

```swift
enum InputError: Error {
    case negativeNumber
}

func checkNumber(_ number: Int) throws {
    if number < 0 {
        throw InputError.negativeNumber
    }
    print("El número es \(number)")
}

do {
    try checkNumber(-5)
} catch InputError.negativeNumber {
    print("Error: El número no puede ser negativo.")
} catch {
    print("Se produjo un error inesperado: \(error)")
}
```

### Ejemplo con Múltiples Errores
El bloque `catch` también puede manejar múltiples tipos de errores:

```swift
enum FileError: Error {
    case fileNotFound
    case unreadable
}

func readFile(at path: String) throws {
    // Simulación de un error de archivo
    throw FileError.fileNotFound
}

do {
    try readFile(at: "ruta/a/archivo.txt")
} catch FileError.fileNotFound {
    print("Error: El archivo no se encontró.")
} catch FileError.unreadable {
    print("Error: No se puede leer el archivo.")
} catch {
    print("Error desconocido: \(error)")
}
```

## Explicación
Al usar `catch`, es importante tener en cuenta algunas consideraciones:

- **Propagación de Errores**: Si un método lanza un error, debe declararse con `throws`. Esto significa que cualquier función que lo llame también debe manejar el error usando `try`.
- **Bloques `catch` Múltiples**: Puedes tener múltiples bloques `catch` para distintos tipos de errores, lo que permite una gestión más granular.
- **Errores No Capturados**: Si no se captura un error específico, el bloque `catch` general manejará cualquier otro error lanzado.

## Resumen en una Línea
El comando `catch` en Swift se utiliza para gestionar errores de manera controlada, permitiendo a los desarrolladores manejar excepciones y mejorar la seguridad del código.