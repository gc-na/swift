<!--
Meta Description: # Swift中的「self」關鍵字：用法與示例 ## 簡介 「self」是在Swift編程語言中用來指向當前對象的關鍵字。它在類和結構體的上下文中，特別是在實現方法和屬性時，起著重要的作用。 ## 文檔 ### 目的 「self」的主要目的是提供對當前實例的引用，這在需要明確區分屬性和方法的參數時...
Meta Keywords: self, name, person, 當方法的參數名稱與屬性名稱相同時, 在swift中
-->

# Swift中的「self」關鍵字：用法與示例

## 簡介
「self」是在Swift編程語言中用來指向當前對象的關鍵字。它在類和結構體的上下文中，特別是在實現方法和屬性時，起著重要的作用。

## 文檔
### 目的
「self」的主要目的是提供對當前實例的引用，這在需要明確區分屬性和方法的參數時特別有用。當方法的參數名稱與屬性名稱相同時，使用「self」可以避免歧義。

### 使用
在Swift中，「self」可以用於以下情況：
1. 在方法內部訪問類或結構體的屬性。
2. 在初始化器中引用當前實例。
3. 在閉包中捕獲對當前實例的引用。

### 詳細說明
- 在方法中，您可以使用「self」來引用當前實例的屬性或方法。例如，當方法的參數名稱與屬性名稱相同時，使用「self」可以確保您訪問的是屬性，而不是參數。
- 在初始化器中，使用「self」可以明確指定要初始化的屬性。
- 在閉包中，使用「self」可以防止強引用循環，尤其是在捕獲`self`時，應使用 `[weak self]` 或 `[unowned self]`。

## 示例
以下是一個簡單的示例，展示「self」的基本用法：

```swift
class Person {
    var name: String

    init(name: String) {
        self.name = name // 使用 self 來區分屬性和參數
    }

    func greet() {
        print("Hello, my name is \(self.name).") // 使用 self 訪問屬性
    }
}

let person = Person(name: "Alice")
person.greet() // 輸出: Hello, my name is Alice.
```

## 解釋
- **常見陷阱**：在Swift中，有時候可能會忘記使用「self」，導致使用不正確的變量。特別是在大型類中，為了清晰起見，建議始終使用「self」來引用屬性。
- **強引用循環**：在閉包中使用「self」時，可能會造成強引用循環。這種情況需要用到`weak`或`unowned`來避免記憶體泄漏。

## 總結
「self」是Swift中用來引用當前實例的重要關鍵字，有助於清晰地管理類或結構體的屬性和方法。