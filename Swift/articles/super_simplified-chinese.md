<!--
Meta Description: # Swift中的super关键字详解 ## 概述 在Swift编程语言中，`super`关键字用于引用父类的属性、方法和初始化器。它是实现继承和多态性的核心组成部分，使得子类可以访问和扩展父类的功能。 ## 文档 ### 目的 `super`关键字的主要目的是允许子类在覆盖父类的方法时仍然能够调用...
Meta Keywords: super, class, child, wheels, print
-->

# Swift中的super关键字详解

## 概述
在Swift编程语言中，`super`关键字用于引用父类的属性、方法和初始化器。它是实现继承和多态性的核心组成部分，使得子类可以访问和扩展父类的功能。

## 文档
### 目的
`super`关键字的主要目的是允许子类在覆盖父类的方法时仍然能够调用父类的实现。这对于需要在子类中扩展或修改父类行为的情况非常有用。

### 用法
在Swift中，当你想在子类中调用父类的方法或属性时，可以使用`super`。例如，在重写一个方法时，你可以使用`super.methodName()`来调用父类的实现。

```swift
class Parent {
    func greet() {
        print("Hello from Parent")
    }
}

class Child: Parent {
    override func greet() {
        super.greet()  // 调用父类的方法
        print("Hello from Child")
    }
}

let child = Child()
child.greet()
// 输出:
// Hello from Parent
// Hello from Child
```

### 细节
- `super`可以用于调用父类的实例方法、类方法和初始化器。
- 在重写父类的初始化器时，必须在初始化器的开头调用`super.init()`。
- 使用`super`时，确保你调用的是正确的父类方法，避免不必要的错误。

## 示例
以下是一些使用`super`的基本示例：

1. **调用父类方法**

    ```swift
    class Animal {
        func makeSound() {
            print("Animal sound")
        }
    }

    class Dog: Animal {
        override func makeSound() {
            super.makeSound()  // 调用父类的方法
            print("Bark")
        }
    }

    let dog = Dog()
    dog.makeSound()
    // 输出:
    // Animal sound
    // Bark
    ```

2. **调用父类初始化器**

    ```swift
    class Vehicle {
        var wheels: Int
        
        init(wheels: Int) {
            self.wheels = wheels
        }
    }

    class Bicycle: Vehicle {
        var type: String
        
        init(type: String) {
            self.type = type
            super.init(wheels: 2)  // 调用父类初始化器
        }
    }

    let bicycle = Bicycle(type: "Mountain")
    print(bicycle.wheels)  // 输出: 2
    ```

## 说明
- **常见陷阱**：在重写方法时，一定要记得调用`super`，否则父类的功能将不会被执行，这可能导致意外的行为。
- **多态性**：`super`关键字让你能够利用多态性，允许子类扩展父类的功能，而不需要完全重写它们。
- **限制**：在类的扩展中不能使用`super`，因为扩展并没有继承关系。

## 一句话总结
`super`关键字在Swift中用于引用父类的属性和方法，帮助实现继承和扩展父类功能。