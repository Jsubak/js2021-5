# 박수정 [202030311]
## [5월 11일]
***
## 내용 요약
- Date 객체생성
```javascript
// 현재 시간을 기반으로 Date 객체를 생성
let dateA = new Date();
// 유닉스 타임(1970년 1월 1일 00시 00분 00초부터 경과한 밀리초)
let dateB = new Date(692281800000);
// 문자열을 기반으로 Date 객체를 생성
let dateC = new Date("December 9, 1991 21:30:00");
```
- 메소드 <br>
-- getㅁㅁ(), setㅁㅁ() : FullYear, Month, Day, Hours 등등 <br>
- getTimes() : 유닉스 타임
- Array 객체 : 파괴적 메소드로 자기 자신을 변경

| 메소드 | 설명 |
|:----:|:----:|
| cancat() | 매개변수로 입력한 배열의 요소 -> 모두 합친 배열 |
| join() | 배열 안의 모든 요소 -> 문자열 |
| pop()* | 배열 마지막 요소를 제거 |
| push()* | 배열 마지막 요소를 제거 |
| reverse()* | 배열 요소 순서를 뒤집음 |
| slice() | 배열 요소의 지정한 부분 |
| spilce()* | 배열 요소의 지정한부분을 삭제하고 삭제한 요소 |

- 배열 가공
```javascript
let array = [{
    name: '고구마',
    price : 1000
}, {
    name: '감자',
    price : 500
}, {
    name: '바나나',
    price : 1500
}];
```
- 추가된 Array 객체의 메소드

| 메소드 | 설명 |
|:----:|:----:|
| forEach() | 배열의 요소를 하나씩 뽑아 반복 돌림 |
| map() | 콜백 함수에서 리턴하는 것을 기반으로 새로운 배열을 만듦 |
| filter() | 콜백 함수에서 true를 리턴하는 것만으로 새로운 배열 만들어서 리턴 |
- 프로토타입에 메소드 추가 <br>
-- 해당 자료형 전체에 추가 가능
```javascript
// 프로토타입에 메소드를 추가
String prototype.contain = function (input) {
    return this.indexOf(input) >= -1;
}
```
- underscore.js 라이브러리
- JSON 객체
```javascript
[
    {
        "name": "고구마",
        "price": 1000
    },
    {
        "name": "감자",
        "price": 500
    },
    {
        "name": "바나나",
        "price": 1500
    }
]
```
- 제약 사항 <br>
-- 문자열은 큰 따옴표로 <br>
-- 모든 키는 큰 따옴표로 <br>
-- 숫자, 문자열, 불 자료형만 사용가능

- 메소드

| 메소드 | 설명 |
|:----:|:----:|
| JSON.stringify(<객체>,<변환 함수>,<공백 개수>) | 자바스크립트 객체를 문자로 만듦 (문자열 리턴) |
| JSON.parse(<문자열>) | 문자열을 자바스크립트 객체로 파싱 (객체 리턴) |

- 예외처리
- 예외 : 실행에 문제가 발생하면 자동 중단
- 예외 처리 : 오류에 대처할 수 있게 하는 것

- try catch finally 수문
```javascript
try {
    // 예외가 발생하면
} catch (exception) {
    // 여기서 처리
} finally {
    // 여기는 무조건 실행
}
```
- catch 혹은 finally 구문 생략가능
- 예외 강제 발생 <br>
-- throw 키워드 사용
-- throw 키워드 뒤에는 문자열 또는 Error 객체 입력
- throw '강제 예외';
***
## [5월 4일]
***
## 내용 요약
- 프로토 타입 (prototype) : 모든 함수가 가지고 있는 속성으로 해당 함수를 생성자함수로 사용했을때만 의미있음.
```javascript
// 생성자 함수
function Product(name, price) {
    this.name = name;
    this.price = price;
}

// 프로토타입에 메소드를 선언합니다.
Product.prototype.print = function () {
    console.log(`${product.name}의 가격은 ${product.price}원 입니다.`);
};

// 객체를 생성합니다.
let product = new Product("바나나", 1200);

// 메소드를 호출합니다.
product.print();
```
- null :변수처럼 활용, null값을 가진 객체(object) <br>
-- undefined 상태를 인위적으로 만듦, 아예 값이 없는 상태 구분할 때
- 숫자, 문자열, 불은 typeof를 사용하면 object가 나옴 즉, 객체라는 의미
- 기본자료형과 객체 자료형 모두 속성과 메소드를 사용할 수 있음 <br>
-- 기본 자료형의 속성 또는 메소드를 사용할 떄 기본 자료형이 자동으로 객체로 변환
- Number 객체는 기본 자료형과 객체 자료형 모두를 의미
```javascript
let numberFromLiteral = 273;
let numberFromConstructor = new Number(273);
```
- Number 메소드

