<!--
Meta Description: # استخدام الكلمة "in" في لغة Swift: دليلك الشامل ## ملخص تُستخدم الكلمة "in" في لغة Swift لتحديد نطاقات الحلقات، وكذلك في تعريف القيم التي تتواجد داخل...
Meta Keywords: number, swift, استخدام, الحلقات, الـ
-->

# استخدام الكلمة "in" في لغة Swift: دليلك الشامل

## ملخص
تُستخدم الكلمة "in" في لغة Swift لتحديد نطاقات الحلقات، وكذلك في تعريف القيم التي تتواجد داخل بنى معينة مثل الـ closures. تعتبر هذه الكلمة عنصرًا أساسيًا في بناء الجمل الشرطية والحلقات.

## الوثائق
### الغرض
تساعد الكلمة "in" المبرمجين في Swift على تحديد نطاقات الحلقات والـ closures، مما يسهل كتابة الأكواد بشكل أكثر تنظيمًا ووضوحًا.

### الاستخدام
1. **داخل الحلقات**: تُستخدم "in" لتحديد نطاق العناصر في الحلقات مثل `for` loops.
   
   ```swift
   for number in 1...5 {
       print(number)
   }
   ```

2. **داخل الـ closures**: تُستخدم "in" لفصل قائمة المعاملات عن جسم الـ closure.
   
   ```swift
   let closureExample: (Int) -> Int = { number in
       return number * 2
   }
   ```

### التفاصيل
- في الحلقات، يتم استخدام "in" لتحديد مجموعة القيم التي سيتم تكرارها.
- في الـ closures، تفصل "in" بين قائمة المعاملات وجسم الـ closure، مما يسهل فهم الوظيفة.

## أمثلة
### مثال 1: استخدام "in" في حلقة for
```swift
for i in 1..<5 {
    print("Current number is \(i)")
}
```

### مثال 2: استخدام "in" في Closure
```swift
let square: (Int) -> Int = { number in
    return number * number
}
print(square(4)) // النتيجة: 16
```

### مثال 3: استخدام "in" مع دالة map
```swift
let numbers = [1, 2, 3, 4]
let doubled = numbers.map { number in
    return number * 2
}
print(doubled) // النتيجة: [2, 4, 6, 8]
```

## الشرح
- **الأخطاء الشائعة**: يمكن أن يحدث لبس بين استخدام "in" في الحلقات وداخل الـ closures. تأكد من استخدام السياق المناسب.
- **ملاحظات إضافية**: يجب الانتباه إلى أن "in" لا تعني دائمًا أن هناك قيمة داخلية، بل تحدد فقط نطاقات معينة. 

## ملخص بجملة واحدة
تستخدم الكلمة "in" في Swift لتحديد نطاقات الحلقات والفصل بين قائمة المعاملات وجسم الـ closures، مما يسهل كتابة أكواد أكثر وضوحًا.