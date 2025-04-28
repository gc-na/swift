<!--
Meta Description: # Swift `case`: Fallunterscheidung in der Swift-Programmierung ## Synopsis Das `case`-Schlüsselwort in Swift wird verwendet, um Mustervergleiche in `s...
Meta Keywords: case, die, der, ist, swift
-->

# Swift `case`: Fallunterscheidung in der Swift-Programmierung

## Synopsis
Das `case`-Schlüsselwort in Swift wird verwendet, um Mustervergleiche in `switch`-Anweisungen durchzuführen. Es ermöglicht Entwicklern, verschiedene Bedingungen zu überprüfen und entsprechend zu reagieren.

## Dokumentation
Das `case`-Schlüsselwort ist ein zentraler Bestandteil der `switch`-Anweisung in Swift. Es ermöglicht die Handhabung verschiedener Werte und Muster in einer eleganten und lesbaren Weise. Die Syntax für die Verwendung von `case` ist einfach und erlaubt es, spezifische Werte, Bereiche, oder Muster zu definieren, die mit dem Wert, der in der `switch`-Anweisung überprüft wird, verglichen werden sollen.

### Zweck
`case` wirdprimär verwendet, um eine Vielzahl von möglichen Werten in einer `switch`-Anweisung zu behandeln. Dadurch wird der Code klarer und einfacher zu lesen als die Verwendung von mehreren `if-else`-Anweisungen.

### Verwendung
Die Grundstruktur einer `switch`-Anweisung mit `case` sieht folgendermaßen aus:

```swift
switch wert {
case muster1:
    // Aktion für muster1
case muster2:
    // Aktion für muster2
default:
    // Aktion für alle anderen Fälle
}
```

## Beispiele
Hier sind einige grundlegende Beispiele für die Verwendung von `case` in Swift:

### Beispiel 1: Einfacher Wertvergleich
```swift
let zahl = 2

switch zahl {
case 1:
    print("Die Zahl ist 1.")
case 2:
    print("Die Zahl ist 2.")
default:
    print("Die Zahl ist weder 1 noch 2.")
}
```

### Beispiel 2: Bereichsvergleich
```swift
let temperatur = 30

switch temperatur {
case 0...10:
    print("Es ist kalt.")
case 11...25:
    print("Es ist angenehm.")
case 26...35:
    print("Es ist warm.")
default:
    print("Es ist heiß.")
}
```

### Beispiel 3: Nutzung von Tupeln
```swift
let punkt = (2, 3)

switch punkt {
case (0, 0):
    print("Der Punkt liegt im Ursprung.")
case (let x, 0):
    print("Der Punkt liegt auf der X-Achse bei x = \(x).")
case (0, let y):
    print("Der Punkt liegt auf der Y-Achse bei y = \(y).")
case (let x, let y):
    print("Der Punkt hat die Koordinaten (\(x), \(y)).")
}
```

## Erklärung
Ein häufiges Problem beim Umgang mit `case` und `switch` in Swift ist die Vergesslichkeit, den `default`-Fall zu definieren. Wenn keiner der definierten Fälle zutrifft und kein `default`-Fall angegeben ist, führt dies zu einem Kompilierungsfehler. Zudem ist es wichtig, zu beachten, dass `switch` in Swift eine vollständige Kontrolle über die Werte bietet, wenn sie verwendet werden, was bedeutet, dass alle möglichen Fälle behandelt werden sollten, um sicherzustellen, dass der Code robust ist.

## Zusammenfassung in einem Satz
Das `case`-Schlüsselwort in Swift ermöglicht die effektive und lesbare Fallunterscheidung innerhalb von `switch`-Anweisungen.