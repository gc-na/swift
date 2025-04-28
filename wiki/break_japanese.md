<!--
Meta Description: # Swiftの「break」ステートメントの使い方と注意点 ## 概要 Swiftにおける「break」ステートメントは、ループやswitch文の実行を中断するために使用される重要な構文です。これにより、特定の条件を満たした場合に処理を早期に終了することができます。 ## ドキュメンテーション 「...
Meta Keywords: break, print, number, swift, case
-->

# Swiftの「break」ステートメントの使い方と注意点

## 概要
Swiftにおける「break」ステートメントは、ループやswitch文の実行を中断するために使用される重要な構文です。これにより、特定の条件を満たした場合に処理を早期に終了することができます。

## ドキュメンテーション
「break」ステートメントは、主に以下の目的で使用されます。

- **ループの中断**: for、while、repeat-whileループ内で使用し、ループの実行を中止します。
- **switch文の中断**: switch文内でcaseを処理する際に、他のcaseの実行を防ぎます。

### 使用方法
「break」は、次のように記述します。

```swift
break
```

### 詳細情報
- **ループ内での使用**: ループが実行されている間に特定の条件が満たされると、「break」を使うことでループを終了します。
- **switch文内での使用**: 各caseの後に「break」を明示的に記述することで、そのcaseが実行された後に他のcaseに進むことを防ぎます。

## 例
### ループでの使用例
```swift
for number in 1...10 {
    if number == 5 {
        break
    }
    print(number)
}
// 出力: 1, 2, 3, 4
```

### switch文での使用例
```swift
let number = 3

switch number {
case 1:
    print("One")
case 2:
    print("Two")
case 3:
    print("Three")
    break // これは省略可能です
case 4:
    print("Four")
default:
    print("Unknown")
}
// 出力: Three
```

## 説明
「break」を使用する際の一般的な落とし穴は、ループやswitch文の中での誤った位置に配置することです。特に、ネストされたループの中で「break」を使用すると、外側のループも中断されてしまうことがあります。これを避けるためには、ラベル付きの「break」を使用することができます。

### ラベル付きの「break」
```swift
outerLoop: for i in 1...3 {
    for j in 1...3 {
        if i == 2 && j == 2 {
            break outerLoop // outerLoopを終了
        }
        print("i: \(i), j: \(j)")
    }
}
// 出力: i: 1, j: 1, i: 1, j: 2, i: 1, j: 3, i: 2, j: 1
```

## 一文要約
Swiftの「break」ステートメントは、ループやswitch文の実行を早期に中断するために使用される構文です。