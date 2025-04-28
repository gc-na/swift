<!--
Meta Description: # Swift 中的 Switch 語句：全面指南和範例 ## 摘要 在 Swift 中，`switch` 語句是一種強大的控制流語句，能夠根據變數的值執行不同的程式碼區塊。它支援多種資料型別的匹配，提供了比傳統的 `if-else` 結構更為清晰和高效的選擇方式。 ## 文檔 ### 目的 `sw...
Meta Keywords: case, switch, print, swift, default
-->

# Swift 中的 Switch 語句：全面指南和範例

## 摘要
在 Swift 中，`switch` 語句是一種強大的控制流語句，能夠根據變數的值執行不同的程式碼區塊。它支援多種資料型別的匹配，提供了比傳統的 `if-else` 結構更為清晰和高效的選擇方式。

## 文檔
### 目的
`switch` 語句的主要目的是根據特定表達式的值來決定執行哪一段程式碼。這使得代碼更加簡潔易讀，尤其是在處理多個條件時。

### 使用方法
`switch` 語句的基本語法如下：

```swift
switch expression {
case pattern1:
    // 執行的程式碼
case pattern2:
    // 執行的程式碼
default:
    // 當所有模式都不匹配時執行的程式碼
}
```

- `expression` 是要進行匹配的變數或常量。
- 每個 `case` 後面接著的 `pattern` 定義了匹配的條件。
- `default` 是可選的，用於處理所有未匹配的情況。

### 詳細說明
- `switch` 語句自動處理了許多邊界條件，並且每個 `case` 標籤後都需要有一個 `break`，這意味著每個 `case` 是獨立的。
- `switch` 支援多種資料型別，包括整數、字符、字符串，甚至是元組和資料類型匹配。
- 使用 `fallthrough` 關鍵字可以讓控制流直接跳到下一個 `case`，但需謹慎使用，因為這可能會造成邏輯混淆。

## 範例
### 基本用法
以下是使用 `switch` 語句的基本範例：

```swift
let number = 3

switch number {
case 1:
    print("數字是一")
case 2:
    print("數字是二")
case 3:
    print("數字是三")
default:
    print("數字不在範圍內")
}
```

### 使用元組
`switch` 還可以用於元組的匹配：

```swift
let point = (1, 1)

switch point {
case (0, 0):
    print("在原點")
case (1, 1):
    print("在 (1, 1)")
case (-1, -1):
    print("在 (-1, -1)")
default:
    print("在其他位置")
}
```

## 說明
### 常見陷阱
- `switch` 語句中的每個 `case` 都必須是唯一的，否則編譯器將會報錯。
- 如果使用 `fallthrough`，需要確認後續 `case` 的邏輯是正確的，否則可能會導致意外行為。
- 使用 `default` 是一種良好的習慣，能夠處理未預見的情況，避免程序崩潰。

## 一句總結
Swift 的 `switch` 語句是一種靈活且強大的條件控制工具，能夠根據變數的值執行相應的程式碼。