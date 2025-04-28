<!--
Meta Description: # Swiftにおける「init」：初期化の基本 ## 概要 Swiftの「init」は、クラスや構造体のインスタンスを生成するための初期化メソッドです。このメソッドを使用することで、オブジェクトのプロパティに初期値を設定し、オブジェクトを適切に構築することができます。 ## ドキュメンテーション ...
Meta Keywords: init, var, string, self, name
-->

# Swiftにおける「init」：初期化の基本

## 概要
Swiftの「init」は、クラスや構造体のインスタンスを生成するための初期化メソッドです。このメソッドを使用することで、オブジェクトのプロパティに初期値を設定し、オブジェクトを適切に構築することができます。

## ドキュメンテーション
### 目的
「init」は、Swiftにおけるオブジェクト指向プログラミングの基本的な概念の一つであり、クラスや構造体のインスタンスを安全に初期化するための手段です。

### 使用法
「init」は、クラスや構造体の中で定義され、特定の引数を取ることができます。また、デフォルトの初期化子を使用することも可能です。初期化子は、インスタンスが生成されるときに必ず呼び出され、すべてのプロパティが初期化されることを保証します。

```swift
class Person {
    var name: String
    var age: Int
    
    // 初期化子
    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
}

// インスタンスの生成
let person = Person(name: "山田太郎", age: 30)
```

### 詳細
- **デフォルト初期化子**: プロパティに初期値が設定されている場合、Swiftは自動的にデフォルトの初期化子を提供します。
- **イニシャライザのオーバーロード**: 同じクラス内で複数の初期化子を定義することが可能です。
- **必要な初期化子**: 必要なプロパティを全て初期化することが求められます。これにより、インスタンスが完全な状態で存在することが保証されます。

## 例
### 基本的な使用例
以下は、シンプルな構造体とクラスの初期化子の例です。

```swift
struct Rectangle {
    var width: Double
    var height: Double
    
    init(width: Double, height: Double) {
        self.width = width
        self.height = height
    }
}

let rect = Rectangle(width: 10.0, height: 5.0)
```

```swift
class Car {
    var brand: String
    var model: String
    
    init(brand: String, model: String) {
        self.brand = brand
        self.model = model
    }
}

let myCar = Car(brand: "トヨタ", model: "カローラ")
```

## 説明
- **共通の落とし穴**: 初期化子内でプロパティを初期化する前に、selfを参照するとエラーが発生します。これは、インスタンスが完全に初期化されていないためです。
- **循環参照**: 初期化子で他のオブジェクトを生成する際、循環参照が発生しないように注意が必要です。
- **必須の初期化子**: すべてのプロパティが初期化されるまで、インスタンスを使用することはできません。このため、全てのプロパティを初期化する必要があります。

## 一文の要約
Swiftの「init」は、クラスや構造体のインスタンスを安全に初期化するためのメソッドです。