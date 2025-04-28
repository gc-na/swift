<!--
Meta Description: # Understanding `fileprivate` in Swift: Access Control for Encapsulation ## Synopsis `fileprivate` is a Swift access control modifier that restricts t...
Meta Keywords: fileprivate, access, file, swift, within
-->

# Understanding `fileprivate` in Swift: Access Control for Encapsulation

## Synopsis
`fileprivate` is a Swift access control modifier that restricts the visibility of entities to the defining file. This feature enhances encapsulation by allowing developers to manage access to properties, methods, and types within a single file while preventing external access.

## Documentation
In Swift, access control is crucial for ensuring that the internal workings of your code remain hidden from other parts of your program. The `fileprivate` modifier facilitates this by limiting access to the scope of the file in which it is declared. 

### Purpose
The intent behind `fileprivate` is to provide a fine-grained level of access control. It allows multiple types or extensions within the same file to interact with each other while keeping them hidden from the rest of the module.

### Usage
To use `fileprivate`, simply prepend the keyword to the declaration of a variable, constant, function, or type. Here’s how it can be applied:

```swift
fileprivate var hiddenVariable: Int = 42

fileprivate func hiddenFunction() {
    print("This is a fileprivate function.")
}
```

In the above example, both `hiddenVariable` and `hiddenFunction` can only be accessed within the same Swift file. If you attempt to access them from another file, you will encounter a compile-time error.

### Details
- `fileprivate` is more restrictive than `internal` (the default access level), which allows access anywhere within the same module.
- It is less restrictive than `private`, which limits access to the enclosing declaration and its extensions.
- Use `fileprivate` when you need to share functionality or data across multiple types or extensions within the same file but want to prevent access from outside that file.

## Examples
### Example 1: Basic Usage
```swift
// File: Example.swift
fileprivate class ExampleClass {
    fileprivate var exampleProperty: String = "Hello, World!"

    fileprivate func exampleMethod() {
        print(exampleProperty)
    }
}

let instance = ExampleClass()
instance.exampleMethod()  // This will work
```

### Example 2: Multiple Types
```swift
// File: MultipleTypes.swift
fileprivate struct FilePrivateStruct {
    fileprivate var value: Int = 10
}

fileprivate extension FilePrivateStruct {
    fileprivate func printValue() {
        print(value)
    }
}

let myStruct = FilePrivateStruct()
myStruct.printValue()  // This will work
```

## Explanation
### Common Pitfalls
- **Accessing from Another File**: Attempting to access `fileprivate` members from another file will result in a compilation error. Ensure that all code that requires access is in the same file.
- **Overusing `fileprivate`**: While `fileprivate` is useful, overusing it can lead to code that is less modular and harder to understand. Use it judiciously to maintain a balance between encapsulation and code readability.

### Gotchas
- **Confusion with Scoping**: Developers may confuse `fileprivate` with `private`. Remember that `fileprivate` allows access across the entire file, while `private` only allows access within the immediate enclosing scope.
- **Access Levels Hierarchy**: Understanding how `fileprivate` fits within the Swift access control hierarchy (public > internal > fileprivate > private) is essential for proper implementation.

## One Line Summary
`fileprivate` restricts the visibility of entities to the defining file in Swift, promoting encapsulation while allowing internal interaction within that file.