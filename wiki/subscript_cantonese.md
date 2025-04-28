<!--
Meta Description: # Swift 中的下標 (Subscript) 用法詳解 ## 簡介 在 Swift 程式語言中，下標是一種簡潔的語法，用來訪問集合、序列或其他類型的元素。下標的使用能夠提高程式碼的可讀性並簡化數據的存取。 ## 文檔 下標（Subscript）是 Swift 提供的一種語法結構，允許對集合、數組...
Meta Keywords: swift, columns, int, rows, matrix
-->

# Swift 中的下標 (Subscript) 用法詳解

## 簡介
在 Swift 程式語言中，下標是一種簡潔的語法，用來訪問集合、序列或其他類型的元素。下標的使用能夠提高程式碼的可讀性並簡化數據的存取。

## 文檔
下標（Subscript）是 Swift 提供的一種語法結構，允許對集合、數組或自定義類型的元素進行快速訪問。與方法不同，下標的語法更為簡潔，使用中括號來指定索引。下標可以用來讀取和修改元素。

### 目的
下標的主要目的是為了提供一種方便的方式來訪問對象中的特定值，而不需要使用傳統的函數調用方式。

### 使用方式
在 Swift 中可以為類、結構和列舉定義下標。下標的基本語法如下：

```swift
subscript(index: Int) -> ElementType {
    get {
        // 返回指定索引的元素
    }
    set(newValue) {
        // 設置指定索引的元素
    }
}
```

### 詳細說明
- **索引類型**：下標的索引可以是任何類型，可以是整數、字符串或其他類型。
- **返回類型**：下標可以返回任何類型的數據。
- **可讀可寫**：下標可以是只讀的（只有 get），也可以是可讀可寫的（有 get 和 set）。
  
## 示例
以下是一些基本的下標用法示例：

### 示例 1：數組下標
```swift
var numbers = [10, 20, 30, 40]
let firstNumber = numbers[0]  // 取得第一個元素
numbers[1] = 25                // 修改第二個元素
```

### 示例 2：自定義類型下標
```swift
struct Matrix {
    let rows: Int, columns: Int
    var grid: [Double]

    init(rows: Int, columns: Int) {
        self.rows = rows
        self.columns = columns
        grid = Array(repeating: 0.0, count: rows * columns)
    }

    subscript(row: Int, column: Int) -> Double {
        get {
            return grid[(row * columns) + column]
        }
        set {
            grid[(row * columns) + column] = newValue
        }
    }
}

var matrix = Matrix(rows: 2, columns: 2)
matrix[0, 1] = 3.0  // 設置第一行第二列的值
let value = matrix[0, 1]  // 取得該值
```

## 解釋
使用下標時，開發者應注意以下幾點：
- **索引越界**：訪問不在範圍內的索引會引發運行時錯誤，建議在使用下標前檢查索引的有效性。
- **性能考量**：在頻繁訪問的情況下，確保下標的實現效率，特別是在自定義類型中。
- **可讀性**：雖然下標能提高簡潔性，但過度使用可能會降低代碼的可讀性，應適度使用。

## 一句總結
下標是 Swift 中一種方便的數據訪問方式，能夠簡化對集合和自定義類型元素的讀取和修改。