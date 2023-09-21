# union

#include <stdio.h>
union MyUnion {
    int i;
    float f;
    char str[20];
};
int main() {
    union MyUnion u;
    u.i = 42;
    printf("Integer: %d\n", u.i);
    u.f = 3.14;
    printf("Float: %f\n", u.f);
    strcpy(u.str, "Hello, Union!");
    printf("String: %s\n", u.str);
    return 0;
}

# 설명
이 코드는 C 언어를 사용하여 `union`을 사용하는 간단한 예제입니다. `union`을 정의하고, `union` 변수를 선언하며, 다양한 데이터 형식으로 이 변수를 사용하는 방법을 보여줍니다.
1. `#include <stdio.h>`: 표준 입력 및 출력 함수를 사용하기 위한 라이브러리를 포함합니다.
2. `union MyUnion { ... };`: `MyUnion`이라는 `union`을 정의합니다. 이 `union`에는 세 가지 멤버가 있습니다.
   - `int i`: 정수형 멤버
   - `float f`: 부동 소수점형 멤버
   - `char str[20]`: 20개의 문자로 이루어진 문자열 멤버
3. `int main() { ... }`: 프로그램의 진입점인 `main` 함수를 정의합니다.
4. `union MyUnion u;`: `MyUnion` 타입의 `union` 변수 `u`를 선언합니다.
5. `u.i = 42;`: `u`의 `i` 멤버에 정수 값 42를 할당합니다.
6. `printf("Integer: %d\n", u.i);`: `u`의 `i` 멤버를 출력하여 "Integer: 42"와 같은 결과를 출력합니다.
7. `u.f = 3.14;`: `u`의 `f` 멤버에 부동 소수점 값 3.14를 할당합니다.
8. `printf("Float: %f\n", u.f);`: `u`의 `f` 멤버를 출력하여 "Float: 3.140000"과 같은 결과를 출력합니다.
9. `strcpy(u.str, "Hello, Union!");`: `strcpy` 함수를 사용하여 `u`의 `str` 멤버에 문자열 "Hello, Union!"을 복사합니다. 문자열은 `str` 배열에 저장됩니다.
10. `printf("String: %s\n", u.str);`: `u`의 `str` 멤버를 출력하여 "String: Hello, Union!"과 같은 결과를 출력합니다.
이 코드는 `union`을 사용하여 다양한 데이터 형식을 동일한 메모리 공간에서 공유하고 다루는 방법을 보여줍니다. 주의해야 할 점은 하나의 멤버에 값을 할당하면 다른 멤버의 내용이 덮어쓰이므로 주의해야 합니다.

# enum

#include <stdio.h>
enum Boolean {
    false, // 0
    true   // 1
};
int main() {
    enum Boolean isTrue = true;
    if (isTrue) {
        printf("isTrue는 참(True)입니다.\n");
    } else {
        printf("isTrue는 거짓(False)입니다.\n");
    }
    return 0;
}

# 설명
이 코드는 C 언어를 사용하여 열거형(`enum`)을 정의하고, `enum` 상수를 사용하여 참(`true`)과 거짓(`false`)을 나타내는 간단한 프로그램을 보여줍니다.
1. `#include <stdio.h>`: 표준 입력 및 출력 함수를 사용하기 위한 라이브러리를 포함합니다.
2. `enum Boolean { false, true };`: `enum` 키워드를 사용하여 `Boolean`이라는 열거형을 정의합니다. 이 열거형은 `false`와 `true` 두 개의 상수를 가집니다. C에서는 열거형 상수는 기본적으로 0부터 시작하여 순서대로 증가합니다. 따라서 `false`는 0, `true`는 1의 값을 가지게 됩니다.
3. `int main() { ... }`: 프로그램의 진입점인 `main` 함수를 정의합니다.
4. `enum Boolean isTrue = true;`: `Boolean` 타입의 `isTrue` 변수를 선언하고, 초기값으로 `true`를 할당합니다.
5. `if (isTrue) { ... } else { ... }`: `if` 문을 사용하여 `isTrue` 변수의 값이 참(`true`)인지 거짓(`false`)인지를 확인합니다. 만약 `isTrue`가 참이면 "isTrue는 참(True)입니다."를 출력하고, 그렇지 않으면 "isTrue는 거짓(False)입니다."를 출력합니다.
결과적으로, 이 코드는 `enum Boolean`을 사용하여 논리적인 참과 거짓을 나타내고, `if` 문을 사용하여 `isTrue` 변수의 값에 따라 다른 메시지를 출력합니다. 이렇게 `enum`을 사용하면 가독성이 향상되고 코드의 의도가 명확해집니다.
