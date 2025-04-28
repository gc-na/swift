<!--
Meta Description: # Swift 的下標（Subscript）：用於數據訪問的強大工具 ## 簡介 在 Swift 中，下標（Subscript）是一種便捷的語法，允許你通過特定的索引或鍵來訪問集合、數組或自定義類型的元素。下標提供了一種簡潔直觀的方式來讀取和修改數據結構中的值。 ## 文檔 下標是一種特殊的語法，允...
Meta Keywords: columns, int, swift, rows, array
-->

# Swift 的下標（Subscript）：用於數據訪問的強大工具

## 簡介
在 Swift 中，下標（Subscript）是一種便捷的語法，允許你通過特定的索引或鍵來訪問集合、數組或自定義類型的元素。下標提供了一種簡潔直觀的方式來讀取和修改數據結構中的值。

## 文檔
下標是一種特殊的語法，允許你用更簡單的方式來訪問數據結構中的元素。你可以在類、結構或枚舉中定義下標，並為它們指定索引或鍵的類型。下標可以是讀取型（getter）或寫入型（setter），也可以同時包含兩者。

### 目的
下標主要用於方便地訪問和修改數據結構中的元素，增加了代碼的可讀性和可維護性。

### 使用方式
一個下標可以這樣定義：

```swift
subscript(index: Int) -> Type {
    get {
        // 返回指定索引的元素
    }
    set(newValue) {
        // 設定指定索引的元素
    }
}
```

### 詳細說明
- **定義**：下標的定義可以在類、結構或枚舉內部進行。
- **索引類型**：下標的索引類型可以是任何類型，包括基本類型、自定義類型、甚至是元組。
- **返回類型**：可以根據需求定義返回的數據類型。
- **多個下標**：一個類或結構可以定義多個下標，這些下標可以有不同的索引類型。
- **使用範例**：下標在數組、字典和自定義類型中的應用非常廣泛。

## 範例
以下是使用下標的基本範例：

### 數組的下標
```swift
var array = [10, 20, 30]
print(array[0]) // 輸出: 10
array[1] = 25
print(array[1]) // 輸出: 25
```

### 自定義類型的下標
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
matrix[0, 1] = 1.1
print(matrix[0, 1]) // 輸出: 1.1
```

## 解釋
使用下標時，開發者需要注意以下幾點：
- **索引範圍**：確保索引不超出數據結構的範圍，否則會引發運行時錯誤。
- **性能考量**：對於大型數據結構，過多的計算可能會影響性能，應合理使用下標。
- **可讀性**：儘管下標提高了代碼的可讀性，但過度使用或不當使用下標可能會導致代碼可讀性下降。

## 一句話總結
Swift 的下標為數據結構提供了一種方便、直觀的訪問和修改方式。