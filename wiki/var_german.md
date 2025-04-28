<!--
Meta Description: # Swift: Verwendung von "var" zur Deklaration von Variablen ## Synopsis In Swift wird das Schlüsselwort "var" verwendet, um veränderliche Variablen zu...
Meta Keywords: der, var, variablen, swift, von
-->

# Swift: Verwendung von "var" zur Deklaration von Variablen

## Synopsis
In Swift wird das Schlüsselwort "var" verwendet, um veränderliche Variablen zu deklarieren, die während der Laufzeit geändert werden können. 

## Dokumentation
Das Schlüsselwort "var" in Swift ist essenziell für die Definition von Variablen, deren Werte im Verlauf der Programmausführung geändert werden können. Variablen sind grundlegende Bausteine in Swift, die es ermöglichen, Daten zu speichern und zu manipulieren. Im Gegensatz zu "let", das für die Deklaration konstanter Werte verwendet wird, erlaubt "var" eine flexible Handhabung von Daten.

### Verwendung
Die Syntax zur Deklaration einer Variablen mit "var" ist wie folgt:

```swift
var variableName: Type = initialValue
```

- **variableName**: Der Name der Variable, der den Wert repräsentiert.
- **Type**: Der Datentyp der Variable (optional, da Swift auch Typinferenz unterstützt).
- **initialValue**: Der Anfangswert, der der Variablen zugewiesen wird.

### Details
- Variablen können in verschiedenen Gültigkeitsbereichen (Scopes) deklariert werden, z. B. innerhalb von Funktionen, Klassen oder global.
- Swift unterstützt Typinferenz, was bedeutet, dass der Compiler den Typ der Variablen automatisch bestimmen kann, wenn kein Typ angegeben wird.
- Es ist möglich, eine Variable ohne einen initialen Wert zu deklarieren, aber sie muss vor der Verwendung initialisiert werden.

## Beispiele
Hier sind einige grundlegende Beispiele zur Verwendung von "var":

```swift
// Deklaration und Initialisierung einer Ganzzahl
var alter: Int = 25

// Deklaration ohne Typ und Initialisierung
var name = "Max"

// Ändern des Wertes der Variablen
alter = 26
name = "Moritz"

// Deklaration einer Fließkommazahl
var gewicht: Double = 70.5
```

## Erklärung
Ein häufiges Missverständnis bei der Verwendung von "var" ist, dass man annehmen könnte, Variablen könnten beliebige Datentypen speichern. In Swift ist der Datentyp jedoch statisch und muss vor der Zuweisung eines Wertes bekannt sein. Zudem kann der Wert einer "var"-Variablen jederzeit geändert werden, was in manchen Fällen zu unerwartetem Verhalten führen kann, wenn man nicht vorsichtig mit der Verwaltung des Zustands umgeht.

Ein weiterer Punkt ist, dass, obwohl "var" eine veränderliche Variable deklariert, Swift eine starke Typüberprüfung durchführt. Das bedeutet, dass man niemals einen Wert eines anderen Typs zuweisen kann, ohne den Typ vorher zu konvertieren.

## Ein-Satz-Zusammenfassung
"var" in Swift dient zur Deklaration von veränderlichen Variablen, die während der Programmausführung geändert werden können.