| 메소드 | 설명 |
|:----:|:----:|
| toExponential() | 숫자 -> 지수 표시로 나타낸 문자열 |
| toFixed() | 숫자 -> 고정소수점 표시로 나타낸 문자열 |
| toPrecision() | 숫자 -> 지수 또는 고정소수점표시로 나타낸 문자열 |

-- Number 생성자 함수에도 속성이 있다.

| 속성 | 설명 |
|:----:|:----:|
| MAX_VALUE | 숫자가 나타낼 수 있는 최대 숫자 |
| MIN_VALUE | 숫자가 나타낼 수 있는 최소 숫자 |
| NaN | 숫자로 나타낼 수 없는 숫자 |
| POSITIVE_INFINITY | 양의 무한대 숫자 |
| NEGATIVE_INFINITY | 음의 무한대 숫자 |

- string 객체
```javascript
let stringFromLiteral = '안녕하세요';
let stringFromConstructor = new String('안녕하세요');
```
- 속성 <br>
-- length : 문자열 길이

| 속성 | 설명 |
|:----:|:----:|
| charAt(position) | position에 위치하는 문자 |
| charCodeAt(position) | positon에 위치하는 유니코드 번호
| concat(args) | 매개 변수로 입력한 문자열 |
| indexOf(searchString, position) | 앞에서부터 일치하는 문자열의 위치 |
| lastindexOf(searchString, position) | 뒤에서부터 일치하는 문자열 위치 |

... 등등
- 자기자신을 변경하는게 아니라 변경된 값을 리턴하는 것
***
## [4월 27일]
***
## 내용 요약
- 객체 : 여러 개의 자료형을 한 번에 저장하는 자료형
-- 배열과 객체는 상당히 유사 <br>
-- 배열은 요소에 접근할때 인덱스를 사용 하지만 객체는 키를 사용<br>
```javascript
let product = {
    제품명: '70 건조 망고',
    유형: '당절임'
}

product['제품명']
product['당절임']
product.제품명
```
- 객체 뒤에 대괄호를 사용해 키를 입력하면 객체의 속성에 접근 혹은 3번째 방법처럼 깔끔하게 사용
- 반복문 : for in 키 로 사용한다.
- 속성 : 객체 내부에 있는 값 하나하나
- 메소드 : 객체 속성 중 자료형이 함수인 속성
```javascript
let object = {
    name: '바나나',
    price: 1200,
    print: function () {
        console.log(`${this.name}의 가격은 ${this.price}원입니다`)
    }
}
```
-- print 속성은 자료형이 함수여서 메소드라고함.<br>
-- 자신의 가지고있는 속성이라는 것을 표시할 때 this 키워드 사용<br>
-- 화살표 함수를 사용해 메소드를 만들면 undefined가 나옴
```javascript
let products = [
    { name: '바나나', price: 1200 },
    { name: '사과', price: 2000 },
    { name: '배', price: 3000 },
    { name: '고구마', price: 700 },
    { name: '감자', price: 600 },
    { name: '수박', price: 5000 }
];
```
- 객체 형태로 데이터로 표현하는 것 -> JSON 
(Javascript Object Notation)
```javascript
let products = [{
    name: '바나나',
    price: 1200,
    print: function () {
        console.log(`${this.name}의 가격은 ${this.price}원입니다.`)
    } 
}];
```
- 메소드를 가진 객체배열
- 함수와 객체를 따로 적으면 안되나? -> 한 객체의 속성과 기능은 한 객체를 기준으로 처리할 수 있게한다라는 규칙성을 가지기 때문에 되도록이면 위에 처럼 만든다.
- 생성자 함수 : 객체를 만드는 함수 <br>
-- 대문자로 시작하는 이름을 사용
```javascript
// 생성자함수
function Product(name, price) {
    this.name = name;
    this.price = price;
}
// 객체 생성
let product = new Product("바나나", 1200);
```
- new 키워드와 함께 객체를 생성
- 간단하게 생성한 객체에는 이름이 없었는데 이러한 객체는 익명객체 라고 함
- new 키워드를 앞에 붙이지 않으면 일반 함수 호출
***
## [4월 13일]
***
## 내용 요약
- 함수(자료형) : 코드의 집합, 중괄호 내부에 코드를 넣으라는 것
-- 익명 함수 : 이름을 붙이지 않고 함수를 생성<br>
-- 선언적 함수 : 이름을 붙여 함수를 생성 <br>
- 익명 함수
```javascript
let <변수 이름> = function () { };
```
- 선언적 함수
```javascript
function <함수 이름> { }
```
- 화살표 함수 : 익명 함수를 더 간단하게 생성
```javascript
() => { }

//응용
let 함수 = () => { }
```
- 함수의 기본 형태
```javascript
function <함수 이름>(<매개 변수>) {
    <함수 코드>
    return <리턴 값>
}
```
-- 매개 변수를 넣으면 메소드 내부에서 특정한 처리를 하고 값을 반환<br>
- 리턴 : 메소드 내부에서 일어나는 처리에 비중을 둠
-- 화살표 함수경우 중괄호 없이 표현식 하나만 놓으면 해당 표현식 리턴
- 무언가를 리턴하는 함수
```javascript
function (<매개 변수>, <매개 변수>) {
    let output = <초기값>;
    //output 계산
    return output;
}
```
- 매개변수를 입력하지 않아도 함수가 호출됨.
-- undefined가 나옴
- 콜백 함수 : 힘수의 매개 변수로 전달되는 함수
- 숫자 변환 함수 <br>

