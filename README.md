# 이수용

## 23.03.09 2주차 정리

### HTML (Hyper Text Markup Language)
<br/>

웹 사이트의 뼈대가 되는 언어이며, 시작는 문서와 문서를 잇는 인터넷 기반 hyper text에서 시작되어 현재는 웹에서 빼놓을 수 없는 마크업 언어다. <br/>

HTML의 요소는 태그로 선언한다. ex) <div> / <input> 등 <br/><br/>

<br/>

### CSS (Cascading Style Sheets)
<br/>

HTML은 웹페이지의 구역만 정하는 반면, <br/>

CSS는 요소들의 색이나 자세한 위치를 정의하여 배치해주는 언어이다. <br/>

### JS (Java Script)
<br/>

HTML과 CSS만을 사용한 페이지는 서버의 데이터가 변경되지 않는 한 항상 같은 페이지를 보여주는 **정적인** 웹 페이지 이지만, <br/>
JS는 사용자의 다양한 요청들에 의해 변경되는 **동적인** 웹 페이지를 만들 수 있다.

작성일자를 기준으로 표준으로 사용되는 것은 EC6(ECMAScript6)이다. 익명함수, 구조분해 할당 등이 추가된 버전이다.<br/>

> ECMAScript : Ecma International에서 ECMA-262 기술 규격에 따라 정의하고 있는 표준화된 스크립트 언어 <br/>

#### JSON (Java Script Object Notation)
<br/>

인터넷에서 서버와 유저 컴퓨터가 통신하는 과정에서 데이터를 텍스트 기반으로 표현한 **데이터 포멧**이다. <br/>

`key-value`의 형태로 이루어 진다. <br/>

#### JS의 자료형
<br/>

|자료형|중복선언|재할당| <br/>
|:-:|:-:|:-:|:-:|
|var|O|O|
|let|X|O|
|const|X|X| <br/>

> 중복 선언 : 해당 변수의 자료형을 변경시키는 행위 (ex : `int -> String`)<br/>
재할당 : 변수의 값을 변경하는 행위 (ex : `a = 1 -> a = 2`) <br/>

#### JS의 연산자
<br/>

JS의 연산자에는 '==' 와 '===' 가 구분되어 있는데, <br/>
2개는 변수의 타입을 고려하지 않고 값만 비교하지만 <br/>
3개는 2개와 달리 변수의 타입까지 고려한다. <br/>

>`a = 1, b = '1'` <br/>
`a == b -> true, a === b -> false`

#### JS의 함수
<br/>

JS에서는 함수의 형태에는 2가지가 있다. <br/>

1. 일반적인 함수의 형태 <br/>
2. 화살표 함수 <br/>

``` JavaScript
//일반적인 함수의 형태의 예시
let basic = function (a, b) {
    return a * b;
};

//위의 예시를 화살표함수로 표현한 예시
let arrow = (a, b) => a * b;
```
