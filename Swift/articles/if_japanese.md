<!--
Meta Description: # Swiftにおける「if」文の使い方 ## 概要 Swiftにおける「if」文は、条件に基づいてコードの実行を制御するための基本的な制御構造です。条件が真である場合に特定のブロックのコードを実行し、そうでない場合には他の処理を行うことができます。 ## ドキュメント ### 目的 「if」文は、...
Meta Keywords: else, print, swift, score, swiftにおける
-->

# Swiftにおける「if」文の使い方

## 概要
Swiftにおける「if」文は、条件に基づいてコードの実行を制御するための基本的な制御構造です。条件が真である場合に特定のブロックのコードを実行し、そうでない場合には他の処理を行うことができます。

## ドキュメント
### 目的
「if」文は、条件に基づいてプログラムのフローを制御するために使用されます。条件式が真の場合にのみ、特定の処理を実行することができます。

### 使用法
基本的な構文は以下の通りです。

```swift
if 条件 {
    // 条件が真のときに実行されるコード
} else {
    // 条件が偽のときに実行されるコード（省略可能）
}
```

また、複数の条件をチェックするために `else if` を使用することもできます。

```swift
if 条件1 {
    // 条件1が真のときに実行されるコード
} else if 条件2 {
    // 条件2が真のときに実行されるコード
} else {
    // どちらの条件も偽のときに実行されるコード
}
```

## 例
### 基本的な使用例

```swift
let number = 10

if number > 0 {
    print("正の数です")
} else {
    print("0または負の数です")
}
```

### 複数条件の例

```swift
let score = 85

if score >= 90 {
    print("優秀")
} else if score >= 75 {
    print("良好")
} else {
    print("もっと頑張りましょう")
}
```

## 説明
### よくある落とし穴と注意点
- **条件式の評価**: 条件式には比較演算子（`==`, `!=`, `<`, `>`, `<=`, `>=`）や論理演算子（`&&`, `||`）を使用することができますが、誤った演算子を使用すると意図した通りに動作しない場合があります。
- **ブロックのスコープ**: `if` 文内で定義した変数は、そのブロック内でのみ有効です。ブロックを出ると変数は使用できなくなります。
- **型の一致**: `if` 文で評価する条件式の型は、Boolean型である必要があります。異なる型同士の比較に注意してください。

## 一文要約
Swiftの「if」文は条件に基づいてコードの実行を制御するための基本的な構文です。