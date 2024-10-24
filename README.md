# java-racingcar-precourse

## **구현 기능 목록**

### [✅] 기능 1: 자동차 이름 입력 및 검증
- 사용자가 경주할 자동차 이름을 입력하면 쉼표(,)를 기준으로 각 자동차의 이름을 분리한다.
  - 각 자동차 이름은 5자 이하만 가능하다.
  - 잘못된 이름이 입력된 경우 `IllegalArgumentException`을 발생시키고 애플리케이션은 종료된다.
  - (`validateCarNames` 함수로 입력된 자동차 이름을 검증한다.)

### [✅] 기능 2: 자동차 전진 및 정지 처리
- 각 자동차는 0에서 9 사이의 무작위 값을 바탕으로 전진하거나 멈춘다.
  - 무작위 값이 4 이상일 경우 자동차는 전진한다.
  - (`moveCar` 함수로 무작위 값을 기반으로 자동차를 이동시킨다.)

### [✅] 기능 3: 이동 횟수 입력 및 검증
- 사용자가 자동차 경주 시도 횟수를 입력하면, 해당 횟수만큼 경주가 진행된다.
  - 잘못된 값이 입력된 경우 `IllegalArgumentException`을 발생시키고 애플리케이션은 종료된다.
  - (`validateAttemptCount` 함수로 입력된 시도 횟수를 검증한다.)

### [✅] 기능 4: 경주 진행 및 결과 출력
- 각 시도마다 모든 자동차의 이동 결과를 출력한다.
  - 예: `pobi : --`, `woni : ----`, `jun : ---`
  - (`printRaceResult` 함수로 각 시도 결과를 출력한다.)

### [] 기능 5: 우승자 판별
- 모든 이동이 끝난 후 가장 많이 전진한 자동차를 우승자로 판별한다.
  - 우승자가 여러 명일 경우 쉼표(,)로 구분하여 출력한다.
  - (`determineWinners` 함수로 최종 우승자를 판별한다.)
  - 예: `최종 우승자 : pobi, jun`

### [] Test: 테스트 케이스 작성 및 실행


## **개선할 사항**
- 고정된 값(예: 무작위 값의 범위, 전진 기준값 등)은 상수로 관리하여 유지보수를 용이하게 한다.
- 예외 처리 시 명확한 예외 메시지를 설정하여 가독성을 높인다.
- 에러메세지를 상수 혹은 Enum으로 관리한다.
- 함수명 및 변수명은 기능을 명확히 드러내도록 작성한다.


# **과제 진행 요구 사항**

### [] Commit Convention
- Git의 커밋 단위는 앞 단계에서 README.md에 정리한 기능 목록 단위로 추가한다.
- [AngularJS Git Commit Message Conventions](https://gist.github.com/stephenparish/9941e89d80e2bc58a153)을 참고해 커밋 메시지를 작성한다.
- 자세한 과제 진행 방법은 프리코스 진행 가이드 문서를 참고한다.


# **프로그래밍 요구 사항**

### [✅] 프로그래밍 요구 사항 1
- JDK 21 버전에서 실행 가능해야 한다.
- 프로그램 실행의 시작점은 `Application`의 `main()`이다.
- build.gradle 파일은 변경할 수 없으며, 제공된 라이브러리 이외의 외부 라이브러리는 사용하지 않는다.
- 프로그램 종료 시 `System.exit()`를 호출하지 않는다.
- 자바 코드 컨벤션을 지키면서 프로그래밍한다.
- 기본적으로 Java Style Guide를 원칙으로 한다.

### [✅] 프로그래밍 요구 사항 2
- 들여쓰기 깊이(Indent depth)를 2까지만 허용한다.
- 삼항 연산자를 사용하지 않는다.
- 함수(또는 메서드)는 한 가지 일만 하도록 최대한 작게 만들어라.
- JUnit 5와 AssertJ를 이용하여 정리한 기능 목록이 정상적으로 작동하는지 테스트 코드로 확인한다.


### [✅]  라이브러리
- `camp.nextstep.edu.missionutils`에서 제공하는 `Randoms` 및 `Console` API를 사용하여 구현해야 한다.
- Random 값 추출은 `camp.nextstep.edu.missionutils.Randoms`의 `pickNumberInRange()`를 활용한다.
- 사용자가 입력하는 값은 `camp.nextstep.edu.missionutils.Console`의 `readLine()`을 활용한다.