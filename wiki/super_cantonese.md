<!--
Meta Description: # Swift 中的 "super" 關鍵字：用法與示例 ## 摘要 在 Swift 編程語言中，`super` 是一個關鍵字，用於訪問父類中的方法、屬性和初始化器，特別是在子類中覆蓋父類的功能時。 ## 文檔 `super` 關鍵字的主要目的是允許子類別直接訪問其父類別的成員。當你在子類中覆蓋父類...
Meta Keywords: super, speak, swift, animal, dog
-->

# Swift 中的 "super" 關鍵字：用法與示例

## 摘要
在 Swift 編程語言中，`super` 是一個關鍵字，用於訪問父類中的方法、屬性和初始化器，特別是在子類中覆蓋父類的功能時。

## 文檔
`super` 關鍵字的主要目的是允許子類別直接訪問其父類別的成員。當你在子類中覆蓋父類的方法或屬性時，可以使用 `super` 來調用父類的實現，以確保父類的邏輯和功能不會被完全忽略。

### 用法
- 在方法中使用 `super` 來調用父類的方法。
- 在屬性中使用 `super` 來獲取父類的屬性值。
- 在初始化器中使用 `super` 來調用父類的初始化器。

使用 `super` 的基本語法是：

```swift
super.methodName()
```

其中 `methodName` 是你希望從父類中調用的方法。

## 示例
以下是 `super` 的基本用法示例：

```swift
class Animal {
    func speak() {
        print("Animal sound")
    }
}

class Dog: Animal {
    override func speak() {
        super.speak() // 調用父類的 speak 方法
        print("Bark")
    }
}

let myDog = Dog()
myDog.speak()
// 輸出：
// Animal sound
// Bark
```

在這個例子中，`Dog` 類重寫了 `speak` 方法，並在方法內部使用 `super.speak()` 來調用 `Animal` 類的 `speak` 方法。

## 解釋
使用 `super` 時需要注意以下幾點：

1. **方法重寫**：確保子類的方法正確地使用 `override` 關鍵字來重寫父類的方法。
2. **初始化器**：當你定義自訂的初始化器時，必須在初始化器內部調用 `super.init()`，以確保父類的初始化邏輯可以正確執行。
3. **可選鏈接**：在使用 `super` 訪問屬性時，需確保該屬性在父類中正確定義，否則會導致編譯錯誤。

## 一句總結
在 Swift 中，`super` 關鍵字用於子類中訪問父類的成員，確保父類的邏輯和功能可被正確調用。