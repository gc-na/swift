<!--
Meta Description: # Swift 中的 fileprivate 关键字详解 ## 摘要 `fileprivate` 是 Swift 编程语言中用于访问控制的关键字，允许在同一文件内的任何地方访问被标记的属性或方法。 ## 文档 `fileprivate` 关键字用于定义访问权限，限制对声明的可见性，以便只有同一文件中...
Meta Keywords: fileprivate, swift, private, privatevariable, func
-->

# Swift 中的 fileprivate 关键字详解

## 摘要
`fileprivate` 是 Swift 编程语言中用于访问控制的关键字，允许在同一文件内的任何地方访问被标记的属性或方法。

## 文档
`fileprivate` 关键字用于定义访问权限，限制对声明的可见性，以便只有同一文件中的代码可以访问它。与 `private` 不同，`fileprivate` 允许在同一文件的不同类型之间共享访问权限。其主要目的是提供更灵活的封装，同时又能保持代码的合理结构。

### 语法
```swift
fileprivate var variableName: Type
fileprivate func functionName() { }
```

### 用法
- 使用 `fileprivate` 关键字可以控制类、结构体、枚举、扩展及其成员的可访问性。
- 适用于需要在同一文件内的多个类型中共享的成员。
- 提供比 `private` 更宽松的访问权限。

## 示例
以下是 `fileprivate` 的基本用法示例：

```swift
class MyClass {
    fileprivate var privateVariable = 42
    
    fileprivate func printPrivateVariable() {
        print(privateVariable)
    }
}

class AnotherClass {
    func accessMyClass() {
        let myClassInstance = MyClass()
        myClassInstance.printPrivateVariable() // 可以访问
        print(myClassInstance.privateVariable) // 可以访问
    }
}
```

在上述示例中，`MyClass` 内的 `privateVariable` 和 `printPrivateVariable` 方法都被标记为 `fileprivate`，因此 `AnotherClass` 可以访问它们。

## 解释
- **常见误区**：开发者可能会误以为 `fileprivate` 与 `private` 是相同的。实际上，`private` 仅允许在声明的类型内访问，而 `fileprivate` 允许在同一文件内的其他类型访问。
- **性能方面**：使用 `fileprivate` 不会对性能产生负面影响，因为 Swift 编译器在编译时会优化访问权限。
- **最佳实践**：尽量避免过度使用 `fileprivate`，以保持代码的清晰度和可维护性，除非确实需要在同一文件的不同类型间共享状态或行为。

## 一句话总结
`fileprivate` 关键字在 Swift 中用于限制属性和方法的访问范围，使其在同一文件内可被访问。