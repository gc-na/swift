<!--
Meta Description: # Swift 中的 "init" 初始化器详解 ## 摘要 在 Swift 编程语言中，`init` 是用于初始化对象的特殊方法，确保实例在使用之前处于有效状态。 ## 文档 `init` 是 Swift 中的初始化器，用于为类、结构体或枚举的实例设置初始值。当创建一个新实例时，`init` 方法...
Meta Keywords: init, swift, celsius, name, age
-->

# Swift 中的 "init" 初始化器详解

## 摘要
在 Swift 编程语言中，`init` 是用于初始化对象的特殊方法，确保实例在使用之前处于有效状态。

## 文档
`init` 是 Swift 中的初始化器，用于为类、结构体或枚举的实例设置初始值。当创建一个新实例时，`init` 方法会被自动调用，并为属性赋予初始值。一个类或结构体可以有多个初始化器，这样可以提供不同的初始化方式。

### 目的
`init` 的主要目的是确保所有实例在创建时都被初始化为有效状态，避免未初始化的属性导致程序错误。

### 用法
初始化器可以定义在类、结构体或枚举内部，语法如下：

```swift
init(参数名: 参数类型) {
    // 初始化代码
}
```

### 细节
- 如果类或结构体中定义了属性，必须在初始化器中为这些属性赋值。
- 可以使用`self`关键字在初始化器中引用当前实例。
- Swift 支持可失败初始化器（failable initializer），可以返回 nil 表示初始化失败。
- 如果没有自定义初始化器，Swift 会自动生成一个默认初始化器。

## 示例
### 基本用法
```swift
class Person {
    var name: String
    var age: Int

    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
}

let person = Person(name: "张三", age: 30)
print(person.name)  // 输出: 张三
```

### 可失败初始化器
```swift
struct Temperature {
    var celsius: Double

    init?(celsius: Double) {
        if celsius < -273.15 {
            return nil // 不允许低于绝对零度
        }
        self.celsius = celsius
    }
}

if let temp = Temperature(celsius: -300) {
    print(temp.celsius)
} else {
    print("温度无效")
}
```

## 解释
在使用 `init` 时，常见的陷阱包括：
- 忘记为所有属性赋初值，导致编译错误。
- 使用可失败初始化器时未妥善处理返回值，可能导致意外的 nil 值。
- 不同初始化器之间使用相同的参数类型导致模糊，可能会引发歧义。

## 一句话总结
`init` 是 Swift 中用于创建类和结构体实例的初始化器，确保实例的有效性和完整性。