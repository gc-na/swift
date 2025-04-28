<!--
Meta Description: # Understanding Structs in Swift: A Comprehensive Guide ## Synopsis In Swift, a `struct` is a powerful and flexible data structure used to encapsulate...
Meta Keywords: struct, swift, data, structs, properties
-->

# Understanding Structs in Swift: A Comprehensive Guide

## Synopsis
In Swift, a `struct` is a powerful and flexible data structure used to encapsulate related properties and behaviors, enabling developers to create complex data models with ease.

## Documentation
A `struct` in Swift is a value type that allows you to create custom data types that can contain properties and methods. Structs are particularly useful for modeling simple data structures, such as points, sizes, and rectangles, and they are commonly used in app development for organizing data.

### Purpose
- To define a collection of related data and functionality in a single entity.
- To provide encapsulation and organization of data, enhancing code readability and maintainability.

### Usage
When defining a struct, you use the `struct` keyword followed by the name of the structure. Inside the struct, you can define properties and methods. Unlike classes, structs are value types, meaning they are copied when passed around in your code.

### Syntax
```swift
struct StructName {
    // Properties
    var propertyName: PropertyType
    
    // Initializer
    init(propertyName: PropertyType) {
        self.propertyName = propertyName
    }
    
    // Methods
    func methodName() {
        // Method implementation
    }
}
```

## Examples

### Basic Struct Definition
```swift
struct Point {
    var x: Int
    var y: Int
}

let pointA = Point(x: 10, y: 20)
print("Point A: (\(pointA.x), \(pointA.y))")
```

### Struct with Methods
```swift
struct Rectangle {
    var width: Double
    var height: Double
    
    func area() -> Double {
        return width * height
    }
}

let rect = Rectangle(width: 5.0, height: 10.0)
print("Area of rectangle: \(rect.area())")
```

### Mutating Methods
```swift
struct Counter {
    var count: Int = 0
    
    mutating func increment() {
        count += 1
    }
}

var counter = Counter()
counter.increment()
print("Counter value: \(counter.count)")
```

## Explanation
When working with structs in Swift, it’s important to remember the following:

- **Value Type Behavior**: Structs are copied when assigned to a variable or constant, or when passed to a function. This can lead to unexpected behavior if you are accustomed to reference types, such as classes.
  
- **Mutability**: To modify properties of a struct within its own methods, you must declare the method with the `mutating` keyword. This indicates that the method alters the instance itself.

- **Inheritance**: Unlike classes, structs do not support inheritance. However, they can conform to protocols, allowing for shared behaviors.

- **Immutability**: If a struct instance is declared as a constant (using `let`), its properties cannot be modified. This helps enforce immutability in your code.

## One Line Summary
Structs in Swift are value types that encapsulate related properties and behaviors, enabling the creation of complex data models in a clean and efficient manner.