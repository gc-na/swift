<!--
Meta Description: # Swift 協議 (Protocol) 的詳盡介紹 ## 摘要 在 Swift 中，協議是一種藉由定義方法和屬性來描述特定工作或任務的藍圖。協議可以被類別、結構體和列舉遵循，從而實現多態性。 ## 文檔 ### 目的 協議的主要目的是為了定義一組必須實現的功能，這使得不同類別或結構體能夠以相同的...
Meta Keywords: name, swift, func, protocol, string
-->

# Swift 協議 (Protocol) 的詳盡介紹

## 摘要
在 Swift 中，協議是一種藉由定義方法和屬性來描述特定工作或任務的藍圖。協議可以被類別、結構體和列舉遵循，從而實現多態性。

## 文檔
### 目的
協議的主要目的是為了定義一組必須實現的功能，這使得不同類別或結構體能夠以相同的方式互動。協議提供了一種靈活的方式來設計可重用的程式碼架構。

### 使用方式
在 Swift 中，定義協議使用 `protocol` 關鍵字，後面接協議名稱。協議可以包含方法、屬性和其他協議。

**定義協議範例：**
```swift
protocol Vehicle {
    var numberOfWheels: Int { get }
    func startEngine()
}
```

### 詳細說明
- **遵循協議**：類別、結構體或列舉可以遵循協議，並必須實現協議中定義的方法和屬性。
- **協議的繼承**：協議可以繼承其他協議，這樣可以建立更複雜的協議層次結構。
- **選擇性要求**：使用 `@objc` 標記的協議可以定義選擇性要求，這些要求不必被遵循。

## 範例
### 基本使用示例
以下是如何定義和遵循協議的範例：

```swift
protocol Animal {
    var name: String { get }
    func makeSound()
}

class Dog: Animal {
    var name: String
    
    init(name: String) {
        self.name = name
    }
    
    func makeSound() {
        print("Woof!")
    }
}

let myDog = Dog(name: "Buddy")
print("\(myDog.name) says: ", terminator: "")
myDog.makeSound()
```

### 協議繼承示例
```swift
protocol Pet: Animal {
    func play()
}

class Cat: Pet {
    var name: String
    
    init(name: String) {
        self.name = name
    }
    
    func makeSound() {
        print("Meow!")
    }
    
    func play() {
        print("\(name) is playing.")
    }
}

let myCat = Cat(name: "Whiskers")
myCat.makeSound()
myCat.play()
```

## 解釋
### 常見陷阱
- **未實現要求**：當一個類別或結構體聲明遵循某個協議時，如果未實現協議中的所有要求，會導致編譯錯誤。
- **協議與擴展**：協議可以通過擴展添加默認實現，這樣遵循協議的類別或結構體就不必實現所有方法。

### 附加說明
協議在 Swift 中是實現多型和解耦合的重要工具，適當使用協議可以提高程式碼的可讀性和可維護性。

## 一句總結
Swift 的協議是一種強大的功能，能夠為多樣化的類別和結構體提供統一的接口和行為。