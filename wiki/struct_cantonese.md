<!--
Meta Description: # Swift 中的 Struct：結構體的全面指南 ## 簡介 在 Swift 中，`struct`（結構體）是一種用來定義複合數據類型的方式，可以用來封裝數據和行為。結構體是一種值類型，提供了一種簡潔且強大的方法來組織代碼。 ## 文件說明 結構體在 Swift 中是一種基本的數據結構，允許開發...
Meta Keywords: swift, struct, var, double, property
-->

# Swift 中的 Struct：結構體的全面指南

## 簡介
在 Swift 中，`struct`（結構體）是一種用來定義複合數據類型的方式，可以用來封裝數據和行為。結構體是一種值類型，提供了一種簡潔且強大的方法來組織代碼。

## 文件說明
結構體在 Swift 中是一種基本的數據結構，允許開發者創建自定義的數據類型。與類別（class）不同，結構體是值類型，這意味著當它們被賦值或傳遞時，會創建一個副本。結構體可以包含屬性、方法、初始化器，以及遵循協議。它們非常適合用來表示輕量級的數據結構，如點、矩形或顏色等。

### 目的
使用結構體可以幫助開發者更好地組織代碼，並創建清晰易懂的數據模型，特別是在處理不需要繼承的情況下。

### 使用方式
在 Swift 中，你可以使用 `struct` 關鍵字來定義一個結構體。以下是基本語法：
```swift
struct StructName {
    // 屬性
    var property: Type
    
    // 初始化器
    init(property: Type) {
        self.property = property
    }
    
    // 方法
    func methodName() {
        // 方法實現
    }
}
```

## 範例
### 基本使用範例
以下是一個簡單的結構體範例，表示一個矩形：
```swift
struct Rectangle {
    var width: Double
    var height: Double
    
    func area() -> Double {
        return width * height
    }
}

// 使用結構體
let myRectangle = Rectangle(width: 5.0, height: 10.0)
print("矩形面積: \(myRectangle.area())") // 輸出: 矩形面積: 50.0
```

### 結構體包含方法
結構體可以包含方法來處理自己的數據：
```swift
struct Circle {
    var radius: Double
    
    func circumference() -> Double {
        return 2 * .pi * radius
    }
}

let myCircle = Circle(radius: 3.0)
print("圓周: \(myCircle.circumference())") // 輸出: 圓周: 18.84955592153876
```

## 說明
### 常見陷阱及注意事項
- **值類型**：由於結構體是值類型，當你將結構體賦值給另一個變量時，會創建一個副本，而不是引用。這可能導致意想不到的行為。
- **不可變性**：如果你使用 `let` 定義結構體實例，則不能修改其屬性。你需要使用 `var` 定義可變的實例。
- **初始器**：如果結構體沒有自定義初始器，Swift 會自動生成一個。當你添加自定義初始器時，確保調用所有屬性的初始值。

## 總結
在 Swift 中，`struct` 是一種強大的數據結構，適合用來創建清晰、易於管理的值類型。