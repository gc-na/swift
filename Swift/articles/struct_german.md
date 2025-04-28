<!--
Meta Description: # Swift `struct`: Eine umfassende Anleitung zur Verwendung von Strukturen in Swift ## Synopsis In Swift sind `structs` (Strukturen) ein grundlegendes ...
Meta Keywords: swift, der, von, strukturen, und
-->

# Swift `struct`: Eine umfassende Anleitung zur Verwendung von Strukturen in Swift

## Synopsis
In Swift sind `structs` (Strukturen) ein grundlegendes Konstrukt zur Erstellung von benutzerdefinierten Datentypen, die Werte speichern und Methoden enthalten können. Sie bieten eine effiziente Möglichkeit, Daten zu organisieren und zu verwalten.

## Dokumentation
`struct` in Swift ist ein wertbasierter Datentyp, der es Entwicklern ermöglicht, komplexe Datenstrukturen einfach zu modellieren. Strukturen sind besonders nützlich, wenn Sie Daten zusammenfassen möchten, die logisch zusammengehören, und sie bieten eine Vielzahl von Funktionen, einschließlich der Definition von Eigenschaften, Methoden, Initialisierern und der Implementierung von Protokollen.

### Zweck
Strukturen sind ideal für die Modellierung von Daten, die in Ihrer Anwendung verwendet werden, beispielsweise geometrische Formen, Datenmodelle oder Konfigurationseinstellungen.

### Verwendung
Um eine Struktur in Swift zu definieren, verwenden Sie das Schlüsselwort `struct` gefolgt vom Namen der Struktur. Innerhalb der Struktur können Sie Eigenschaften und Methoden definieren. 

Hier ist die grundlegende Syntax:

```swift
struct StrukturName {
    // Eigenschaften
    var eigenschaft: Typ
    
    // Initialisierer
    init(eigenschaft: Typ) {
        self.eigenschaft = eigenschaft
    }
    
    // Methoden
    func methode() {
        // Methodenkörper
    }
}
```

## Beispiele
### Beispiel 1: Grundlegende Struktur
```swift
struct Person {
    var name: String
    var alter: Int
    
    func beschreibung() -> String {
        return "\(name) ist \(alter) Jahre alt."
    }
}

let person = Person(name: "Max", alter: 25)
print(person.beschreibung())  // Ausgabe: Max ist 25 Jahre alt.
```

### Beispiel 2: Struktur mit Initialisierung
```swift
struct Rechteck {
    var breite: Double
    var hoehe: Double
    
    func flaeche() -> Double {
        return breite * hoehe
    }
}

let rechteck = Rechteck(breite: 10.0, hoehe: 5.0)
print(rechteck.flaeche())  // Ausgabe: 50.0
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von Strukturen in Swift ist das Verständnis des Unterschieds zwischen Werttypen und Referenztypen. Strukturen sind Werttypen, was bedeutet, dass beim Kopieren einer Struktur eine neue Instanz erstellt wird, und Änderungen an der Kopie haben keine Auswirkungen auf das Original. 

Ein weiterer Punkt ist der Mutabilitätsstatus von Eigenschaften. Wenn eine Struktur als konstant (let) deklariert wird, können ihre Eigenschaften nicht geändert werden, auch wenn sie als variabel (var) deklariert sind.

Ein häufiges Missverständnis ist auch die Annahme, dass Strukturen keine Methoden oder Initialisierer unterstützen. Tatsächlich können Strukturen sowohl Methoden als auch benutzerdefinierte Initialisierer enthalten.

## Ein-Satz-Zusammenfassung
`struct` in Swift ist ein wertbasierter Datentyp, der es Entwicklern ermöglicht, komplexe Datenstrukturen zu erstellen und Methoden zur Manipulation dieser Daten zu definieren.