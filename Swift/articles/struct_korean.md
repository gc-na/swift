<!--
Meta Description: # Swift에서 Struct: 구조체의 이해와 활용 ## 개요 Swift의 `struct`는 데이터와 관련된 속성(프로퍼티)과 메서드를 포함하는 사용자 정의 데이터 타입입니다. Swift의 구조체는 값 타입으로, 데이터의 복사본이 생성되어 전달됩니다. 이는 메모리 관...
Meta Keywords: struct, name, 데이터, 구조체는, var
-->

# Swift에서 Struct: 구조체의 이해와 활용

## 개요
Swift의 `struct`는 데이터와 관련된 속성(프로퍼티)과 메서드를 포함하는 사용자 정의 데이터 타입입니다. Swift의 구조체는 값 타입으로, 데이터의 복사본이 생성되어 전달됩니다. 이는 메모리 관리와 데이터 안전성을 높이는 데 도움을 줍니다.

## 문서화
Swift에서 `struct`는 복잡한 데이터 모델을 만들기 위해 사용됩니다. 구조체는 속성과 메서드를 정의할 수 있으며, 이를 통해 데이터와 동작을 함께 묶어 사용할 수 있습니다. 구조체는 클래스와 유사하지만, 클래스와는 달리 상속이 불가능하고 값 타입입니다. 

### 목적
- 데이터 모델링: 관련된 데이터를 그룹화하여 표현합니다.
- 메서드 정의: 데이터를 조작하는 기능을 추가합니다.
- 값 타입: 데이터의 안전한 복사를 보장합니다.

### 사용법
구조체는 `struct` 키워드를 사용해 정의합니다. 초기화 메서드와 다양한 메서드를 포함할 수 있으며, 프로퍼티를 통해 상태를 유지합니다. 기본적으로 Swift는 구조체에 멤버와이즈 초기화(memberswise initialization)를 제공합니다.

## 예제
### 기본 구조체 정의
```swift
struct Person {
    var name: String
    var age: Int
}

let john = Person(name: "John", age: 30)
print("이름: \(john.name), 나이: \(john.age)")
```

### 메서드 포함
```swift
struct Rectangle {
    var width: Double
    var height: Double
    
    func area() -> Double {
        return width * height
    }
}

let myRectangle = Rectangle(width: 5.0, height: 3.0)
print("사각형의 면적: \(myRectangle.area())")
```

### 구조체의 값 타입 특성
```swift
var original = Person(name: "Jane", age: 25)
var copy = original
copy.name = "Alice"

print("원본 이름: \(original.name), 복사본 이름: \(copy.name)")
```

## 설명
구조체를 사용할 때 주의할 점은 다음과 같습니다:
- **값 타입**: 구조체는 값 타입이므로, 변수에 할당할 때마다 복사본이 생성됩니다. 이는 데이터의 독립성을 보장하지만, 의도치 않은 데이터 변경을 방지하는 데 주의해야 합니다.
- **상속 불가능**: 구조체는 클래스와 달리 다른 구조체로부터 상속받을 수 없습니다. 따라서, 기능 확장이 필요할 경우 클래스를 고려해야 합니다.
- **이니셜라이저**: 기본 이니셜라이저가 자동으로 제공되지만, 커스텀 초기화를 원하는 경우, 사용자 정의 초기화 메서드를 추가할 수 있습니다.

## 한 줄 요약
Swift의 `struct`는 데이터와 관련된 속성 및 메서드를 포함하는 값 타입의 사용자 정의 데이터 구조체입니다.