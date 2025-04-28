<!--
Meta Description: # Understanding `init` in Swift: The Essential Guide to Initializers ## Synopsis In Swift, `init` is a fundamental keyword used to define initializers...
Meta Keywords: initializers, init, initializer, swift, self
-->

# Understanding `init` in Swift: The Essential Guide to Initializers

## Synopsis
In Swift, `init` is a fundamental keyword used to define initializers, which are special methods responsible for creating instances of a class, structure, or enumeration.

## Documentation
### What is `init`?
The `init` keyword in Swift is used to define an initializer, a method that is called when an instance of a type is created. Initializers set the initial values for properties and perform any necessary setup before an object can be used.

### Purpose
The primary purpose of initializers in Swift is to ensure that all properties of an instance are initialized to a valid state before the instance is used. Swift enforces this rule to maintain type safety and reliability.

### Usage
Initializers can be defined in classes, structures, and enumerations. Swift provides two types of initializers:
1. **Designated Initializers**: The main initializer for a class, responsible for ensuring that all properties are initialized and calling the superclass’s initializer.
2. **Convenience Initializers**: Secondary initializers that call designated initializers, providing a shortcut for common initialization tasks.

### Details
- Initializers in Swift do not return a value and are defined using the `init` keyword followed by parameters, if any.
- The `required` keyword can be used to indicate that all subclasses must implement the initializer.
- Initializers can have default parameter values, making it easier to create instances with various configurations.

## Examples
### Basic Initializer Example
```swift
class Dog {
    var name: String
    var age: Int
    
    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
}

let myDog = Dog(name: "Buddy", age: 3)
```

### Designated Initializer Example
```swift
class Vehicle {
    var wheels: Int
    
    init(wheels: Int) {
        self.wheels = wheels
    }
}

class Car: Vehicle {
    var model: String
    
    init(model: String) {
        self.model = model
        super.init(wheels: 4)
    }
}

let myCar = Car(model: "Toyota")
```

### Convenience Initializer Example
```swift
struct Rectangle {
    var width: Double
    var height: Double
    
    init(width: Double, height: Double) {
        self.width = width
        self.height = height
    }
    
    // Convenience initializer
    init(sideLength: Double) {
        self.init(width: sideLength, height: sideLength)
    }
}

let square = Rectangle(sideLength: 5)
```

## Explanation
### Common Pitfalls
- Forgetting to call the superclass initializer in a designated initializer can lead to runtime errors.
- Not initializing all properties before calling `self` can cause a compile-time error.
- Using `self` before initializing all properties in the initializer will also lead to errors.

### Additional Notes
- Swift provides memberwise initializers for structures, allowing you to automatically generate an initializer that takes parameters for each property.
- You cannot define an initializer for a type that is marked as `final`, as it cannot be subclassed.

## One Line Summary
The `init` keyword in Swift is essential for defining initializers that create and initialize instances of classes, structures, and enumerations, ensuring type safety and reliability.