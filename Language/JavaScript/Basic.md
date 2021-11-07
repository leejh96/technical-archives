2021-11-07
작성자 leejy001

## JavaScript 

JavaScript는 웹페이지를 동적으로, 프로그래밍적으로 제어하기 위해서 고안된 언어  
HTML이 한번 화면에 출력된 후에는 그 형태나 동작방법을 바꿀 수 없는 문제를 해결하기 위해서 네스케이프에서 만들어졌다.  
이후에 이 언어는 마이크로소프트의 인터넷 익스플로러에 jscript라는 이름으로 탑재된다.  
후에 ECMA라는 표준화 기구로 이 언어의 관리 주체가 옮겨졌다.  

**console.log()**
console.log()를 이용하면 원하는 내용을 브라우저의 콘솔 탭에 출력할 수 있다.

**세미콜론**
세미콜론은 해당 코드가 끝났다는 것을 알려주는 기호이다.  
만약 한줄에 여러 줄의 코드를 입력하려면 세미콜론을 통해 구분해주면 된다.

```
console.log(); console.log()
```

**자료형**
숫자형  
정수(integer), 소수(floating point)  
숫자형은 사칙연산이 가능  

문자형
" ,  '로 나타내줄 수 있다.  
'+' 기호를 통해 문자열을 서로 연결해주는 것이 가능하다.  

Boolean
참과 거짓을 나타낸다.  
어떤 조건에 의한 결과값으로 사용  

**추상화**
추상이란 **여러 가지 사물이나 개념에서 공통되는 특성이나 속성 따위를 추출하여 파악하는 작용**을 의미한다.  
추상화는 구체적인 정보는 숨기고 꼭 필요한 핵심만 뽑아서 나타내준다.  
추상화의 핵심 (목적은 명확히, 불필요한 것들은 숨기기, 핵심만 드러내기)

**변수 (variable)**
반복적으로 입력되는 어떠한 값은 오타를 만들어내며 어떤 값에 대한 의미를 제대로 전달하기 어렵다.  
그렇기 때문에 변수를 선언하여 값을 초기화 시켜줌으로서 의미를 정확하게 전달하며 오타도 줄일 수 있다.

```
let 변수이름 = 값;
```

### 변수 이름을 만들기 위한 몇가지 rule
**꼭 지켜야 하는 rule (지키지 않으면 오류)**  
(1) JavaScript 식별자는 **문자(a-z, A-Z)**, **밑줄(_)** 혹은 **달러 기호($)** 로 시작해야 한다. 두 번째 글자부터는 '숫자(0-9)'도 가능하다.  
(2) **대문자**와 **소문자**는 구별한다. myname과 myName은 다른 이름이다.  
(3) **예약어(JavaScript가 찜해놓은 단어)** 는 사용하면 안 된다. 예를 들어서 if, for, let 같은 것들이 있다.  

**지키면 좋은 rule (더 좋은 스타일을 위해)**  
(1) 의미 없는 이름은 좋지 않다.  
이름이 의미없이 정해져 있다면 나중에 어떤 값을 저장해뒀는지 찾기도 어려우며 활용하기도 힘들다.  
또한 프로그램의 가독성이 떨어져 나중에 스스로 프로그램을 살펴볼 때나 공동 작업을 진행할 때 매우 불편한 상황이 올 수 있다.  

(2) 너무 추상적인 이론은 좋지 않다.  
만약 변수의 이름을 name이라고 지었다. 물론 단순히 name이라는 변수명이 적합한 상황도 올 수 있지만  
긴 프로그램을 쓰다 보면 다양한 '이름'들이 있을 수 있기에 name은 너무나 추상적이다.

(3) 모든 변수 이름은 'camelCase'로 쓰는 것이 좋다.
변수는 띄어쓰기 대신 camelCase 방식을 사용한다. 첫 번째 글자는 소문자로 하며 그 이후의 띄어쓰기가 오는 각 단어의 첫 문자를 대문자로 표기하는 방법이다. 

## 함수
변수는 값을 저장한다.  
함수는 다양한 명령들을 저장한다.  
함수 선언은 function이라는 keyword를 사용한다.  

```
function 함수이름() {
    명령;
    명령;
}
```

함수 선언은 그 함수가 사용될 때 어떤 행동을 할지 정의만 해주며 함수 호줄은 해당 함수의 이름을 적으면 된다.

```
function 함수이름() {
    명령;
    명령;
}

함수이름();
```

