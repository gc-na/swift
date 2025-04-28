<!--
Meta Description: # Uso del bucle "while" en Swift: Guía Completa ## Sinopsis El bucle "while" en Swift permite ejecutar un bloque de código de manera repetitiva mientr...
Meta Keywords: condición, bucle, contador, while, que
-->

# Uso del bucle "while" en Swift: Guía Completa

## Sinopsis
El bucle "while" en Swift permite ejecutar un bloque de código de manera repetitiva mientras se cumpla una condición específica, facilitando la creación de algoritmos eficientes y controlados.

## Documentación
El bucle "while" es una estructura de control de flujo que permite repetir un bloque de código mientras una condición booleana sea verdadera. Su sintaxis es sencilla y flexible, lo que lo convierte en una herramienta poderosa para manejar iteraciones en la programación.

### Sintaxis
```swift
while condición {
    // Código a ejecutar mientras la condición sea verdadera
}
```

### Propósito
El propósito principal del bucle "while" es ejecutar un conjunto de instrucciones de forma repetitiva hasta que la condición especificada deje de ser verdadera. Esto es útil en situaciones donde no se conoce de antemano cuántas veces se debe repetir el bloque de código.

### Uso
1. **Inicialización**: Antes de comenzar el bucle, es importante inicializar cualquier variable que se use en la condición.
2. **Condición**: La expresión que se evalúa antes de cada iteración. Si es verdadera, el bloque de código se ejecuta. Si es falsa, el bucle se detiene.
3. **Modificación**: Dentro del bloque de código, se debe modificar la variable de control para evitar bucles infinitos.

## Ejemplos

### Ejemplo 1: Contador simple
```swift
var contador = 0

while contador < 5 {
    print("El contador es \(contador)")
    contador += 1
}
```
**Salida:**
```
El contador es 0
El contador es 1
El contador es 2
El contador es 3
El contador es 4
```

### Ejemplo 2: Leer entrada hasta una condición
```swift
var entrada: String?

while entrada != "salir" {
    print("Introduce un comando (escribe 'salir' para terminar):")
    entrada = readLine()
}
```

## Explicación
### Errores Comunes
- **Bucle infinito**: Uno de los errores más comunes es no actualizar la variable de control dentro del bucle, lo que causa que la condición siempre sea verdadera y el bucle nunca termine.
- **Condiciones incorrectas**: Asegúrate de que la condición esté correctamente formulada para evitar resultados inesperados.

### Notas Adicionales
- El bucle "while" se evalúa antes de cada iteración, lo que significa que si la condición es falsa desde el principio, el bloque de código no se ejecutará en absoluto.
- Para situaciones donde se desea garantizar al menos una ejecución del bloque de código, se puede considerar el uso de `repeat-while`.

## Resumen en una línea
El bucle "while" en Swift permite ejecutar repetidamente un bloque de código mientras se cumpla una condición booleana, facilitando la iteración controlada.