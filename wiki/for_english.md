<!--
Meta Description: # Understanding the "for" Loop in Swift: A Comprehensive Guide ## Synopsis The "for" loop in Swift is a fundamental control flow structure that allows...
Meta Keywords: loop, swift, over, index, print
-->

# Understanding the "for" Loop in Swift: A Comprehensive Guide

## Synopsis
The "for" loop in Swift is a fundamental control flow structure that allows developers to iterate over sequences, such as arrays, ranges, and dictionaries, efficiently and succinctly.

## Documentation
The `for` loop in Swift is primarily used to execute a block of code multiple times, iterating over a sequence or a collection. This control structure is essential for repetitive tasks where the number of iterations is known or can be calculated.

### Purpose
The purpose of the `for` loop is to automate repetitive actions, making code more concise, readable, and maintainable.

### Usage
The basic syntax of the `for` loop in Swift can be structured as follows:

```swift
for index in sequence {
    // Code to be executed for each index
}
```

- **index**: A constant representing the current value in each iteration.
- **sequence**: A collection or range that defines the set of values to iterate over.

### Details
The `for` loop can iterate over:
- **Arrays**: Accessing each element in sequence.
- **Ranges**: Running a block of code a specified number of times.
- **Dictionaries**: Iterating over key-value pairs.

### Variations
1. **For-In Loop**: Iterates over collections.
   ```swift
   let fruits = ["Apple", "Banana", "Cherry"]
   for fruit in fruits {
       print(fruit)
   }
   ```

2. **For-Each Loop**: A method to apply a function on each element in a collection.
   ```swift
   fruits.forEach { fruit in
       print(fruit)
   }
   ```

3. **For Loop with Indices**: Useful for when you need both the index and the value.
   ```swift
   for index in fruits.indices {
       print("Index \(index): \(fruits[index])")
   }
   ```

## Examples
### Basic Array Iteration
```swift
let numbers = [1, 2, 3, 4, 5]
for number in numbers {
    print(number)
}
```

### Iterating Over a Range
```swift
for i in 1...5 {
    print("Iteration \(i)")
}
```

### Dictionary Iteration
```swift
let ages = ["Alice": 25, "Bob": 30, "Charlie": 35]
for (name, age) in ages {
    print("\(name) is \(age) years old.")
}
```

## Explanation
While the `for` loop is straightforward, there are a few common pitfalls to be aware of:

- **Off-by-One Errors**: When using ranges, ensure that the range is correctly defined (e.g., using `1...5` includes 5, while `1..<5` does not).
- **Mutable Collections**: If the collection being iterated over is modified during the loop, it can lead to unexpected behavior or runtime errors.
- **Loop Variable Scope**: The loop variable is a constant within the loop’s scope. If you need to modify it, you must create a new variable.

## One Line Summary
The `for` loop in Swift is a powerful control structure that facilitates iteration over sequences, enhancing code efficiency and readability.