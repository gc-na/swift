<!--
Meta Description: # Standardwerte in Swift: Eine umfassende Anleitung ## Synopsis In Swift beziehen sich Standardwerte auf die vordefinierten Werte, die Argumenten in F...
Meta Keywords: die, standardwerte, swift, parameter, der
-->

# Standardwerte in Swift: Eine umfassende Anleitung

## Synopsis
In Swift beziehen sich Standardwerte auf die vordefinierten Werte, die Argumenten in Funktionen oder Initialisierern zugewiesen werden, wenn keine spezifischen Werte übergeben werden. Diese Funktionalität verbessert die Benutzerfreundlichkeit und Flexibilität des Codes.

## Dokumentation
Standardwerte in Swift ermöglichen es Entwicklern, Funktionen und Initialisierer zu definieren, die Parameter mit einem vordefinierten Wert versehen, falls der Benutzer keinen Wert angibt. Dies ist besonders nützlich, um die Anzahl der übergebenen Argumente zu reduzieren und gleichzeitig die Lesbarkeit des Codes zu erhöhen.

### Verwendung
Um einen Standardwert für einen Parameter in Swift festzulegen, wird der Wert im Funktions- oder Initialisierer-Header direkt nach dem Typ angegeben. Hier ein Beispiel:

```swift
func begrüße(person: String, mitNachricht nachricht: String = "Willkommen!") {
    print("\(nachricht), \(person)")
}
```

In diesem Beispiel hat der Parameter `nachricht` einen Standardwert von "Willkommen!". Wenn der Benutzer die Funktion ohne den zweiten Parameter aufruft, wird dieser Standardwert verwendet.

### Details
- **Flexibilität**: Standardwerte ermöglichen es, Funktionen flexibler zu gestalten, da sie in verschiedenen Szenarien ohne Überladung verwendet werden können.
- **Lesbarkeit**: Der Code bleibt übersichtlich, da nicht immer alle Parameter angegeben werden müssen.
- **Typensicherheit**: Standardwerte müssen mit dem Typ des Parameters übereinstimmen. Andernfalls führt dies zu einem Kompilierungsfehler.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung von Standardwerten in Swift:

### Beispiel 1: Funktion mit Standardwert
```swift
func addiere(a: Int, b: Int = 5) -> Int {
    return a + b
}

let result1 = addiere(a: 10) // result1 ist 15
let result2 = addiere(a: 10, b: 20) // result2 ist 30
```

### Beispiel 2: Initialisierer mit Standardwert
```swift
class Auto {
    var marke: String
    var farbe: String

    init(marke: String, farbe: String = "Schwarz") {
        self.marke = marke
        self.farbe = farbe
    }
}

let meinAuto = Auto(marke: "BMW") // meinAuto.farbe ist "Schwarz"
let deinAuto = Auto(marke: "Audi", farbe: "Rot") // deinAuto.farbe ist "Rot"
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von Standardwerten ist die Verwirrung über die Reihenfolge der Parameter in Funktionen. Standardwerte können nur für Parameter am Ende der Parameterliste definiert werden. Zudem können Standardwerte nicht für Parameter verwendet werden, die in einer Überladung einer Funktion bereits spezifische Typen haben.

Ein weiteres Problem kann auftreten, wenn Standardwerte in Kombination mit variadischen Parametern oder Closures verwendet werden, da dies die Lesbarkeit und den Codefluss beeinträchtigen kann.

## Ein Satz Zusammenfassung
Standardwerte in Swift verbessern die Flexibilität und Lesbarkeit von Funktionen und Initialisierern, indem sie vordefinierte Werte für Parameter bereitstellen, die nicht immer angegeben werden müssen.