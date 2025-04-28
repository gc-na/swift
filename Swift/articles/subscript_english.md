<!--
Meta Description: # Understanding Subscripts in Swift: A Comprehensive Guide ## Synopsis Subscripts in Swift provide a convenient way to access elements of collections,...
Meta Keywords: subscripts, you, int, index, swift
-->

# Understanding Subscripts in Swift: A Comprehensive Guide

## Synopsis
Subscripts in Swift provide a convenient way to access elements of collections, lists, or custom types using a straightforward, index-based syntax.

## Documentation
Subscripts are a powerful feature in Swift that allows you to define shortcuts for accessing elements within a collection or a custom data type. They enable you to query data structures in a more intuitive manner, making your code cleaner and easier to read.

### Purpose
Subscripts are particularly useful when you want to access elements by index or key, enabling you to simplify the syntax needed to retrieve or modify data.

### Usage
To define a subscript in Swift, you use the `subscript` keyword, followed by one or more input parameters and an optional return type. Subscripts can be defined for classes, structures, and enumerations.

### Syntax
```swift
subscript(index: Int) -> ElementType {
    get {
        // Return the element at the specified index
    }
    set(newValue) {
        // Set the element at the specified index
    }
}
```

You can also define subscripts with multiple parameters or custom types as indices.

## Examples

### Basic Example
Here’s a simple example using a custom structure that represents a collection of integers.

```swift
struct IntegerCollection {
    private var numbers: [Int] = []

    subscript(index: Int) -> Int {
        get {
            return numbers[index]
        }
        set(newValue) {
            numbers[index] = newValue
        }
    }

    mutating func append(_ number: Int) {
        numbers.append(number)
    }
}

var collection = IntegerCollection()
collection.append(10)
collection.append(20)
print(collection[0]) // Output: 10
collection[0] = 30
print(collection[0]) // Output: 30
```

### Multi-Parameter Subscript
You can also create a subscript that takes multiple parameters. Here’s an example using a 2D grid:

```swift
struct Grid {
    private var matrix: [[Int]]

    init(rows: Int, columns: Int) {
        matrix = Array(repeating: Array(repeating: 0, count: columns), count: rows)
    }

    subscript(row: Int, column: Int) -> Int {
        get {
            return matrix[row][column]
        }
        set {
            matrix[row][column] = newValue
        }
    }
}

var grid = Grid(rows: 3, columns: 3)
grid[0, 1] = 5
print(grid[0, 1]) // Output: 5
```

## Explanation
### Common Pitfalls
1. **Out of Bounds Access**: Attempting to access an index that is out of bounds will result in a runtime crash. Always ensure you check the bounds before accessing an index.
2. **Mutable vs Immutable**: Subscripts can be read-only or read-write. If you only define a getter, the subscript will be read-only, meaning you cannot assign values to it.
3. **Type Inference**: Swift can infer the type of the subscript, but it’s good practice to explicitly define the types for clarity.

### Additional Notes
- Subscripts can be overloaded, meaning you can define multiple subscripts with different parameter types or counts.
- Use subscripts sparingly; they are most effective when they enhance readability and maintainability.

## One Line Summary
Subscripts in Swift provide a succinct syntax for accessing elements in collections and custom types, enhancing code readability and usability.