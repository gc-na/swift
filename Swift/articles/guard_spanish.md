<!--
Meta Description: # Uso de `guard` en Swift: Control de Flujo Efectivo ## Sinopsis El comando `guard` en Swift es una herramienta fundamental para el control de flujo q...
Meta Keywords: guard, que, edad, usuario, contraseña
-->

# Uso de `guard` en Swift: Control de Flujo Efectivo

## Sinopsis
El comando `guard` en Swift es una herramienta fundamental para el control de flujo que permite manejar condiciones de forma clara y concisa. Su uso es esencial para garantizar que se cumplan ciertas condiciones antes de continuar con la ejecución del código, mejorando la legibilidad y la seguridad del mismo.

## Documentación
El `guard` es una declaración que permite verificar condiciones que deben ser verdaderas para que el flujo de ejecución continúe en una función, método o bloque de código. Si la condición no se cumple, se ejecuta un bloque de código de salida (usualmente mediante `return`, `break`, o `continue`).

### Propósito
El propósito principal de `guard` es facilitar el manejo de errores y la validación de estados previos a la ejecución del código principal. Esto ayuda a evitar el anidamiento excesivo de condicionales y mejora la claridad del código.

### Uso
La sintaxis básica de `guard` es la siguiente:

```swift
guard condición else {
    // Código que se ejecuta si la condición no se cumple
    return
}
```

Se puede usar en:
- Funciones
- Métodos
- Closures

### Detalles
- Las condiciones de `guard` deben ser booleanas.
- El contexto de las variables declaradas dentro de un `guard` es accesible después de la declaración, lo que es diferente de un `if`.
- Es una buena práctica usar `guard` para comprobar parámetros de entrada, valores opcionales y otros estados críticos.

## Ejemplos
### Ejemplo Básico
```swift
func procesarEdad(edad: Int?) {
    guard let edadDesenvuelta = edad else {
        print("Edad no proporcionada.")
        return
    }
    print("La edad es \(edadDesenvuelta).")
}

procesarEdad(edad: nil)  // Salida: Edad no proporcionada.
procesarEdad(edad: 25)   // Salida: La edad es 25.
```

### Ejemplo con Múltiples Condiciones
```swift
func validarUsuario(usuario: String?, contraseña: String?) {
    guard let usuarioDesenvuelto = usuario, let contraseñaDesenvuelta = contraseña else {
        print("Usuario o contraseña no proporcionados.")
        return
    }
    print("Usuario: \(usuarioDesenvuelto), Contraseña: \(contraseñaDesenvuelta).")
}

validarUsuario(usuario: nil, contraseña: "1234")  // Salida: Usuario o contraseña no proporcionados.
validarUsuario(usuario: "user", contraseña: "1234") // Salida: Usuario: user, Contraseña: 1234.
```

## Explicación
Al usar `guard`, es importante recordar que el bloque de salida debe garantizar que el flujo del programa se detenga si la condición no se cumple. Un error común es olvidar incluir el bloque de salida, lo que resultará en un error de compilación.

Además, a diferencia de `if`, las variables declaradas en un `guard` son accesibles fuera de su bloque, lo que permite un uso más flexible de las variables desenvueltas.

## Resumen en Una Línea
El comando `guard` en Swift es una herramienta de control de flujo que permite validar condiciones y manejar errores de manera clara y efectiva.