<!--
Meta Description: # Swift 中的枚舉 (enum): 使用指南與範例 ## 概述 在 Swift 中，枚舉（enum）是一種強大的數據類型，用於定義一組相關的值。它不僅可以用來表示簡單的類型，還能夠包含方法和計算屬性，進一步提升代碼的可讀性和可維護性。 ## 文檔 枚舉在 Swift 中的主要目的是將一組相關的...
Meta Keywords: case, swift, let, int, enum
-->

# Swift 中的枚舉 (enum): 使用指南與範例

## 概述
在 Swift 中，枚舉（enum）是一種強大的數據類型，用於定義一組相關的值。它不僅可以用來表示簡單的類型，還能夠包含方法和計算屬性，進一步提升代碼的可讀性和可維護性。

## 文檔
枚舉在 Swift 中的主要目的是將一組相關的常量組織在一起。與其他編程語言中的枚舉相比，Swift 的枚舉更加靈活，可以具有關聯值和方法。這使得它們能夠更好地表達意圖，並提高代碼的清晰度。

### 用法
使用 `enum` 關鍵字來定義枚舉。每個枚舉的成員稱為「案例」（case），可以簡單地是一組值，也可以包含關聯值。

### 主要特性
- **關聯值**：可以在枚舉的每個案例中附加額外的信息。
- **方法**：枚舉可以擁有方法，這些方法可以操作枚舉的數據。
- **遵循協議**：枚舉可以遵循協議，這使得它們可以用於多種上下文。

## 範例
### 基本用法
以下是定義和使用枚舉的基本範例：

```swift
enum Direction {
    case north
    case south
    case east
    case west
}

let currentDirection = Direction.north
```

### 帶有關聯值的枚舉
```swift
enum HTTPStatus {
    case success(code: Int)
    case failure(code: Int, message: String)
}

let response = HTTPStatus.success(code: 200)
```

### 使用方法的枚舉
```swift
enum Calculator {
    case add(Int, Int)
    case subtract(Int, Int)

    func compute() -> Int {
        switch self {
        case .add(let a, let b):
            return a + b
        case .subtract(let a, let b):
            return a - b
        }
    }
}

let operation = Calculator.add(5, 3)
let result = operation.compute() // result = 8
```

## 解釋
在使用枚舉時，常見的陷阱包括：
- 忘記使用 `switch` 語句處理所有案例，這會導致編譯錯誤。
- 對於帶有關聯值的案例，必須在使用時提供所有必要的參數。
- 如果沒有為所有情況提供處理，編譯器將報錯，因此使用 `default` 案例時需要謹慎。

## 一行總結
Swift 的枚舉是一個靈活且功能強大的工具，用於組織相關的數據和邏輯。