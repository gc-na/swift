<!--
Meta Description: # Swift의 fallthrough: 사용법 및 예제 ## 개요 Swift의 `fallthrough`는 switch 문에서 사용되는 키워드로, 서로 다른 케이스 간에 제어 흐름을 전달할 수 있도록 합니다. 기본적으로 Swift의 switch 문은 각 케이스의 실행 후...
Meta Keywords: fallthrough, switch, swift의, 케이스로, print
-->

# Swift의 fallthrough: 사용법 및 예제

## 개요
Swift의 `fallthrough`는 switch 문에서 사용되는 키워드로, 서로 다른 케이스 간에 제어 흐름을 전달할 수 있도록 합니다. 기본적으로 Swift의 switch 문은 각 케이스의 실행 후에 자동으로 종료되지만, `fallthrough`를 사용하면 다음 케이스로 넘어갈 수 있습니다.

## 문서화
`fallthrough`는 Swift의 switch 문에서 특정 조건을 만족한 후, 다음 케이스로 제어를 넘기기 위해 사용됩니다. 이는 특히 여러 케이스가 비슷한 코드를 실행해야 할 때 유용합니다. 

### 목적
`fallthrough`의 주된 목적은 각 케이스에서 코드 실행을 멈추지 않고, 다음 케이스로 진행할 수 있게 하는 것입니다. 이는 C 언어와 같은 다른 언어에서의 switch 문과 비슷한 동작을 제공합니다.

### 사용법
`fallthrough`는 switch 문 내에서 특정 케이스의 코드 블록 끝에 위치합니다. 이를 사용하면 현재 케이스에서 실행이 완료된 후, 다음 케이스로 자동으로 이동합니다.

## 예제
다음은 `fallthrough`의 기본 사용 예제입니다.

```swift
let number = 2

switch number {
case 1:
    print("One")
case 2:
    print("Two")
    fallthrough
case 3:
    print("Three")
default:
    print("Other")
}
```
위의 예제에서 `number`가 2일 경우, 출력 결과는 다음과 같습니다:
```
Two
Three
```
`fallthrough`를 사용하지 않았다면 `Two`만 출력되었을 것입니다.

## 설명
`fallthrough`를 사용할 때 주의해야 할 점은, 다음 케이스로 넘어갈 때 조건이 평가되지 않는다는 것입니다. 즉, 다음 케이스가 실행될 때 그 케이스의 조건이 충족되지 않아도 실행됩니다. 이로 인해 의도치 않은 결과가 발생할 수 있습니다.

### 일반적인 함정
- `fallthrough`를 사용할 경우, 다음 케이스에 대한 조건이 무시되므로 주의해야 합니다.
- 코드의 가독성을 해칠 수 있으므로, 명확한 의도가 있을 때만 사용하는 것이 좋습니다.
- Swift의 `fallthrough`는 C 언어의 `fallthrough`와는 다소 다르게 작동하며, C의 경우에는 조건 평가가 유지됩니다.

## 한 줄 요약
Swift의 `fallthrough`는 switch 문에서 현재 케이스를 종료하지 않고 다음 케이스로 제어를 넘길 수 있도록 하는 기능입니다.