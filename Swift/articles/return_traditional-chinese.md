<!--
Meta Description: # Swift 中的 return 關鍵字完整指南 ## 簡介 `return` 是 Swift 程式語言中用來結束函式或閉包執行的重要關鍵字。它不僅可以返回值，也可用於結束函式的執行流。 ## 文檔 在 Swift 中，`return` 關鍵字的主要功能是中止當前函式或閉包的執行並可選擇性地返回一...
Meta Keywords: return, swift, int, func, name
-->

# Swift 中的 return 關鍵字完整指南

## 簡介
`return` 是 Swift 程式語言中用來結束函式或閉包執行的重要關鍵字。它不僅可以返回值，也可用於結束函式的執行流。

## 文檔
在 Swift 中，`return` 關鍵字的主要功能是中止當前函式或閉包的執行並可選擇性地返回一個值。這個關鍵字的使用在函式定義中是必不可少的，特別是當函式需要返回特定類型的值時。

### 用法
- **結束函式執行**：當執行到 `return` 語句時，函式立即停止執行。
- **返回值**：`return` 可以用來返回任何類型的值，這取決於函式的定義。例如，如果一個函式定義為返回整數類型，那麼 `return` 後面必須跟一個整數。

### 詳情
- **無返回值的函式**：如果函式不需要返回任何值，可以省略 `return`，這種情況下函式的返回類型應該是 `Void` 或省略。
- **多重返回**：在某些情況下，可以根據條件使用多個 `return` 語句來返回不同的值。
- **使用在閉包內**：`return` 同樣可以在閉包中使用，以結束閉包的執行並返回結果。

## 範例
### 基本用法示例
```swift
func add(a: Int, b: Int) -> Int {
    return a + b
}

let result = add(a: 5, b: 3) // result 為 8
```

### 無返回值的函式
```swift
func greet(name: String) {
    print("Hello, \(name)!")
}

greet(name: "Alice") // 輸出：Hello, Alice!
```

### 使用多個 return
```swift
func checkEvenOrOdd(number: Int) -> String {
    if number % 2 == 0 {
        return "Even"
    } else {
        return "Odd"
    }
}

let numberType = checkEvenOrOdd(number: 7) // numberType 為 "Odd"
```

## 解釋
在使用 `return` 時，開發者需要注意以下幾點：
- **返回類型匹配**：必須確保 `return` 後的值類型與函式定義的返回類型相符，否則編譯器將報錯。
- **無法在無返回值的函式中使用返回值**：如果函式被定義為不返回值（`Void`），則不應使用 `return` 返回任何值，這將導致錯誤。
- **結束函式執行**：`return` 將會導致整個函式的執行被終止，這意味著 `return` 後的所有代碼將不會被執行。

## 一句總結
`return` 是 Swift 中用於結束函式或閉包執行並可選擇性返回值的關鍵字。