# 박수정 [202030311]
## [6월 1일]
***
## 내용요약
### 웹 브라우저의 자바스크립트
- let 키워드와 const 키워드

| 최신 버전 자바스크립트 코드 | 인터넷 익스플로러에서 사용해야하는 코드 |
|:----:|:----:|
| let variable = 273; | var variableA = 273; |
| const constant = "Hello World"; | var variable = "Hello World"; |

- 템플릿 문자열

| 최신 버전 자바스크립트 코드 | 인터넷 익스플로러에서 사용해야하는 코드 |
|:----:|:----:|
| let variable = 273;<br>console.log(`변수의 값은 ${variable}입니다.`); | var variableA = 273;<br>console.log('변수의 값은 '+variable+'입니다'); |

- 화살표 함수

| 최신 버전 자바스크립트 코드 | 인터넷 익스플로러에서 사용해야하는 코드 |
|:----:|:----:|
| const functionLiteral = () => { }; | var functionLiteral = function () { }; |
| const constant = "Hello World"; | var variable = "Hello World"; |

- for of 반복문

| 최신 버전 자바스크립트 코드 | 인터넷 익스플로러에서 사용해야하는 코드 |
|:----:|:----:|
| const array = ['가','나','다'];<br>for (let item of array) { console.log(item); } | var array = ['가','나','다'];<br>for (var item in array) { console.log(array[i]); } |

- 익스플로러는 forEach를 쓸 수 없어 자바 처럼 사용 <br>

- 웹 브라우저와 관련된 객체
- window 객체 : 웹 페이지 자체를 나타냄 <br>
-- 화면 열고, 브라우저 크기 변경, 경고를 출력하는 경고창과 입력하는 프롬프트 제공

| 함수 | 설명 |
|:----:|:----:|
| alert(<메세지>) | 경고창 출력 |
| prompt(<메세지>, <임시 글자>) | 프롬프트 출력 |

- screen 객체 속성

| 속성 | 설명 |
|:----:|:----:|
| width | 화면의 너비 |
| height | 화면의 높이 |
| availWidth | 실제 화면에서 사용 가능한 너비 |
| availHeight | 실제 화면에서 사용 가능한 높이 |
| colorDepth | 사용 가능한 색상 수 |
| pixelDepth | 한 픽셀당 비트 수 |

- location 객체 속성

