<!--
Meta Description: # Understanding "super" in Swift: A Comprehensive Guide ## Synopsis The `super` keyword in Swift is used to refer to the superclass of a class, enabli...
Meta Keywords: super, superclass, method, name, class
-->

# Understanding "super" in Swift: A Comprehensive Guide

## Synopsis
The `super` keyword in Swift is used to refer to the superclass of a class, enabling access to methods, properties, and initializers inherited from that superclass.

## Documentation
In Swift, the `super` keyword serves a crucial role in object-oriented programming by allowing subclasses to interact with their parent classes. When a subclass overrides a method from its superclass, it may still need to call the superclass's implementation of that method. The `super` keyword provides a straightforward way to achieve this.

### Purpose
- **Access Superclass Methods:** `super` allows subclasses to call methods defined in their superclass, ensuring that inherited behaviors are preserved.
- **Access Properties:** It can also be used to access properties of the superclass.
- **Initializer Chains:** `super` is essential for calling superclass initializers for proper initialization of inherited properties.

### Usage
The `super` keyword can be used in various contexts, such as within instance methods, initializers, or property accessors. Here’s how it is typically used:

- **Calling Methods:** Use `super.methodName()` to call an overridden method from the superclass.
- **Accessing Properties:** Use `super.propertyName` to access properties defined in the superclass.

## Examples

### Example 1: Calling a Superclass Method
```swift
class Animal {
    func makeSound() {
        print("Animal sound")
    }
}

class Dog: Animal {
    override func makeSound() {
        super.makeSound() // Calls the superclass method
        print("Bark")
    }
}

let dog = Dog()
dog.makeSound()
// Output:
// Animal sound
// Bark
```

### Example 2: Accessing a Superclass Property
```swift
class Vehicle {
    var wheels: Int = 4
}

class Bicycle: Vehicle {
    override var wheels: Int {
        get {
            return super.wheels // Access superclass property
        }
        set {
            super.wheels = newValue
        }
    }
}

let bike = Bicycle()
print(bike.wheels) // Output: 4
```

### Example 3: Using Super in Initializers
```swift
class Person {
    var name: String

    init(name: String) {
        self.name = name
    }
}

class Student: Person {
    var studentID: String

    init(name: String, studentID: String) {
        self.studentID = studentID
        super.init(name: name) // Calls the superclass initializer
    }
}

let student = Student(name: "Alice", studentID: "S123")
print(student.name) // Output: Alice
print(student.studentID) // Output: S123
```

## Explanation
While using `super`, there are several common pitfalls to be aware of:

1. **Cannot Use Outside Class Scope:** The `super` keyword can only be used within methods or initializers of the subclass. Attempting to use it outside these contexts will result in a compile-time error.

2. **Method Must Be Overridden:** When calling a method using `super`, ensure that the method exists in the superclass and has been overridden in the subclass. If the method isn't overridden, directly calling `super.methodName()` will not compile.

3. **Initializer Order:** When working with designated and convenience initializers, ensure that you call `super.init()` at the appropriate point in your initializer chain to avoid initialization errors.

## One Line Summary
The `super` keyword in Swift allows subclasses to access and invoke methods, properties, and initializers from their superclass, ensuring proper inheritance and behavior in object-oriented programming.