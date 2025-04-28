<!--
Meta Description: # Swift 中的 deinit：自定義類別的解構器 ## 簡介 `deinit` 是 Swift 編程語言中的一個特殊方法，用來在類別實例被釋放前執行清理操作。它對於管理資源和避免內存洩漏至關重要。 ## 文檔 ### 目的 `deinit` 方法在類別實例的生命周期結束時自動調用。此方法可用於...
Meta Keywords: deinit, resource, swift, init, print
-->

# Swift 中的 deinit：自定義類別的解構器

## 簡介
`deinit` 是 Swift 編程語言中的一個特殊方法，用來在類別實例被釋放前執行清理操作。它對於管理資源和避免內存洩漏至關重要。

## 文檔
### 目的
`deinit` 方法在類別實例的生命周期結束時自動調用。此方法可用於釋放資源、保存狀態或進行必要的清理工作。

### 使用
`deinit` 方法不接受任何參數，且沒有返回值。每個類別只能有一個 `deinit` 方法，並且在類別的實例被釋放時自動調用。它與 `init` 方法相對應，無需顯式調用。

### 詳細說明
- **自動調用**：當一個類別的實例被釋放時，`deinit` 會自動被調用。不需要手動調用。
- **資源釋放**：適合釋放文件、網絡連接或其他系統資源。
- **單一性**：每個類別只能定義一個 `deinit` 方法。

## 示例
```swift
class Resource {
    init() {
        print("Resource is initialized")
    }

    deinit {
        print("Resource is being deinitialized")
    }
}

var resource: Resource? = Resource() // 輸出: Resource is initialized
resource = nil // 輸出: Resource is being deinitialized
```

## 解釋
- **常見陷阱**：如果一個類別的實例仍然被引用，則 `deinit` 不會被調用，這可能導致資源未被釋放，從而造成內存洩漏。
- **循環引用**：在使用閉包時，注意循環引用的情況。使用 `weak` 或 `unowned` 關鍵字可以避免這個問題。
- **多重引用**：確保沒有其他強引用保留對象，否則 `deinit` 不會被調用。

## 一句總結
`deinit` 是 Swift 中用於釋放資源和進行清理操作的重要方法，確保類別實例在不再需要時正確地被清理。