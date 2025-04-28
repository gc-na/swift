<!--
Meta Description: # Understanding `var` in Swift: Declaration of Variables ## Synopsis The `var` keyword in Swift is used to declare variables that can be modified afte...
Meta Keywords: var, variable, swift, variables, value
-->

# Understanding `var` in Swift: Declaration of Variables

## Synopsis
The `var` keyword in Swift is used to declare variables that can be modified after their initial assignment, allowing for flexible and dynamic data handling in your applications.

## Documentation
In Swift, `var` is a fundamental keyword that stands for "variable." It is used to declare a variable, which is a storage location that can hold data and whose value can change over time. The `var` keyword introduces mutable variables, meaning the value assigned to a variable declared with `var` can be modified throughout the program.

### Purpose
The primary purpose of using `var` is to create variables whose values can be adjusted as needed, making it ideal for scenarios where the data is expected to change during the execution of the program.

### Usage
When declaring a variable with `var`, you can optionally specify a type. If you don't specify a type, Swift infers it from the assigned value. Here’s the syntax:

```swift
var variableName: Type = initialValue
```

- **variableName**: The name of the variable.
- **Type**: The data type of the variable (optional).
- **initialValue**: The value assigned at the time of declaration.

### Example of Declaring Variables
```swift
var age: Int = 25
var name = "Alice" // Type inferred as String
```

In the above examples:
- The variable `age` is explicitly declared as an `Int`.
- The variable `name` is inferred as a `String` based on the assigned value.

## Examples
Here are a few more examples demonstrating the use of `var`:

1. **Basic Variable Initialization**
    ```swift
    var score = 100
    print(score) // Output: 100
    ```

2. **Modifying a Variable**
    ```swift
    var temperature = 20
    print(temperature) // Output: 20
    temperature = 25
    print(temperature) // Output: 25
    ```

3. **Using Variables in Calculations**
    ```swift
    var a = 5
    var b = 10
    var sum = a + b
    print(sum) // Output: 15
    ```

## Explanation
While using `var`, here are some common pitfalls and considerations:

- **Type Inference**: Swift will automatically infer the type of the variable from the initial value, which may lead to unexpected types if the initial value is ambiguous. It’s a good practice to explicitly define types when clarity is needed.
  
- **Mutability**: Remember that variables declared with `var` are mutable. If you need an immutable variable, consider using `let` instead, which declares constants that cannot be changed.

- **Scope**: The scope of a variable declared with `var` is limited to the block of code in which it is defined. Be mindful of where you declare your variables to avoid unintended overwrites or access issues.

- **Default Values**: If a variable is declared without an initial value, it must be initialized before use, or the compiler will throw an error.

## One Line Summary
The `var` keyword in Swift is essential for declaring mutable variables that can be modified throughout the program, providing flexibility in data handling.