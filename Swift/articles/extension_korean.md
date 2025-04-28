<!--
Meta Description: # Swift에서의 Extension: 기능 확장하기 ## 개요 Swift의 Extension은 기존 클래스, 구조체, 열거형, 프로토콜에 새로운 기능을 추가할 수 있는 강력한 기능입니다. 이 기능을 통해 소스 코드를 깔끔하게 유지하고, 코드 재사용성을 높이며, 기능을...
Meta Keywords: 기능을, 새로운, customtype, 타입에, extension
-->

# Swift에서의 Extension: 기능 확장하기

## 개요
Swift의 Extension은 기존 클래스, 구조체, 열거형, 프로토콜에 새로운 기능을 추가할 수 있는 강력한 기능입니다. 이 기능을 통해 소스 코드를 깔끔하게 유지하고, 코드 재사용성을 높이며, 기능을 쉽게 확장할 수 있습니다.

## 문서화
Extension은 Swift에서 타입에 새로운 메서드, 프로퍼티, 초기화 방법, 서브스크립트 등을 추가할 수 있는 방법입니다. 이를 통해 기존 타입의 기능을 변경하지 않고도 추가적인 기능을 구현할 수 있습니다. Swift에서 Extension은 다음과 같은 목적으로 사용됩니다:

- **기능 추가**: 기존 타입에 메서드나 프로퍼티를 추가하여 기능을 확장합니다.
- **프로토콜 준수**: 기존 타입에 프로토콜을 적용하여 새로운 기능을 부여합니다.
- **코드 구조화**: 관련된 기능을 그룹화하여 코드의 가독성을 높입니다.

Extension의 기본 문법은 다음과 같습니다:

```swift
extension SomeType {
    // 새로운 메서드 또는 프로퍼티 추가
}
```

## 예제
### 기본 사용 예제

```swift
// String 타입에 Extension 추가
extension String {
    func isPalindrome() -> Bool {
        return self == String(self.reversed())
    }
}

// 사용 예
let word = "level"
print(word.isPalindrome()) // true
```

### 프로토콜 준수 예제

```swift
// CustomType 정의
struct CustomType {
    var value: Int
}

// CustomType에 Equatable 프로토콜 준수 추가
extension CustomType: Equatable {
    static func == (lhs: CustomType, rhs: CustomType) -> Bool {
        return lhs.value == rhs.value
    }
}

// 사용 예
let item1 = CustomType(value: 10)
let item2 = CustomType(value: 10)
print(item1 == item2) // true
```

## 설명
Extension을 사용할 때 주의해야 할 몇 가지 사항이 있습니다:

- **타입 제약**: Extension은 기존 타입에 대해서만 사용할 수 있으며, 새로운 타입을 생성할 수는 없습니다.
- **상속 불가**: Extension에서 추가된 메서드나 프로퍼티는 상속되지 않습니다. 즉, 서브클래스에서 자동으로 사용할 수 없습니다.
- **기존 기능의 재정의 불가**: Extension을 사용하여 기존 메서드를 재정의하거나 변경할 수 없습니다. 만약 동일한 이름의 메서드를 추가하면, 이는 새로운 메서드로 간주됩니다.

이러한 점들을 유념하여 Extension을 활용하면, 더 나은 코드 구조를 가진 Swift 애플리케이션을 작성할 수 있습니다.

## 한 줄 요약
Swift의 Extension은 기존 타입에 새로운 기능을 추가하여 코드의 재사용성과 가독성을 높이는 유용한 도구입니다.