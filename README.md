# functional_programming_study

함수형 프로그래밍 자바스크립트 스터디

교제로 사용하는 책은 함수형 자바스크립트 한빛미디어: http://www.hanbit.co.kr/store/books/look.php?p_code=B2731337630

책의 자세한 내용은 작성하지 않고 계념적으로 얻는 부분과 기억하면 좋을 키워드 및 계념을 정리하기 위한 repo

## 1회차 (2018.10.2)

1장에서는 순수함수에 대한 설명이 대부분이었다. 무상태성 불변성을 확보하는 방법과, 효용성에대 한 설명이었음.

무상태성에 대한 이해는 전역으로 어디에서든 접근하고 조작이 가능한 상태값을 함수에서 제어 할수 있게 하지 않아야 한다는 의미였다.
참조투명성이란 계념을 추가해서 인자로 넘어온 값을 제어 하기 위함으로 함수를 사용하고 외부 변수에 종속적이지 않은 반환값을 내야 한다.

example
```js
var fnc = value => value * value;
```

개인적은 경험으로 봤을때 글로벌, 지역적 상태값이 많아지면 그에 따른 비동기적 처리나 많은 상태간의 연결성 때문에 복잡성이 커진다고 생각은 하고 있었다.
함수형 프로그래밍이 이 문제에 대한 대안이라고 하는데, 솔직히 아직까지는 확실하게 어떻게 해결되어 지는지 알수 없다.
명확하고 순수한 함수를 사용함으로 인해 얻을 수 있는 점은 테스트의 용의성, 코드의 재활용성, 로직이 어떤 일을 수행하는지 파악하기 쉽다 정도에 그치지,
많은 상태를 가져야 하는 앱의 경우 그 상태를 함수로 대체했을때 복잡성이 해결되는지 의문이다.

불변성이 사이드 이팩트를 없애고 좀 더 신뢰성 높은 기능을 구현 할수 있다는 점에서는 완벽하게 동의하고 공감되었다.

이책에서 말하는 작업의 단위는 현재 내가 하고 있는 업무 프로세스인 에자일방법론에 맞는 방법같기도 했다. (닫기 버튼을 누르면 해당 모달이 닫힌다. 등의 기능을 하나의 명령어 형태로 나타낼수 있는 작업의 단위)


## 스터디 노트

### 느슨한 평가
함수 체인으로 함수 지연 평가를 하는 방법이 존재한다. => https://edykim.com/ko/post/introduction-to-lodashs-delay-evaluation-by-filip-zawada/
재사용성 확보와 안전한 데이타 활용이 가능해진다라는 의견이 있었음.

### 커링을 사용하는 상황
함수체인에서 인자를 조작해야 하는 경우 사용한다.

### 객체 그래프 렌즈로 탐색/수정(함수형 레퍼런스)

### 객체를 삭제해야 할때
https://medium.com/@laziel/javascript-%EA%B0%9D%EC%B2%B4%EC%9D%98-%EC%86%8D%EC%84%B1%EC%9D%84-%EC%A0%9C%EA%B1%B0%ED%95%A0-%EB%95%8C-delete-%EC%97%B0%EC%82%B0%EC%9E%90%EB%B3%B4%EB%8B%A4-undefined-%EB%82%98-null-%EA%B0%92%EC%9C%BC%EB%A1%9C-%EB%A7%8C%EB%93%9C%EB%8A%94-%EA%B2%83%EC%9D%B4-%EB%82%AB%EB%8B%A4-2db597f64514


2장은 생각보다 리뷰할 내용이 없으므로 패스!


## 2회차

#### 명령형 프로그램
C# C++ java 등 OOP언어들은 대부분 명령형 프로그래밍을 지원하기 위해 디자인 되었다. 목표를 이루기 위해 수행하는 단계를 자세히 기술해야 하고, 이는 작업을 수행하는 루프 분기, 변수들로 매워져 있다. 직면한 문제를 해결 하기 위해서 클래스의 계층 구조를 디자인 하고, 추상화 하여 문제를 처리한다.

#### 선언적 프로그램
스칼라, 하스켈, 클로져 등 함수형 언어들은 정의된 블랙박스연산들이 연결되어 문제를 해결하는 방식이다.

