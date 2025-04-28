<!--
Meta Description: # Swift에서의 self: 객체 지향 프로그래밍의 핵심 ## 개요 Swift에서 `self`는 현재 인스턴스를 참조하는 특별한 키워드입니다. 객체 지향 프로그래밍에서 인스턴스 변수와 메서드를 구분하는 데 유용하며, 클래스와 구조체에서 자주 사용됩니다. ## 문서화 ...
Meta Keywords: self, property, name, 사용하여, 인스턴스
-->

# Swift에서의 self: 객체 지향 프로그래밍의 핵심

## 개요
Swift에서 `self`는 현재 인스턴스를 참조하는 특별한 키워드입니다. 객체 지향 프로그래밍에서 인스턴스 변수와 메서드를 구분하는 데 유용하며, 클래스와 구조체에서 자주 사용됩니다.

## 문서화
`self`는 다음과 같은 목적과 용도로 사용됩니다:

- **현재 인스턴스 참조**: 클래스나 구조체의 메서드 내에서 현재 객체의 속성이나 메서드에 접근할 때 사용됩니다.
- **이름 충돌 해결**: 매개변수와 프로퍼티의 이름이 같을 때, `self`를 사용하여 현재 인스턴스의 프로퍼티를 명확히 구분할 수 있습니다.
- **클로저 내에서의 참조**: 클로저에서 `self`를 사용하여 인스턴스에 접근할 수 있습니다.

### 사용법
`self`는 클래스, 구조체, 또는 열거형의 메서드와 초기화 구문 내에서 사용되며, 다음과 같은 형식으로 표현됩니다:

```swift
class MyClass {
    var property: Int

    init(property: Int) {
        self.property = property // self를 사용하여 인스턴스의 property에 접근
    }

    func display() {
        print("Property value: \(self.property)") // self를 사용하여 메서드 내 인스턴스 변수 참조
    }
}
```

## 예제
다음은 `self`를 사용하는 간단한 예제입니다:

```swift
class Person {
    var name: String
    
    init(name: String) {
        self.name = name // 매개변수 name과 프로퍼티 name의 구분
    }
    
    func greet() {
        print("안녕하세요, 제 이름은 \(self.name)입니다.")
    }
}

let person = Person(name: "홍길동")
person.greet() // 출력: 안녕하세요, 제 이름은 홍길동입니다.
```

## 설명
`self`를 사용할 때 주의해야 할 몇 가지 사항이 있습니다:

- **명시적 필요성**: 매개변수와 인스턴스 프로퍼티의 이름이 같을 경우, `self`를 사용하여 어떤 값을 참조하고 있는지 명확히 해야 합니다.
- **클로저의 강한 참조**: 클로저 내에서 `self`를 사용할 때, 강한 참조 사이클을 피하기 위해 `[weak self]` 또는 `[unowned self]`를 사용하는 것이 좋습니다.
- **상속**: 상속에서 `self`는 서브클래스의 인스턴스를 가리키므로, 부모 클래스의 메서드를 호출할 때 주의해야 합니다.

## 한 줄 요약
Swift에서 `self`는 현재 인스턴스를 참조하며, 객체의 속성과 메서드를 명확히 구분하는 데 중요한 역할을 합니다.