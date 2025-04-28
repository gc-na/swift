<!--
Meta Description: # Understanding "public" Access Control in Swift: A Comprehensive Guide ## Synopsis In Swift, the `public` access control modifier allows entities suc...
Meta Keywords: public, module, access, swift, modules
-->

# Understanding "public" Access Control in Swift: A Comprehensive Guide

## Synopsis
In Swift, the `public` access control modifier allows entities such as classes, structs, and functions to be accessible from any source file within the same module or from any other module that imports the defining module. This article explores the purpose, usage, and best practices of the `public` access modifier in Swift.

## Documentation
The `public` access level is one of Swift's four primary access control levels: `open`, `public`, `internal`, and `private`. The `public` modifier is crucial for enabling the sharing of code across different modules while maintaining encapsulation for internal code.

### Purpose
The purpose of the `public` modifier is to enhance code modularity and reusability by enabling developers to expose certain components of their code to other modules. This is particularly useful when creating frameworks or libraries that are intended to be used by other applications.

### Usage
To declare an entity as `public`, simply prefix the declaration with the `public` keyword. This can be applied to classes, structs, enums, properties, methods, and initializers.

```swift
public class MyPublicClass {
    public var myPublicProperty: Int
    
    public init(value: Int) {
        self.myPublicProperty = value
    }

    public func myPublicMethod() {
        print("This is a public method.")
    }
}
```

### Details
- **Modules**: A module can be a single Swift file, a group of files, or an entire framework. When a module imports another module, it gains access to all public entities declared in that module.
- **Inheritance**: In contrast to `open`, which allows subclasses in other modules, `public` only permits access to subclasses within the same module.
- **Structs and Functions**: Similar to classes, structs and functions can also be declared `public`, making them accessible across different modules.
  
## Examples
### Example 1: Public Class
```swift
public class Animal {
    public var name: String
    
    public init(name: String) {
        self.name = name
    }
    
    public func makeSound() {
        print("Animal sound")
    }
}
```

### Example 2: Public Function
```swift
public func greet() {
    print("Hello from a public function!")
}
```

### Example 3: Public Struct
```swift
public struct Point {
    public var x: Int
    public var y: Int
    
    public init(x: Int, y: Int) {
        self.x = x
        self.y = y
    }
}
```

## Explanation
### Common Pitfalls
1. **Misunderstanding Access Levels**: Developers often confuse `public` with `open`. Remember that `public` allows access but restricts subclassing to within the same module.
2. **Not Importing Modules**: If you are trying to use a `public` entity from another module and it's not accessible, make sure you have imported the module correctly.
3. **Initialization**: If a property of a public class is `private`, it cannot be accessed or modified outside the class, which can lead to confusion about the object’s state.

### Additional Notes
- Use `public` judiciously to avoid exposing too much of your internal code structure.
- Consider marking functions and properties as `internal` or `private` if they are not intended for use outside their defining module.

## One Line Summary
The `public` access control modifier in Swift allows classes, structs, and functions to be accessible across different modules, promoting code reusability while maintaining encapsulation.