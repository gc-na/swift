<!--
Meta Description: # Swiftにおける「struct」の徹底解説 ## 概要 Swiftの「struct」は、データを表現するための強力な構造体であり、値型としての特性を持ちます。この構造体は、データのグループ化やカスタムデータ型の作成に役立ちます。 ## ドキュメンテーション ### 目的 Swiftにおける「s...
Meta Keywords: struct, propertyname, person, var, name
-->

# Swiftにおける「struct」の徹底解説

## 概要
Swiftの「struct」は、データを表現するための強力な構造体であり、値型としての特性を持ちます。この構造体は、データのグループ化やカスタムデータ型の作成に役立ちます。

## ドキュメンテーション
### 目的
Swiftにおける「struct」は、複数の関連するプロパティやメソッドをまとめて一つの複合データ型を作成するための基本的な手段です。値型であるため、変数や定数に代入されると、その値がコピーされます。

### 使用法
`struct`を定義する際は、以下のような構文を使用します。

```swift
struct StructName {
    // プロパティ
    var propertyName: PropertyType
    
    // イニシャライザ
    init(propertyName: PropertyType) {
        self.propertyName = propertyName
    }

    // メソッド
    func methodName() {
        // 何らかの処理
    }
}
```

### 詳細
- **初期化**: `struct`は自動的にメンバーイニシャライザを提供します。すべてのプロパティに初期値を指定する必要はありませんが、イニシャライザをカスタマイズすることもできます。
- **プロトコル準拠**: `struct`はプロトコルに準拠することができ、カスタムの振る舞いを持たせることができます。
- **不変性**: `struct`はデフォルトで不変のプロパティを持っており、`let`で定義した場合、そのプロパティは変更できません。

## 例
以下は、`struct`の基本的な使用例です。

```swift
struct Person {
    var name: String
    var age: Int
    
    func description() -> String {
        return "\(name) is \(age) years old."
    }
}

// 使用例
let person = Person(name: "Taro", age: 30)
print(person.description()) // Taro is 30 years old.
```

## 説明
- **値型の特性**: `struct`は値型であるため、別の変数に代入した際に新しいコピーが作成され、元のデータには影響を与えません。
- **継承不可**: `struct`はクラスとは異なり、継承をサポートしていません。もし継承が必要な場合は、クラスを使用する必要があります。
- **ミュータブルなプロパティ**: `mutating`キーワードを使用することで、`struct`内のプロパティを変更することができます。このキーワードは、メソッドが構造体のプロパティに対して変更を加える場合に必要です。

## 一文要約
Swiftの「struct」は、データを整理し、カスタムデータ型を作成するための値型の構造体です。