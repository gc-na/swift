<!--
Meta Description: # Fallthrough in Swift: Verwendung und Beispiele ## Synopsis Der "fallthrough"-Befehl in Swift ermöglicht es, in einem Switch-Statement die Ausführung...
Meta Keywords: fallthrough, ist, der, fall, die
-->

# Fallthrough in Swift: Verwendung und Beispiele

## Synopsis
Der "fallthrough"-Befehl in Swift ermöglicht es, in einem Switch-Statement die Ausführung in den nächsten Fall fortzusetzen, ohne die Bedingung erneut zu überprüfen. Dies ist besonders nützlich, wenn mehrere Fälle ähnliche Logik teilen.

## Dokumentation
In Swift wird "fallthrough" innerhalb eines Switch-Statements verwendet, um die Kontrolle von einem Fall in den nächsten zu übergeben. Standardmäßig bricht ein Switch-Statement nach der Ausführung des ersten passenden Falls ab. Mit "fallthrough" kann man jedoch explizit angeben, dass die Ausführung im nächsten Fall fortgesetzt werden soll. Dies kann verwendet werden, um gemeinsame Logik zwischen verschiedenen Fällen zu teilen oder um die Ausführung in mehrere Fälle zu lenken, die unterschiedliche Bedingungen erfüllen.

### Verwendung
Um "fallthrough" zu verwenden, platziere es am Ende des gewünschten Fall-Blocks innerhalb eines Switch-Statements. Beachte, dass der nächste Fall nicht dessen Bedingung überprüfen wird; stattdessen wird der Code im nächsten Fall direkt ausgeführt.

### Details
- "fallthrough" kann nur in Switch-Statements verwendet werden.
- Es ist nicht möglich, "fallthrough" in if-else-Anweisungen oder anderen Kontrollstrukturen zu verwenden.
- Der nächste Fall muss keinen Codeblock haben, aber es ist wichtig, dass der Code im nächsten Fall nicht von einer Bedingung abhängt, da diese nicht erneut geprüft wird.

## Beispiele

### Einfaches Beispiel
```swift
let zahl = 2

switch zahl {
case 1:
    print("Eins")
case 2:
    print("Zwei")
    fallthrough
case 3:
    print("Drei")
default:
    print("Keine Zahl")
}
```
**Ausgabe:**
```
Zwei
Drei
```

### Beispiel mit gemeinsamen Logik
```swift
let farbe = "rot"

switch farbe {
case "rot":
    print("Farbe ist rot")
    fallthrough
case "blau":
    print("Farbe ist blau")
    fallthrough
case "grün":
    print("Farbe ist grün")
default:
    print("Unbekannte Farbe")
}
```
**Ausgabe:**
```
Farbe ist rot
Farbe ist blau
Farbe ist grün
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von "fallthrough" ist, dass der Programmierer nicht erkennt, dass der nächste Fall sofort ausgeführt wird, ohne dass dessen Bedingung überprüft wird. Dies kann zu unerwarteten Ergebnissen führen, wenn der nächste Fall nicht wirklich zutrifft oder wenn dort Code vorhanden ist, der nicht ausgeführt werden sollte. Ein weiterer Punkt ist, dass "fallthrough" nur in Swift erlaubt ist, und es sich von ähnlichen Konzepten in anderen Programmiersprachen unterscheidet. Es ist wichtig, "fallthrough" mit Bedacht zu verwenden, um die Lesbarkeit des Codes zu gewährleisten.

## Ein-Satz-Zusammenfassung
Der "fallthrough"-Befehl in Swift ermöglicht die fortlaufende Ausführung in Switch-Statements, indem die Kontrolle vom aktuellen Fall auf den nächsten Fall übertragen wird.