**파라미터(Parameter)**

함수에 어떤 값을 전달할 때 해당 값을 매개변수(Parameter)라고 한다.
함수를 선언하고 호출할 때 함수 소괄호 내부에 매개변수를 입력하여
값을 전달한다.

```
function 함수이름( 파라미터 ) {
    명령;
    명령;
}

함수이름( 파라미터 );
```

어떤 파라미터를 전달하냐에 따라 다양한 결과를 출력할 수 있다.  
여러 파라미터를 전달하는 방법은 간단하다.  
소괄호 안에 여러 파라미터를 넘겨주면 된다.  

```
function 함수이름( 파라미터, 파라미터 ) {
    명령;
    명령;
}

함수이름( 파라미터, 파라미터 );
```

하지만 너무 많은 파라미터를 정의하면 함수 자체의 명령문도 복잡하므로 처음 함수를 작성할 때 해당 함수의 목적을 명확하게 하고 필요한 파라미터만 작성하도록 한다.

**return**
함수에 파라미터를 input으로 주었다면 output으로 나오는게 있다.  
이때 결과 값을 반환한다는 의미로 return을 사용하며 return 이후의 코드는 실행되지 않는다.  
console.log를 통해 함수를 선언할 때 해당 함수에 return을 따로 작성하지 않는다면 undefined를  return하게 된다.  

**옵셔널 파라미터**
만약 해당 파라미터에 어떠한 값도 전달하지 않았을때 undefined가 아닌 다른 값을 출력하기위해 작성하는것이 옵셔널 피라미터이다.  
함수의 파라미터에 값을 미리 할당해두면 되며 이때 주의할 점은 옵셔널 피라미터는 가장 뒤쪽에 선언해줘야한다.

```
function introduce(name, age, nationality="한국") {
   ...
}
```

**Scope**

어떤 변수의 할당된 값을 사용할 수 있는 유효한 범위, 영역을 의미한다.

```
function myFunc() {
  let x = 'A';
  x = "B";
}

myFunc();
console.log(x);
```

위와 값은 경우 변수 x는 myFunction이라는 함수 내에서만 쓸 수 있는 local변수이기 때문에 오류가 발생하게 된다.  
console.log에 해당 변수 값이 나오게 하려면 다음과 같이 처리해야 한다.

```
let x = "A";

function myFunc() {
  x = "B";
}

myFunc();
console.log(x);
```

다음은 어떤 결과가 나올까?

```
let x = 120;

function myFunc() {
  let x = 20;
  console.log(x);
}

myFunc();
console.log(x);
```

로컬 변수와 글로벌 변수 둘다 변수 이름이 같다.  
일단 로컬 변수는 해당 함수 내에서만 유효하며 함수 바깥을 벗어나게 되면 사용할 수 없다.  
반대로 글로벌 변수는 함수 안이든 바깥이든 전부 사용이 가능하다.  
여기선 함수 내에 이미 x라는 변수가 선언되었으므로 함수 내부의 console.log는 20이 출력되며 바깥쪽의 console.log는 글로벌 변수 값인 120이 출력된다.  

**상수**

상수는 변수와 달리 값이 절대 변하지 않는다.  
따라서 변동이 있는 값은 변수로, pi 같은 절대 변경되지 않는 값은 상수로 표현하자 상수 선언시 const를 이용하여 선언할 수 있다.  
상수는 선언시 변수를 전부 대문자로 표현해준다.

```
const PI = 3.14;
let number = 0;
```

## 조건문

if, else, else if 를 이용하여 각 조건마다 실행을 다르게 해줄 수 있다.

```
function printGrade(midtermScore, finalScore){
	let totalScore = midtermScore + finalScore;
  if (totalScore >= 90) {
    console.log('A');
  } else if (totalScore >= 80) {
    console.log('B');
  } else if (totalScore >= 70) {
    console.log('C');
  } else if (totalScore >= 60) {
    console.log('D');
  } else {
    console.log('F');
  }
}

printGrade(25, 35);
printGrade(50, 45);
printGrade(29, 24);
printGrade(37, 42);
```

**중첩 조건문**

조건문 내부에 여러 조건문을 이용하여 결과를 나눠줄 수도 있다.

