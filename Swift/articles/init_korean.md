<!--
Meta Description: # Swift의 init: 초기화 메서드에 대한 완벽 가이드 ## 개요 Swift에서 `init`은 인스턴스를 초기화하는 데 사용되는 초기화 메서드입니다. 객체 지향 프로그래밍에서 클래스나 구조체의 속성을 설정하고 초기 상태를 정의하는 필수적인 부분입니다. ## 문서화...
Meta Keywords: 초기화, init, string, title, self
-->

# Swift의 init: 초기화 메서드에 대한 완벽 가이드

## 개요
Swift에서 `init`은 인스턴스를 초기화하는 데 사용되는 초기화 메서드입니다. 객체 지향 프로그래밍에서 클래스나 구조체의 속성을 설정하고 초기 상태를 정의하는 필수적인 부분입니다.

## 문서화
`init` 메서드는 클래스 또는 구조체의 인스턴스를 생성할 때 호출됩니다. 이 메서드는 인스턴스를 생성하기 위해 필요한 초기값을 설정할 수 있도록 해줍니다. Swift에서는 기본 초기화, 사용자 정의 초기화, 그리고 편의 초기화(convenience initializer)를 포함한 다양한 초기화 방법을 지원합니다.

### 사용법
- **기본 초기화**: 모든 속성이 기본값을 가질 때 자동으로 생성됩니다.
- **사용자 정의 초기화**: 매개변수를 통해 속성을 설정할 수 있습니다.
- **편의 초기화**: 기본 초기화를 호출하여 다른 초기화 메서드를 보완합니다.

### 초기화 메서드 정의 예시
```swift
class Person {
    var name: String
    var age: Int

    // 사용자 정의 초기화
    init(name: String, age: Int) {
        self.name = name
        self.age = age
    }
}
```

## 예제
아래는 `init`의 기본 사용법을 보여주는 코드 예제입니다.

### 기본 초기화
```swift
class Car {
    var model: String
    var year: Int

    // 사용자 정의 초기화
    init(model: String, year: Int) {
        self.model = model
        self.year = year
    }
}

let myCar = Car(model: "Tesla Model 3", year: 2020)
```

### 편의 초기화
```swift
class Book {
    var title: String
    var author: String

    // 사용자 정의 초기화
    init(title: String, author: String) {
        self.title = title
        self.author = author
    }

    // 편의 초기화
    convenience init(title: String) {
        self.init(title: title, author: "Unknown")
    }
}

let unknownAuthorBook = Book(title: "Swift Programming")
```

## 설명
`init` 메서드 사용 시 주의해야 할 점은 다음과 같습니다:
- 모든 속성이 초기화되어야 합니다. 초기화되지 않은 속성을 사용하려고 하면 컴파일 오류가 발생합니다.
- 클래스의 부모 클래스의 초기화 메서드를 호출해야 하는 경우, `super.init()`을 사용하여 부모 클래스의 초기화 메서드를 호출해야 합니다.
- 초기화가 완료되기 전에 인스턴스의 속성을 사용할 수 없습니다.

## 한 줄 요약
Swift의 `init` 메서드는 객체의 초기 상태를 정의하고 인스턴스를 생성하는 필수적인 기능입니다.