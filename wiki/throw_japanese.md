<!--
Meta Description: # Swiftの「throw」: エラーハンドリングの基本 ## 概要 Swiftにおける「throw」は、エラーを発生させるためのキーワードです。この機能は、関数やメソッドがエラーをスローし、呼び出し元でそのエラーを処理できるようにするために使用されます。 ## ドキュメント 「throw」は、S...
Meta Keywords: throw, catch, error, print, throws
-->

# Swiftの「throw」: エラーハンドリングの基本

## 概要
Swiftにおける「throw」は、エラーを発生させるためのキーワードです。この機能は、関数やメソッドがエラーをスローし、呼び出し元でそのエラーを処理できるようにするために使用されます。

## ドキュメント
「throw」は、Swiftのエラーハンドリング機能の一部で、プログラムの実行中に問題が発生した際にエラーを報告するために使用されます。Swiftでは、エラーはErrorプロトコルに準拠した型で表されます。

### 目的
- エラーが発生したことを示すために使用する。
- エラー処理を呼び出し元に委譲する。

### 使用法
エラーハンドリングを行うための関数では、`throws`キーワードを使用して、その関数がエラーをスローする可能性があることを示します。呼び出し元は、`do-catch`ブロックを使用してエラーをキャッチします。

```swift
enum MyError: Error {
    case exampleError
}

func throwingFunction() throws {
    throw MyError.exampleError
}

do {
    try throwingFunction()
} catch {
    print("エラーが発生しました: \(error)")
}
```

## 例
以下は、Swiftにおける「throw」の基本的な使用例です。

### 例1: シンプルなエラーのスロー
```swift
enum NetworkError: Error {
    case timeout
}

func fetchData() throws {
    throw NetworkError.timeout
}

do {
    try fetchData()
} catch NetworkError.timeout {
    print("ネットワークエラー: タイムアウト")
} catch {
    print("他のエラー: \(error)")
}
```

### 例2: エラー処理のカスタマイズ
```swift
enum ValidationError: Error {
    case invalidInput(String)
}

func validateInput(_ input: String) throws {
    if input.isEmpty {
        throw ValidationError.invalidInput("入力が空です")
    }
}

do {
    try validateInput("")
} catch ValidationError.invalidInput(let message) {
    print("バリデーションエラー: \(message)")
} catch {
    print("その他のエラー: \(error)")
}
```

## 説明
「throw」を使用する際の一般的な注意点や落とし穴には以下のようなものがあります。

- **エラー型の定義**: スローするエラーは、必ず`Error`プロトコルに準拠した型でなければなりません。
- **do-catchブロックの使用**: スローしたエラーを適切にキャッチするために、必ず`do-catch`ブロックを使用する必要があります。これを怠ると、コンパイルエラーが発生します。
- **エラーの伝播**: 関数がエラーをスローする場合、その関数を呼び出す側もエラー処理を行う必要があります。これを行わないと、エラーが隠れてしまう可能性があります。

## 一文の要約
Swiftにおける「throw」は、エラーを発生させ、呼び出し元でそのエラーを処理できるようにするための重要なキーワードです。