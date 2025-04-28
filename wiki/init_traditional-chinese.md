<!--
Meta Description: # Swift中的初始化器(init)：用法與示例 ## 概述 在Swift編程語言中，`init`是一種特殊的方法，用於創建和初始化類或結構的實例。初始化器確保每個實例在使用之前都處於有效狀態。這對於管理資源和確保數據完整性至關重要。 ## 文檔 ### 目的 `init`初始化器的主要目的是設置...
Meta Keywords: init, self, width, height, var
-->

# Swift中的初始化器(init)：用法與示例

## 概述
在Swift編程語言中，`init`是一種特殊的方法，用於創建和初始化類或結構的實例。初始化器確保每個實例在使用之前都處於有效狀態。這對於管理資源和確保數據完整性至關重要。

## 文檔
### 目的
`init`初始化器的主要目的是設置類或結構的初始狀態。這包括為屬性賦值或執行其他設置任務。Swift中的初始化器可以是自定義的，也可以是系統自動提供的。

### 用法
在Swift中，初始化器的語法如下：
```swift
init(parameters) {
    // 初始化代碼
}
```
- **parameters**：可選的參數，用於初始化時傳遞值。

### 詳細說明
1. **類型初始化器**：每個類或結構都至少有一個默認初始化器。當你創建一個新類型並且所有屬性都有默認值時，Swift會自動提供一個初始化器。
2. **指定初始化器**：這種初始化器必須完全初始化所有屬性，並且可以指定一些必要的參數。例如：
   ```swift
   class Person {
       var name: String
       var age: Int
       
       init(name: String, age: Int) {
           self.name = name
           self.age = age
       }
   }
   ```
3. **便利初始化器**：這是輔助初始化器，用於簡化初始化過程。便利初始化器必須調用同一類型的指定初始化器，並且必須在其內部完全初始化所有屬性。

## 示例
以下是使用`init`的基本示例：
```swift
struct Rectangle {
    var width: Double
    var height: Double
    
    init(width: Double, height: Double) {
        self.width = width
        self.height = height
    }
}

let myRectangle = Rectangle(width: 10.0, height: 5.0)
print("寬度: \(myRectangle.width), 高度: \(myRectangle.height)")
```

## 解釋
在使用`init`時，開發者需要注意以下幾點：
- **所有屬性必須初始化**：在使用指定初始化器時，所有屬性都必須在初始化器返回之前被初始化。
- **循環引用**：在某些情況下，初始化器可能導致循環引用，特別是在使用閉包作為屬性時。應謹慎設計以避免此問題。
- **使用`self`**：在初始化器中使用`self`表示當前實例，必須在所有屬性被初始化之前不使用。

## 總結
Swift中的`init`初始化器是創建和初始化類或結構實例的關鍵工具，能夠確保對象始終處於有效狀態。