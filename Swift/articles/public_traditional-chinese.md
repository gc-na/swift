<!--
Meta Description: # Swift 中的 "public" 存取修飾符 ## 摘要 在 Swift 中，`public` 是一種存取修飾符，用於定義類別、結構、協議、方法及屬性的可見性，允許它們在模組外部被訪問和使用。 ## 文檔 `public` 存取修飾符的主要目的是讓開發者能夠控制其代碼的可見性和訪問權限。當一個...
Meta Keywords: public, swift, int, var, self
-->

# Swift 中的 "public" 存取修飾符

## 摘要
在 Swift 中，`public` 是一種存取修飾符，用於定義類別、結構、協議、方法及屬性的可見性，允許它們在模組外部被訪問和使用。

## 文檔
`public` 存取修飾符的主要目的是讓開發者能夠控制其代碼的可見性和訪問權限。當一個類別或方法被標記為 `public` 時，這意味著它可以被其他模組自由訪問。這對於構建庫或框架時非常重要，因為它使得開發者能夠提供 API 給其他開發者使用。

### 使用方法
在 Swift 中，將 `public` 放在類別、結構、協議、方法或屬性前面，即可將其設置為公有。以下是基本語法：

```swift
public class MyClass {
    public var myProperty: Int
    public init(property: Int) {
        self.myProperty = property
    }
    
    public func myMethod() {
        // 方法實現
    }
}
```

以上代碼中，`MyClass`、`myProperty` 和 `myMethod` 都是公有的，這意味著它們可以被其他模組調用。

## 範例
以下是一些使用 `public` 的基本範例：

### 範例 1: 公有類別
```swift
public class Animal {
    public var name: String
    
    public init(name: String) {
        self.name = name
    }
    
    public func speak() {
        print("Animal speaks")
    }
}
```

### 範例 2: 公有結構
```swift
public struct Point {
    public var x: Int
    public var y: Int
    
    public init(x: Int, y: Int) {
        self.x = x
        self.y = y
    }
}
```

## 解釋
使用 `public` 時需要注意以下幾點：

1. **兼容性**：`public` 方法和屬性必須提供完全的實現，因為它們在模組外部被訪問時，無法有未實現的部分。
2. **模組限制**：`public` 的可見性只限於模組的邊界，另一個模組需要導入當前模組才能使用 `public` 成員。
3. **對比其他存取修飾符**：與 `internal`（預設）和 `private` 相比，`public` 允許更廣泛的訪問權限。

## 單行摘要
`public` 存取修飾符使得 Swift 中的類別、結構和方法可在模組外部訪問，是構建可重用代碼的關鍵。