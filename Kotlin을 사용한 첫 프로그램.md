# Kotlin을 사용한 첫 프로그램

[Welcome to Android Basics with Compose](https://youtu.be/lNKk-RSL7wg)

Compose 사용 시 알아야 하는 Android 기본 사항

스니펫 : 재사용 가능한 소스 코드, 텍스트의 작은 부분 간단하게 코드의 일부분을 발췌한 것

```jsx
fun main(){
printfln("Hello, world!")
}
```

Kotlin 프로그램에는 *main 함수*가 있어야 합니다. main 함수란 코드에서 Kotlin 컴파일러가 시작되는 특정 위치입니다. main 함수는 프로그램의 진입점 또는 시작점입니다.

컴파일러 : Kotlin 코드를 컴퓨터가 이해할 수 있는 언어로 바꾸어주는 번역기

함수 → 규격에 맞춰 함수 정의

*함수*
는 특정 작업을 실행하는 프로그램의 세그먼트입니다. 프로그램에 여러 함수를 포함할 수도 있고 하나만 포함할 수도 있습니다.

- fun 키워드
- 함수 이름
- 소괄호
- 중괄호

## **함수 정의와 함수 호출 비교**

먼저 코드에 함수를 *정의*합니다. 즉, 작업을 실행하는 데 필요한 모든 명령을 지정합니다.

함수가 정의되면 함수를 *호출*할 수 있으므로 이 함수 내의 명령을 실행할 수 있습니다.

이렇게 비유해 보겠습니다. 초콜릿 케이크를 만드는 방법에 관한 단계별 명령을 작성합니다. 이 명령 세트의 이름은 `bakeChocolateCake`일 수 있습니다. 케이크를 만들려고 할 때마다 `bakeChocolateCake` 명령을 실행할 수 있습니다. 케이크 3개를 원한다면 `bakeChocolateCake` 명령을 3번 실행해야 합니다. 먼저 단계를 정의하고 이름을 지정합니다. 이를 함수 정의라고 간주할 수 있습니다. 그런 다음 실행하고 싶을 때마다 단계를 참조합니다. 이를 함수 호출로 간주할 수 있습니다.

**참고:** '함수를 선언하다'라는 대체 문구를 들어본 적이 있을 것입니다. '선언하다'와 '정의하다'라는 단어는 서로 바꿔 사용할 수 있으며 의미가 동일합니다. 함수를 정의하는 정확한 코드를 가리키는 '함수 정의' 또는 '함수 선언'이라는 용어도 들어본 적이 있을 것입니다.

## **함수 정의**

다음은 함수를 정의하는 데 필요한 핵심 부분입니다.

- 함수에는 **이름**이 있어야 나중에 호출할 수 있습니다.
- 함수에는 **입력**, 즉 함수 호출 시 제공해야 하는 정보도 필요할 수 있습니다. 함수는 이러한 입력을 사용하여 목적을 달성합니다. 입력이 필요한 것은 선택사항이며 일부 함수에는 입력이 필요하지 않습니다.
- 함수에는 작업을 실행하는 명령이 포함된 **본문**도 있습니다.

### **함수 키워드**

Kotlin에서 함수를 정의하려고 한다는 것을 나타내려면 새 줄에 `fun`(함수의 줄임말)이라는 특수 단어를 사용하세요. 표시된 대로 정확하게 모두 소문자로 `fun`을 입력해야 합니다. func나 function, 다른 철자로 사용할 수 없습니다. Kotlin 컴파일러가 의미를 인식하지 못하기 때문입니다.

이러한 특수 단어는 Kotlin에서 *키워드*라고 하며 Kotlin에서 새 함수를 만드는 등의 특정한 목적으로 예약되어 있습니다.

### **함수 이름**

함수에는 이름이 있어 서로 구별할 수 있습니다. 사람들을 이름으로 식별하는 것과 비슷합니다. 함수 이름은 `fun` 키워드 뒤에 있습니다.

[Kotlin 키워드](https://kotlinlang.org/docs/keyword-reference.html)는 함수 이름으로 사용하지 않는 것이 좋습니다.

함수 이름은 *카멜 표기법* 규칙을 따라야 합니다. 여기서 함수 이름의 첫 번째 단어는 모두 소문자입니다. 이름에 단어가 여러 개 있는 경우 단어 사이에는 공백이 없어야 하며 다른 모든 단어는 대문자로 시작해야 합니다.

![Untitled](Kotlin%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%89%E1%85%A1%E1%84%8B%E1%85%AD%E1%86%BC%E1%84%92%E1%85%A1%E1%86%AB%20%E1%84%8E%E1%85%A5%E1%86%BA%20%E1%84%91%E1%85%B3%E1%84%85%E1%85%A9%E1%84%80%E1%85%B3%E1%84%85%E1%85%A2%E1%86%B7%20e3108d3473a54eefbd36d073902b7c8a/Untitled.png)

### **함수 입력**

함수 이름 뒤에는 항상 괄호가 옵니다. 이러한 괄호는 함수의 입력을 나열하는 위치입니다.

Kotlin에서 지금까지 학습한 내용과 관련된 스타일 가이드 권장사항입니다.

- 함수 이름은 카멜 표기법을 사용해야 하며 동사 또는 동사구여야 합니다.
- 각 문은 한 줄에 하나씩 입력해야 합니다.
- 여는 중괄호는 함수가 시작되는 줄의 끝에 표시되어야 합니다.
- 여는 중괄호 앞에는 공백이 있어야 합니다.
- 함수 본문은 4개 공백으로 들여쓰기되어야 합니다. Tab 문자를 사용하여 코드를 들여쓰기하지 마세요. 공백 4개를 입력하세요.
- 닫는 중괄호는 함수 본문의 마지막 코드 줄 뒤 자체 줄에 있습니다. 닫는 중괄호는 함수 시작 부분에 있는 `fun` 키워드와 정렬되어야 합니다.

## 연습

1. Kotlin 플레이그라운드에서 실행하지 않고 이 프로그램의 코드를 읽고 출력이 무엇인지 추측할 수 있나요?

```kotlin
fun main() {
    println("1")
    println("2")
    println("3")
}

```

추측한 후에는 이 코드를 복사하여 Kotlin 플레이그라운드에 붙여넣고 답을 확인하세요.

`1`

`2`

`3`

1. 프로그램 출력은 다음과 같습니다.

```
1
2
3
```

1. Kotlin 플레이그라운드를 사용하여 다음 메시지를 출력하는 프로그램을 만듭니다.

```kotlin
I'm
learning
Kotlin!

fun main() {
    println("I'm")
    println("learning")
    println("Kotlin!")
}
```

1. 프로그램의 코드는 다음과 같습니다.

```kotlin
fun main() {
    println("I'm")
    println("learning")
    println("Kotlin!")
}
```

1. 이 프로그램을 복사하여 Kotlin 플레이그라운드에 붙여넣습니다.

```kotlin
fun main() {
    println("Tuesday")
    println("Thursday")
    println("Wednesday")
    println("Friday")
    println("Monday")
}

```

1. 다음은 프로그램의 올바른 코드입니다.

```kotlin
fun main() {
    println("Monday")
    println("Tuesday")
    println("Wednesday")
    println("Thursday")
    println("Friday")
}
```

다음 출력이 인쇄되도록 프로그램을 수정합니다.

문제 해결에 관한 초기 연습을 위해 아래 연습에서 오류를 수정합니다. 각 연습의 경우 코드를 브라우저의 Kotlin 플레이그라운드에 복사합니다. 프로그램을 실행해 보면 오류 메시지가 표시됩니다.

1. 올바른 출력이 생성되도록 이 프로그램의 오류를 수정합니다.

```kotlin
fun main() {
    println("Tomorrow is rainy")

```

올바른 출력은 다음과 같습니다.

```kotlin
Tomorrow is rainy
fun main() {
    println("Tomorrow is rainy")}
//괄호를 안닫음
```

1. `main` 함수의 함수 본문 끝을 나타내는 닫는 중괄호가 프로그램의 세 번째 줄에 없습니다.

올바른 코드는 다음과 같습니다.

```kotlin
fun main() {
    println("Tomorrow is rainy")
}
```

1. 올바른 출력이 생성되도록 이 프로그램의 오류를 수정합니다.

```kotlin
fun main() {
    printLine("There is a chance of snow")
}
//Unresolved reference: printLine
```

올바른 출력은 다음과 같습니다.

```kotlin
//There is a chance of snow
fun main() {
    println("There is a chance of snow")
}
```

1. 프로그램을 실행하면 `Unresolved reference: printLine` 오류가 표시됩니다. `printLine()`이 Kotlin에서 인식되는 함수가 아니기 때문입니다. 오류를 일으키는 코드 부분이 Kotlin 플레이그라운드에서 빨간색으로 강조표시된 것도 확인할 수 있습니다. 함수 이름을 `println`으로 변경하여 텍스트 줄을 출력에 인쇄하면 오류가 수정됩니다.

올바른 코드는 다음과 같습니다.

```kotlin
fun main() {
    println("There is a chance of snow")
}
```

1. 올바른 출력이 생성되도록 이 프로그램의 오류를 수정합니다.

```kotlin
fun main() {
    println("Cloudy") 
		println("Partly Cloudy") 
		println("Windy")
}

```

올바른 출력은 다음과 같습니다.

```
Cloudy
Partly Cloudy
Windy
//엔터 주의
```

1. 프로그램을 실행하면 `Unresolved reference: println` 오류가 표시됩니다. 이 메시지에는 문제 해결 방법이 직접 설명되어 있지 않습니다. 이는 오류 문제를 해결할 때 발생할 수도 있으므로 예기치 않은 동작을 해결하려면 코드를 자세히 살펴봐야 합니다.

자세히 살펴보면 코드에서 두 번째 `println()` 함수 호출이 빨간색이며 이는 문제가 발생한 위치를 나타냅니다. Kotlin은 각 줄에 하나의 문만 예상합니다. 이 경우 두 번째와 세 번째 `println()` 함수 호출을 별도의 새 줄로 이동하여 문제를 해결할 수 있습니다.

올바른 코드는 다음과 같습니다.

```kotlin
fun main() {
    println("Cloudy")
    println("Partly Cloudy")
    println("Windy")
}
```

1. 올바른 출력이 생성되도록 이 프로그램의 오류를 수정합니다.

```kotlin
fun main() {
    println("How's the weather today?")
}
//대괄호 주의
```

올바른 출력은 다음과 같습니다.

```
How's the weather today?

```

1. 프로그램을 실행하면 `Function 'main' must have a body` 오류가 표시됩니다. 함수 본문은 여는 괄호와 닫는 괄호( )가 아닌 여는 중괄호와 닫는 중괄호{ } 내에 있어야 합니다.

올바른 코드는 다음과 같습니다.

```kotlin
fun main() {
    println("How's the weather today?")
}
```

## **요약**

- Kotlin 프로그램에는 프로그램의 진입점으로 main 함수가 필요합니다.
- Kotlin에서 함수를 정의하려면 `fun` 키워드, 함수 이름, 괄호로 묶인 입력, 중괄호로 묶인 함수 본문을 차례로 사용합니다.
- 함수 이름은 카멜 표기법 규칙을 따르고 소문자로 시작해야 합니다.
- `println()` 함수 호출을 사용하여 텍스트를 출력에 인쇄합니다.
- Kotlin으로 코딩할 때 따라야 할 형식 지정 및 코드 규칙은 Kotlin 스타일 가이드를 참고하세요.
- 문제 해결은 코드의 오류를 해결하는 프로세스입니다.