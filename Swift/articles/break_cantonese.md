<!--
Meta Description: # Swift 中的 "break" 語句：控制流程的關鍵字 ## 摘要 在 Swift 語言中，`break` 是一個用來終止循環、條件語句或 switch 語句的控制流程關鍵字。它能夠簡化代碼結構，提升可讀性。 ## 文檔 ### 目的 `break` 的主要目的是立即停止當前的控制結構（如 f...
Meta Keywords: break, switch, case, swift, print
-->

# Swift 中的 "break" 語句：控制流程的關鍵字

## 摘要
在 Swift 語言中，`break` 是一個用來終止循環、條件語句或 switch 語句的控制流程關鍵字。它能夠簡化代碼結構，提升可讀性。

## 文檔
### 目的
`break` 的主要目的是立即停止當前的控制結構（如 for 循環、while 循環、switch 語句），並跳出到該控制結構的外層代碼。這在需要根據特定條件提前終止執行時非常有用。

### 用法
`break` 關鍵字可以在以下幾種情況下使用：
1. **循環結構**：在 for、while 或 repeat-while 循環中，當滿足特定條件時，可以使用 `break` 來提前結束循環。
2. **switch 語句**：在 switch 語句中，`break` 用來防止執行到下一個 case。

### 詳細說明
- 使用 `break` 關鍵字時，必須確保它位於控制結構的內部。
- 在 switch 語句中，若不使用 `break`，則會導致 "fall-through" 行為，即執行接下來的 case。

## 範例
### 循環結構中的使用
```swift
for i in 1...10 {
    if i == 5 {
        break
    }
    print(i)
}
// 輸出：1 2 3 4
```

### switch 語句中的使用
```swift
let number = 3
switch number {
case 1:
    print("一")
case 2:
    print("二")
case 3:
    print("三")
    break
default:
    print("其他")
}
// 輸出：三
```

## 解釋
- **常見問題**：初學者可能會忘記在 switch 語句的 case 中添加 `break`，這會導致不必要的代碼執行。
- **注意事項**：在 Swift 中，switch 語句預設是非 fall-through 的，這意味著每個 case 會自動結束，除非使用 `fallthrough` 關鍵字。

## 一行總結
`break` 是 Swift 中一個強大的控制流程關鍵字，用於提前終止循環或 switch 語句。