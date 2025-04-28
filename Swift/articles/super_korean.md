<!--
Meta Description: # Swift에서 "super" 키워드의 이해 ## 개요 Swift 프로그래밍 언어에서 "super" 키워드는 서브클래스가 슈퍼클래스의 메서드나 프로퍼티에 접근할 때 사용되는 중요한 키워드입니다. 이 키워드는 상속 관계를 효과적으로 관리하고, 부모 클래스의 기능을 확장...
Meta Keywords: super, 메서드, 초기화, 슈퍼클래스의, 클래스의
-->

# Swift에서 "super" 키워드의 이해

## 개요
Swift 프로그래밍 언어에서 "super" 키워드는 서브클래스가 슈퍼클래스의 메서드나 프로퍼티에 접근할 때 사용되는 중요한 키워드입니다. 이 키워드는 상속 관계를 효과적으로 관리하고, 부모 클래스의 기능을 확장하거나 재정의할 수 있도록 돕습니다.

## 문서화
### 목적
"super"는 서브클래스가 슈퍼클래스의 메서드, 초기화 메서드 및 프로퍼티에 접근할 수 있도록 해줍니다. 이를 통해 상속된 기능을 활용하거나 수정할 수 있습니다.

### 사용법
"super"는 주로 메서드 오버라이딩 시 사용되며, 슈퍼클래스의 메서드를 호출할 때 사용됩니다. 예를 들어, 서브클래스에서 부모 클래스의 초기화 메서드를 호출할 때 사용될 수 있습니다.

### 세부사항
- 메서드 오버라이딩: 서브클래스에서 슈퍼클래스의 메서드를 재정의할 때 "super"를 사용하여 부모 메서드를 호출할 수 있습니다.
- 초기화: 서브클래스의 초기화 메서드에서 "super.init()"를 호출하여 부모 클래스의 초기화 메서드를 실행해야 합니다.
- 프로퍼티 접근: 서브클래스에서 슈퍼클래스의 프로퍼티를 사용할 때도 "super"를 사용할 수 있습니다.

## 예제
### 기본 사용 예제
```swift
class Animal {
    func makeSound() {
        print("Some sound")
    }
}

class Dog: Animal {
    override func makeSound() {
        super.makeSound() // 부모 클래스의 메서드 호출
        print("Bark")
    }
}

let myDog = Dog()
myDog.makeSound() // 출력: Some sound\nBark
```

### 초기화 메서드 예제
```swift
class Vehicle {
    var wheels: Int

    init(wheels: Int) {
        self.wheels = wheels
    }
}

class Car: Vehicle {
    var brand: String

    init(brand: String) {
        self.brand = brand
        super.init(wheels: 4) // 부모 클래스 초기화 호출
    }
}

let myCar = Car(brand: "Toyota")
print(myCar.wheels) // 출력: 4
```

## 설명
"super" 키워드를 사용할 때 주의해야 할 점은 메서드 오버라이딩 시 부모 메서드의 호출 순서입니다. 오버라이딩한 메서드 내에서 "super"를 호출하지 않으면 부모 클래스의 기능이 실행되지 않을 수 있습니다. 또한, 초기화 메서드에서 반드시 "super.init()"을 호출하여 부모 클래스의 초기화가 완료되어야 합니다. 그렇지 않으면 컴파일 오류가 발생할 수 있습니다.

## 한 줄 요약
Swift의 "super" 키워드는 서브클래스가 슈퍼클래스의 메서드와 프로퍼티에 접근하는 데 사용되는 핵심 키워드입니다.