<!--
Meta Description: # Uso de la declaración "if" en Swift: Condicionales en la Programación ## Sinopsis La declaración "if" en Swift permite a los desarrolladores tomar d...
Meta Keywords: que, swift, condiciones, declaración, código
-->

# Uso de la declaración "if" en Swift: Condicionales en la Programación

## Sinopsis
La declaración "if" en Swift permite a los desarrolladores tomar decisiones en su código, ejecutando diferentes bloques de código en función de condiciones booleanas. Esta estructura de control es fundamental para la lógica de programación.

## Documentación
La declaración "if" es una herramienta esencial en Swift que permite evaluar una condición y ejecutar un bloque de código si la condición se cumple. La sintaxis básica de la declaración "if" es:

```swift
if condición {
    // Código a ejecutar si la condición es verdadera
}
```

### Propósito
El propósito de la declaración "if" es controlar el flujo de un programa, permitiendo que ciertas partes del código se ejecuten solo cuando se cumplen condiciones específicas, lo que facilita la toma de decisiones en la lógica de la aplicación.

### Uso
La declaración "if" puede ser utilizada de varias maneras:
- **Condición simple**: Comprueba una única condición.
- **Condiciones múltiples**: Se puede usar `else if` para evaluar múltiples condiciones.
- **Condición alternativa**: Utiliza `else` para ejecutar un bloque de código cuando la condición inicial no se cumple.

### Detalles
- Las condiciones dentro de la declaración "if" deben ser de tipo booleano.
- Se pueden agrupar múltiples condiciones utilizando operadores lógicos como `&&` (y) y `||` (o).
- Swift permite el uso de declaraciones "if" anidadas.

## Ejemplos

### Ejemplo básico
```swift
let numero = 10

if numero > 5 {
    print("El número es mayor que 5.")
}
```

### Ejemplo con `else`
```swift
let numero = 4

if numero > 5 {
    print("El número es mayor que 5.")
} else {
    print("El número no es mayor que 5.")
}
```

### Ejemplo con `else if`
```swift
let numero = 7

if numero > 10 {
    print("El número es mayor que 10.")
} else if numero > 5 {
    print("El número es mayor que 5 pero menor o igual a 10.")
} else {
    print("El número es 5 o menor.")
}
```

### Ejemplo con condiciones múltiples
```swift
let edad = 18

if edad < 13 {
    print("Niño")
} else if edad < 20 {
    print("Adolescente")
} else {
    print("Adulto")
}
```

## Explicación
Al utilizar la declaración "if", es crucial recordar que:
- Las condiciones deben evaluarse a un valor booleano (`true` o `false`).
- Si se olvida cerrar las llaves `{}`, el código puede fallar en tiempo de compilación.
- Anidar declaraciones "if" puede hacer que el código sea menos legible, por lo que se recomienda mantener la lógica clara y concisa.
- Las condiciones que no se evalúan correctamente pueden llevar a errores lógicos en la ejecución del programa.

## Resumen en una línea
La declaración "if" en Swift permite ejecutar bloques de código basados en condiciones booleanas, facilitando la toma de decisiones en programación.