| 속성 | 설명 | 예 |
|:----:|:----:|:----:|
| href | 문서 URL 주소 | |
| host | 호스트 이름과 포트 번호 | localhost:52273 |
| hostname | 호스트 이름 | localhost |
| port | 포트 번호 | 52273 |
| pathname | 디렉터리 경로 | /folder/HTMLPage.html |
| hash | 앵커 이름(#~) | #test |
| search | 요청 매개 변수 | ?param=10 |
| protocol | 프로토콜 종류 | http: |

- location 객체 메소드

| 메소드 | 설명 |
|:----:|:----:|
| assign(<링크>) | 매개 변수로 전달한 위치로 이동 |
| reload() | 새로고침 |
| replace() | 매개 변수로 전달한 위치로 이동 (뒤로 가기 불가능) |

- history 객체

| 메소드 | 설명 |
|:----:|:----:|
| forward() | 앞으로 이동 |
| back() | 뒤로 이동 |

- navigator 객체
-- 실행하는 브라우저 정보 <br>
-- 사용자의 웹 브라우저, 운영체제 구분 <br>

| 속성 | 설명 |
|:----:|:----:|
| appCodeName | 웹 브라우저 코드 이름 |
| appName | 웹 브라우저 코드 이름 |
| appVersion | 웹 브라우저 버전 |
| platform | 사용 중인 운영체제의 시스템 환경 |
| userAgent | 웹 브라우저 전체적 정보 |

- 문서 객체 모델
-- 넓은 의미 : 웹 브라우저 HTML 페이지를 인식하는 방법 <br>
-- 좁은 의미 : document 객체와 관련된 객체 집합 <br>

- 문서 객체 : HTML 태크를 자바스크립트에 사용 할 수 있는 객체
- 노드 : 각 요소
-- 요소 노드 : h1 태그와 script 태그처럼 요소를 생성하는 노드 <br>
-- 텍스트 노드 : 화면에 출력되는 문자열 <br>

- 정적 생성 : 처음 실행할 때 HTML 페이지에 있는 태그를 읽으면서 생성
- 동적 생성 : 자바스크립트를 사용해 프로그램 실행 중 생성 <br>

- 문자 객체 조작 순서 - script 태그 아래 삽입 -> HTML 페이지 규모가 클 때 유지 보수 어려움 -> 이벤트 기능 사용
- 문서 객체 선택 : HTML -> (자바스크립트에서) 문서 객체

- 1개의 문서 객체 선택

| 메소드 | 설명 |
|:----:|:----:|
| document.getElementById(아이디) | 아이디를 사용해 문서 객체 선택 |
| document.querySelector(선택자) | 선택자를 사용해 문서 객체 선택 |
->(2번째 메소드) 매개 변수로 전달한 CSS 선택자로 선택되는 첫 번째 태그만 선택

- 여러 개의 문서 객체 선택

| 메소드 | 설명 |
|:----:|:----:|
| document.getElementByName(이름) | name 속성으로 여러 개의 문서 객체 선택 |
| document.getElementsByClassName(클래스) | class 속성으로 여러 개의 문서 객체 선택 |
| document.querySelectAll(선택자) | 선택자로 여러 개의 문서 객체 선택 |

- 문자 조작
innerHTML : 문서 객체 내부의 글자를 나타냄
- 스타일 조작

| 자바스크립트의 스타일 속성 |
|:----:|
| backgroundColor |
| borderRedius |
| borderBottom |

- 속성 조작

| 메소드 | 설명 |
|:----:|:----:|
| setAttribute(속성 이름, 속성 값) | 속성 지정 |
| getAttribute(속성 이름) | 속성 추출 |
-> 웹 표준에서 지원하지 않는 속성을 지정할 때

- 이벤트
```javascript
window.onload = function () { };
```
- 이벤트 속성 : onload
- 이벤트 이름, 이벤트 타입 : load 
- 이벤트 리스너, 이벤트 핸들러 : 이벤트 속성에 넣는 함수
- 이벤트 모델 : 문서 객체에 이벤트를 연결하는 방법 <br>

- 인라인 이벤트 모델 <br>
-- HTML 태그에서 on 문자열로 시작하는 속성을 이벤트와 관련 <br>
-- script 태그 내부에 있는 함수 호출<br>

- 고전 이벤트 모델
```javascript
var image = document.getElementById('image');
image.width = 100;
image.height = 100;
```
- 이벤트 객체 <br>
-- 익스플로러 : window 객체의 event 속성이 이벤트 객체 <br>
- 기본 이벤트 제거 <br>
-- return fasle; 리턴 <br>
-- a,form 태그에 자주 사용 <br>

- jQuery 사용 방법 : 파일 다운, cdn 사용
- $(<매개 변수>).메소드(<매개 변수>, <매개 변수>)
```javascript
window.jQuery = window.$ = jQuery;
```
- 객체 생성
```javascript
// 일반 문서 객체로 jQuery 객체 생성
$(document)

// CSS 선택자로 
$('h1')

// HTML 문자열로
$('<h1></h1>')
```
- 객체 탐색

| 메소드 | 설명 |
|:----:|:----:|
| parent() | 부모 태그 선택 |
| find() | 후손 태그 찾음 |

- 선택된 문서 객체의 수 : length
- 선택된 문서 객체 추출 : get() (객체 중 하나 선택)
- each() : 선택한 문서 객체에 반복을 적용
-> forEach() 메소드와 인덱스, 요소 순서가 다름 <br>

| Array 객체의 forEach() 메소드 | jQuery의 each() 메소드 |
|:----:|:----:|
| [].forEach(function (item, index) { }); | $('h1').each(function (index, item) { }); |

- 문자 조작
- text() : html 태그 내부의 문자 조작 -> 여러 개 문서 객체 선택할 때 모든 문서 객체 내부의 문자를 출력
- html() : html 태그 내부의 문자 조작 (HTML태그 인식) -> 첫 번째 문서 객체 내부의 문자를 출력 <br>
- css() : 스타일 조작
- attr() : 속성을 조작

- 문서 객체 추가

| 메소드 | 설명 |
|:----:|:----:|
| $((A).prependTo(<B>)) | A를 B 안쪽 앞에 추가 |
| $((A).appendTo(<B>)) | A를 B 안쪽 뒤에 추가 |
| $((A).insertBefore(<B>)) | A를 B 앞에 추가 |
| $((A).insertAfter(<B>)) | A를 B 뒤에 추가 |

- jQuery 이벤트 메소드

| 메소드 | 설명 |
|:----:|:----:|
| on() | 이벤트 연결 |
| off() | 이벤트 제거 |

- 이벤트 직접 연결
```javascript
$(<선택자>).on(<이벤트 이름>, <콜백 함수>)
```
| 메소드 | 설명 |
|:----:|:----:|
| keydown() | 키보드 키 눌렀을 때 |
| keypress() | 키가 입력되었을 때 |
| keyup() | 키보드 키 떼었을 때 |
| click() | 마우스 클릭했을 때 |
| dbclick() | 마우스 더블 클릭했을 때 |
| mousedown() | 마우스 버튼 눌렀을 때 |
| mouseenter() | 마우스 커서가 해당 태그로 들어갔을 때 |
| mouseleave() | 마우스 커서가 해당 태그에서 나갔을 때 |
| mousemove() | 마우스 움직일 때 |
| mouseup() | 마우스 버튼 땔 때 |
| blur() | 입력 양식 값 입력 종료할 때 |
| change() | 입력 양식의 값 변경될 때 |
| focus() | 입력 양식에 값 입력 시작할 때 |
| select() | type 속성이 select인 입력 양식의 목록에서 값을 선택했을 때 |
| submit() | type 속성이 submit인 입력 양식을 클릭했을 때 |
| resize() | 브라우저 크기변경 |
| scroll() | 브라우저 스크롤 |

- 이벤트 간접 연결 : 부모에게 이벤트를 위임해 부모가 이벤트를 처리
- 이벤트 제거 : off() 메소드 사용
- one() : 이벤트를 한번만 연결하는 메소드
- animate() : 애니메이션 메소드 -> 스타일에 적용
```javascript
$(<선택자>).animate(<속성>, <시간>, <콜백 함수>)
```
-> 콜백 함수는 애니메이션이 종료후 호출, 생략 가능
***
## [5월 25일]
***
## 내용 요약
- 웹 서버를 만들 떄는 이것이 필요하고, Node.js를 도구로 활용
- 웹 서버 : 요청과 응답의 요청
- 요청하는 대상 : 클라이언트(사용자)
- 응답하는 대상 : 서버(제공자)
- 요청 메세지 : 클라이언트가 서버로 보내는 편지
- 응답 메세지 : 서버가 클라이언트로 보내는 편지
- express 모듈의 기본 메소드

| 메소드 | 설명 |
|:----:|:----:|
| express() | 서버 어플리케이션 객체를 생성 |
| app.use() | 요청이 왔을 때 실행할 함수를 지정 |
| app.listen() | 서버를 실행 |

```javascript
// 모듈을 추출합니다.

const express = require('express');

// 서버를 생성

onst app = express();

// request 이벤트 리스너를 설정

app.use((request, response) => {
    response.send('<h1>Hello express</h1>');
});

// 서버를 실행

app.listen(52273, () => {
    console.log('Server running at http://127.0.0.1:52273');
});
```
- 페이지 라우팅 : 클라이언트 요청에 적절한 페이지를 제공하는 기술

- express 모듈의 페이지 라우팅 메소드

| 메소드 | 설명 |
|:----:|:----:|
| get(path, callback) | GET 요청이 발생했을 때 이벤트 리스너를 지정 |
| post(path, callback) | POST 요청이 발생했을 때 이벤트 리스너를 지정 |
| pull(path, callback) | PUT 요청이 발생했을 때 이벤트 리스너를 지정 |
| delete(path, callback) | DELETE 요청이 발생했을 때 이벤트 리스너를 지정 |
| all(path, callback) | 모든 요청이 발생했을 때 이벤트 리스너를 지정 |

- response 객체

| 메소드 | 설명 |
|:----:|:----:|
| send() | 데이터 본문을 제공 |
| status() | 상태 코드를 제공 |
| set() | 헤더를 설정 |

- send() 메소드 : 사용자에게 데이터 본문을 제공 <br>
-- 가장 마지막에 실행해야 하며, 두 번 실행x
```javascript
// request 이벤트 리스너를 설정

app.get('*', (request, response) => {
    response.status(404);
    response.set('methodA','ABCDE');
    response.set({
        'methodB1': 'FGHIJ',
        'methodB2': 'KLMNO'
    });
});
// set('문자얼','문자열') 또는 set(객체) 형태로 입력할 수 있다
```
- Content-Type <br>
-- 서버가 Content-Type을 제공 : 웹 브라우저는 헤더를 확인, 제공된 데이터의 형태를 확인(MIME라는 문자열로 제공)

| MINE 형식 | 설명 |
|:----:|:----:|
| text/plain | 기본적인 텍스트를 의미 |
| text/html | html 데이터를 의미 |
| image/png | png 데이터를 의미 |
| audio/mpe | MP3 음악 파일을 의미 |
| video/mpeg | MPEG 비디오 파일을 의미 |
| application/json | json 데이터를 의미 |
| multipart/form-data | 입력 양식 데이터를 의미 |

- MIME 형식을 지정 : type() 메소드 사용

| HTTP 상태 코드 | 설명 | 예 |
|:----:|:----:|:----:|
| 1XX | 처리 중 | 100 Continue |
| 2XX | 성공 | 200 OK |
| 3XX | 리다이렉트 | 300 Multple Choices |
| 4XX | 클라이언트 오류 | 400 Bad Request |
| 5XX | 서버 오류 | 500 Internal Server Error |

- 상태 코드를 지정 : status () 메소드 사용
- 리다이렉트 -> 특수한 상태 코드 <br>
-- 웹 브라우저가 리다이렉트를 확인하면 화면을 출력x, 응답 헤더에 있는 Location 속성을 확인 -> 위치로 이동 <br>
-- 특정 경로로 웹 브라우저를 인도 할 때 사용

- redirect() : 리다이렉트

- request 객체

| 분류 | 값 | 설명 |
|:----:|:----:|:----:|
| 프로토콜 | HTTPS | 통신에 사용되는 규칙 |
| 호스트 | (search.)naver.com | 애플리케이션 서버(또는 분산 장치 등)의 위치 |
| URL | search.naver | 애플리케이션 서버 내부에서 라우트 위치 |
| 요청 매개 변수 | ?where=nexearch &query=초콜릿 &sm=top_hty &fbm=0 &ie=utf8 | 추가적인 정보를 의미 |

use() : 미들웨어를 설정

- 정적 파일 제공
- 웹 페이지에서 변경되지 않는 요소를 쉽게 제공
- morgan 미들웨어 : 로그 출력 미들웨어
- 로그 : 관련된 정보를 가진 글자
- 로그 출력 미들웨어 : 웹 요청과 관련된 내용을 출력하는 미들웨어
```javascript
const app = express();
app.use(express.static('public'));
app.use(morgan('combined'));
```
- body-parser 미드웨어 : 요청 본문을 분석 <br>
-- 클라이언트에서 서버로 데이터 전송
- URL을 사용한 요청
- 요청 본문 <br>
-- 클라이언트가 서버로 본문을 전달할 때 요청 본문의 종류 함께 전달

| MIME 형식 | 설명 |
|:----:|:----:|
| application/x-www-form-urlencoded | 웹 브라우저에서 입력 양식을 POST, PUT, DELETE 방식 등으로 전달할 때 사용하는 기본적인 요청 형식 |
| application/json | JSON 데이터로 요청하는 방식 |
| multipart/form-data | 대용량 파일을 전송할 때 사용하는 요청 방식 |

- 속성 정리 : 클라이언트가 서버로 데이터를 전송하는 방법 <br>
-- params 객체 : URL의 토큰 - 보기가 간편 <br>
-- query 객체 : URL의 요청 매개 변수 - 토큰보다 많은 데이터를 전달할 수 있으며, 주소로 어떤 데이터가 오고 가는지 확인가능 <br>
-- body 객체 : 대용량 문자열 등을 전송할 때 사용- 주소에 데이터를 기록하지 못하므로 새로고침이나 즐겨찾기 기능 등을 활용할 수 없음

- REST 규정에 맞게 만든 ROA를 따르는 웹 서비스 디자인 표준

| 메소드 | 컬렉션(배열) | 요소 |
|:----:|:----:|:----:|
|  | /collection | collection/id |
| GET | 컬렉션을 조화 | 컬렉션의 특정 요소를 조회 |
| POST | 컬렉션에 새로운 데이터 추가 | 사용 X |
| PUT | 컬렉션에 전체를 한꺼번에 변겅 | 컬렉션에 특정 요소를 수정 |
| DELETE | 컬렉션에 전체를 삭제 | 컬렉션에 특정 요소를 삭제 |

- 사용자 관련 정보 (예시)
- GET/user : 사용자 전체를 조회
- GET/user/273 : 273번 사용자를 조회
- POST/user : 사용자를 추가
- DELETE/user/273 : 273번 사용자를 삭제

| 메소드 | 경로 | 설명 |
|:----:|:----:|:----:|
| GET | /user | 모든 사용자 정보 조회 |
| POST | /user | 사용자 추가 |
| GET | /user/:id | 특정 사용자 정보 조회 |
| PUT | /user/:id | 특정 사용자 정보 수정 |
| DELETE | /user/:id | 특정 사용자 정보 제거 |

***
## [5월 18일]
***
## 내용 요약
- Node.js
- 전역 변수, 전역 함수, 전역 객체 : 모든 곳에서 사용할 수 있는 것들

| 변수 | 설명 |
|:----:|:----:|
| __filename | 현재 실행 중인 코드 파일 경로 |
| __dimame | 현재 실행 중인 코드의 폴더 경로 |

- process에 전역 객체를 제공
- process 객체는 프로세스 정보 제공 + 제어 기능

| 속성 | 설명 |
|:----:|:----:|
| env | 컴퓨터 환경 정보 |
| version | Node.js 버전 |
| versions | Node.js와 종속된 프로그램 버전 |
| arch | 프로세서의 아키텍처 |
| platform | 플랫폼 |

| 메소드 | 설명 |
|:----:|:----:|
| exit([exitCode = 0]) | 프로그램 종료 |
| memoryUsage() | 메모리 사용 정보 객체 |
| uptime() | 현재 프로그램이 실행된 시간 |
```javascript
// process 객체의 속성과 메소드를 사용
console.log('- process.arch:', process.arch );
```
- Node.js의 이벤트 연결 메소드

| 메소드 | 설명 |
|:----:|:----:|
| on(<이벤트 이름>,<이벤트 핸들러>) | 이벤트 연결 |

| 이벤트 | 설명 |
|:----:|:----:|
| exit | 프로세스 종료될 때 발생 |
| uncaughtException | 프로세스 종료될 때 발생 |

```javascript
// 이런식으로 연결
process.on('exit', () => {
    console.log('프로세스 종료');
});
```
- 이벤트 매개 변수 : 이벤트 핸들러의 매개 변수로 전달되는 매개 변수
```javascript
process.on('exit', (code) => {
    console.log(`About to exit with code: ${code}`);
});
```
- os 모듈 사용
```javascript
const os = require('os');

// 모듈을 추출
const OS = require('OS');
```

| 메소드 | 설명 |
|:----:|:----:|
| hostname() | 운영체제의 호스트 이름 |
| type() | 운영체제의 이름 |
| platform() | 운영체제의 플랫폼 |
| arch() | 운영체제의 아키텍처 |
| release() | 운영체제의 버전 |
| uptime() | 운영체제가 실행된 시간 |
| loadavg() | 로드 에버리지 정보를 담은 배열 |
| totalmem() | 시스템의 총 메모리 |
| freemem() | 시스템의 사용 가능한 메모리 |
| cups() | CPU의 정보를 담은 객체 |
| getNetworkInterfaces() | 네트워크 인터페이스의 정보를 담은 배열 |

- url 모듈
```javascript
const url = require('url');
```
| 메소드 | 설명 |
|:----:|:----:|
| parse(urlStr,[.parseQueryString = false, slashesDenoteHost = false]) | URL문자열을 URL객체로 변환 |
| format(urlObj) | URL객체를 URL문자열로 변환 |
| resolve(from, to) | 매겨 변수를 조합하여 완전한 URL문자열을 생성 |

- File System
```javascript
const fs = require('fs');
```
- 파일읽기

| 메소드 | 설명 |
|:----:|:----:|
| fs.readFileSync(<파일 이름>) | 동기적으로 파일을 읽어드림 |
| fs.readFile(<파일 이름>,<콜백 함수>) | 비동기적으로 파일을 읽어드림 |

- 동기 : 메소드 뒤에 Sync문자가 붙음,코드 순서대로 실행
- 비동기 : Node.js가 제공하는 메소드 대부분, 빠른코드를 쉽게 만듬 <br>
-- 비동기 처리의 장점 <br>
-- 개발 속도와 유지 보수성이 좋은 프로그래밍 언어를 사용
C++, 자바 보다 느리지만 Node.js를 사용하면 손쉽게 비동기 처리 구현 -> 빠른 처리가능 <br>
- 파일 쓰기

| 메소드 | 설명 |
|:----:|:----:|
| fs.writeFileSync(<파일 이름>, <문자열>) | 동기적으로 파일을 씀 |
| fs.writeFile(<파일 이름>,<문자열>,<콜백 함수>) | 비동기적으로 파일을 씀 |

- 파일 처리와 예외 처리 <br>
-- 동기 코드 예외처리 : try catch 구문 <br>
-- 비동기 코드 예외처리 : 콜백함수의 첫 번째 매개 변수 error를 활용 <br>

```javascript
const request = require('request');

// request 모듈 사용
const url = 'http://www.hanbit.co.kr/store/books/new_book_list.html';
request(url, (error, response, body) => {
    console.log(body);
});
```
- 단순한 HTML 문자열, 여기에서 원하는 정보를 추출해야 단순한 데이터가 정보가 됨 -> 파싱
- cheerio 모듈 : 가져온 웹 페이지의 특정 위치에서 손쉽게 데이터를 추출
```javascript
const cheerio = require('cheerio');
```
- async 모듈
```javascript
const async = require('async');
```
***
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

>예외처리
>> 예외 : 실행에 문제가 발생하면 자동 중단 <br>
 예외 처리 : 오류에 대처할 수 있게 하는 것

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
-- throw 키워드 사용 <br>
-- throw 키워드 뒤에는 문자열 또는 Error 객체 입력
>throw '강제 예외';
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