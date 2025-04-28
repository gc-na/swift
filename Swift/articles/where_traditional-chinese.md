<!--
Meta Description: # 在 Swift 中的 "where" 關鍵字 ## 摘要 "where" 是 Swift 編程語言中的一個關鍵字，常用於泛型、條件語句和擴展，能夠增加語法的靈活性與表達能力。 ## 文檔 在 Swift 中，"where" 關鍵字的主要作用是用來增加條件以限制泛型類型或協議的使用，並可用於控制流...
Meta Keywords: where, swift, element, func, print
-->

# 在 Swift 中的 "where" 關鍵字

## 摘要
"where" 是 Swift 編程語言中的一個關鍵字，常用於泛型、條件語句和擴展，能夠增加語法的靈活性與表達能力。

## 文檔
在 Swift 中，"where" 關鍵字的主要作用是用來增加條件以限制泛型類型或協議的使用，並可用於控制流程語句的條件判斷。這使得開發者能夠撰寫更清晰、更具表達性的代碼。

### 用途
- **泛型約束**：在定義泛型函數或類別時，可以用 "where" 來指定類型的附加條件。
- **協議擴展**：可以在協議擴展中使用 "where" 來限制協議的適用範圍。
- **控制流**：在 switch 語句中，"where" 可用於添加額外的條件。

### 使用方式
"where" 的基本語法如下：

1. **泛型約束**
   ```swift
   func example<T>(value: T) where T: Equatable {
       // 這裡的 T 必須符合 Equatable 協議
   }
   ```

2. **協議擴展**
   ```swift
   extension Collection where Element: Equatable {
       func contains(element: Element) -> Bool {
           return self.contains { $0 == element }
       }
   }
   ```

3. **控制流**
   ```swift
   let numbers = [1, 2, 3, 4, 5]
   for number in numbers where number % 2 == 0 {
       print(number) // 只會列印偶數
   }
   ```

## 範例
以下是 "where" 在不同情境中的使用範例：

### 泛型約束範例
```swift
func printValue<T>(value: T) where T: CustomStringConvertible {
    print(value.description)
}
```

### 協議擴展範例
```swift
protocol Describable {
    var description: String { get }
}

extension Array where Element: Describable {
    func printDescriptions() {
        for item in self {
            print(item.description)
        }
    }
}
```

### 控制流範例
```swift
let ages = [18, 20, 15, 22]
for age in ages where age >= 18 {
    print("成年: \(age)")
}
```

## 解釋
使用 "where" 時，開發者需注意以下幾點：
- 確保在使用 "where" 時，條件邏輯是正確的，避免造成意料之外的錯誤。
- 在泛型約束中，只能使用 Type 的特性進行條件限制，無法使用實例的特性。
- "where" 只能在特定上下文中使用，對於不適用的場景，編譯器會報錯。

## 一句總結
"where" 是 Swift 中用於增強泛型、協議及控制流條件的強大工具。