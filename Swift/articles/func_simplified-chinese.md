<!--
Meta Description: # Swift中的函数（func）：深入理解与应用 ## 摘要 在Swift编程语言中，`func`是定义函数的关键字。函数是可重用的代码块，允许开发者将特定的功能封装起来，以便在程序中多次调用。 ## 文档 ### 目的 `func`用于定义函数，帮助开发者组织代码并实现模块化编程。通过使用函数，...
Meta Keywords: int, func, swift, let, print
-->

# Swift中的函数（func）：深入理解与应用

## 摘要
在Swift编程语言中，`func`是定义函数的关键字。函数是可重用的代码块，允许开发者将特定的功能封装起来，以便在程序中多次调用。

## 文档
### 目的
`func`用于定义函数，帮助开发者组织代码并实现模块化编程。通过使用函数，可以提高代码的可读性和可维护性。

### 用法
在Swift中，定义一个函数的基本语法如下：

```swift
func 函数名(参数名: 参数类型) -> 返回类型 {
    // 函数体
}
```

- **函数名**：用于标识函数的名称，必须是唯一的。
- **参数名**：传递给函数的输入值，可以有多个，形式为`参数名: 参数类型`。
- **返回类型**：函数执行后返回的值类型，使用`->`符号指定。

### 详细信息
- 函数可以没有参数和返回值。
- 可以使用默认参数值来简化函数调用。
- 支持可变参数，可以传入不定数量的参数。
- 函数可以返回多个值，使用元组（tuple）来实现。
- 可以将函数作为参数传递给其他函数，支持高阶函数。

## 示例
以下是一些基本用法示例：

1. **简单函数定义**
    ```swift
    func greet(name: String) -> String {
        return "Hello, \(name)!"
    }
    
    let greeting = greet(name: "Swift")
    print(greeting) // 输出: Hello, Swift!
    ```

2. **函数带有默认参数**
    ```swift
    func multiply(a: Int, b: Int = 2) -> Int {
        return a * b
    }
    
    let result1 = multiply(a: 3) // 使用默认参数b=2
    print(result1) // 输出: 6
    
    let result2 = multiply(a: 3, b: 4) // 指定b=4
    print(result2) // 输出: 12
    ```

3. **返回多个值**
    ```swift
    func divide(_ a: Int, _ b: Int) -> (quotient: Int, remainder: Int) {
        return (a / b, a % b)
    }
    
    let result = divide(10, 3)
    print("商: \(result.quotient), 余数: \(result.remainder)") // 输出: 商: 3, 余数: 1
    ```

## 说明
- **常见陷阱**：确保函数参数类型与调用时传入的值类型完全一致，否则会导致编译错误。
- **参数的标签**：Swift允许为函数参数指定外部标签，提高可读性。例如：`func add(first a: Int, second b: Int) -> Int`。
- **闭包与函数**：在Swift中，函数是一种特殊的闭包类型，了解闭包的概念有助于更好地使用函数。

## 一句话总结
`func`是Swift中定义和实现函数的关键字，为代码的可重用性和组织性提供了强大的支持。