#### 메서드 체이닝
함수형으로 메서드 체이닝을 하면 안에서 밖으로 해석해야 함으로 가독성이 떨어짐...

example
```js
result(sum(write('something like')))
```


#### 함수 체이닝




### 토론주제

게속 책을 읽어 보니 함수형 프로그래밍은 어떤 작업 할지 명확안 목표를 위해 만들어가는 것 보다 리액트에서 컴퍼넌트 쪼개서 재사용 하듯 어디에 어떤 상황에 사용될지 확실히 명환한 경우의 수를 가진 함수 말고 유용하고 하는일이 명확하고 확실한, 함수를 만들어가면서 추상화 하는거라고 생각되어 진다.
어디로 이동해야 하는 문제를 해결하는 것을 함수형으로 사고한다면, 가는곳 좌표을 말해주는 함수(목적지 주소) => 전달 받은 이자의 주소가 존재하는 확인하고 진행해주는 함수 => 전달 받은 주소에 도착하는 방법을 사고하는 함수 => 목적지에 가는 함수 => 목적지에 도착했다는것을 알려주는 함수




## 3회차 (2018.10.29)

1. 순수합수기반의 오듈적인 코드는 테스트 하기 쉽다.
이유 > 단위테스트에서 순수함수 정말 기초 단위 테스트만을 수행해도 되는 단순한 원리이다. 순서를 뒤집어도 아무리 다양한 값을 넣어도 함수가 동작하는 것은 한가지다
그렇게에 테스트 하기 쉽고, 간결한 테스트가 가능하다. BDD 철학과도 비슷하다는 느낌이다. 함수의 간단한 동작을 테스트 하는 것이다. 개인적으로 TDD로 모든 코드를 짤수 없다고 생각하기 때문에...

2. 제어의 흐름이 직관적이어야 한다.
이유 > 명령형 프로그래임이 들어간 로직의 경우 제어의 흐름에 그것이 아니라면 이것 과 같은 장황한 제어 구분이 들어가게 된다 그렇게 되면 테스트 할때 원하는 값이 나올수 없는 경우가 생기고 테스트 코드 또한 복잡성을 띄게 된다.

3. 복잡성과 단순성
이유 > 코드를 짤때 제어의 흐름을 최대한 단순화 시키고 최대한 명령어 안에서 많은 통제를 하지 않으려는 노력을 하면 수정이 용이 하고 테스트가 간편하고, 재사용성이 높아진다고 생각하고 느끼고 있다. 하지만 모든 코드를 그렇게 순수한 형태의 함수 조합으로 짤 수 있는건 아니라고 생각이 되기도 한다. 하지만 그런 필수적인 경우를 제외하고 코드를 단순화 해서 짜게 되면 장점이 많다고 동의한다.

4. 함수형 코드는 성능상 이점이 있다? 없다?
견해 > 함수형 코드는 일반적인 명령형 코드보다는 어쩔수 없이? 필연적으로? 거쳐야 하는 부분이 늘어날수가 있다. 그건 답을 찾아가는 과정이 나한테 주어진 함수를 응용해서 찾아가야 하는 것이기? 때문일지도 모른다. 가령 밥은 전기와 쌀, 밭솥이 있다면 지을수 있다. 말을 함수형으로 짓는다면, 전기가 있는지 확인 > 쌀이 있는지 확인 > 밥솥이 있는지 확인 > 밥을 지을수 있다. 라는 긴 문장이 될수 있다고 생각되어 진다. 하지만 함수형 라이브러리를 이용해서 평가 지연을 하거나, 현재 하드웨어의 발전으로 인해 사소한 성능상의 핸디캡은 있을수 있고 오히려 나중에 버그가 적고 내가 원하는 결과물을 좀더 편하게 만들 수 있는 함수형의 이점이 더 많다고 생각한다.

5. 메모화
개인적인 생각으로 성능을 극한으로 끌어올릴때 사용할 순 있겠지만, 나는 절대 안쓸껏 같다... 왜냐 손이 너무 많이간다. 비용이 아깝다..
차라리 좀더 안정적인 코드를 짜기 위한 시간을 투자할것이다.




