<!--
Meta Description: # Das Schlüsselwort "continue" in Swift: Verwendung und Beispiele ## Synopsis Das Schlüsselwort "continue" in Swift ermöglicht es, den aktuellen Durch...
Meta Keywords: continue, schleife, while, swift, und
-->

# Das Schlüsselwort "continue" in Swift: Verwendung und Beispiele

## Synopsis
Das Schlüsselwort "continue" in Swift ermöglicht es, den aktuellen Durchlauf einer Schleife zu überspringen und mit dem nächsten Durchlauf fortzufahren. Es wird häufig in Schleifen verwendet, um bestimmte Bedingungen zu überprüfen und unerwünschte Iterationen zu vermeiden.

## Dokumentation
In Swift wird "continue" in Schleifen wie `for`, `while` und `repeat-while` verwendet. Der Hauptzweck von "continue" besteht darin, den aktuellen Schleifendurchlauf zu beenden und zur nächsten Iteration überzugehen. Dies ist besonders nützlich, wenn man eine Bedingung hat, die, wenn sie erfüllt ist, den Rest des Schleifen Körpers überspringen soll.

### Verwendung
Das Schlüsselwort "continue" wird innerhalb des Schleifen Körpers platziert. Es kann in Kombination mit einer Bedingung verwendet werden, um gezielt bestimmte Iterationen zu überspringen. 

### Details
- "continue" kann nur in Schleifen verwendet werden.
- Es kann in allen Schleifenarten (for, while, repeat-while) genutzt werden.
- Wenn "continue" in einer geschachtelten Schleife verwendet wird, betrifft es nur die innere Schleife.

## Beispiele
### Beispiel 1: Verwendung in einer for-Schleife
```swift
for i in 1...10 {
    if i % 2 == 0 {
        continue // Überspringt gerade Zahlen
    }
    print(i) // Gibt nur ungerade Zahlen aus: 1, 3, 5, 7, 9
}
```

### Beispiel 2: Verwendung in einer while-Schleife
```swift
var count = 0
while count < 10 {
    count += 1
    if count == 5 {
        continue // Überspringt die Ausgabe, wenn count 5 ist
    }
    print(count) // Gibt 1, 2, 3, 4, 6, 7, 8, 9, 10 aus
}
```

### Beispiel 3: Verwendung in einer repeat-while-Schleife
```swift
var num = 0
repeat {
    num += 1
    if num == 3 {
        continue // Überspringt die Ausgabe, wenn num 3 ist
    }
    print(num) // Gibt 1, 2, 4, 5 aus
} while num < 5
```

## Erklärung
Ein häufiger Fehler beim Einsatz von "continue" ist, dass Entwickler nicht bedenken, dass es nur den aktuellen Schleifendurchlauf beeinflusst. Wenn Sie "continue" in einer geschachtelten Schleife verwenden, wird nur die innere Schleife beeinflusst. Auch sollte darauf geachtet werden, dass durch übermäßigen Gebrauch von "continue" der Code schwerer lesbar werden kann. Daher sollte es sparsam und nur dort eingesetzt werden, wo es die Logik klarer macht.

## Ein-Satz-Zusammenfassung
Das Schlüsselwort "continue" in Swift überspringt den aktuellen Schleifendurchlauf und setzt die Schleife mit der nächsten Iteration fort.