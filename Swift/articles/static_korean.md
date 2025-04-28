<!--
Meta Description: # Swift의 static 키워드: 정적 속성과 메소드 이해하기 ## 개요 Swift에서 `static` 키워드는 클래스, 구조체, 또는 열거형 내에서 정적 속성 및 메소드를 정의하는 데 사용됩니다. 이는 인스턴스가 아닌 타입 자체에 속하는 속성과 메소드를 나타냅니다...
Meta Keywords: static, 속성과, 키워드는, 메소드를, 있습니다
-->

# Swift의 static 키워드: 정적 속성과 메소드 이해하기

## 개요
Swift에서 `static` 키워드는 클래스, 구조체, 또는 열거형 내에서 정적 속성 및 메소드를 정의하는 데 사용됩니다. 이는 인스턴스가 아닌 타입 자체에 속하는 속성과 메소드를 나타냅니다.

## 문서화
`static` 키워드는 주로 다음과 같은 목적을 가집니다:

- **정적 속성 정의**: `static`을 사용하여 클래스나 구조체에 속하는 속성을 정의할 수 있습니다. 이러한 속성은 인스턴스를 생성하지 않고도 접근할 수 있습니다.
- **정적 메소드 정의**: `static` 메소드는 타입에 소속되어 있으며, 인스턴스를 생성하지 않고도 호출할 수 있습니다.
- **전역 상태 관리**: 공통적으로 사용되는 데이터를 관리하거나, 공통 기능을 제공하는 데 적합합니다.

### 사용 방법
`static` 키워드는 다음과 같이 사용됩니다:

```swift
class MyClass {
    static var staticProperty = "나는 정적 속성입니다."
    
    static func staticMethod() {
        print("나는 정적 메소드입니다.")
    }
}
```

정적 속성과 메소드는 타입 이름을 통해 접근할 수 있습니다:

```swift
print(MyClass.staticProperty) // 출력: 나는 정적 속성입니다.
MyClass.staticMethod() // 출력: 나는 정적 메소드입니다.
```

## 예제
다음은 `static`을 사용한 간단한 예제입니다.

```swift
struct Circle {
    static let pi = 3.14
    
    static func area(radius: Double) -> Double {
        return pi * radius * radius
    }
}

let areaOfCircle = Circle.area(radius: 5) // 출력: 78.5
print("원의 면적: \(areaOfCircle)")
```

## 설명
### 일반적인 함정 및 주의 사항
- **인스턴스와의 혼동**: `static` 속성 및 메소드는 인스턴스와는 다릅니다. 인스턴스의 속성이나 메소드를 사용하려면 `self` 키워드를 사용해야 하며, `static`과 혼동해서는 안 됩니다.
- **상속 불가**: `static` 메소드는 서브클래스에서 오버라이드할 수 없습니다. 이는 정적 메소드가 타입에 고정되기 때문입니다.
- **전역 상태 관리 주의**: 정적 속성을 사용하면 전역 상태를 관리할 수 있지만, 이로 인해 상태 관리가 복잡해질 수 있으므로 주의가 필요합니다.

## 한 줄 요약
Swift의 `static` 키워드는 클래스, 구조체, 또는 열거형에 속하는 정적 속성과 메소드를 정의하는 데 사용됩니다.