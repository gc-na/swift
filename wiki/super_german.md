<!--
Meta Description: # Der `super`-Befehl in Swift: Eine umfassende Anleitung ## Synopsis Der `super`-Befehl in Swift wird verwendet, um auf Methoden, Eigenschaften und In...
Meta Keywords: der, super, klasse, basisklasse, die
-->

# Der `super`-Befehl in Swift: Eine umfassende Anleitung

## Synopsis
Der `super`-Befehl in Swift wird verwendet, um auf Methoden, Eigenschaften und Initialisierer der übergeordneten Klasse zuzugreifen. Dies ist besonders nützlich in der objektorientierten Programmierung, um Funktionalitäten von Basisklassen zu erweitern oder zu überschreiben.

## Dokumentation
In Swift ermöglicht der `super`-Befehl den Zugriff auf die Mitglieder der übergeordneten Klasse, insbesondere wenn Sie eine Methode oder Eigenschaft in einer abgeleiteten Klasse überschreiben. Durch die Verwendung von `super` können Sie sicherstellen, dass die Implementierung der übergeordneten Klasse ordnungsgemäß aufgerufen wird, was wichtig für die korrekte Funktionalität und Initialisierung ist.

### Zweck
Der Hauptzweck von `super` besteht darin, die Beziehung zwischen Basisklasse und abgeleiteter Klasse zu nutzen. Es erlaubt Entwicklern, auf die Funktionen der Basisklasse zuzugreifen und diese gegebenenfalls zu erweitern.

### Verwendung
- **Methodenaufrufe:** Um eine Methode der übergeordneten Klasse innerhalb einer überschriebenen Methode der abgeleiteten Klasse aufzurufen.
- **Eigenschaften:** Um auf Eigenschaften der Basisklasse zuzugreifen.
- **Initialisierer:** Um Initialisierer der Basisklasse aus der abgeleiteten Klasse aufzurufen.

### Details
Der Zugriff auf `super` erfolgt in der Regel innerhalb einer Methode oder eines Initialisierers. Dabei wird `super` gefolgt vom Namen der Methode, Eigenschaft oder Initialisierer, die aufgerufen werden soll.

## Beispiele
Hier sind einige grundlegende Beispiele für die Verwendung von `super` in Swift:

### Beispiel 1: Methodenaufruf
```swift
class BaseClass {
    func greet() {
        print("Hallo aus der Basisklasse!")
    }
}

class SubClass: BaseClass {
    override func greet() {
        super.greet()  // Aufruf der Methode der Basisklasse
        print("Hallo aus der abgeleiteten Klasse!")
    }
}

let obj = SubClass()
obj.greet()
// Ausgabe:
// Hallo aus der Basisklasse!
// Hallo aus der abgeleiteten Klasse!
```

### Beispiel 2: Initialisierer
```swift
class Animal {
    var name: String
    
    init(name: String) {
        self.name = name
    }
}

class Dog: Animal {
    var breed: String
    
    init(name: String, breed: String) {
        self.breed = breed
        super.init(name: name)  // Aufruf des Initialisierers der Basisklasse
    }
}

let myDog = Dog(name: "Bello", breed: "Labrador")
print("\(myDog.name) ist ein \(myDog.breed).")
// Ausgabe: Bello ist ein Labrador.
```

## Erklärung
Ein häufiger Stolperstein bei der Verwendung von `super` ist, dass Entwickler vergessen, `super` aufzurufen, wenn sie eine Methode oder einen Initialisierer überschreiben, der in der Basisklasse definiert ist. Dies kann zu unerwartetem Verhalten führen, da die Funktionalität der Basisklasse nicht ausgeführt wird.

Zusätzlich ist es wichtig zu beachten, dass `super` nur in einer Kontext verwendet werden kann, in dem es eine übergeordnete Klasse gibt. Wenn eine Klasse keine Basisklasse hat, ist die Verwendung von `super` nicht möglich.

## Einzeilensummary
Der `super`-Befehl in Swift ermöglicht den Zugriff auf Methoden und Eigenschaften der übergeordneten Klasse, um deren Funktionalität in abgeleiteten Klassen zu erweitern.