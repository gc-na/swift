<!--
Meta Description: # Uso de "case" en Swift: Estructuras de Control y Patrones de Coincidencia ## Sinopsis El comando "case" en Swift se utiliza en el contexto de estruc...
Meta Keywords: case, print, switch, swift, una
-->

# Uso de "case" en Swift: Estructuras de Control y Patrones de Coincidencia

## Sinopsis
El comando "case" en Swift se utiliza en el contexto de estructuras de control, específicamente en las declaraciones de `switch` y en la coincidencia de patrones. Permite verificar un valor contra múltiples condiciones y ejecutar el código correspondiente según la coincidencia.

## Documentación
En Swift, el comando `case` es una parte fundamental de la declaración `switch`, que permite manejar diferentes posibles valores de una variable o constante. Es especialmente útil para realizar comparaciones más complejas que las que se pueden lograr con simples declaraciones `if`.

### Propósito
El propósito principal del comando `case` es proporcionar una manera clara y eficiente de manejar múltiples condiciones y ejecutar diferentes bloques de código según el valor de una expresión.

### Uso
La sintaxis básica de una declaración `switch` con `case` es la siguiente:

```swift
switch expresión {
case valor1:
    // código a ejecutar si expresión es igual a valor1
case valor2:
    // código a ejecutar si expresión es igual a valor2
default:
    // código a ejecutar si expresión no coincide con ninguno de los valores anteriores
}
```

### Detalles
- Los valores especificados en `case` pueden ser valores literales, rangos o patrones más complejos.
- Se puede usar `fallthrough` para continuar la ejecución en el siguiente `case`, aunque no es necesario especificar explícitamente un caso.
- El bloque `default` es opcional, pero se recomienda incluirlo para manejar valores inesperados.

## Ejemplos
### Ejemplo 1: Uso básico de `case`
```swift
let numero = 3

switch numero {
case 1:
    print("Uno")
case 2:
    print("Dos")
case 3:
    print("Tres")
default:
    print("Número no reconocido")
}
```
*Salida: "Tres"*

### Ejemplo 2: Uso de rangos
```swift
let edad = 25

switch edad {
case 0..<13:
    print("Niño")
case 13..<20:
    print("Adolescente")
case 20..<65:
    print("Adulto")
default:
    print("Adulto mayor")
}
```
*Salida: "Adulto"*

### Ejemplo 3: Coincidencia de patrones
```swift
let punto = (2, 0)

switch punto {
case (0, 0):
    print("Origen")
case (let x, 0):
    print("En el eje X, x=\(x)")
case (0, let y):
    print("En el eje Y, y=\(y)")
default:
    print("Punto en el plano")
}
```
*Salida: "En el eje X, x=2"*

## Explicación
Al utilizar `case` en Swift, es importante tener en cuenta algunas consideraciones:

- **Exclusividad**: Cada `case` se evalúa en orden, y una vez que se encuentra una coincidencia, se ejecuta el bloque correspondiente y se sale del `switch`.
- **Valores duplicados**: No se pueden tener dos `case` con el mismo valor. Esto generará un error de compilación.
- **Complejidad**: Si bien la declaración `switch` es poderosa, su uso excesivo o innecesario puede llevar a un código menos legible. Es recomendable evaluar si se puede simplificar el control de flujo.

## Resumen en una línea
El comando `case` en Swift permite gestionar múltiples condiciones en declaraciones `switch`, facilitando la coincidencia de patrones y la ejecución de bloques de código específicos según el valor de una expresión.