<!--
Meta Description: # Throws in Swift: Fehlerbehandlung für sichere Programmierung ## Synopsis In Swift ermöglicht das Schlüsselwort `throws` Entwicklern, Fehler in Funkt...
Meta Keywords: throws, fehler, die, swift, funktion
-->

# Throws in Swift: Fehlerbehandlung für sichere Programmierung

## Synopsis
In Swift ermöglicht das Schlüsselwort `throws` Entwicklern, Fehler in Funktionen zu kennzeichnen und zu behandeln, was zu einer robusteren und sichereren Fehlerbehandlung führt.

## Dokumentation
Das Schlüsselwort `throws` wird in Swift verwendet, um anzugeben, dass eine Funktion potenziell Fehler auslösen kann. Diese Fehler können dann in der aufrufenden Funktion behandelt werden, wodurch die Kontrolle über den Programmfluss bei unerwarteten Bedingungen bleibt.

### Zweck
Die Verwendung von `throws` in Swift erhöht die Lesbarkeit und Wartbarkeit des Codes, indem sie klare Schnittstellen für Fehlerbehandlungen definiert. Funktionen, die `throws` verwenden, müssen in der Lage sein, Fehler zu propagieren, die dann von den aufrufenden Funktionen behandelt werden können.

### Verwendung
Eine Funktion, die Fehler werfen kann, wird mit dem Schlüsselwort `throws` deklariert. Aufrufende Funktionen müssen diese Fehler entweder fangen oder ebenfalls als `throws` deklariert werden.

### Syntax
```swift
func functionName() throws -> ReturnType {
    // Funktionale Logik
}
```

## Beispiele

### Beispiel 1: Einfache Fehlerbehandlung
```swift
enum FileError: Error {
    case fileNotFound
}

func readFile(at path: String) throws -> String {
    guard let content = try? String(contentsOfFile: path) else {
        throw FileError.fileNotFound
    }
    return content
}

do {
    let fileContent = try readFile(at: "example.txt")
    print(fileContent)
} catch FileError.fileNotFound {
    print("Datei wurde nicht gefunden.")
} catch {
    print("Ein unbekannter Fehler ist aufgetreten.")
}
```

### Beispiel 2: Fehlerpropagation
```swift
func parseInt(from string: String) throws -> Int {
    guard let number = Int(string) else {
        throw NSError(domain: "InvalidNumber", code: 1, userInfo: nil)
    }
    return number
}

func convertAndPrint(value: String) {
    do {
        let number = try parseInt(from: value)
        print("Die Zahl ist \(number).")
    } catch {
        print("Fehler beim Konvertieren: \(error.localizedDescription)")
    }
}

convertAndPrint(value: "42") // Gibt "Die Zahl ist 42." aus
convertAndPrint(value: "abc") // Gibt "Fehler beim Konvertieren: ..." aus
```

## Erklärung
Ein häufiges Missverständnis ist, dass die Verwendung von `throws` bedeutet, dass eine Funktion immer einen Fehler auslösen muss. Das ist nicht der Fall. Eine Funktion kann auch fehlerfrei ausgeführt werden. Entwickler sollten auch darauf achten, dass sie Fehler in der richtigen Reihenfolge behandeln, um unerwartete Abstürze zu vermeiden.

Ein weiterer Punkt ist, dass Fehler, die in einer `throws`-Funktion auftreten, nicht ignoriert werden können. Sie müssen entweder in einem `do-catch`-Block behandelt oder an die aufrufende Funktion weitergegeben werden.

## Ein-Satz-Zusammenfassung
Das Schlüsselwort `throws` in Swift ermöglicht eine effektive und strukturierte Fehlerbehandlung in Funktionen, die potenziell fehlerhafte Operationen durchführen.