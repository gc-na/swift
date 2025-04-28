<!--
Meta Description: # Swift에서의 "case" 사용법: 열거형과 패턴 매칭 ## 개요 Swift의 `case`는 주로 열거형(Enums)과 switch 문에서 사용되며, 다양한 조건을 검사하거나 특정 패턴에 따라 분기하는 데 유용합니다. 이 명령은 코드의 가독성을 높이고, 조건부 로...
Meta Keywords: case, switch, print, 사용됩니다, 열거형의
-->

# Swift에서의 "case" 사용법: 열거형과 패턴 매칭

## 개요
Swift의 `case`는 주로 열거형(Enums)과 switch 문에서 사용되며, 다양한 조건을 검사하거나 특정 패턴에 따라 분기하는 데 유용합니다. 이 명령은 코드의 가독성을 높이고, 조건부 로직을 간결하게 작성할 수 있도록 돕습니다.

## 문서화
`case`는 Swift의 제어 흐름 문 중 하나로, 주로 switch 문에서 사용됩니다. 또한, 열거형의 각 케이스를 정의하는 데에도 사용됩니다. 

### 목적
- 여러 조건을 간결하게 처리하기 위해 사용됩니다.
- 열거형의 각 값에 대해 특정 동작을 정의할 수 있습니다.

### 사용법
`case`는 switch 문 내에서 다음과 같이 사용됩니다:

```swift
switch someValue {
case value1:
    // value1에 대한 동작
case value2:
    // value2에 대한 동작
default:
    // 기본 동작
}
```

열거형을 정의할 때는 다음과 같이 사용할 수 있습니다:

```swift
enum Direction {
    case north
    case south
    case east
    case west
}
```

## 예제
다음은 `case`를 사용한 간단한 예제입니다.

### 열거형 예제
```swift
enum Weather {
    case sunny
    case rainy
    case cloudy
}

let todayWeather = Weather.sunny

switch todayWeather {
case .sunny:
    print("오늘은 맑습니다.")
case .rainy:
    print("오늘은 비가 옵니다.")
case .cloudy:
    print("오늘은 흐립니다.")
}
```

### 스위치 문 예제
```swift
let number = 3

switch number {
case 1:
    print("숫자는 1입니다.")
case 2:
    print("숫자는 2입니다.")
case 3:
    print("숫자는 3입니다.")
default:
    print("숫자는 1, 2, 3이 아닙니다.")
}
```

## 설명
`case`를 사용할 때 주의할 점은 다음과 같습니다:

- **순서**: switch 문은 위에서 아래로 실행되므로, 더 구체적인 케이스는 더 일반적인 케이스보다 위에 위치해야 합니다.
- **default**: 모든 가능한 케이스를 다루지 않을 경우, `default`를 사용하여 처리하지 않은 경우를 지정할 수 있습니다.
- **열거형의 연관 값**: 열거형에 연관 값을 사용할 경우, `case`를 활용해 조건부로 값을 추출할 수 있습니다.

## 한 줄 요약
Swift에서 `case` 키워드는 주로 switch 문과 열거형의 분기를 처리하는 데 사용됩니다.