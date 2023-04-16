# **이수용**

## ***23.04.13 7주차 정리***

## 훅(Hook)
>클래스형 컴포넌트가 아닌 함수형 컴포넌트에서 상태를 관리하기 위한 함수의 기능을 사용할 수 있게 추가된 기능

중간에 갈고리로 걸어서 중간에 빼오는, 일종의 트리거..라고 생각해도 괜찮을거 같다. 과거의 클래스형 컴포넌트에서는 setState()를 사용해서 상태관리를 했지만. 함수형 컴포넌트에선 이를 사용할 수 없어서 이 같은 기능이 만들어졌다.  
  
훅의 이름은 모두 `use`로 시작하며 
커스텀훅(사용자 정의)또한 설정시 `use`로 시작해야 함.

## **규칙**

### 1. 컴포넌트의 최상위 레벨에서만 호출해야 함
- 반복문, 조건문, 내부 정의된 함수에서 호출 불가능
### 2. 리액트 함수(컴포넌트)에서만 호출해야 함
- 당연하지만 컴포넌트가 아닌 일반 js파일에선 호출 할 수 없다.

## **예시**
- useState
- useEffect
- useMemo
- useCallback
- useRef  

이 중 상태관리를 위한 useState와 마운트되거나, state가 변경되거나, props값이 변할 때 발동되는 useEffect를 가장 많이 사용한다. 


<hr/>

## ***23.03.23 4주차 정리***

## **JSX**
### JavaScript에 XML와 HTML태그를 넣어서 쓸 수 있는 확장언어

만일 JS로만 작업을 할 경우, 직접 이를 작성해줘야 하므로 가독성과 효율이 떨어진다.  
리액트에선 JSX 문법을 createElement를 통해 변환해주고, 브라우저에서는 실행하기전 babel을 통해 바닐라 JS  형태로 변환된다.  

 ## **JSX의 장점** 
1. 코드가 간결해진다. 
2. 가독성이 향상된다.
3. JS 악성코드를 Injection 하여 해킹하는것을 방지한다.

> React DOM escapes any values embedded in JSX before rendering them. Thus it ensures that you can never inject anything that’s not explicitly written in your application. Everything is converted to a string before being rendered.  

>React DOM은 렌더링하기 전에 JSX에 포함된 모든 값을 이스케이프 처리합니다. 따라서 애플리케이션에 명시적으로 작성되지 않은 것은 주입할 수 없습니다. 모든 것은 렌더링되기 전에 문자열로 변환됩니다.  
<span style="font-size:75%">출처 : https://iq.js.org/questions/react/how-jsx-prevents-injection-attacks</span>

 

<hr/>

## 23.03.16 3주차 정리

## React란?

React는 사용자 인터페이스를 만들기위한 자바스크립트 라이브러리로, 이름에서 알 수 있듯이 사용자의 반응과 리액션에 대해 반응해주는 웹을 만들기 위해 있는 라이브러리다.  
SPA(Single Page application)을 쉽고 빠르게 만들 수 있으며 최근 버전인 18에선 SSR(Server Side Render)도 지원예정이다.

## 장점과 특징
1. 빠른 업데이트와 렌더링 속도
Virtual DOM을 사용하여 렌더링을 하고, SPA특유의 빠른 렌더링 전환이 특징이다.

2. 컴포넌트와 재사용
React는 각 웹의 요소를 컴포넌트로 분할시켜 사용하기 때문에 자주 사용하는 웹 요소(NavBar, footer, header)등은 쉽게 재사용이 가능하다.

3. 뒷배가 든든함
아무리 페이스북이 조졌어도 대기업은 대기업

4. 수많은 추가 라이브러리와 넷상에 있는 수많은 예제코드, 뉴비에게 아주 좋다.

5. 수틀릴 경우 Native로 모바일도 개발가능.
React Native로 크로스플랫폼 모바일앱을 개발 가능하다.

## 단점
1. SPA특유의 불안정성과 느린 반응
네이버같은 대형 플랫폼등은 결국 이때문에 SSR을 택하는 경우가 많아짐.
2. 높은 상태 관리 복잡도
수많은 컴포와 하위컴포, state에서 펼쳐지는 props의 굴레..


<hr/>

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
