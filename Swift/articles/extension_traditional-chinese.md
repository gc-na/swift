<!--
Meta Description: # Swift 擴展 (Extension)：提升程式碼靈活性與可讀性 ## 概要 Swift 擴展 (Extension) 是一種強大的功能，允許開發者在不修改原始類別、結構或列舉的情況下，為其新增功能。這使得程式碼更加模組化，並提升了可讀性和維護性。 ## 文件說明 擴展讓你能夠： - 為現有的...
Meta Keywords: swift, extension, self, string, int
-->

# Swift 擴展 (Extension)：提升程式碼靈活性與可讀性

## 概要
Swift 擴展 (Extension) 是一種強大的功能，允許開發者在不修改原始類別、結構或列舉的情況下，為其新增功能。這使得程式碼更加模組化，並提升了可讀性和維護性。

## 文件說明
擴展讓你能夠：
- 為現有的類別、結構、列舉或協議新增屬性和方法。
- 遵循協議並實現其要求。
- 提供初始值設定器與其他功能。

### 使用方式
使用擴展的基本語法如下：

```swift
extension 類別名稱 {
    // 新增方法或屬性
}
```

### 目的
擴展的主要目的是讓開發者能夠在不破壞原有代碼的情況下，靈活地為類別和結構添加新功能。

## 範例
### 範例 1：為 Int 類別新增一個計算平方的方法
```swift
extension Int {
    func square() -> Int {
        return self * self
    }
}

let number = 5
print(number.square()) // 輸出: 25
```

### 範例 2：為 String 類別新增一個檢查是否為回文的方法
```swift
extension String {
    func isPalindrome() -> Bool {
        return self == String(self.reversed())
    }
}

let word = "level"
print(word.isPalindrome()) // 輸出: true
```

### 範例 3：遵循協議
```swift
protocol Describable {
    var description: String { get }
}

extension Int: Describable {
    var description: String {
        return "這是一個整數：\(self)"
    }
}

let number = 42
print(number.description) // 輸出: 這是一個整數：42
```

## 解釋
使用擴展時，有幾個常見的注意事項：
- 擴展無法新增存儲屬性，但可以新增計算屬性。
- 擴展可以遵循協議，並實現協議的要求。
- 擴展只能在其定義的範圍內被使用，無法在其他範圍中使用。
- 適當使用擴展可以提高程式碼的可讀性與可維護性，但過度使用可能會使代碼難以追蹤。

## 一句總結
Swift 擴展 (Extension) 是一種靈活的工具，用於為現有類別、結構和協議添加新功能，而無需修改原始代碼。