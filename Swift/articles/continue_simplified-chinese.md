<!--
Meta Description: # Swift 中的 "continue" 语句详解 ## 概述 在 Swift 编程语言中，`continue` 是一种控制流语句，用于提前结束当前循环的当前迭代，并立即开始下一次迭代。它在需要跳过当前循环中某些代码的情况下非常有用，尤其是在满足特定条件时。 ## 文档 `continue` 语句...
Meta Keywords: continue, while, swift, number, count
-->

# Swift 中的 "continue" 语句详解

## 概述
在 Swift 编程语言中，`continue` 是一种控制流语句，用于提前结束当前循环的当前迭代，并立即开始下一次迭代。它在需要跳过当前循环中某些代码的情况下非常有用，尤其是在满足特定条件时。

## 文档
`continue` 语句适用于所有类型的循环，包括 `for` 循环、`while` 循环和 `repeat-while` 循环。其主要目的是提高代码的可读性和执行效率，减少不必要的嵌套，并简化逻辑。

### 用法
在使用 `continue` 时，您只需在循环体内放置 `continue` 语句，并在需要跳过的条件下触发它。例如：

```swift
for number in 1...10 {
    if number % 2 == 0 {
        continue
    }
    print(number)
}
```

在上面的代码中，偶数会被跳过，只有奇数会被打印。

### 详细信息
- **适用范围**：`continue` 语句可以在 `for`、`while` 和 `repeat-while` 循环中使用。
- **控制流**：`continue` 只影响包含它的循环，不会影响外层循环或其他代码块的执行。
- **条件语句**：通常与条件语句（如 `if`）结合使用，以决定何时调用 `continue`。

## 示例
以下是几个简单的示例，展示了 `continue` 的用法：

### 示例 1：跳过偶数
```swift
for number in 1...10 {
    if number % 2 == 0 {
        continue
    }
    print(number) // 输出：1, 3, 5, 7, 9
}
```

### 示例 2：使用 while 循环
```swift
var count = 0
while count < 10 {
    count += 1
    if count % 3 == 0 {
        continue
    }
    print(count) // 输出：1, 2, 4, 5, 7, 8, 10
}
```

### 示例 3：与 repeat-while 结合使用
```swift
var index = 0
repeat {
    index += 1
    if index == 5 {
        continue
    }
    print(index) // 输出：1, 2, 3, 4, 6, 7, 8, ...
} while index < 10
```

## 解释
使用 `continue` 时，开发者需要注意以下几点：
- 确保在适当的上下文中使用，以避免意外跳过重要逻辑。
- 在嵌套循环中，`continue` 只影响最内层的循环。
- 过度使用 `continue` 可能会导致代码难以阅读，建议在逻辑清晰的情况下使用。

## 一句话总结
`continue` 语句在 Swift 中用于跳过当前循环的迭代，直接进入下一次迭代，提高代码的执行效率和可读性。