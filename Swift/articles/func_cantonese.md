<!--
Meta Description: # Swift 中的 `func` 函數定義：用法與範例 ## 概述 `func` 是 Swift 編程語言中用於定義函數的關鍵字。函數是組織代碼的基本單元，能夠接收輸入、執行特定操作並返回結果。 ## 文檔 在 Swift 中，函數的主要目的是封裝可重用的代碼塊，從而提高代碼的可讀性和維護性。使用...
Meta Keywords: swift, func, int, hello, name
-->

# Swift 中的 `func` 函數定義：用法與範例

## 概述
`func` 是 Swift 編程語言中用於定義函數的關鍵字。函數是組織代碼的基本單元，能夠接收輸入、執行特定操作並返回結果。

## 文檔
在 Swift 中，函數的主要目的是封裝可重用的代碼塊，從而提高代碼的可讀性和維護性。使用 `func` 關鍵字可以創建一個函數，該函數可以接收參數並返回一個值。函數的基本語法如下：

```swift
func functionName(parameters) -> ReturnType {
    // 函數體
}
```

- **functionName**：函數的名稱，用於調用該函數。
- **parameters**：可以是一個或多個參數，格式為 `parameterName: Type`。
- **ReturnType**：函數返回值的類型，若不返回值則使用 `Void`。

函數可以在全局範圍內定義，也可以作為類、結構或枚舉的一部分。

## 範例
以下是一些基本的 `func` 使用範例：

### 範例 1：簡單的加法函數
```swift
func addNumbers(a: Int, b: Int) -> Int {
    return a + b
}

let sum = addNumbers(a: 5, b: 3) // sum 會是 8
```

### 範例 2：無返回值的函數
```swift
func printHello() {
    print("Hello, World!")
}

printHello() // 輸出 "Hello, World!"
```

### 範例 3：帶有預設參數的函數
```swift
func greet(name: String, greeting: String = "Hello") {
    print("\(greeting), \(name)!")
}

greet(name: "Alice") // 輸出 "Hello, Alice!"
greet(name: "Bob", greeting: "Hi") // 輸出 "Hi, Bob!"
```

## 解釋
使用 `func` 定義函數時，開發者應注意以下幾點：

1. **參數標籤**：Swift 允許為函數參數指定標籤，增加可讀性。例如：
   ```swift
   func multiply(firstNumber a: Int, secondNumber b: Int) -> Int {
       return a * b
   }
   ```

2. **返回類型**：如果函數不返回任何值，應明確指定返回類型為 `Void` 或省略返回類型。

3. **函數重載**：Swift 允許重載函數，即可以根據參數類型或數量定義多個同名函數。

4. **閉包與函數**：函數是一種特殊類型的閉包，可以作為參數傳遞或返回值。

## 一句總結
`func` 是 Swift 中用於定義函數的關鍵字，能夠封裝代碼，提高代碼的可讀性和可重用性。