<!--
Meta Description: # القيمة "true" في لغة البرمجة سويفت ## ملخص تُعتبر القيمة "true" واحدة من القيم البوليانية الأساسية في لغة سويفت، حيث تُستخدم لتحديد الحالة الصحيحة أ...
Meta Keywords: true, القيمة, ستخدم, الشرطية, سويفت
-->

# القيمة "true" في لغة البرمجة سويفت

## ملخص
تُعتبر القيمة "true" واحدة من القيم البوليانية الأساسية في لغة سويفت، حيث تُستخدم لتحديد الحالة الصحيحة أو الإيجابية في التعبيرات الشرطية.

## الوثائق
تُستخدم القيمة "true" في سويفت للإشارة إلى حالة صحيحة، وهي جزء لا يتجزأ من أنواع البيانات البوليانية. تُعتبر البوليانات، والتي تشمل "true" و "false"، من الأنواع الأساسية التي تُستخدم في التحكم في تدفق البرنامج عبر الشروط والحلقات. 

### الغرض
تساعد القيمة "true" المطورين على اتخاذ قرارات برمجية بناءً على الشروط، مما يسمح بإجراء العمليات المختلفة استنادًا إلى القيم المنطقية.

### الاستخدام
يمكن استخدام "true" في التعبيرات الشرطية، مثل الجمل الشرطية (if statements) والحلقات (loops) لتحديد متى يجب تنفيذ كود معين.

## أمثلة
### مثال 1: استخدام "true" في جملة شرطية
```swift
let isUserLoggedIn = true

if isUserLoggedIn {
    print("مرحبًا بك!")
} else {
    print("يرجى تسجيل الدخول.")
}
```

### مثال 2: استخدام "true" في حلقة تكرار
```swift
var keepRunning = true

while keepRunning {
    print("الحلقة تعمل.")
    keepRunning = false // لضمان إنهاء الحلقة
}
```

## الشرح
من الشائع أن يواجه المطورون بعض المفاهيم الخاطئة حول استخدام "true". على سبيل المثال، قد يعتقد البعض أن "true" يمكن أن تُستخدم كقيمة افتراضية في جميع المواضع، لكن يجب دائمًا مراعاة النوع المحدد للمتغيرات. 

### ملاحظات إضافية
- استخدم "true" في التعبيرات الشرطية فقط عندما تكون الحالة تمثل حقيقة منطقية.
- تأكد من عدم خلط "true" مع القيم الأخرى مثل الأرقام أو السلاسل النصية.

## ملخص جملة واحدة
القيمة "true" في سويفت تُستخدم لتحديد الحالة الصحيحة في التعبيرات الشرطية، مما يسهل التحكم في تدفق البرنامج.