```
let myAge = 26;
let myGender = 'male';

let callOlderBrother = '형';
let callOlderSister = '누나';
let callFriend = '친구';
let callYoungerSister = '여동생';
let callYoungerBrother = '남동생';

function whatShouldICallYou(yourAge, yourGender) {
  if (yourAge === myAge) {
    return callFriend
  } else if (yourAge < myAge) {
    if (yourGender === "female") {
      return callYoungerSister
    } else {
      return callYoungerBrother
    }
  } else {
    if (yourGender === "female") {
      return callOlderSister
    } else {
      return callOlderBrother
    }
  }
}

let result1 = whatShouldICallYou(25, 'female');
let result2 = whatShouldICallYou(20, 'male');
let result3 = whatShouldICallYou(26, 'female');
let result4 = whatShouldICallYou(30, 'male');
let result5 = whatShouldICallYou(31, 'female');

console.log(result1);
console.log(result2);
console.log(result3);
console.log(result4);
console.log(result5);
```

**switch**

if문을 이용하여 switch문을 if문으로도 대체할 수 있다.  
보통 어떤 넓은 범위를 만족하는 조건식을 만들 때는 if문을 활용하는 것이 좀 더 효과적이고 특정한 값에 일치하는 조건을 만들 때는 switch문이 좀 더 효과적이다.  

```
let myChoice = '2';

switch(myChoice) {
  case 1:
    console.log('토끼를 선택한 당신, ...');
    break;
  case 2:
    console.log('고양이를 선택한 당신, ...');
    break;
  case 3:
    console.log('코알라를 선택한 당신, ...');
    break;
  case 4:
    console.log('강아지를 선택한 당신, ...');
    break;
  default:
    console.log('1에서 4사이의 숫자를 선택해 주세요.'); 
}
```

위와 같은 코드를 실행 시 default가 나오게 된다.  
이유는 switch문은 암시적인 형 변환을 허용하지 않기 때문이다.  
switch문을 사용시 반드시 값들을 비교할 때 자료형을 엄격하게 구분해야한다.

## 반복문

컴퓨터는 반복적인 작업을 하기에 최적화되어있다. 반복문에는 for와 while이 있다.

**for문**

for문의 구조는 다음과 같다.

```
for (초기화부분; 조건부분; 추가동적부분) {
    동작부분
}
```

**for문은 추가동작부분을 꼭 채울 필요는 없다.**  
추가동작부분에서 i를 1씩 증가시키는 부분이 여기 동작부분에 들어가도 문제는 없다.

```
for (let i = 1; i <= 10;) {
    console.log(`${i}`);
    i++;
}
```

**초기화부분에서 생성한 변수는 for문의 로컬변수다.** 
for 반복문의 초기화 부분에서 생성한 변수는 for문 안에서의 로컬변수가 된다.

```
for (let i = 1; i <= 10; i++) {
  console.log(`${i}`);
}

console.log(i); // Error !!
```

for문 안에서 생성한 로컬변수이기 때문에 for 반복문이 종료되고 나서 for 반복문 밖에서 변수를 사용하려고 하면 오류가 발생한다.

**초기화 부분도 반드시 채울 필요는 없다.** 단,for문의 소괄호 안쪽 가장 첫번째 세미콜론은 생략할 수 없다.

```
let i = 1; 
for (; i <= 10; i++) {
    console.log(`${i}`);
}
```

저 세미콜론은 초기화부분과, 조건부분을 구분하는 세미콜론이기 때문에 초기화 부분의 코드를 생략하더라도 세미콜론 만큼은 생략해선 안된다.


**while문**

while의 기본구조는 다음과 같다.

```
while (조건부분) {
    동작부분
}
```

 while은 조건 부분에 종료조건을 넣어도 되며 동작 부분에도 조건문을 이용하여 종료조건을 넣어줄 수 있다.

```
const N = 180;
let i = 0;
let count = 0;
while (i <= N) {
    if (N % i === 0) {
        console.log(i)
        count++;
    }
    i++;
}

console.log(`${N}의 약수는 총 ${count}개입니다.`);
```

**break, continue**

반복문에서 break를 쓰게되면 해당 반복문이 더 이상 실행되지않고 종료하게 되며 continue를 사용한다면 종료되지 않고 continue 밑의 코드들은 생략하며 다음 반복문을 실행하게 된다.

코드

```
let i = 1;

while (i <= 20) {
  if (i === 5) {
    break;
  }
  console.log(i);
  i++;
}
```

결과

```
1
2
3
4
```

코드

```
for (let i = 1; i <= 10; i++) {
    if (i % 2 !== 0) {
        continue;
    }
    console.log(i);
    i++;
}
```

결과

```
2
4
6
8
10
```
