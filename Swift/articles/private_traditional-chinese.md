<!--
Meta Description: # Swift 中的 "private" 訪問控制關鍵字 ## 摘要 在 Swift 程式語言中，`private` 是一種訪問控制關鍵字，旨在限制對類別、結構或擴展內部成員的訪問範圍，確保數據隱私和封裝性。 ## 文檔 `private` 關鍵字用於定義屬性、方法或初始化器的可見性。當你將一個成員...
Meta Keywords: private, swift, balance, amount, account
-->

# Swift 中的 "private" 訪問控制關鍵字

## 摘要
在 Swift 程式語言中，`private` 是一種訪問控制關鍵字，旨在限制對類別、結構或擴展內部成員的訪問範圍，確保數據隱私和封裝性。

## 文檔
`private` 關鍵字用於定義屬性、方法或初始化器的可見性。當你將一個成員標記為 `private` 時，它只能在定義它的類別或結構的範圍內訪問，無法從外部訪問。這是實現封裝的重要手段，有助於保護內部狀態，防止不必要的干擾。

### 用法
在 Swift 中，`private` 可以應用於類別、結構內的變量、常量或方法。例如：

```swift
class Example {
    private var secretNumber: Int = 42

    private func displaySecret() {
        print("The secret number is \(secretNumber)")
    }
}
```

在上述範例中，`secretNumber` 和 `displaySecret()` 只能在 `Example` 類別內部訪問。這樣可以防止外部對這些成員的直接訪問和修改。

## 範例
以下是使用 `private` 的基本範例：

```swift
class BankAccount {
    private var balance: Double = 0.0

    func deposit(amount: Double) {
        if amount > 0 {
            balance += amount
        }
    }

    func getBalance() -> Double {
        return balance
    }
}

let account = BankAccount()
account.deposit(amount: 100.0)
print(account.getBalance()) // 100.0
// print(account.balance) // 這行會報錯，因為 balance 是 private
```

在這個例子中，`balance` 變數被標記為 `private`，所以它無法被外部直接訪問。

## 解釋
使用 `private` 時需要注意以下幾點：

1. **範圍限制**：`private` 會限制成員的訪問僅限於定義它的類別或結構。這意味著你不能在子類別中訪問 `private` 成員。
  
2. **封裝性**：使用 `private` 可以幫助你保持類別的內部實現細節隱藏，從而減少耦合，使程式碼更易於維護。

3. **命名衝突**：在同一個類別或結構中，`private` 成員的名稱必須是唯一的，以避免命名衝突。

4. **測試挑戰**：對於單元測試來說，`private` 成員可能會使測試變得困難，因為它們無法直接訪問。如果需要進行測試，可以考慮使用 `internal` 或 `fileprivate`。

## 一句總結
在 Swift 中，`private` 關鍵字用於限制成員的訪問範圍，以增強數據封裝性和保護內部狀態。