<!--
Meta Description: # Swift의 private 접근 제어자 ## 개요 Swift에서 `private` 키워드는 클래스, 구조체, 열거형 및 확장 내에서 정의된 속성이나 메소드를 외부에서 접근할 수 없도록 제한하는 접근 제어자입니다. 이를 통해 코드의 캡슐화를 강화하고, 객체 지향 프로...
Meta Keywords: private, 접근할, example, 구조체, 코드의
-->

# Swift의 private 접근 제어자

## 개요
Swift에서 `private` 키워드는 클래스, 구조체, 열거형 및 확장 내에서 정의된 속성이나 메소드를 외부에서 접근할 수 없도록 제한하는 접근 제어자입니다. 이를 통해 코드의 캡슐화를 강화하고, 객체 지향 프로그래밍의 원칙을 준수할 수 있습니다.

## 문서화
`private` 접근 제어자는 해당 요소가 정의된 범위 내에서만 접근할 수 있도록 제한합니다. 이는 코드의 유지 보수성과 안전성을 높이는 데 기여합니다. `private`로 선언된 속성과 메소드는 같은 클래스나 구조체 내에서만 사용 가능하며, 외부 클래스나 구조체에서 접근할 수 없습니다.

### 사용 목적
- **캡슐화**: 객체의 내부 상태를 보호하고, 외부의 직접적인 접근을 차단합니다.
- **코드 안전성**: 잘못된 데이터 변경으로 인한 오류를 예방합니다.
- **유지 보수성**: 코드의 구조를 명확히 하여, 다른 개발자가 코드를 이해하기 쉽게 만듭니다.

## 예제
```swift
class Example {
    private var secretNumber: Int = 42
    
    private func revealSecret() -> Int {
        return secretNumber
    }
    
    func showSecret() -> Int {
        return revealSecret() // 내부에서 접근 가능
    }
}

let example = Example()
// print(example.secretNumber) // 오류 발생: 'secretNumber'에 접근할 수 없음
print(example.showSecret()) // 42 출력
```

## 설명
- **내부 접근 제한**: `private`으로 선언된 속성이나 메소드는 해당 클래스 또는 구조체 내에서만 접근할 수 있으므로, 외부에서 직접적으로 접근하려고 하면 컴파일 오류가 발생합니다.
- **확장 및 서브클래싱**: `private`으로 선언된 요소는 그 요소가 선언된 타입의 서브클래스에서도 접근할 수 없습니다. 따라서, 접근 제어를 통해 속성과 메소드의 노출을 완전히 차단할 수 있습니다.
- **예외 처리**: `private`로 설정된 요소가 필요한 경우, 공용 메소드를 통해 간접적으로 접근할 수 있도록 설계하는 것이 좋습니다.

## 한 줄 요약
Swift의 `private` 접근 제어자는 클래스나 구조체 내에서만 접근할 수 있도록 제한하여 코드의 안전성과 유지 보수성을 높이는 데 기여합니다.