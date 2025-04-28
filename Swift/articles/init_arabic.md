<!--
Meta Description: # استخدام init في لغة Swift: الدليل الشامل ## الملخص `init` هو مبدأ أساسي في لغة Swift يُستخدم لتهيئة الكائنات (objects) وتحديد القيم الأولية للخصائص ...
Meta Keywords: init, self, swift, var, الكائنات
-->

# استخدام init في لغة Swift: الدليل الشامل

## الملخص
`init` هو مبدأ أساسي في لغة Swift يُستخدم لتهيئة الكائنات (objects) وتحديد القيم الأولية للخصائص (properties) عند إنشاء الكائنات من الفئات (classes) أو التركيب (structs).

## الوثائق
تُعتبر دالة `init` (المُهيئ) جزءًا أساسيًا من جميع الفئات والتركيبات في Swift. يتم استخدامه لتعيين القيم الأولية لخصائص الكائن. تقوم `init` بتأمين أن كل كائن يتم إنشاؤه يكون في حالة صالحة للاستخدام. يمكنك تعريف مُهيئات متعددة (overloaded initializers) داخل نفس الفئة أو التركيب، مما يوفر مرونة في كيفية إنشاء الكائنات.

### الهدف
- تهيئة الكائنات مع القيم الأولية.
- ضمان أن الكائنات تكون في حالة صالحة.

### الاستخدام
يمكن استخدام `init` كالتالي:
```swift
class ClassName {
    var propertyName: Type

    init(propertyName: Type) {
        self.propertyName = propertyName
    }
}
```
يمكنك أيضًا استخدام المُهيئات الافتراضية (default initializers) لتركيبات لا تحتوي على خصائص متعمدة.

## أمثلة
### مثال 1: مُهيئ بسيط
```swift
struct Person {
    var name: String
    var age: Int

    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
}

let person = Person(name: "أحمد", age: 30)
```

### مثال 2: مُهيئ افتراضي
```swift
struct Car {
    var make: String
    var model: String
    var year: Int
    
    // مُهيئ افتراضي
    init() {
        self.make = "غير محدد"
        self.model = "غير محدد"
        self.year = 2023
    }
}

let defaultCar = Car()
```

### مثال 3: مُهيئ متعدد
```swift
class Rectangle {
    var width: Double
    var height: Double

    init(width: Double, height: Double) {
        self.width = width
        self.height = height
    }

    init(squareSide: Double) {
        self.width = squareSide
        self.height = squareSide
    }
}

let rect = Rectangle(width: 5.0, height: 10.0)
let square = Rectangle(squareSide: 4.0)
```

## الشرح
### الأخطاء الشائعة
- **عدم تهيئة الخصائص:** إذا لم تقم بتهيئة جميع الخصائص قبل انتهاء المُهيئ، ستواجه خطأ في الكود.
- **استخدام المُهيئات المتعددة بنفس المعلمات:** قد يحدث لبس إذا كانت أسماء المعلمات متشابهة، لذا يُفضل استخدام أسماء واضحة.

### ملاحظات إضافية
- يُمكن استخدام `self` للإشارة إلى الخصائص داخل المُهيئ لتجنب أي لبس مع المعلمات.
- يمكن أن تحتوي الفئات على مُهيئات مخصصة تجعلها أكثر مرونة في كيفية إنشاء الكائنات.

## ملخص بجملة واحدة
`init` في Swift هو وسيلة حيوية لتهيئة الكائنات وتحديد خصائصها عند إنشائها.