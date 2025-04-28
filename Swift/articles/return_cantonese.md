<!--
Meta Description: # Swift 中的「return」關鍵字使用指南 ## 簡介 在 Swift 程式語言中，「return」關鍵字用於從函數或方法中返回值，並結束該函數的執行。這是一個基本但重要的功能，讓開發者能夠有效地管理函數的輸出。 ## 文檔 ### 目的 「return」關鍵字的主要目的是結束當前函數的執行...
Meta Keywords: return, swift, func, int, message
-->

# Swift 中的「return」關鍵字使用指南

## 簡介
在 Swift 程式語言中，「return」關鍵字用於從函數或方法中返回值，並結束該函數的執行。這是一個基本但重要的功能，讓開發者能夠有效地管理函數的輸出。

## 文檔
### 目的
「return」關鍵字的主要目的是結束當前函數的執行並將值傳遞回調用該函數的地方。這對於需要從函數獲取計算結果或狀態的情況非常重要。

### 用法
在 Swift 中，使用「return」的基本語法如下：

```swift
func functionName(parameters) -> ReturnType {
    // 函數邏輯
    return value
}
```

- **functionName**：函數的名稱。
- **parameters**：傳遞給函數的參數。
- **ReturnType**：函數返回值的類型。
- **value**：要返回的值。

### 詳細說明
1. **返回類型**：函數的返回類型必須與「return」語句後的值類型一致。
2. **多個返回語句**：函數內可以有多個「return」語句，根據條件來決定哪一個被執行。
3. **無返回值函數**：若函數不需要返回值，則可以省略返回類型，並使用「return」語句結束函數執行。

## 範例
### 基本用法範例

```swift
func addNumbers(a: Int, b: Int) -> Int {
    return a + b
}

let result = addNumbers(a: 5, b: 7)
print(result)  // 輸出: 12
```

### 無返回值的函數

```swift
func printMessage(message: String) {
    print(message)
    return  // 可以省略
}

printMessage(message: "Hello, Swift!")
```

## 解釋
### 常見陷阱
- **返回類型不匹配**：確保「return」後的值類型與函數聲明的返回類型一致。
- **漏掉返回語句**：如果函數定義為返回某個值，但在所有控制流路徑中都沒有「return」，編譯器將報錯。
- **在閉包中使用**：「return」也可以在閉包中使用，需注意閉包的結束條件。

### 額外注意事項
- 在使用可選類型時，返回的值可能是 nil，這在設計函數時需考慮。
- Swift 的編譯器會自動推斷返回類型，若有明確的返回類型宣告則更佳。

## 一句總結
「return」關鍵字在 Swift 中用於結束函數執行並返回值，是編寫清晰且高效代碼的基本工具。