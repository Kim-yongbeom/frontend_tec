# 프론트엔드 기술면접

## 브라우저 작동원리
<img width="701" alt="스크린샷 2022-05-11 오전 12 03 40" src="https://user-images.githubusercontent.com/89058117/167660451-2f21e802-766a-4cc8-b2e6-67a64aa1ad1a.png">


## 자바스크립트의 특징
- 자바스크립트는 객체 기반의 스크립트 언어이다.
- 자바스크립트는 동적이며, 타입을 명시할 필요가 없는 인터프리터 언어이다.
- 자바스크립트는 객체 지향형 프로그래밍과 함수형 프로그래밍을 모두 표현할 수 있다.
```
C언어와 같은 언어는 소스 파일을 작성한 후, 해당 파일을 컴파일(compile)하여 사용자가 실행할 수 있는 실행 파일(.exe)로 만들어 사용합니다.
하지만 인터프리터 언어는 이러한 컴파일 작업을 거치지 않고, 소스 코드를 바로 실행할 수 있는 언어를 의미합니다.
자바스크립트는 웹 브라우저에 포함된 자바스크립트 인터프리터가 소스 코드를 직접 해석하여 바로 실행해 줍니다.
```

## 변수 설정
- var는 함수 스코프이다. 함수 스코프는 함수 내에서 선언된 변수만 지역 변수가 된다
- let, const는 블록 스코프이다. 블록 스코프는 모든 코드 블록에서 선언된 변수는 코드 블록 내에서만 유효하며 외부에서는 접근할 수 없다.

## 호이스팅
- JavaScript에서 호이스팅(hoisting)이란, 
- 인터프리터가 변수와 함수의 메모리 공간을 선언 전에 미리 할당하는 것을 의미합니다.
- 호이스팅을 설명할 땐 주로 "변수의 선언과 초기화를 분리한 후, 선언만 코드의 최상단으로 옮기는" 것으로 말하곤 합니다.
- 스코프 내부 어디서든 변수 선언은 최상위에서 선언된 것 처럼 행동
- var는 선언과 초기화가 동시에 일어나 호이스팅시 정상 작동, 그러나 초기엔 undefined
- let은 선언과 초기화가 따로 일어난다 호이스팅되면서 선언 단계가 이뤄지지만 초기화 단계는 실제 코드에 도달했을때 되기때문에 레퍼런스 에러가 발생한다.
- const는 선언, 초기화, 할당이 동시에 이뤄진다.
```
catName("클로이");

function catName(name) {
  console.log("제 고양이의 이름은 " + name + "입니다");
}

/*
결과: "제 고양이의 이름은 클로이입니다"
*/
```
- 함수 호출이 함수 자체보다 앞서 존재하지만, 그럼에도 불구하고 이 코드 역시 동작합니다. 이것이 JavaScript에서 실행 맥락이 동작하는 방식입니다.

## 클로저
