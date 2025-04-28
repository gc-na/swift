<!--
Meta Description: # Understanding Protocols in Swift: A Comprehensive Guide ## Synopsis In Swift, a protocol is a powerful tool that defines a blueprint of methods, pro...
Meta Keywords: protocol, protocols, swift, requirements, type
-->

# Understanding Protocols in Swift: A Comprehensive Guide

## Synopsis
In Swift, a protocol is a powerful tool that defines a blueprint of methods, properties, and other requirements that suit a particular task or functionality, allowing for flexible and reusable code through abstraction.

## Documentation
### Purpose
Protocols in Swift serve as a contract that defines a set of methods and properties that a conforming type must implement. They enable abstraction, making it possible to write flexible and reusable code by allowing different types to share the same interface.

### Usage
Protocols can be adopted by classes, structures, and enumerations. You define a protocol using the `protocol` keyword followed by its name and the requirements it includes. Types that conform to the protocol must implement all its requirements to be considered compliant.

### Details
- **Declaration**: A protocol is declared using the `protocol` keyword.
- **Conformance**: A type conforms to a protocol by using a colon followed by the protocol name in its definition.
- **Inheritance**: Protocols can inherit from other protocols, allowing for a hierarchy of requirements.
- **Optional Requirements**: Protocols can define optional requirements using the `@objc` attribute, but this is limited to classes that inherit from `NSObject`.

### Example of Protocol Declaration
```swift
protocol Vehicle {
    var numberOfWheels: Int { get }
    func startEngine()
}
```

### Example of Conforming to a Protocol
```swift
class Car: Vehicle {
    var numberOfWheels: Int {
        return 4
    }

    func startEngine() {
        print("Engine started")
    }
}
```

## Examples
### Basic Usage Example
Here is a simple example demonstrating the creation and usage of a protocol in Swift:

```swift
protocol Describable {
    var description: String { get }
}

struct Person: Describable {
    var name: String
    var age: Int
    
    var description: String {
        return "Name: \(name), Age: \(age)"
    }
}

let person = Person(name: "Alice", age: 30)
print(person.description) // Output: Name: Alice, Age: 30
```

### Protocol with Inheritance
Protocols can inherit from other protocols. Below is an example that illustrates this feature:

```swift
protocol Drivable: Vehicle {
    func drive()
}

class Motorcycle: Drivable {
    var numberOfWheels: Int {
        return 2
    }

    func startEngine() {
        print("Motorcycle engine started")
    }

    func drive() {
        print("Motorcycle is driving")
    }
}
```

## Explanation
### Common Pitfalls
- **Non-conformance**: If a type does not implement all required methods and properties of a protocol, it will not compile. Always ensure that all requirements are fulfilled.
- **Protocol Composition**: You can define a type that conforms to multiple protocols using protocol composition, but remember that all requirements from all protocols must be implemented.
- **Type Erasure**: When using protocols as types, be cautious of type erasure, especially when working with generics and closures.

### Gotchas
- Ensure that optional protocol requirements are marked appropriately if you're using `@objc`.
- Be aware of the distinction between protocol methods that are defined as `mutating` and those that are not, especially in structures.

## One Line Summary
Protocols in Swift provide a blueprint for methods and properties that enable flexible and reusable code through type abstraction.