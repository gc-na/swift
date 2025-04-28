<!--
Meta Description: # Swift 中的 import 指令詳解 ## 概述 `import` 是 Swift 編程語言中的一個關鍵字，用於引入外部模組或框架，以便在程式中使用其定義的功能和類別。這使得開發者可以更方便地利用現有的代碼庫，提升開發效率。 ## 文檔 `import` 指令的主要目的是使得 Swift 程...
Meta Keywords: swift, import, foundation, uikit, testable
-->

# Swift 中的 import 指令詳解

## 概述
`import` 是 Swift 編程語言中的一個關鍵字，用於引入外部模組或框架，以便在程式中使用其定義的功能和類別。這使得開發者可以更方便地利用現有的代碼庫，提升開發效率。

## 文檔
`import` 指令的主要目的是使得 Swift 程式能夠使用其他模組中定義的類別、結構、函式等。當你需要使用某個模組或框架提供的功能時，可以通過 `import` 指令來引入。

### 用法
在 Swift 中，`import` 的基本語法如下：

```swift
import 模組名稱
```

如果需要引入多個模組，可以使用多個 `import` 指令。例如：

```swift
import Foundation
import UIKit
```

### 詳細說明
- **模組**：模組是 Swift 程式碼的組織單位，可以是系統提供的框架或自定義的框架。
- **可選導入**：Swift 允許通過 `@testable import` 指令來導入模組，以便在單元測試中訪問其內部成員。
- **名稱衝突**：如果導入的模組中存在相同名稱的類別或函式，可以使用 `typealias` 或指定模組名稱來避免衝突。

## 範例
以下是一些基本的使用範例：

### 範例 1：導入 Foundation 模組
```swift
import Foundation

let currentDate = Date()
print("今天的日期是：\(currentDate)")
```

### 範例 2：導入 UIKit 模組
```swift
import UIKit

let label = UILabel()
label.text = "Hello, Swift!"
```

### 範例 3：使用 @testable 導入
```swift
@testable import MyFramework

class MyTests: XCTestCase {
    func testExample() {
        let myObject = MyClass()
        XCTAssertEqual(myObject.someMethod(), expectedValue)
    }
}
```

## 說明
在使用 `import` 時，有幾個常見的注意事項：
- **導入順序**：雖然 Swift 允許以任何順序導入模組，但有時候某些模組的依賴關係可能會影響編譯。如果遇到問題，檢查導入的順序可能會有所幫助。
- **性能考量**：每次導入模組時，Swift 會自動處理重複導入，因此即使在多個檔案中導入同一模組也不會影響性能。
- **版本相容**：確保所導入的模組或框架與當前的 Swift 版本相容，否則可能會出現編譯錯誤。

## 一句話總結
`import` 指令在 Swift 中用於引入外部模組或框架，以便使用其定義的功能和類別。