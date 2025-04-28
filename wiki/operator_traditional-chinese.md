<!--
Meta Description: # Swift中的運算符：使用與範例 ## 摘要 在Swift編程語言中，運算符是一種特殊的符號，用於執行特定的數學或邏輯操作。Swift提供了多種內建運算符，包括算術運算符、比較運算符、邏輯運算符等，讓開發者可以簡潔地表達計算和邏輯關係。 ## 文檔 運算符在Swift中扮演著重要的角色，能夠幫助...
Meta Keywords: let, swift, false, int, 比較運算符
-->

# Swift中的運算符：使用與範例

## 摘要
在Swift編程語言中，運算符是一種特殊的符號，用於執行特定的數學或邏輯操作。Swift提供了多種內建運算符，包括算術運算符、比較運算符、邏輯運算符等，讓開發者可以簡潔地表達計算和邏輯關係。

## 文檔
運算符在Swift中扮演著重要的角色，能夠幫助開發者對變量和常量進行數據操作。Swift支持多種類型的運算符：

1. **算術運算符**：包括加法 (`+`)、減法 (`-`)、乘法 (`*`)、除法 (`/`) 和取餘 (`%`)。
2. **比較運算符**：用於比較兩個值，例如相等 (`==`)、不相等 (`!=`)、大於 (`>`)、小於 (`<`) 等。
3. **邏輯運算符**：用於處理布林值，包括邏輯與 (`&&`)、邏輯或 (`||`) 以及邏輯非 (`!`)。
4. **位元運算符**：用於對整數進行位元運算，如 AND (`&`)、OR (`|`)、NOT (`~`)。
5. **範圍運算符**：用於創建範圍，包括閉合範圍運算符 (`...`) 和開放範圍運算符 (`..<`)。
6. **自定義運算符**：開發者可以根據需要定義自己的運算符，並指定其行為。

使用運算符時，開發者應了解其優先級和結合性，以正確地執行運算。

## 範例
以下是Swift中運算符的基本用法示例：

### 算術運算符
```swift
let a = 10
let b = 5
let sum = a + b        // 結果：15
let difference = a - b // 結果：5
let product = a * b    // 結果：50
let quotient = a / b   // 結果：2
let remainder = a % b  // 結果：0
```

### 比較運算符
```swift
let x = 10
let y = 20
let isEqual = x == y        // 結果：false
let isGreater = x > y       // 結果：false
let isLessOrEqual = x <= y  // 結果：true
```

### 邏輯運算符
```swift
let isTrue = true
let isFalse = false
let andResult = isTrue && isFalse // 結果：false
let orResult = isTrue || isFalse   // 結果：true
```

### 自定義運算符
```swift
infix operator ** : MultiplicationPrecedence

func **(base: Int, exponent: Int) -> Int {
    return Int(pow(Double(base), Double(exponent)))
}

let powerResult = 2 ** 3  // 結果：8
```

## 解釋
在使用運算符時，有幾個常見的陷阱需要注意：

1. **運算符優先級**：不同運算符之間的優先級會影響運算的結果，開發者應該清楚運算符的優先級規則。
2. **類型不匹配**：運算符要求操作數是相同類型，否則會導致編譯錯誤。
3. **自定義運算符的使用**：自定義運算符需要正確設置優先級和結合性，否則可能會導致難以預測的行為。

## 一句總結
運算符是Swift編程語言中執行數學和邏輯操作的基礎工具，開發者可利用多種內建和自定義運算符來簡化代碼表達。