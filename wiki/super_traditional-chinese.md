<!--
Meta Description: # Swift 中的「super」關鍵字：用法與詳細說明 ## 摘要 在 Swift 中，「super」關鍵字用於引用父類別的方法、屬性和初始化器。這對於繼承和方法重寫時的功能擴展至關重要。 ## 文件說明 在物件導向編程中，繼承是一個重要的概念。當一個類別從另一個類別繼承時，子類別可以使用父類別的...
Meta Keywords: super, wheels, swift, class, dog
-->

# Swift 中的「super」關鍵字：用法與詳細說明

## 摘要
在 Swift 中，「super」關鍵字用於引用父類別的方法、屬性和初始化器。這對於繼承和方法重寫時的功能擴展至關重要。

## 文件說明
在物件導向編程中，繼承是一個重要的概念。當一個類別從另一個類別繼承時，子類別可以使用父類別的屬性和方法。這時，「super」關鍵字便派上用場。它允許子類別訪問父類別的實現，從而在重寫方法時保留父類別的功能。

### 目的
使用「super」可以：
- 調用父類別的實現，避免重複代碼。
- 在子類別中擴展或修改父類別的方法行為。

### 用法
「super」關鍵字通常用於以下情況：
1. 在重寫方法中調用父類別的方法。
2. 在自定義初始化器中調用父類別的初始化器。

```swift
class Parent {
    func greet() {
        print("Hello from Parent")
    }
}

class Child: Parent {
    override func greet() {
        super.greet() // 調用父類別的 greet 方法
        print("Hello from Child")
    }
}
```

## 範例
以下是使用「super」的基本範例：

### 範例 1：重寫方法
```swift
class Animal {
    func speak() {
        print("Animal speaks")
    }
}

class Dog: Animal {
    override func speak() {
        super.speak() // 調用 Animal 的 speak 方法
        print("Dog barks")
    }
}

let dog = Dog()
dog.speak()
// 輸出：Animal speaks
// Dog barks
```

### 範例 2：自定義初始化器
```swift
class Vehicle {
    var wheels: Int

    init(wheels: Int) {
        self.wheels = wheels
    }
}

class Car: Vehicle {
    var brand: String

    init(wheels: Int, brand: String) {
        self.brand = brand
        super.init(wheels: wheels) // 調用父類別的初始化器
    }
}

let myCar = Car(wheels: 4, brand: "Toyota")
print(myCar.wheels) // 輸出：4
```

## 說明
使用「super」時，有幾個常見的陷阱和注意事項：
- 在重寫方法時，不能在沒有調用「super」的方法中使用「super」。
- 如果父類別的方法被標記為 `final`，則無法重寫此方法，也無法使用「super」訪問。
- 確保父類別的初始化器在子類別的初始化器中被正確調用，以避免初始化不完全的情況。

## 一句總結
在 Swift 中，「super」關鍵字用於引用父類別的方法和屬性，從而在子類別中實現功能擴展與重用。