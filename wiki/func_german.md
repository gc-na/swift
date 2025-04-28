<!--
Meta Description: # Swift `func`: Funktionsdefinitionen und -verwendung in Swift ## Synopsis In Swift ist `func` das Schlüsselwort zur Definition von Funktionen, die ei...
Meta Keywords: die, und, funktion, von, der
-->

# Swift `func`: Funktionsdefinitionen und -verwendung in Swift

## Synopsis
In Swift ist `func` das Schlüsselwort zur Definition von Funktionen, die eine zentrale Rolle in der Programmierung spielen. Funktionen ermöglichen die Gruppierung von Code, um wiederholte Aufgaben auszuführen und die Code-Wartbarkeit zu verbessern.

## Dokumentation
Das Schlüsselwort `func` wird verwendet, um eine Funktion zu deklarieren. Eine Funktion ist ein Block von Code, der eine bestimmte Aufgabe ausführt. Funktionen können Parameter annehmen und Werte zurückgeben. Sie sind essenziell für die Strukturierung von Programmen und helfen, den Code modular und wiederverwendbar zu gestalten.

### Zweck
- Strukturierung von Code in wiederverwendbare Einheiten.
- Verbesserung der Lesbarkeit und Wartbarkeit des Codes.
- Ermöglichen von Parameterübergabe und Rückgabewerten.

### Verwendung
Um eine Funktion zu definieren, verwenden Sie das Schlüsselwort `func`, gefolgt vom Funktionsnamen, einer Parameterliste in runden Klammern und einem Rückgabetyp. Die grundlegende Syntax lautet:

```swift
func funktionsname(parametername: Typ) -> Rückgabetyp {
    // Funktionskörper
}
```

### Details
- **Funktionsname**: Der Name der Funktion, der zur Aufrufung verwendet wird.
- **Parameter**: Eine optionale Liste von Eingabewerten, die an die Funktion übergeben werden.
- **Rückgabetyp**: Der Datentyp des Wertes, den die Funktion zurückgibt. Dies ist optional; wenn die Funktion keinen Wert zurückgibt, wird `Void` verwendet.

## Beispiele
### Beispiel 1: Einfache Funktion ohne Parameter
```swift
func halloWelt() {
    print("Hallo, Welt!")
}

halloWelt() // Ausgabe: Hallo, Welt!
```

### Beispiel 2: Funktion mit Parametern und Rückgabewert
```swift
func addiere(zahl1: Int, zahl2: Int) -> Int {
    return zahl1 + zahl2
}

let ergebnis = addiere(3, 5) // ergebnis ist 8
```

### Beispiel 3: Funktion mit optionalem Rückgabewert
```swift
func teile(zahl1: Int, zahl2: Int) -> Int? {
    guard zahl2 != 0 else { return nil }
    return zahl1 / zahl2
}

if let ergebnis = teile(10, 2) {
    print("Ergebnis: \(ergebnis)") // Ausgabe: Ergebnis: 5
} else {
    print("Division durch Null!")
}
```

## Erklärung
Ein häufiges Problem bei der Verwendung von Funktionen ist das Missverständnis über den Gültigkeitsbereich von Variablen. Variablen, die innerhalb einer Funktion definiert sind, sind lokal und können nicht außerhalb der Funktion verwendet werden. Ein weiterer Stolperstein ist die korrekte Handhabung von Rückgabewerten. Stellen Sie sicher, dass der Rückgabetyp korrekt angegeben wird, um Kompilierungsfehler zu vermeiden.

Zusätzlich sollten Sie darauf achten, dass Sie die Parameter in der richtigen Reihenfolge übergeben, da Swift die Typen und die Reihenfolge während des Funktionsaufrufs strengen Regeln unterwirft.

## Einzeiler Zusammenfassung
Das Schlüsselwort `func` in Swift ermöglicht die Definition von Funktionen, die wiederverwendbaren und strukturierten Code bereitstellen.