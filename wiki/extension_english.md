<!--
Meta Description: # Understanding Extensions in Swift: Enhance Your Code with Ease ## Synopsis In Swift, extensions allow you to add new functionality to existing class...
Meta Keywords: extensions, swift, can, type, add
-->

# Understanding Extensions in Swift: Enhance Your Code with Ease

## Synopsis
In Swift, extensions allow you to add new functionality to existing classes, structures, enumerations, or protocols without modifying their original source code. This feature promotes code organization, reusability, and maintainability.

## Documentation
Extensions in Swift enable developers to extend the capabilities of existing types. They can be used to add computed properties, methods, initializers, and even conform a type to a protocol. This functionality enhances Swift's type system, making it more flexible and powerful.

### Purpose
The primary purpose of extensions is to enable separation of concerns and to enhance the functionality of types without subclassing. This is particularly useful when working with types defined in external libraries or frameworks where you cannot modify the original implementation.

### Usage
To define an extension in Swift, use the `extension` keyword followed by the name of the type you want to extend. You can then add new properties, methods, and initializers within the curly braces.

```swift
extension SomeType {
    // New functionality
}
```

### Details
- **Adding Computed Properties**: Extensions can add computed properties to existing types.
- **Adding Instance and Type Methods**: You can also add new methods that can be called on instances of the type or the type itself.
- **Adding Initializers**: Extensions can provide new initializers to an existing type.
- **Conforming to Protocols**: Extensions can make existing types conform to protocols, providing the necessary method implementations.

## Examples

### Adding a Computed Property
```swift
extension Double {
    var squared: Double {
        return self * self
    }
}

let number: Double = 3.0
print(number.squared)  // Output: 9.0
```

### Adding a Method
```swift
extension String {
    func reversed() -> String {
        return String(self.reversed())
    }
}

let greeting = "Hello"
print(greeting.reversed())  // Output: "olleH"
```

### Conforming to a Protocol
```swift
protocol Describable {
    var description: String { get }
}

extension Int: Describable {
    var description: String {
        return "The number is \(self)"
    }
}

let myNumber: Int = 42
print(myNumber.description)  // Output: "The number is 42"
```

## Explanation
While extensions are powerful, there are some common pitfalls to be aware of:

- **Limitations**: You cannot override existing methods or properties in a type via extension. Extensions can only add new functionality.
- **Stored Properties**: Extensions cannot add stored properties; they can only add computed properties or methods.
- **Access Control**: The access level of extensions must match the access level of the original type. For example, if a class is declared as `public`, the extension must also be declared as `public`.
- **Initializers**: Extensions can add new initializers, but they cannot override the existing initializers defined in the original type.

## One Line Summary
Extensions in Swift allow you to enhance existing types by adding new functionality, making your code more modular and maintainable.