| 함수 | 설명 |
|:----:|:----:|
| Number() | 문자열 -> 숫자 |
| parselnt() | 문자열 -> 정수 |
| parseFloat() | 문자열 -> 실수 |
- 타이머 함수 : 특정 시간후에,특정시간 마다 어떤 일을 할 때 사용

| 함수 | 설명 |
|:----:|:----:|
| SetTimeOut(함수, 시간) | 특정 시간 후에 함수를 실행 |
| SetInterval(함수, 시간) | 특정 시간마다 함수를 실행 |
| clearInterval(아이디) | 특정 시간마다 실행하던 함수 호출을 정지 (setInterval()) |
- 생성 순서 (같은 이름일 경우) <br>
-- 변수의 경우 : 뒤에 선언한 변수가 앞 변수를 덮어씀<br>
-- 함수의 경우 : 뒤에 함수가 앞 함수를 덮어씀 <br>
=> 위에서부터 내려가면서 함수를 선언하고 변수에 할당하기 때문 <br>
-- 선언적 함수는 코드를 실행하기 전에 생성
- 익명함수와 화살표 함수는 차이가 있다.
***
## [4월 6일]
***
## 오늘 배운 내용 요약
- 중첩 반복문 : 반복문을 여러 번 중첩해서 사용
- ex)
```javascript
let output = "";

for (let i = 0; i < 10; i++) {
    for (let j = 0; j < i+1 j++) {
        output += "*";
    }
    output += "\n";
}
```
-- 별을 응용해서 만든 다른 예제는 js파일로 올림.(ch-4-7-8.js)
- 배열 메소드
-- Array.pop(); : 배열 뒷부분의 값을 삭제<br>
-- Array.push(); : 배열 뒷부분에 값을 삽입<br>
-- Array.splice(index,제거할 요소 개수, 배열에 추가될 요소) : 배열의 특정위치에 요소를 추가 또는 삭제<br>
- break : switch 조건문이나 반복문을 벗어날 때 사용
- contiue : 반복문 내부에서 현재 반복을 멈추고 다음 반복을 진행
```javascript
for (let i = 1; i <10; i++) {
    if ( i % 2 == 0) {
        continue // 짝수라면 다음 반복으로 넘어감 for 문을 컨티뉴 if x
    }
    console.log(i);
}
```
- 스코프(scope) : 변수를 사용할 수 있는 범위, 변수는 선언 위치에 따라 사용할 수 있는 범위가 제한
-- 스코프 == 블록
- 호이스팅(Hoisting) : 해당 블록에서 사용할 변수를 미리 확인해서 정리하는 작업
- var : 익스플로러에서 let키워드 대신사용
-- var , let 차이점 : 변수의 스코프 <br>
-- var 키워드로 생성한 변수는 모든 곳에서 사용 <br>
-- let 키워드로 생성한 변수는 해당 블록 내부에서만 사용
***
## [3월 30일]
***
## 오늘 배운 내용 요약
- 중첩 조건문 : 조건문 안에 조건문을 중첩해 사용하는 것
```javascript
if (불 표현식[조건식]) {
    if (불 표현식) {
        문장;
    } else {
        문장;
    }
} else {
    if (불 표현식) {
        문장;
    } else {
        문장;
    }
}
```
- if else if 조건문 : 조건이 한 문장이라면 조건문의 중괄호을 생략 가능
```javascript
if (<불 표현식>) {
    
} else if (<불 표현식>) {

} else if (<불 표현식>) {

} else {

}
```
- switch 조건문
```javascript
switch (<비교할 값>) {
    case <값>:
        <문장>
        break;
    case <값>:
        <문장>
        break;
    default:
        <문장>
        break;
}
``` 
-- break : 조건문,반복문을 빠져나갈때 사용
- 삼항 연산자 : 조건을 구분 ( 해당 변수가 undefined인지 확인할 때 )
```javsscript
<불 표현식> ? <참> : 거짓
```
- 짧은 초기화 조건문 : || 연산자 활용
-- A || B 에서 A가 참이라면 A로 대치<br>
-- A || B 에서 A가 거짓이라면 B로 대치
- ex)
```javascript
let test;

test = test || "초기화합니다_1"
console.log(test);

test = test || "초기화합니다_2"
console.log(test);
```
-- 결과 : 초기화합니다_1 (2번나옴)<br>
-- 변수가 test가 undefined일 때 || 기호 뒤의 값으로 초기화한다<br>
-- && 연산자는 반대로 동작, 짧은 초기화 조건문으로는 거의 활용x
- 배열 : 여러 개의 자료를 한꺼번에 다룰 수 있는 자료형
> let 이름 = [자료, 자료, 자료, 자료, 자료]<br>
-- 요소 (element) : 배열 안에 들어 있는 각 자료<br>
-- 인덱스 (index) : 대괄호 안에 넣는 숫자<br>
-- .length 배열에 몇 개의 요소가 있는지 확인
- while 반복문
```javascript
while (<불 표현식>) {
    // 불 표현식이 참인 동안 실행할 문장
}
```
- 무한 반복문 (무한루프)
```javascript
while (true) {
    console.log("무한 반복");
}
```
- for 반복문 : 원하는 횟수만큼 반복하고 싶을때 사용
```javascript
for (let i = 0; i < <반복 횟수>; i++) {

}
```
- 역 for 반복문 : 배열 반복을 뒤에서부터 실행 해야 할 떄 사용
```javascript
for (let i = length -1; i >= 0; i--){

}
```
- for in 반복문, for of 반복문 : 객체에 쉽게 반복문을 적용할때 사용
```javascript
for (let 인덱스 in 배열) {

}
for (let 요소 of 배열) {
    
}
```
***
## [3월 23일]
***
## 오늘 배운 내용 요약
- 나머지 연산자의 부호는 왼쪽의 피연산자의 부호를 따른다<br>
- 소수점이 있는 숫자에도 나머지 연산자 적용 가능<br><br>
- 따옴표앞에 \를 붙이면 따옴표를 문자 그대로 사용 가능<br><br>
- 템플릿 문자열(ECMAScript6)<br>
-- `기호로 생성<br>
-- 생성 이후는 일반 문자열과 똑같이 취급<br>
-- ${<표현식>} 표현식이 계산되어 문자열로 들어감<br><br>
- 불 : 참과 거짓을 표현할때 사용 (true/false)<br><br>
- 변수 : 값을 저장할때 사용하는 식별자<br>
-- var (식별자) -> let (식별자)<br><br>
- 상수 : 항상 같은 수 (변수와 반대되는 개념)<br>
-- const (식별자)<br><br>
- if 조건문<br>
- else if 조건문
***
## [3월16일]
***
## 오늘 배운 내용 요약
- 자바 스크립트는 모든 웹 브라우저에서 실행 할 수 있는 유일한 프로그래밍 언어<br><br>
- 네이티브 애플리케이션 : 스마트폰에서 기본적으로 인식할 수 있는 프로그래밍 언어로 만든 애플리케이션 <br><br>
- React Native : 페이스북이 자바스크립트로 네이티브 애플리케이션을 개발할 수 있는(내부적으로 프로그래밍 언어를 변환하는) 만들어 공개 <br><br>
- 표현식 : 값을 만들어내는 간단한 코드<br>
- 문장 : 표현식이 하나 이상 모인것<br>
- 문장을 종결한다는 의미로 세미콜론(;)을 사용<br><br>
- 키워드 : (자바스크립트에서)특별한 의미가 부여된 단어<br><br>
- 식별자 : 이름을 붙일 때 사용하는 단어, 변수와 함수 이름 등등으로 사용<br>
-- 생성자 함수의 이름은 항상 대문자 시작<br>
-- 변수,함수,속성,메소드의 이름은 항상 소문자 시작<br>
-- 여러 단어로 된 식별자는 각 단어의 첫 글자를 대문자<br><br>
- 날짜가 최신것일 수록 위에 적기!!!<br>
- 검사+cosole 가서 js 확인가능<br>
- 터미널 들어가서 node 간단한 실행보기 가능 푸는방법은 ctrl+D

***