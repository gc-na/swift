<!--
Meta Description: # Default en Swift: Comprendiendo su Uso y Aplicaciones ## Sinopsis En Swift, la palabra clave `default` se utiliza principalmente en la declaración d...
Meta Keywords: default, que, switch, para, swift
-->

# Default en Swift: Comprendiendo su Uso y Aplicaciones

## Sinopsis
En Swift, la palabra clave `default` se utiliza principalmente en la declaración de estructuras de control de flujo, como `switch`, para manejar casos que no coinciden con ninguno de los patrones especificados. Esta funcionalidad es esencial para garantizar que se aborden todas las posibilidades en la lógica del programa.

## Documentación
La declaración `default` se emplea en la estructura de control de flujo `switch`, que permite evaluar un valor contra múltiples patrones y ejecutar el bloque de código correspondiente al primer patrón que coincida. Si ninguno de los patrones coincide, el bloque de código dentro de `default` se ejecuta, lo que lo convierte en una herramienta útil para manejar casos inesperados o no definidos.

### Propósito
El propósito del `default` es proporcionar un comportamiento por defecto en las estructuras de control, asegurando que siempre haya un camino de ejecución, incluso si no hay coincidencias específicas. Esto es especialmente útil en situaciones donde se espera que el valor de entrada pueda variar.

### Uso
La sintaxis básica para usar `default` en un `switch` es la siguiente:

```swift
switch valor {
case patrón1:
    // Código para patrón1
case patrón2:
    // Código para patrón2
default:
    // Código si no coincide con ningún patrón
}
```

## Ejemplos

### Ejemplo 1: Uso básico de `default`
```swift
let numero = 3

switch numero {
case 1:
    print("El número es uno.")
case 2:
    print("El número es dos.")
default:
    print("El número no es uno ni dos.")
}
```
**Salida:** El número no es uno ni dos.

### Ejemplo 2: Combinación de patrones
```swift
let letra = "b"

switch letra {
case "a", "e", "i", "o", "u":
    print("Es una vocal.")
default:
    print("Es una consonante.")
}
```
**Salida:** Es una consonante.

## Explicación
Al utilizar `default`, es importante tener en cuenta que debe ser el último caso en la declaración del `switch`. Si `default` se coloca antes de otros casos, el compilador generará un error. Otro punto a considerar es que `default` no es obligatorio; si todos los posibles valores del caso están cubiertos, no se necesita. Sin embargo, utilizarlo puede ayudar a prevenir errores en la lógica del programa al manejar entradas no esperadas.

### Errores comunes
- **Olvidar el `default`:** En algunos casos, puede parecer que todas las posibilidades están cubiertas, pero siempre es recomendable incluir un `default` para manejar situaciones inesperadas.
- **Uso incorrecto de tipos:** Asegúrate de que el tipo de la variable en el `switch` coincida con los tipos de los patrones. De lo contrario, se podría generar un error de compilación.

## Resumen en una línea
La palabra clave `default` en Swift se utiliza en estructuras `switch` para manejar casos que no coinciden con ningún patrón específico, garantizando un flujo de ejecución completo.