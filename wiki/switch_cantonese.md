<!--
Meta Description: # Swift 中的 Switch 語句：完整指南 ## 概述 `switch` 語句是 Swift 中的一種控制結構，允許根據不同的條件選擇執行的代碼塊。它提供了一種簡潔且可讀性強的方式來處理多種情況的分支邏輯。 ## 文檔 `switch` 語句的主要目的是替代長串的 `if-else` 語句，...
Meta Keywords: case, switch, print, swift, default
-->

# Swift 中的 Switch 語句：完整指南

## 概述
`switch` 語句是 Swift 中的一種控制結構，允許根據不同的條件選擇執行的代碼塊。它提供了一種簡潔且可讀性強的方式來處理多種情況的分支邏輯。

## 文檔
`switch` 語句的主要目的是替代長串的 `if-else` 語句，使代碼更易於維護和理解。`switch` 可以檢查變量或常量的值，並根據匹配結果執行相應的代碼。

### 語法
```swift
switch <expression> {
case <pattern1>:
    // 執行語句
case <pattern2>:
    // 執行語句
default:
    // 預設執行語句
}
```

### 目的與使用
- **多條件判斷**：`switch` 允許你對一個變量進行多種可能值的判斷。
- **可擴展性**：你可以輕易添加更多的 `case`，使得代碼更具可擴展性。
- **強類型檢查**：Swift 的 `switch` 提供了強類型檢查，確保所有可能的值都被處理。

## 示例
### 基本使用示例
```swift
let number = 3

switch number {
case 1:
    print("一")
case 2:
    print("二")
case 3:
    print("三")
default:
    print("其他")
}
```
輸出：
```
三
```

### 使用元組
```swift
let point = (2, 0)

switch point {
case (0, 0):
    print("在原點")
case (_, 0):
    print("在 x 軸上")
case (0, _):
    print("在 y 軸上")
case (-2...2, -2...2):
    print("在方格內")
default:
    print("在方格外")
}
```
輸出：
```
在 x 軸上
```

## 解釋
在使用 `switch` 語句時，有幾個常見的陷阱需要注意：
- **缺少 default**：如果沒有提供 `default` 情況，並且沒有涵蓋所有可能的值，則編譯器會報錯。
- **無法使用重複的 case**：每個 `case` 樣式必須是唯一的，不能有重複的條件。
- **fallthrough**：Swift 的 `switch` 不會自動“瀕臨”到下一個 `case`，如果需要這樣做，必須顯式使用 `fallthrough` 關鍵字。

## 一句總結
Swift 中的 `switch` 語句是一個強大而靈活的控制結構，能夠根據多種條件優雅地選擇執行的代碼。