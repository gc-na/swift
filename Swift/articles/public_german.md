<!--
Meta Description: # Das Schlüsselwort "public" in Swift: Zugriffssteuerung verstehen ## Synopsis Das Schlüsselwort "public" in Swift ist ein Zugriffsmodifizierer, der e...
Meta Keywords: public, die, von, ist, das
-->

# Das Schlüsselwort "public" in Swift: Zugriffssteuerung verstehen

## Synopsis
Das Schlüsselwort "public" in Swift ist ein Zugriffsmodifizierer, der es Entwicklern ermöglicht, die Sichtbarkeit von Klassen, Strukturen, Funktionen und Variablen über das Modul hinaus festzulegen. Es ist ein zentrales Konzept in der objektorientierten Programmierung und fördert die Wiederverwendbarkeit von Code.

## Documentation
In Swift wird der Zugriffsmodifizierer "public" verwendet, um den Zugriff auf bestimmte Teile des Codes zu ermöglichen, die von anderen Modulen verwendet werden können. Wenn ein Element als "public" deklariert wird, kann es von jedem anderen Modul, das das Modul importiert, aufgerufen werden.

### Zweck
Der Hauptzweck von "public" ist es, die Interoperabilität zwischen verschiedenen Modulen zu gewährleisten und die Struktur von größeren Projekten zu organisieren.

### Verwendung
Public kann auf die folgenden Elemente angewendet werden:
- Klassen
- Strukturen
- Enumerationen
- Protokolle
- Eigenschaften
- Methoden

Die Verwendung des Modifizierers erfolgt direkt vor der Deklaration des Elements. 

### Details
- **Standardzugriffslevel**: Wenn kein Zugriffsmodifizierer angegeben ist, ist das Standardzugriffslevel "internal", was bedeutet, dass es nur innerhalb des Moduls sichtbar ist.
- **"public" vs. "open"**: Der Modifizierer "public" erlaubt den Zugriff auf das Element, "open" hingegen erlaubt zusätzlich die Unterklasse in anderen Modulen.

## Examples
Hier sind einige grundlegende Anwendungsbeispiele für den "public" Modifizierer:

### Beispiel 1: Öffentliche Klasse
```swift
public class Fahrzeug {
    public var marke: String

    public init(marke: String) {
        self.marke = marke
    }

    public func fahren() {
        print("\(marke) fährt.")
    }
}
```

### Beispiel 2: Öffentliche Funktion
```swift
public func begruessen(name: String) {
    print("Hallo, \(name)!")
}
```

## Explanation
Ein häufiger Stolperstein beim Arbeiten mit dem Modifizierer "public" ist, dass viele Entwickler nicht verstehen, dass "public" nicht automatisch bedeutet, dass alle Eigenschaften und Methoden innerhalb einer Klasse auch "public" sind. Jedes Element muss individuell deklariert werden. 

Außerdem sollte beachtet werden, dass "public" nicht das gleiche wie "open" ist. Während "public" den Zugriff von außen erlaubt, erlaubt "open" die Vererbung in anderen Modulen, was in Situationen, in denen Erweiterbarkeit wichtig ist, von Bedeutung sein kann.

## One Line Summary
Der "public" Modifizierer in Swift ermöglicht den Zugriff auf Klassen, Funktionen und Eigenschaften von anderen Modulen, was die Wiederverwendbarkeit und Interoperabilität von Code fördert.