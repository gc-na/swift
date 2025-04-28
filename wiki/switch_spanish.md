<!--
Meta Description: # Uso del comando "switch" en Swift: Guía completa y ejemplos ## Sinopsis El comando "switch" en Swift es una estructura de control fundamental que pe...
Meta Keywords: print, case, switch, swift, una
-->

# Uso del comando "switch" en Swift: Guía completa y ejemplos

## Sinopsis
El comando "switch" en Swift es una estructura de control fundamental que permite gestionar múltiples condiciones de forma concisa y legible. A diferencia de otros lenguajes, el "switch" en Swift es más seguro y potente, permitiendo evaluar patrones complejos.

## Documentación
El comando "switch" se utiliza para ejecutar diferentes bloques de código dependiendo del valor de una variable o expresión. Su propósito es facilitar la toma de decisiones en el flujo del programa, permitiendo evaluar múltiples casos y ejecutar el código correspondiente al caso que coincida.

### Uso y Sintaxis
La sintaxis básica del "switch" es la siguiente:

```swift
switch valor {
case patrón1:
    // Código a ejecutar si valor coincide con patrón1
case patrón2:
    // Código a ejecutar si valor coincide con patrón2
default:
    // Código a ejecutar si valor no coincide con ningún patrón
}
```

### Detalles Importantes
- Los patrones pueden ser valores constantes, rangos, o incluso expresiones booleanas.
- El uso de `break` no es necesario en Swift, ya que el "switch" finaliza automáticamente después de ejecutar el bloque de código correspondiente.
- Se pueden utilizar múltiples patrones en un solo caso utilizando comas.
- El caso `default` es opcional, pero se recomienda incluirlo como una forma de manejar entradas no esperadas.

## Ejemplos
### Ejemplo Básico
```swift
let díaDeLaSemana = 3

switch díaDeLaSemana {
case 1:
    print("Lunes")
case 2:
    print("Martes")
case 3:
    print("Miércoles")
case 4:
    print("Jueves")
case 5:
    print("Viernes")
case 6, 7:
    print("Fin de semana")
default:
    print("Día no válido")
}
```

### Ejemplo con Rangos
```swift
let nota = 85

switch nota {
case 0..<60:
    print("Insuficiente")
case 60..<75:
    print("Suficiente")
case 75..<90:
    print("Bien")
case 90...100:
    print("Excelente")
default:
    print("Nota no válida")
}
```

### Ejemplo de Patrón con tuplas
```swift
let coordenadas = (x: 0, y: 0)

switch coordenadas {
case (0, 0):
    print("Origen")
case (let x, 0):
    print("Eje X en \(x)")
case (0, let y):
    print("Eje Y en \(y)")
default:
    print("Punto en el plano")
}
```

## Explicación
Aunque el "switch" en Swift es intuitivo, hay algunas trampas y detalles a tener en cuenta:
- **Falta de `break`:** A diferencia de otros lenguajes, no es necesario usar `break` para salir de un caso, lo que puede ser confuso para quienes vienen de otros lenguajes como C o Java.
- **Patrones complejos:** El uso de patrones puede causar confusión si no se comprenden bien las reglas de coincidencia. Asegúrate de conocer cómo funcionan los rangos y las tuplas.
- **Eficiencia:** El "switch" se compila en una estructura de datos optimizada, lo que puede ser más eficiente que múltiples declaraciones `if` en ciertos casos.

## Resumen en una línea
El comando "switch" en Swift es una herramienta poderosa para manejar múltiples condiciones de manera clara y eficiente.