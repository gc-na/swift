<!--
Meta Description: # Klassen in Swift: Grundlagen und Anwendung ## Synopsis In Swift sind Klassen grundlegende Bausteine der objektorientierten Programmierung, die es er...
Meta Keywords: und, swift, klassen, die, klasse
-->

# Klassen in Swift: Grundlagen und Anwendung

## Synopsis
In Swift sind Klassen grundlegende Bausteine der objektorientierten Programmierung, die es ermöglichen, benutzerdefinierte Datentypen zu erstellen und deren Verhalten zu definieren.

## Dokumentation
Eine Klasse in Swift ist ein Entwurf für Objekte, die Eigenschaften (Variablen) und Methoden (Funktionen) enthalten. Klassen ermöglichen es, Daten und Funktionen, die auf diese Daten operieren, zu kapseln. Sie unterstützen Konzepte wie Vererbung, Polymorphismus und Kapselung, was sie zu einem zentralen Bestandteil der Swift-Programmierung macht.

### Zweck
Klassen werden verwendet, um komplexe Datenstrukturen zu modellieren und deren Verhalten zu definieren. Sie bieten eine Möglichkeit, verwandte Daten und Funktionalitäten zusammenzufassen.

### Verwendung
Um eine Klasse in Swift zu definieren, verwenden Sie das Schlüsselwort `class`, gefolgt vom Klassennamen und einer geschweiften Klammer, die die Mitglieder der Klasse umschließt. Hier ist ein einfaches Beispiel:

```swift
class Auto {
    var marke: String
    var baujahr: Int

    init(marke: String, baujahr: Int) {
        self.marke = marke
        self.baujahr = baujahr
    }

    func fahren() {
        print("\(marke) fährt.")
    }
}
```

In diesem Beispiel definiert die Klasse `Auto` zwei Eigenschaften (`marke` und `baujahr`) und eine Methode (`fahren`), die beschreibt, was das Auto tut.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung von Klassen in Swift:

```swift
// Definition der Klasse
class Person {
    var name: String
    var alter: Int

    init(name: String, alter: Int) {
        self.name = name
        self.alter = alter
    }

    func vorstellen() {
        print("Hallo, ich heiße \(name) und ich bin \(alter) Jahre alt.")
    }
}

// Instanziierung der Klasse
let person1 = Person(name: "Max", alter: 28)
person1.vorstellen()  // Ausgabe: Hallo, ich heiße Max und ich bin 28 Jahre alt.
```

### Vererbung
Klassen in Swift unterstützen auch Vererbung, was bedeutet, dass eine Klasse von einer anderen Klasse abgeleitet werden kann:

```swift
class Fahrzeug {
    var typ: String

    init(typ: String) {
        self.typ = typ
    }
}

class Motorrad: Fahrzeug {
    var ps: Int

    init(typ: String, ps: Int) {
        self.ps = ps
        super.init(typ: typ)
    }

    func beschleunigen() {
        print("Das \(typ) mit \(ps) PS beschleunigt.")
    }
}

let meinMotorrad = Motorrad(typ: "Sportbike", ps: 150)
meinMotorrad.beschleunigen()  // Ausgabe: Das Sportbike mit 150 PS beschleunigt.
```

## Erklärung
Ein häufiges Missverständnis bei der Verwendung von Klassen in Swift ist der Umgang mit Referenztypen. Klassen sind Referenztypen, was bedeutet, dass zwei Variablen auf dasselbe Objekt verweisen können. Änderungen an einem Objekt über eine dieser Variablen wirken sich auf alle Verweise aus. Dies kann zu unerwarteten Verhalten führen, wenn Sie nicht vorsichtig sind.

Ein weiteres wichtiges Konzept ist die Verwendung des `deinit`-Schlüsselworts, das einen Deinitialisierer definiert. Dies ist nützlich, um Ressourcen freizugeben, wenn eine Instanz der Klasse nicht mehr benötigt wird.

## Ein-Satz-Zusammenfassung
Klassen in Swift sind leistungsstarke Werkzeuge zur Erstellung benutzerdefinierter Datentypen, die Eigenschaften und Methoden kapseln und objektorientierte Programmierung unterstützen.