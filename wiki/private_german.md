<!--
Meta Description: # Das Schlüsselwort "private" in Swift: Sichtbarkeit und Zugriffskontrolle ## Synopsis Das Schlüsselwort "private" in Swift dient der Zugriffskontroll...
Meta Keywords: private, und, die, swift, auf
-->

# Das Schlüsselwort "private" in Swift: Sichtbarkeit und Zugriffskontrolle

## Synopsis
Das Schlüsselwort "private" in Swift dient der Zugriffskontrolle und definiert die Sichtbarkeit von Eigenschaften und Methoden innerhalb von Klassen und Strukturen. Es sorgt dafür, dass bestimmte Teile des Codes vor dem Zugriff von außen geschützt sind.

## Dokumentation
In Swift wird das Schlüsselwort "private" verwendet, um den Zugriff auf Eigenschaften, Methoden und Subskripte innerhalb einer Klasse oder Struktur zu beschränken. Elemente, die als "private" deklariert sind, können nur innerhalb des gleichen Typs (Klasse oder Struktur) verwendet werden. Diese Zugriffskontrolle ist besonders nützlich, um die Integrität der Daten zu wahren und eine saubere Kapselung der Logik zu gewährleisten.

### Verwendung
- **Klassen und Strukturen**: Sie können "private" für Eigenschaften und Methoden in Klassen und Strukturen verwenden.
- **Extensions**: "private" hat auch Einfluss auf Extensions, die zur gleichen Klasse oder Struktur gehören.

### Details
- **Sichtbarkeit**: "private" schränkt den Zugriff auf die Deklaration auf die umgebende Klasse oder Struktur ein. Das bedeutet, dass keine Subklassen oder externen Klassen auf die private Mitglieder zugreifen können.
- **Zugriff auf private Mitglieder**: In einer Extension, die zur gleichen Klasse gehört, können Sie auch auf private Mitglieder zugreifen.

## Beispiele
Hier sind einige einfache Beispiele, die die Verwendung von "private" in Swift veranschaulichen:

### Beispiel 1: Private Eigenschaft
```swift
class BankAccount {
    private var balance: Double = 0.0

    func deposit(amount: Double) {
        balance += amount
    }

    func getBalance() -> Double {
        return balance
    }
}

let account = BankAccount()
account.deposit(amount: 100.0)
// account.balance  // Fehler: 'balance' ist privat
print(account.getBalance())  // Ausgabe: 100.0
```

### Beispiel 2: Private Methode
```swift
class Calculator {
    private func add(a: Int, b: Int) -> Int {
        return a + b
    }

    func calculateSum(a: Int, b: Int) -> Int {
        return add(a: a, b: b)
    }
}

let calc = Calculator()
// calc.add(a: 2, b: 3)  // Fehler: 'add' ist privat
print(calc.calculateSum(a: 2, b: 3))  // Ausgabe: 5
```

## Erklärung
Ein häufiges Missverständnis besteht darin, dass "private" Mitglieder möglicherweise nicht in Extensions verwendet werden können. Dies ist jedoch nicht der Fall, solange die Extension zur gleichen Klasse oder Struktur gehört. Ein weiteres häufiges Problem ist, dass Entwickler dazu neigen, "private" übermäßig zu verwenden, was die Testbarkeit und Flexibilität des Codes beeinträchtigen kann. Es ist wichtig, ein Gleichgewicht zwischen Kapselung und der Notwendigkeit für Tests und Wartung zu finden.

## Einzeiler Zusammenfassung
Das Schlüsselwort "private" in Swift schützt Eigenschaften und Methoden vor externem Zugriff und fördert die Datenkapselung in Klassen und Strukturen.