<!--
Meta Description: # Understanding "private" Access Control in Swift ## Synopsis The `private` access control modifier in Swift restricts access to properties and method...
Meta Keywords: private, access, username, swift, class
-->

# Understanding "private" Access Control in Swift

## Synopsis
The `private` access control modifier in Swift restricts access to properties and methods within the defining scope, enhancing encapsulation and safeguarding your code from unintended external access.

## Documentation
In Swift, access control is a critical feature that determines the visibility of properties, methods, and other declarations. The `private` access level is designed to limit the accessibility of these declarations to the enclosing declaration (the class, struct, or extension) and to extensions of that declaration in the same file.

### Purpose
The primary purpose of using `private` is to encapsulate implementation details, ensuring that external code cannot modify or access the internals of a class or struct. This is crucial for maintaining the integrity of the code and preventing unintended interactions.

### Usage
To declare a property or method as `private`, simply prefix it with the `private` keyword. This will restrict its access to the enclosing scope.

```swift
class MyClass {
    private var secretNumber: Int = 42

    private func revealSecret() {
        print("The secret number is \(secretNumber)")
    }

    func publicMethod() {
        revealSecret() // This is allowed
    }
}
```

## Examples
Here are some basic usage examples of the `private` access modifier:

### Example 1: Private Variable
```swift
class BankAccount {
    private var balance: Double = 0.0

    func deposit(amount: Double) {
        balance += amount
    }

    func getBalance() -> Double {
        return balance
    }
}
```

### Example 2: Private Method
```swift
class User {
    private var username: String

    init(username: String) {
        self.username = username
    }

    private func displayUsername() {
        print("Username: \(username)")
    }

    func showUserInfo() {
        displayUsername() // Allowed
    }
}

let user = User(username: "SwiftUser")
user.showUserInfo() // Output: Username: SwiftUser
// user.displayUsername() // Error: 'displayUsername' is inaccessible due to 'private' protection level
```

## Explanation
While `private` is a powerful tool for encapsulation, there are some common pitfalls and gotchas to be aware of:

1. **Scope Limitation**: The `private` keyword restricts access strictly to the defining scope. If you define a variable or method as `private` in a class, it cannot be accessed from subclasses or even from extensions outside the class.

2. **Nested Types**: If a type is defined inside another type, `private` properties or methods can be accessed by the enclosing type, even if they are declared `private`.

3. **Debugging**: When debugging, you might encounter issues if you forget that certain properties or methods are private, leading to confusion about why they cannot be accessed.

4. **Alternative Access Levels**: If you need slightly broader access, consider using `fileprivate`, which allows access within the same file, or `internal`, which allows access within the same module.

## One Line Summary
The `private` access control modifier in Swift restricts access to properties and methods to the enclosing scope, enhancing code encapsulation and integrity.