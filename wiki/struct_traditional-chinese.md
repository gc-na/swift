<!--
Meta Description: # Swift 中的 Struct：結構體的深入解析 ## 摘要 在 Swift 程式語言中，`struct`（結構體）是一種重要的資料類型，用於定義複雜資料結構。結構體可以封裝數據和行為，使程式碼更具可讀性和可維護性。 ## 文檔 ### 目的 結構體是 Swift 中的基本資料類型之一，與類別（...
Meta Keywords: swift, struct, var, width, height
-->

# Swift 中的 Struct：結構體的深入解析

## 摘要
在 Swift 程式語言中，`struct`（結構體）是一種重要的資料類型，用於定義複雜資料結構。結構體可以封裝數據和行為，使程式碼更具可讀性和可維護性。

## 文檔
### 目的
結構體是 Swift 中的基本資料類型之一，與類別（class）相似，但有一些關鍵的差異。結構體是值類型，這意味著當它們被複製時，會創建一個新的實例，而不是引用原始實例。這使得結構體在需要處理輕量級資料時非常有用。

### 使用方式
在 Swift 中定義結構體使用 `struct` 關鍵字，其基本語法如下：

```swift
struct StructName {
    // 屬性
    var propertyName: PropertyType
    // 方法
    func methodName() {
        // 方法實現
    }
}
```

### 詳細信息
1. **屬性**：結構體可以包含多種屬性，包括常數（`let`）和變數（`var`）。
2. **方法**：結構體可以包含方法，這些方法可以操作結構體的屬性。
3. **初始器**：Swift 自動為結構體提供了一個成員逐一初始化器，但開發者也可以自定義初始化器。
4. **值類型**：結構體是值類型，這意味著每次賦值或傳遞時都會創建一個新的實例。
5. **擴展**：結構體支持擴展，允許開發者新增功能而不修改原始定義。

## 範例
### 基本用法
以下是一個簡單的結構體範例，展示如何定義和使用結構體：

```swift
struct Person {
    var name: String
    var age: Int
    
    func introduce() -> String {
        return "你好，我是 \(name)，我 \(age) 歲。"
    }
}

let person1 = Person(name: "小明", age: 25)
print(person1.introduce())
```

### 使用初始器
自定義初始化器範例如下：

```swift
struct Rectangle {
    var width: Double
    var height: Double
    
    init(width: Double, height: Double) {
        self.width = width
        self.height = height
    }
    
    func area() -> Double {
        return width * height
    }
}

let rect = Rectangle(width: 5.0, height: 10.0)
print("面積：\(rect.area())")
```

## 解釋
### 常見陷阱
- **值類型的行為**：因為結構體是值類型，對結構體的修改不會影響原始實例。這在傳遞參數時需要特別注意。
- **與類別的區別**：結構體與類別在繼承和參考行為上有所不同，開發者需根據需求選擇使用。
- **不支持參考型別特性**：結構體無法使用參考型別的特性，如 deinitializers 和 type inheritance。

## 一句總結
`struct` 在 Swift 中是一種強大的值類型，用於定義複雜的資料結構，提供了良好的封裝和方法支持。