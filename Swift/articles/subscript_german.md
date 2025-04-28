<!--
Meta Description: # Subscript in Swift: Zugriff auf Elemente in Collections und benutzerdefinierten Typen ## Synopsis Ein Subscript in Swift ermöglicht den direkten Zug...
Meta Keywords: index, subscript, und, swift, subscripts
-->

# Subscript in Swift: Zugriff auf Elemente in Collections und benutzerdefinierten Typen

## Synopsis
Ein Subscript in Swift ermöglicht den direkten Zugriff auf Elemente in Collections wie Arrays, Dictionaries und benutzerdefinierten Typen. Es bietet eine prägnante Syntax, um Elemente über Indizes oder Schlüssel abzurufen oder festzulegen.

## Documentation
### Zweck
Subscripts bieten eine elegante Möglichkeit, auf Elemente in einer Collection zuzugreifen, ohne explizite Methodenaufrufe verwenden zu müssen. Sie können für Arrays, Dictionaries und sogar für benutzerdefinierte Klassen und Strukturen definiert werden.

### Verwendung
Subscripts werden mit dem Schlüsselwort `subscript` definiert und können in einer Klasse, Struktur oder einem Enum enthalten sein. Sie können sowohl Lese- als auch Schreibzugriffe ermöglichen. Die Syntax für die Definition eines Subscripts sieht wie folgt aus:

```swift
subscript(index: Int) -> ElementType {
    get {
        // Rückgabe des Wertes für den angegebenen Index
    }
    set {
        // Setzen des Wertes für den angegebenen Index
    }
}
```

### Details
- **Indizes und Schlüssel**: Subscripts können mit verschiedenen Parametertypen definiert werden, um verschiedene Zugriffsarten zu ermöglichen.
- **Mehrdimensionale Subscripts**: Sie können auch mehrere Parameter verwenden, um auf mehrdimensionale Datenstrukturen zuzugreifen.
- **Standardwerte**: Es ist möglich, Standardwerte für Subscripts zu definieren, um die Flexibilität zu erhöhen.

## Examples
### Einfaches Beispiel für ein Subscript
```swift
struct Quadrat {
    var seitenlaenge: Double
    
    subscript(index: Int) -> Double {
        get {
            return seitenlaenge * Double(index)
        }
        set {
            seitenlaenge = newValue / Double(index)
        }
    }
}

var meinQuadrat = Quadrat(seitenlaenge: 4.0)
print(meinQuadrat[2]) // Ausgabe: 8.0
meinQuadrat[2] = 16.0
print(meinQuadrat.seitenlaenge) // Ausgabe: 8.0
```

### Subscript in einer Klasse
```swift
class Notizen {
    private var notizen: [String] = []

    subscript(index: Int) -> String {
        get {
            return notizen[index]
        }
        set {
            notizen[index] = newValue
        }
    }
}

let meineNotizen = Notizen()
meineNotizen[0] = "Swift lernen"
print(meineNotizen[0]) // Ausgabe: Swift lernen
```

## Explanation
### Häufige Fallstricke und Hinweise
- **Out of Bounds**: Achten Sie darauf, dass Sie keinen Index verwenden, der außerhalb der Grenzen der Collection liegt, da dies zu einem Laufzeitfehler führt.
- **Schreibzugriff**: Wenn ein Subscript nur einen `get`-Zugriff hat, aber keinen `set`, können Sie den Wert nicht ändern.
- **Leistung**: Bei sehr großen Collections kann der Zugriff über Subscripts Auswirkungen auf die Leistung haben, insbesondere bei komplexen Berechnungen im Getter oder Setter.

## One Line Summary
Subscripts in Swift ermöglichen den einfachen Zugriff auf Elemente in Collections und benutzerdefinierten Typen, wodurch der Code prägnanter und lesbarer wird.