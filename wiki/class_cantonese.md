<!--
Meta Description: # Swift 中的 Class：物件導向程式設計的基礎 ## 概述 在 Swift 語言中，`class` 是一個用於定義物件的藍圖，支持物件導向程式設計的特性，如繼承和多型。透過 `class`，開發者可以創建自定義資料類型，並將屬性和方法封裝在一起。 ## 文件 ### 目的 `class` ...
Meta Keywords: class, swift, name, age, propertyname
-->

# Swift 中的 Class：物件導向程式設計的基礎

## 概述
在 Swift 語言中，`class` 是一個用於定義物件的藍圖，支持物件導向程式設計的特性，如繼承和多型。透過 `class`，開發者可以創建自定義資料類型，並將屬性和方法封裝在一起。

## 文件
### 目的
`class` 的主要目的是提供一種方式來定義和使用物件，這些物件可以擁有狀態（屬性）和行為（方法）。這使得程式碼更具可重用性和模組化。

### 用法
在 Swift 中，使用 `class` 關鍵字來定義一個類。以下是 `class` 的基本語法：

```swift
class ClassName {
    // 屬性
    var propertyName: DataType
    
    // 初始化器
    init(propertyName: DataType) {
        self.propertyName = propertyName
    }
    
    // 方法
    func methodName() {
        // 方法實現
    }
}
```

### 詳細內容
- **繼承**：Swift 支持類的繼承，讓一個類可以繼承另一個類的屬性和方法。
- **多型**：透過協議和繼承，可以使用多型來處理不同類型的物件。
- **參考類型**：`class` 物件是參考類型，這意味著兩個變數可以引用同一個物件。
- **解構器**：類可以有解構器（deinitializer）來釋放其資源。

## 範例
以下是使用 `class` 的簡單範例：

```swift
class Dog {
    var name: String
    var age: Int
    
    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
    
    func bark() {
        print("\(name) says: Woof!")
    }
}

let myDog = Dog(name: "Buddy", age: 3)
myDog.bark()  // 輸出: Buddy says: Woof!
```

## 解釋
### 常見陷阱
- **參考類型的行為**：在使用 `class` 時，注意對物件的修改會影響所有引用該物件的變數。
- **未初始化屬性**：所有屬性必須在初始化器中初始化，否則會導致編譯錯誤。
- **避免循環參考**：在使用閉包時，注意循環參考的問題，可能導致記憶體洩漏。

## 一句總結
在 Swift 中，`class` 是用於創建物件的基礎，支持物件導向程式設計特性，如繼承和多型。