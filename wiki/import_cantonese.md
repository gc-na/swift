<!--
Meta Description: # Swift 中的 `import` 指令：導入模組的關鍵 ## 簡介 在 Swift 編程中，`import` 指令用於導入外部模組或框架，使得開發者能夠使用這些模組中定義的功能和資源。 ## 文件說明 `import` 是 Swift 語言中的一個關鍵字，主要用於引入系統庫或自定義模組。通過使...
Meta Keywords: import, swift, modulename, foundation, 導入自定義模組
-->

# Swift 中的 `import` 指令：導入模組的關鍵

## 簡介
在 Swift 編程中，`import` 指令用於導入外部模組或框架，使得開發者能夠使用這些模組中定義的功能和資源。

## 文件說明
`import` 是 Swift 語言中的一個關鍵字，主要用於引入系統庫或自定義模組。通過使用 `import`，開發者可以輕鬆地訪問和使用其他地方定義的類、結構、函數等，從而提高代碼的可重用性和組織性。

### 用法
在 Swift 中使用 `import` 的基本語法如下：

```swift
import ModuleName
```

其中 `ModuleName` 是要導入的模組的名稱。導入後，該模組中的所有公共內容都可以在當前文件中直接使用。

### 詳細說明
- **導入標準庫**：Swift 自帶的標準庫可直接使用，無需顯式導入，但為了可讀性，開發者有時會選擇使用 `import Swift`。
- **導入第三方庫**：使用 CocoaPods、Carthage 或 Swift Package Manager 等工具安裝的第三方庫，必須使用 `import` 來訪問其功能。
- **導入自定義模組**：如果你創建了自己的模組，可以使用 `import` 將其引入到其他文件中。

## 範例
以下是導入模組的基本示例：

```swift
import Foundation // 導入 Foundation 模組

let currentDate = Date() // 使用 Foundation 中的 Date 類
print("當前日期：\(currentDate)")
```

另一個示例是導入自定義模組：

```swift
import MyCustomModule // 導入自定義模組

let instance = MyCustomClass() // 使用自定義類別
```

## 解釋
在使用 `import` 時，有幾個常見的陷阱和注意事項：
- **命名衝突**：如果導入的模組中有與當前命名空間衝突的類名，可以使用命名空間來解決，例如 `ModuleName.ClassName`。
- **冗餘導入**：不需要為每個文件都導入相同的模組，通常可以在需要的地方一次性導入，避免不必要的冗餘。
- **模組的可見性**：只有公共模組中的內容才能被導入，私有或內部的內容將無法訪問。

## 一行總結
`import` 指令在 Swift 中用於導入模組，使得開發者能夠使用其他模組中定義的功能。