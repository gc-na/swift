<!--
Meta Description: # Swift 中的 `case` 語句：用於模式匹配的強大工具 ## 概述 在 Swift 編程語言中，`case` 語句主要用於 `switch` 語句中，提供了一種強大而靈活的方式來進行模式匹配。這使得開發者能夠根據不同的條件執行不同的代碼塊，從而提高程式的可讀性和可維護性。 ## 文檔 `c...
Meta Keywords: case, print, swift, switch, default
-->

# Swift 中的 `case` 語句：用於模式匹配的強大工具

## 概述
在 Swift 編程語言中，`case` 語句主要用於 `switch` 語句中，提供了一種強大而靈活的方式來進行模式匹配。這使得開發者能夠根據不同的條件執行不同的代碼塊，從而提高程式的可讀性和可維護性。

## 文檔
`case` 是 Swift 中 `switch` 語句的組成部分，允許開發者根據特定的值或模式來分支執行的代碼。`case` 語句可以匹配各種數據類型，包括整數、字串和枚舉等。這種語法結構不僅簡化了代碼，還增加了程式的表達力。

### 使用方式
`case` 語句的基本語法如下：

```swift
switch value {
case pattern1:
    // 執行的代碼
case pattern2:
    // 執行的代碼
default:
    // 如果沒有匹配到任何模式，執行的代碼
}
```

- **value**：要檢查的變數或常數。
- **pattern**：要匹配的模式，可以是常數、範圍或類型匹配。
- **default**：可選的，當沒有任何 `case` 匹配時執行的代碼塊。

## 範例
### 基本範例
以下是一個簡單的 `case` 使用範例：

```swift
let number = 2

switch number {
case 1:
    print("數字是 1")
case 2:
    print("數字是 2")
case 3:
    print("數字是 3")
default:
    print("數字不在 1 到 3 之間")
}
```

在這個範例中，變數 `number` 的值是 2，因此將輸出 "數字是 2"。

### 枚舉範例
`case` 語句也可以用於枚舉的匹配：

```swift
enum Direction {
    case north, south, east, west
}

let currentDirection = Direction.east

switch currentDirection {
case .north:
    print("朝北")
case .south:
    print("朝南")
case .east:
    print("朝東")
case .west:
    print("朝西")
}
```

在這個範例中，根據 `currentDirection` 的值，將輸出 "朝東"。

## 解釋
在使用 `case` 語句時，開發者應注意以下幾點：

1. **缺省情況**：如果所有 `case` 都沒有匹配到，並且沒有提供 `default`，則編譯器會報錯，因此建議在 `switch` 語句中總是包含一個 `default`。
2. **多重匹配**：可以將多個模式放在同一個 `case` 中，使用逗號分隔。例如：
   ```swift
   switch number {
   case 1, 2, 3:
       print("數字在 1 到 3 之間")
   default:
       print("數字不在範圍內")
   }
   ```
3. **範圍匹配**：可以使用範圍來匹配數字。例如：
   ```swift
   switch number {
   case 1...5:
       print("數字在 1 到 5 之間")
   default:
       print("數字不在範圍內")
   }
   ```

## 一句總結
`case` 語句在 Swift 中是模式匹配的核心工具，能夠根據不同條件執行相應的代碼。