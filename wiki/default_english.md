<!--
Meta Description: # Understanding "default" in Swift: A Comprehensive Guide ## Synopsis In Swift, the term "default" commonly refers to default values in function param...
Meta Keywords: default, swift, print, switch, values
-->

# Understanding "default" in Swift: A Comprehensive Guide

## Synopsis
In Swift, the term "default" commonly refers to default values in function parameters, property initializers, and switch statements. This feature enhances code readability and provides flexibility when working with functions and types.

## Documentation
### Purpose
The "default" mechanism in Swift allows developers to set values that will be used if no specific value is provided. This is particularly useful in functions, where optional parameters may not always be supplied, and in switch statements to handle unexpected cases.

### Usage
1. **Default Parameter Values**: When defining a function, you can assign a default value to its parameters. If the caller does not provide a value, the default will be used.

   ```swift
   func greet(name: String = "Guest") {
       print("Hello, \(name)!")
   }
   
   greet()        // Output: Hello, Guest!
   greet(name: "John") // Output: Hello, John!
   ```

2. **Switch Statement Default Case**: In a switch statement, the `default` case acts as a fallback for any values that do not explicitly match the specified cases.

   ```swift
   let number = 3
   switch number {
   case 1:
       print("One")
   case 2:
       print("Two")
   default:
       print("Other number") // Output: Other number
   }
   ```

3. **Default Properties in Structures and Classes**: You can also provide default initial values for properties in structures and classes.

   ```swift
   struct User {
       var name: String
       var age: Int = 18  // Default age is 18
   }

   let user1 = User(name: "Alice")
   print(user1.age) // Output: 18
   ```

## Examples
### Example 1: Function with Default Parameter
```swift
func multiply(a: Int, b: Int = 2) -> Int {
    return a * b
}

print(multiply(a: 3)) // Output: 6
print(multiply(a: 3, b: 4)) // Output: 12
```

### Example 2: Switch Statement with Default Case
```swift
let fruit = "banana"
switch fruit {
case "apple":
    print("Apple selected")
case "orange":
    print("Orange selected")
default:
    print("Unknown fruit") // Output: Unknown fruit
}
```

### Example 3: Class with Default Property
```swift
class Car {
    var model: String
    var year: Int = 2020 // Default year

    init(model: String) {
        self.model = model
    }
}

let myCar = Car(model: "Toyota")
print(myCar.year) // Output: 2020
```

## Explanation
While the default mechanism in Swift simplifies many coding scenarios, there are a few common pitfalls to watch out for:

- **Overriding Defaults**: When you call a function with default parameters, ensure that the order of arguments does not lead to confusion, especially when mixing default and non-default parameters.
  
- **Exclusivity in Switch Statements**: Always remember to provide a `default` case in switch statements when there are possible values that may not be explicitly handled. This prevents runtime errors and ensures your code is robust.

- **Type Safety**: Default values must be of the same type as the parameter or property they are assigned to. Otherwise, it will lead to compilation errors.

## One Line Summary
In Swift, "default" refers to pre-set values for function parameters, properties, and switch cases, enhancing code flexibility and readability.