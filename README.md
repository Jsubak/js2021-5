# 박수정 [202030311]
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
|:----------:|:----------:|
| Number() | 문자열 -> 숫자 |
| parselnt() | 문자열 -> 정수 |
| parseFloat() | 문자열 -> 실수 |
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