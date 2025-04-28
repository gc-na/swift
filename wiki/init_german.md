<!--
Meta Description: # init in Swift: Der Konstruktor für Ihre Klassen und Strukturen ## Synopsis In Swift ist `init` der Initialisierer, der verwendet wird, um Instanzen ...
Meta Keywords: der, init, initialisierer, swift, und
-->

# init in Swift: Der Konstruktor für Ihre Klassen und Strukturen

## Synopsis
In Swift ist `init` der Initialisierer, der verwendet wird, um Instanzen von Klassen und Strukturen zu erstellen und deren Eigenschaften zu initialisieren.

## Dokumentation
Der `init`-Befehl in Swift ist ein grundlegender Bestandteil der objektorientierten Programmierung. Er ermöglicht es Entwicklern, neue Instanzen von Klassen und Strukturen zu erzeugen. Der Initialisierer wird aufgerufen, wenn eine neue Instanz erstellt wird, und er bietet die Möglichkeit, die Eigenschaften der Instanz mit Werten zu initialisieren.

### Zweck
Der Hauptzweck von `init` besteht darin, sicherzustellen, dass eine Instanz in einem gültigen Zustand ist, bevor sie verwendet wird. In Swift müssen alle Eigenschaften einer Klasse oder Struktur initialisiert werden, bevor die Instanz verwendet werden kann.

### Verwendung
Um einen Initialisierer zu definieren, verwenden Sie das Keyword `init`, gefolgt von den Parametern, die Sie benötigen, um die Eigenschaften zu initialisieren. Sie können auch mehrere Initialisierer in einer Klasse oder Struktur definieren, um verschiedene Möglichkeiten zur Instanziierung zu bieten.

```swift
class Person {
    var name: String
    var alter: Int

    init(name: String, alter: Int) {
        self.name = name
        self.alter = alter
    }
}
```

## Beispiele
Hier sind einige einfache Beispiele zur Veranschaulichung der Verwendung von `init`:

### Beispiel 1: Einfache Klasse
```swift
class Auto {
    var marke: String
    var baujahr: Int

    init(marke: String, baujahr: Int) {
        self.marke = marke
        self.baujahr = baujahr
    }
}

let meinAuto = Auto(marke: "Volkswagen", baujahr: 2020)
```

### Beispiel 2: Struktur mit Standardwerten
```swift
struct Rechteck {
    var breite: Double
    var hoehe: Double

    init(breite: Double = 1.0, hoehe: Double = 1.0) {
        self.breite = breite
        self.hoehe = hoehe
    }
}

let standardRechteck = Rechteck() // verwendet Standardwerte
```

## Erklärung
Einige häufige Fallstricke und Hinweise im Zusammenhang mit `init`:

- **Falsche Reihenfolge der Initialisierungen**: In Swift müssen alle Eigenschaften einer Klasse vor der Verwendung initialisiert werden. Dies schließt die Initialisierung von Eigenschaften in `init` ein, bevor `self` verwendet wird.
  
- **Fälle ohne Parameter**: Wenn Sie einen Parameterlosen Initialisierer benötigen, können Sie diesen explizit definieren. Andernfalls wird Swift keinen solchen Initialisierer automatisch erstellen, wenn Sie benutzerdefinierte Initialisierer definieren.

- **Designierte und Convenience-Initialisierer**: Die Unterscheidung zwischen designierten und Convenience-Initialisierern ist wichtig. Designierte Initialisierer sind die Hauptinitialisierer einer Klasse, während Convenience-Initialisierer einfachere Wege zur Initialisierung bieten.

## Ein-Satz-Zusammenfassung
`init` in Swift ist der entscheidende Initialisierer, der es Entwicklern ermöglicht, Instanzen von Klassen und Strukturen zu erstellen und deren Eigenschaften zu initialisieren.