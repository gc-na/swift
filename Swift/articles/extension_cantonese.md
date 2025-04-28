<!--
Meta Description: # Swift 擴展 (Extension) 教程：提升你的 Swift 編程技巧 ## 概要 在 Swift 中，擴展（Extension）是一種強大的功能，它允許您為現有的類別、結構體、列舉或協議添加新功能，而不需要修改原始代碼。這使得代碼更加模組化和可重用。 ## 文檔 擴展的主要目的在於擴展...
Meta Keywords: swift, extension, self, int, 結構體
-->

# Swift 擴展 (Extension) 教程：提升你的 Swift 編程技巧

## 概要
在 Swift 中，擴展（Extension）是一種強大的功能，它允許您為現有的類別、結構體、列舉或協議添加新功能，而不需要修改原始代碼。這使得代碼更加模組化和可重用。

## 文檔
擴展的主要目的在於擴展現有類型的功能。您可以使用擴展來添加計算屬性、方法、初始化器、下標以及遵循協議。這在 Swift 中提供了靈活性，讓開發者能夠在不改變類型本身的情況下進行擴展。

### 用法
使用擴展的基本語法如下：

```swift
extension TypeName {
    // 添加計算屬性
    var newProperty: PropertyType {
        // 計算屬性的實現
    }

    // 添加方法
    func newMethod() {
        // 方法的實現
    }
}
```

### 詳情
- 擴展可以用於任何類型，包括類別、結構體、列舉和協議。
- 擴展不能添加存儲屬性，只能添加計算屬性。
- 擴展可以添加新的初始化器，但不能添加指定的初始化器。
- 可以為協議擴展提供默認實現，這樣遵循該協議的類別或結構體就能獲得這些默認功能。

## 範例
### 基本用法示例

以下是一個為 `Int` 類型添加擴展的例子：

```swift
extension Int {
    func squared() -> Int {
        return self * self
    }
}

let number = 5
print(number.squared()) // 輸出: 25
```

### 添加計算屬性示例

```swift
extension String {
    var isPalindrome: Bool {
        return self == String(self.reversed())
    }
}

let word = "madam"
print(word.isPalindrome) // 輸出: true
```

## 解釋
在使用擴展時，開發者應注意以下幾點：
- 擴展無法覆蓋原有類型的功能。您無法在擴展中修改或刪除現有的方法或屬性。
- 擴展的名稱必須是唯一的，不能與現有的類型或協議名稱衝突。
- 使用擴展時，若要添加新的初始化器，需確保不會干擾到現有初始化器的行為。

## 總結
擴展（Extension）是 Swift 中一個強大且靈活的特性，允許開發者在不更改原始類型的情況下，為其添加新功能，從而提升代碼的可讀性和可重用性。