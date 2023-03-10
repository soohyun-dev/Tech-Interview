# 23년 3월 둘째주 Weekly Study

<br>

### 📜 목차

1. HTML이 렌더링 중에 JavaScript가 실행되면 멈추는데 그 이유는 무엇일까요?
2. require와 import의 차이점에 대해 설명해주세요.
3. SASS(SCSS)를 사용해본 적이 있나요? 기존 CSS와 비교할 때 어떤 면이 더 좋은가요?
4. CORS에 대처하는 방법과 우회하는 방법에 대해 설명해주세요.
5. React의 라이프 사이클에 대해 설명해주세요.
6. ES6에서 Arrow 함수를 언제 쓰나요? 왜 쓰나요?
7. React의 상태관리 방법에 대해서 설명하시오
8. React의 라이프사이클에 대해 설명해주세요
9. var, let, const의 차이점
10. Flex 속성을 설명해주세요.
11. OOP의 특징에 대해서 설명하시오
12. 웹팩과 바벨은 무엇인가?
13. JWT 방식을 설명하고, 왜 사용했는지?
14. .call과 .apply, bind의 차이점은 무엇인가요?
15. AJAX에 대해 자세히 설명하세요(+장단점)
16. use strict 이 무엇인가요? 사용시 장단점이 무엇인가요?
17. Box model에 대해 설명해주세요.
18. Prototype이란? Prototype Chaining은?
19. forEach와 Map의 차이점은?
20. 화살표 함수와 일반함수의 차이점

<br>

## 📌 1. HTML이 렌더링 중에 JavaScript가 실행되면 멈추는데 그 이유는 무엇일까요?

웹 브라우저는 HTML 문서를 렌더링하면서 JavaScript 코드를 실행합니다.

그러나 JavaScript 코드가 실행될 때 렌더링 작업이 중단될 수도 있습니다.

이는 JavaScript가 브라우저의 싱글 스레드(single-threaded)로 동작하기 때문입니다.

브라우저의 싱글 스레드는 하나의 작업만을 처리할 수 있으므로, JavaScript 코드가 실행되는 동안에는 다른 작업들이 중단됩니다.

즉, 브라우저는 HTML 문서의 렌더링을 중지하고 JavaScript 코드를 실행한 후에 다시 렌더링 작업을 재개합니다.

이러한 이유 때문에 JavaScript 코드가 매우 길거나 복잡하면 렌더링 속도가 느려질 수 있습니다.

JavaScript 코드가 블로킹(blocking) 작업을 수행하면, 렌더링 작업이 중단되어 사용자가 웹 페이지를 볼 수 없게 됩니다.

이는 JavaScript 코드가 실행되는 동안에 다른 작업들이 처리되지 못하기 때문입니다.

이러한 블로킹 작업은 예를 들어, 네트워크 요청을 기다리는 작업이나, 반복문을 실행하는 작업 등이 있을 수 있습니다.

따라서 최적화된 코드 작성과 비동기(asynchronous) 프로그래밍 기술을 사용하는 것이 좋습니다.

이러한 기술을 사용하면 JavaScript 코드가 실행되는 동안에도 다른 작업들이 수행될 수 있으므로, 브라우저의 렌더링 작업을 방해하지 않으면서도 JavaScript 코드를 실행할 수 있습니다.

<br>

## 📌 2. require와 import의 차이점에 대해 설명해주세요.

require와 import는 JavaScript에서 모듈을 가져오는 데 사용되는 키워드입니다.

이 두 키워드는 각각 CommonJS와 ES6 모듈 시스템에서 사용됩니다.

require는 CommonJS 모듈 시스템에서 사용되며, Node.js에서 주로 사용됩니다.

CommonJS는 모듈이 동기적으로 로드되어 실행되는 방식입니다.

require는 파일 경로를 인수로 받아서 해당 모듈을 동기적으로 로드하고, 모듈 객체를 반환합니다.

반면에, import는 ES6 모듈 시스템에서 사용되며, 브라우저나 모던 JavaScript 프레임워크에서 주로 사용됩니다.

ES6 모듈은 비동기적으로 로드되어 실행되는 방식입니다. import는 모듈 경로를 인수로 받아서 해당 모듈을 비동기적으로 로드하고, 모듈 객체를 반환합니다.

또한, import는 require와 다르게 모듈을 가져올 때, 가져온 모듈을 변경할 수 없습니다.

하지만 require를 사용할 경우, 가져온 모듈을 변경할 수 있습니다.

또 다른 차이점은, require는 런타임에 모듈을 로드하기 때문에 조건부로 모듈을 로드할 수 있습니다.

반면에, import는 정적으로 모듈을 로드하기 때문에 조건부로 모듈을 로드할 수 없습니다.

<br>

### 결론

결론적으로, require와 import는 각각 CommonJS와 ES6 모듈 시스템에서 사용되는 키워드입니다.

require는 동기적으로 모듈을 로드하고, import는 비동기적으로 모듈을 로드합니다.

또한, import는 모듈을 변경할 수 없으며, 조건부로 모듈을 로드할 수 없습니다.

<br>

## 📌 3. SASS(SCSS)를 사용해본 적이 있나요? 기존 CSS와 비교할 때 어떤 면이 더 좋은가요?

SASS(SCSS)는 CSS의 전처리기(preprocessor)로, 기존 CSS에 비해 다양한 기능을 제공합니다.

SASS(SCSS)를 사용하면, CSS를 보다 효율적이고 유지보수가 용이한 코드로 작성할 수 있습니다.

SASS(SCSS)는 기본적으로 변수, 함수, 믹스인(mixin), 상속 등을 지원합니다.

변수를 사용하면 스타일에서 반복적으로 사용되는 값을 한 곳에서 관리할 수 있고, 함수와 믹스인을 사용하면 스타일 코드의 중복을 줄일 수 있습니다.

또한, 상속을 사용하면 중복되는 스타일 코드를 상위 요소에서 정의하고 하위 요소에서 상속받아 사용할 수 있습니다.

또한, SASS(SCSS)는 네스팅(nesting) 기능을 지원합니다.

이를 사용하면, HTML 구조와 유사하게 CSS 코드를 작성할 수 있어서 코드 가독성이 향상됩니다.

또한, BEM(Block Element Modifier) 등의 CSS 방법론과도 함께 사용이 가능합니다.

마지막으로, SASS(SCSS)는 기존 CSS와 호환성이 뛰어나기 때문에, 기존 CSS 코드와 쉽게 통합할 수 있습니다.

즉, SASS(SCSS)로 작성된 코드를 CSS로 컴파일하면, 기존 CSS와 완전히 동일한 코드가 생성됩니다.

<br>

## 📌 4. CORS에 대처하는 방법과 우회하는 방법에 대해 설명해주세요.

### 서버 측 설정 변경

CORS 에러는 서버 측에서 발생하는 문제이기 때문에, 서버 측에서 설정을 변경하면 문제를 해결할 수 있습니다.

서버 측에서는 Access-Control-Allow-Origin 헤더를 사용하여, 허용된 도메인만 리소스 요청을 처리하도록 설정할 수 있습니다.

이를 통해, 서버 측에서 CORS 에러를 해결할 수 있습니다.

<br>

### JSONP 사용

JSONP (JSON with Padding)는 서로 다른 도메인에서 스크립트를 호출할 때 사용되는 기술로, CORS 에러를 우회하는 방법 중 하나입니다.

JSONP는 script 태그를 사용하여 호출되며, 호출된 결과는 콜백 함수를 통해 처리됩니다.

<br>

### 프록시 서버 사용

프록시 서버를 사용하면, 클라이언트 측에서 요청을 보내는 대신, 프록시 서버에서 요청을 받아 다시 서버로 요청을 보내는 방식으로 CORS 에러를 우회할 수 있습니다.

<br>

### 크롬 브라우저 확장 프로그램 사용

크롬 브라우저에서는 CORS 에러를 우회할 수 있는 확장 프로그램이 있습니다.

이를 사용하면, 서로 다른 도메인에서 리소스를 요청할 때 발생하는 CORS 에러를 우회할 수 있습니다.

CORS 에러는 보안상의 이유로 발생하는 문제이기 때문에, 보안 정책을 우회하는 방법은 권장되지 않습니다.

따라서, CORS 에러가 발생할 경우에는, 서버 측에서 설정을 변경하거나, JSONP나 프록시 서버 등의 대안 방법을 고려하는 것이 좋습니다.

<br>

## 📌 5. React의 클래스형 라이프 사이클에 대해 설명해주세요.

## Mounting(마운팅)

### 1. constructor()

컴포넌트가 생성될 때 호출되는 메서드입니다.

### 2. static getDerivedStateFromProps(props, state)

props와 state가 변경되어 컴포넌트가 다시 렌더링될 때 호출되는 메서드입니다.

이 메서드는 초기 마운트와 업데이트 모두에서 호출됩니다.

### 3.render()

컴포넌트를 렌더링하는 메서드입니다.

### 4. componentDidMount()

컴포넌트가 브라우저에 마운트된 직후에 호출되는 메서드입니다.

DOM 노드를 조작하거나 외부 데이터를 불러오는 등의 작업을 수행하기에 적합합니다.

<br>

## Updating(업데이트)

### 1. static getDerivedStateFromProps(props, state)

props와 state가 변경되어 컴포넌트가 다시 렌더링될 때 호출되는 메서드입니다.

### 2. shouldComponentUpdate(nextProps, nextState)

컴포넌트가 다시 렌더링해야 하는지 결정하는 메서드입니다.

성능 최적화를 위해 사용됩니다.

### 3. render()

컴포넌트를 렌더링하는 메서드입니다.

### 4. getSnapshotBeforeUpdate(prevProps, prevState)

컴포넌트가 업데이트되기 직전에 호출되는 메서드입니다.

이전 props와 state를 참조하여 DOM에 변경된 내용이 있을 경우에 사용됩니다.

### 5. componentDidUpdate(prevProps, prevState, snapshot)

컴포넌트가 업데이트된 직후에 호출되는 메서드입니다.

이전 props와 state를 참조하여 DOM을 업데이트하는 등의 작업을 수행하기에 적합합니다.

<br>

## Unmounting(언마운팅)

### 1. componentWillUnmount()

컴포넌트가 DOM에서 언마운트되기 전에 호출되는 메서드입니다.

리소스 해제 등의 작업을 수행하기에 적합합니다.

<br>

## Error Handling(에러 처리)

### 1.static getDerivedStateFromError(error)

하위 컴포넌트에서 발생한 에러를 처리하기 위해 호출되는 메서드입니다.

이 메서드를 구현하면 componentDidCatch()는 호출되지 않습니다.

### 2. componentDidCatch(error, info)

하위 컴포넌트에서 발생한 에러를 처리하기 위해 호출되는 메서드입니다.

이전 상태를 저장하거나 로그를 기록하는 등의 작업을 수행하기에 적합합니다.

<br>

React의 라이프사이클은 컴포넌트의 생명 주기에 따라 호출되는 메서드들의 집합입니다.

컴포넌트의 생명 주기는 세 가지 단계로 구성되며, 각 단계에서 다양한 라이프사이클 메서드들이 호출됩니다.

마운팅 단계는 컴포넌트가 브라우저에 마운트될 때 호출되는 메서드들입니다.

이 단계에서는 constructor(), static getDerivedStateFromProps(), render(), componentDidMount() 메서드가 호출됩니다.

업데이트 단계는 컴포넌트의 props나 state가 변경되어 컴포넌트가 다시 렌더링될 때 호출되는 메서드들입니다.

이 단계에서는 static getDerivedStateFromProps(), shouldComponentUpdate(), render(), getSnapshotBeforeUpdate(), componentDidUpdate() 메서드가 호출됩니다.

언마운팅 단계는 컴포넌트가 DOM에서 언마운트될 때 호출되는 메서드입니다.

이 단계에서는 componentWillUnmount() 메서드가 호출됩니다.

에러 처리 단계는 하위 컴포넌트에서 에러가 발생했을 때 호출되는 메서드들입니다.

이 단계에서는 static getDerivedStateFromError(), componentDidCatch() 메서드가 호출됩니다.

React의 라이프사이클 메서드는 컴포넌트의 상태 변화를 감지하여 다양한 작업을 수행할 수 있습니다.

이를 통해 컴포넌트의 상태 변화에 따라 DOM을 업데이트하거나 외부 데이터를 불러오는 등의 작업을 수행할 수 있습니다.

<br>

## 📌 6. ES6에서 Arrow 함수를 언제 쓰나요? 왜 쓰나요?

S6에서 Arrow 함수는 기존의 함수 정의 방식에 비해 간결하고 가독성이 좋아서 많이 사용됩니다.

Arrow 함수를 사용하는 경우는 다음과 같습니다.

### 1. 콜백 함수로 사용하는 경우

Arrow 함수는 콜백 함수로 자주 사용됩니다. 콜백 함수는 보통 함수 안에서 선언되고, 해당 함수가 호출될 때 실행됩니다.

일반 함수로 콜백 함수를 선언하면 함수 내부에서 this 키워드를 사용할 때 주의해야 하지만, Arrow 함수를 사용하면 this를 바인딩할 필요가 없기 때문에 편리합니다.

### 2. 메서드로 사용하는 경우

Arrow 함수는 객체의 메서드로도 자주 사용됩니다.

객체의 메서드는 객체 내부에서 this 키워드를 사용할 수 있어야 합니다.

Arrow 함수를 사용하면 this를 바인딩하지 않아도 상위 스코프의 this를 그대로 사용할 수 있기 때문에 메서드로 사용할 때 유용합니다.

### 3. 함수 표현식으로 사용하는 경우

Arrow 함수는 함수 표현식으로도 사용할 수 있습니다.

함수 표현식은 변수에 함수를 할당하는 것을 말합니다.

Arrow 함수는 함수 표현식으로 사용될 때 코드가 더 간결해지고 가독성이 좋아집니다.

### 4. 함수를 리턴하는 함수를 작성하는 경우

함수를 리턴하는 함수를 작성할 때 Arrow 함수를 사용하면 코드가 더 간결해집니다.

이때 Arrow 함수를 사용하면 내부 함수에서 this를 바인딩하지 않아도 상위 스코프의 this를 그대로 사용할 수 있어서 편리합니다.

<br>

## 📌 7. React의 상태관리 방법에 대해서 설명하시오

React에서는 상태(state)를 효과적으로 관리하기 위해 다양한 방법을 제공합니다.

### 1. Props

React에서 가장 기본적인 상태 전달 방법은 Props를 사용하는 것입니다.

Props는 상위 컴포넌트에서 하위 컴포넌트로 데이터를 전달하는 방법으로, 단방향 데이터 흐름을 가집니다.

Props를 사용하면 상위 컴포넌트에서 하위 컴포넌트로 필요한 데이터를 전달하여 하위 컴포넌트에서 상태를 관리할 수 있습니다.

### 2. State

State는 React 컴포넌트 내부에서 관리되는 상태입니다.

State를 사용하면 컴포넌트 내부에서 상태를 변경하고 렌더링할 수 있습니다. State는 클래스 컴포넌트에서 사용할 수 있습니다.

### 3. React Hooks

Hooks는 React 16.8 버전부터 도입된 기능으로, 함수형 컴포넌트에서 상태를 관리할 수 있게 해줍니다.

useState, useEffect, useContext, useReducer 등 다양한 Hooks를 제공하여 상태 관리를 보다 편리하게 할 수 있습니다.

Hooks는 함수형 컴포넌트에서 상태를 관리할 수 있기 때문에, 코드의 재사용성이 높아지고 컴포넌트의 구조도 간단해집니다.

### 4. Redux

Redux는 React에서 사용하는 상태 관리 라이브러리입니다.

Redux를 사용하면 애플리케이션의 전역 상태를 관리할 수 있습니다.

Redux를 사용하면 상태 변경 로직을 분리하여 구현할 수 있기 때문에, 코드 유지보수성이 높아지고 테스트하기 쉬워집니다.

### 5. MobX

MobX는 React에서 사용하는 다른 상태 관리 라이브러리입니다.

MobX는 데이터 상태를 관찰하고 상태 변경에 따라 자동으로 업데이트하는 방식으로 동작합니다.

이를 통해 코드의 간결성과 유지보수성이 높아지는 장점이 있습니다.

### 6. Context API

Context API는 React에서 제공하는 전역 상태 관리 방법입니다.

Context API를 사용하면 여러 컴포넌트에서 공통으로 사용하는 상태를 간편하게 관리할 수 있습니다.

예를 들어, 로그인 상태나 애플리케이션 설정 정보 등을 Context API를 통해 전역적으로 관리할 수 있습니다.

### 7. Recoil

Recoil은 Facebook에서 개발한 React에서 사용할 수 있는 새로운 상태 관리 라이브러리입니다.

Recoil은 상태를 전역에서 관리하는 것이 아니라, 애플리케이션 내부에서 원하는 곳에서 간편하게 상태를 정의하고 사용할 수 있습니다.

이를 통해 상태의 의존성을 명확하게 표현할 수 있고, 상태 변경 로직을 간단하게 구현할 수 있습니다.

<br>

## 📌 8. React의 함수형 라이프사이클에 대해 설명해주세요

함수형 컴포넌트는 React 16.8 버전에서 Hooks 기능이 추가되면서 함수형 컴포넌트에서도 상태(state)와 생명주기(lifecycle)를 다룰 수 있게 되었습니다.

Hooks는 함수형 컴포넌트에서도 상태 관리와 라이프사이클 기능을 제공하며, 클래스형 컴포넌트에서만 사용할 수 있었던 기능들을 함수형 컴포넌트에서도 사용할 수 있게 만들어 줍니다.

함수형 컴포넌트에서는 useEffect Hook을 사용하여 컴포넌트의 라이프사이클을 다룰 수 있습니다.

useEffect Hook은 클래스형 컴포넌트에서 사용되는 componentDidMount, componentDidUpdate, componentWillUnmount 메서드를 모두 대체할 수 있습니다.

<br>

## 📌 9. var, let, const의 차이점

### var

var은 변수를 선언하는 가장 오래된 방법입니다.

var로 선언된 변수는 함수 스코프를 가지고 있으며, 블록 스코프가 없습니다. 또한 var로 선언된 변수는 호이스팅(hoisting)이 발생합니다.

호이스팅은 변수를 선언하기 전에도 변수를 사용할 수 있는 현상을 의미합니다.

이는 var로 선언된 변수가 블록 스코프가 없기 때문에 발생하는데, 이로 인해 예상치 못한 결과가 발생할 수 있습니다.

### let

let은 var와는 달리 블록 스코프를 가지고 있습니다. 따라서 블록 안에서 선언된 변수는 블록 안에서만 유효합니다.

let으로 선언된 변수는 TDZ(Temporal Dead Zone)를 가집니다.

TDZ는 변수가 선언되었지만 아직 초기화되지 않았을 때, 변수를 사용할 수 없는 상태를 의미합니다.

즉, 변수가 선언되기 이전에 변수를 사용하려고 하면 ReferenceError가 발생합니다.

### const

const는 let과 마찬가지로 블록 스코프를 가지고 있습니다. const로 선언된 변수는 재할당이 불가능합니다.

즉, 상수(constant)로 취급되므로 한 번 할당한 값을 변경할 수 없습니다.

<br>

var, let, const 모두 호이스팅이 발생하지만,

let과 const는 TDZ(Temporal Dead Zone)이 존재합니다.

TDZ는 변수가 선언되었지만 아직 초기화되지 않은 상태를 의미하며, TDZ에서 변수를 사용하려고 하면 ReferenceError가 발생합니다.

이러한 TDZ는 let과 const를 사용할 때 발생하는데, 변수를 선언할 때 메모리에 공간을 할당하기 때문에 JavaScript 엔진이 변수 선언을 최상단으로 옮기는 것을 호이스팅이라고 합니다.

그러나 let과 const는 선언 시 초기화되지 않으므로, 변수가 TDZ에 빠지게 됩니다.

따라서, let과 const를 사용할 때는 변수를 사용하기 전에 반드시 선언과 초기화가 필요하며, 이를 지키지 않으면 ReferenceError가 발생합니다.

반면에, var는 호이스팅 때문에 변수를 선언하기 전에 사용할 수 있습니다.

이는 코드의 예측성을 떨어뜨리므로, ES6에서는 var보다는 let과 const를 사용하는 것을 권장하고 있습니다.

<br>

## 📌 10. Flex 속성을 설명해주세요.

Flexbox(Flexible Box)는 CSS3에서 도입된 레이아웃 모델로, 유연한 박스 모델을 사용하여 요소의 크기와 위치를 관리할 수 있습니다.

Flexbox를 사용하면 요소를 행 또는 열로 배치할 수 있으며, 각 요소의 크기와 위치를 지정할 수 있습니다.

Flexbox에서 사용하는 주요 속성은 다음과 같습니다.

<br>

### 1. display: flex

Flexbox를 적용할 요소에 적용합니다.

### 2. flex-direction

요소를 배치할 방향을 설정합니다. (row, row-reverse, column, column-reverse)

### 3. flex-wrap

요소를 한 줄 또는 여러 줄에 걸쳐 배치할지 여부를 설정합니다. (nowrap, wrap, wrap-reverse)

### 4. justify-content

주 축의 정렬 방법을 설정합니다. (flex-start, flex-end, center, space-between, space-around, space-evenly)

### 5. align-items

교차 축의 정렬 방법을 설정합니다. (stretch, flex-start, flex-end, center, baseline)

### 6. align-content

교차 축에 여유 공간이 있을 때, 여러 줄을 정렬하는 방법을 설정합니다. (stretch, flex-start, flex-end, center, space-between, space-around)

### 7. flex

flex-grow, flex-shrink, flex-basis를 단축하여 설정할 수 있는 속성입니다.

### 8. flex-grow

요소가 사용 가능한 공간에서 얼마나 더 커질 수 있는지를 설정합니다.

### 9. flex-shrink

요소가 사용 가능한 공간에서 얼마나 더 작아질 수 있는지를 설정합니다.

### 10. flex-basis

요소의 초기 크기를 설정합니다.

<br>

## 📌 11. OOP의 특징에 대해서 설명하시오

OOP(Object-Oriented Programming)은 객체지향 프로그래밍의 약자로, 프로그램을 객체 단위로 나누어 개발하는 방식입니다.

객체는 데이터와 메서드를 하나의 단위로 묶어서 캡슐화하며, 다른 객체와의 상호작용을 통해 프로그램이 동작합니다.

OOP의 주요 특징은 다음과 같습니다.

### 1. 캡슐화 (Encapsulation)

객체의 데이터와 메서드를 외부에서 직접 접근할 수 없도록 보호하는 것입니다.

객체 내부의 구현 방식을 숨기고 외부에 제공할 인터페이스만 노출시켜, 객체 간의 상호작용을 안전하게 유지할 수 있습니다.

### 2. 상속 (Inheritance)

부모 클래스의 특성을 자식 클래스가 물려받아 확장하는 것입니다.

상속을 통해 코드의 재사용성을 높일 수 있으며, 객체의 계층 구조를 쉽게 구성할 수 있습니다.

### 3. 다형성 (Polymorphism)

동일한 인터페이스를 가지고 서로 다른 구현을 제공할 수 있는 것을 말합니다.

다형성은 코드의 가독성과 유지보수성을 높이며, 객체 간의 교환성을 높입니다.

### 4. 추상화 (Abstraction)

객체의 공통적인 특징을 추출하여 모델링하는 것입니다.

추상화를 통해 복잡한 현실 세계를 단순화시키고, 객체 모델을 만들어 코드의 가독성을 높일 수 있습니다.

<br>

객체지향 프로그래밍은 이러한 특징을 통해 코드의 재사용성, 가독성, 유지보수성 등을 높일 수 있으며, 대규모 소프트웨어 개발에 매우 적합합니다.

<br>

## 📌 12. 웹팩과 바벨은 무엇인가?

웹팩(Webpack)과 바벨(Babel)은 모두 자바스크립트 언어를 개발하는 데에 사용되는 도구입니다.

### 웹팩팩

웹팩은 애플리케이션의 모든 자원(HTML, CSS, JavaScript, 이미지 등)을 모듈로 보고 이들을 처리하여 하나의 결과물로 만들어주는 번들러(bundler)입니다.

웹팩은 모듈 번들링(module bundling)을 수행하여 여러 파일을 하나의 자바스크립트 파일로 결합하고, 코드를 압축하고 최적화하여 애플리케이션의 성능을 향상시키는 역할을 수행합니다.

### 바벨

바벨은 자바스크립트 코드를 트랜스파일(transpile)하는 도구로, ES6(ES2015) 등의 최신 자바스크립트 문법을 브라우저에서 실행 가능한 이전 버전의 자바스크립트 코드로 변환합니다.

바벨을 사용하면 모든 브라우저에서 동작하는 호환성 높은 코드를 작성할 수 있습니다.

<br>

웹팩과 바벨은 모두 자바스크립트 생태계에서 매우 중요한 역할을 합니다.

웹 개발자들은 이들 도구를 사용하여 더욱 효율적이고 안정적인 애플리케이션을 개발할 수 있습니다.

<br>

### babel과 polyfill의 차이

Babel과 Polyfill은 모두 ES6+ 문법을 이전 버전의 자바스크립트 코드로 변환하여 브라우저 호환성을 해결하기 위한 도구입니다.

Babel은 최신 자바스크립트 코드를 이전 버전의 자바스크립트 코드로 변환하는 역할을 합니다.

이렇게 변환된 코드는 브라우저에서 실행 가능합니다.

하지만, ES6+ 문법 중 일부는 브라우저에서 실행되지 않는 경우도 있습니다. 이런 경우에는 Polyfill이 필요합니다.

Polyfill은 브라우저에서 실행되지 않는 최신 자바스크립트 API를 구현하는 코드입니다.

Polyfill은 이전 버전의 브라우저에서도 최신 자바스크립트 API를 사용할 수 있도록 하기 때문에, Babel과 함께 사용되어야 합니다.

Polyfill을 사용하면 브라우저 호환성을 보다 쉽게 관리할 수 있습니다.

요약하자면, Babel은 최신 자바스크립트 코드를 이전 버전의 자바스크립트 코드로 변환하여 브라우저 호환성을 개선하는 역할을 하며,

Polyfill은 최신 자바스크립트 API를 이전 버전의 브라우저에서도 사용할 수 있도록 하는 코드입니다.

<br>

## 📌 13. JWT 방식을 설명하고, 왜 사용했는지?

JWT는 JSON Web Token의 약어로, 인증과 권한 부여를 위한 토큰 기반의 인증 방식입니다.

JWT는 다음과 같은 구성으로 이루어져 있습니다.

Header : 토큰의 유형과 알고리즘을 지정합니다
.
Payload : 토큰에 담을 정보를 지정합니다. 클라이언트 식별자, 사용자 권한, 만료 시간 등의 정보를 포함할 수 있습니다.

Signature : Header와 Payload를 인코딩하고, 서버에서 생성한 비밀키로 서명한 값입니다. 이를 통해 토큰의 무결성을 검증할 수 있습니다.

<br>

JWT는 클라이언트와 서버 간의 통신에서 사용됩니다.

클라이언트가 서버에 로그인 요청을 보내면, 서버는 해당 사용자의 정보를 확인하고, JWT를 생성하여 클라이언트에게 전달합니다.

이후 클라이언트는 JWT를 저장해두고, 다른 요청을 보낼 때마다 JWT를 함께 전송합니다. 서버는 해당 JWT를 검증하여, 해당 사용자의 인증과 권한 부여를 처리합니다.

<br>

JWT 방식은 다음과 같은 이점을 가지고 있습니다.

Stateless : 서버가 상태를 유지하지 않기 때문에, 서버의 확장성이 높아집니다.

Cross-Domain : JWT는 HTTP 헤더에 저장되기 때문에, 다른 도메인 간의 통신에서도 사용할 수 있습니다.

Security : JWT는 서명되어 있기 때문에, 데이터의 무결성을 검증할 수 있습니다.

따라서, JWT 방식은 인증과 권한 부여를 효율적으로 처리할 수 있는 방식으로, 모바일 애플리케이션, 단일 페이지 어플리케이션 등에서 널리 사용됩니다.

<br>

실제 프로젝트에서는 카카오로그인 기능을 사용하기 위하여 이용하였습니다.

<br>

## 📌 14. .call과 .apply, bind의 차이점은 무엇인가요?

JavaScript에서 함수를 호출할 때, .call(), .apply(), bind() 메서드를 사용할 수 있습니다.

이들 메서드는 모두 함수의 this 값과 인수를 제어하는 방법을 제공하지만, 그 차이점이 있습니다.

.call()과 .apply()는 함수를 즉시 호출하며, 함수 내부에서 사용될 this 값을 인수로 전달받습니다.

### call

.call() 메서드는 함수를 호출할 때, 첫 번째 인수로 사용될 this 값을 전달받고, 나머지 인수는 해당 함수의 파라미터로 전달됩니다.

<br>

### apply

.apply() 메서드도 비슷한 역할을 수행하지만, 두 번째 인수로 배열 형태로 인수를 전달합니다.

<br>

### bind

.bind() 메서드는 함수를 호출하지 않고, 함수 내부에서 사용될 this 값을 영구적으로 바인딩(bind)합니다.

이후 반환되는 함수를 호출하면, 그 this 값이 항상 영구적으로 바인딩됩니다.

<br>

## 📌 15. AJAX에 대해 자세히 설명하세요(+장단점)

AJAX(Asynchronous JavaScript and XML)란 웹 애플리케이션에서 비동기적으로 데이터를 주고받을 수 있는 기술입니다.

이 기술은 브라우저에서 JavaScript를 이용하여 서버와 데이터를 주고받기 때문에, 페이지를 새로고침하지 않고도 필요한 부분만 업데이트할 수 있어 사용성이 뛰어납니다.

### AJAX의 장점

- 비동기적으로 데이터를 주고받으므로, 페이지를 새로고침하지 않아도 필요한 부분만 업데이트할 수 있어 사용자 경험을 향상시킵니다.

- 서버에서 데이터를 받아오는 동안에도 다른 작업을 수행할 수 있습니다.

- 필요한 데이터만 받아오므로, 전체 페이지를 다시 로드하는 것보다 네트워크 사용량이 적습니다.

- 데이터 포맷으로 XML뿐만 아니라 JSON 등 다양한 형식을 사용할 수 있습니다.

### AJAX의 단점

- JavaScript를 이용하므로, 브라우저에서 JavaScript를 지원하지 않는 경우에는 사용할 수 없습니다.

- 서버에서 데이터를 받아오는 과정에서 보안상의 문제가 발생할 수 있습니다.

- 검색 엔진 최적화(SEO)에 불리할 수 있습니다. 검색 엔진은 일반적으로 JavaScript로 생성된 컨텐츠를 크롤링하지 않습니다.

<br>

AJAX는 XMLHttpRequest 객체를 사용하여 구현할 수 있습니다.

최근에는 fetch API나 axios 같은 라이브러리를 사용하여 간편하게 AJAX를 처리할 수 있습니다.

<br>

## 📌 16. use strict 이 무엇인가요? 사용시 장단점이 무엇인가요?

'use strict'는 ECMAScript 5에서 추가된 엄격 모드(strict mode)를 적용하는 방법 중 하나입니다.

이 모드를 사용하면 JavaScript 코드를 더 엄격한 규칙으로 처리하게 됩니다.

<br>

### 장점

1. 암묵적인 전역 변수 사용 방지

'use strict'를 사용하면 변수를 선언하지 않고도 변수에 값을 할당할 수 없습니다.

이는 전역 변수의 생성을 방지하고, 변수의 범위를 한정하여 예기치 않은 변수 충돌을 방지합니다.

2. 안전하지 않은 작성 방식 사용 방지

'use strict'는 안전하지 않은 작성 방식을 사용하는 것을 방지합니다.

예를 들어, 변수를 삭제하거나, 함수의 매개변수에 동일한 이름을 사용하는 것을 방지합니다.

3. 성능 향상

'use strict'를 사용하면 JavaScript 엔진이 코드를 더 빠르게 처리할 수 있습니다.

이는 불필요한 코드 검사와 오류 처리를 줄이기 때문입니다.

### 단점

1. 기존 코드와의 호환성

'use strict'를 적용하면 기존 코드와의 호환성 문제가 발생할 수 있습니다.

예를 들어, 전역 객체에 대한 참조가 변경되는 등의 문제가 있을 수 있습니다.

2. 엄격한 규칙 적용

'use strict'는 코드를 더 엄격하게 처리하기 때문에 일부 작성 방식을 사용할 수 없습니다.

예를 들어, arguments.callee()와 같은 기능을 사용할 수 없습니다.

<br>

따라서 'use strict'를 사용할지 여부는 프로젝트의 특성과 개발자의 취향에 따라 결정되어야 합니다.

일반적으로 새로운 프로젝트에서는 'use strict'를 사용하는 것이 좋습니다.

<br>

## 📌 17. Box model에 대해 설명해주세요.

Box model은 HTML 요소들의 크기와 위치를 결정하는 데 사용되는 개념입니다.

모든 HTML 요소는 content, padding, border, margin의 4개의 영역으로 나뉘어집니다.

1. Content

Content는 HTML 요소가 실제로 보여지는 부분입니다.

예를 들어, div 태그의 텍스트 콘텐츠, img 태그의 이미지 등이 content에 해당합니다.

2. Padding

Padding은 content와 border 사이의 공간입니다.

Padding은 content 주위에 공백을 둘 수 있으며, CSS에서 padding 속성을 사용하여 설정할 수 있습니다.

3. Border

Border는 요소의 테두리입니다.

Border는 content와 padding 주위에 위치하며, CSS에서 border 속성을 사용하여 스타일, 두께, 색상 등을 설정할 수 있습니다.

4. Margin

Margin은 요소의 가장 바깥쪽 영역으로, border 바깥쪽에 위치합니다.

Margin은 두 요소 간의 간격을 설정하는 데 사용됩니다. CSS에서 margin 속성을 사용하여 설정할 수 있습니다.

<br>

Box model의 장점은 디자인과 레이아웃을 쉽게 구성할 수 있다는 것입니다.

그러나 Box model은 때로 다른 요소들과의 상호작용을 제한할 수 있으며, 구성이 복잡해질수록 코드를 유지하기 어려워질 수 있습니다.

<br>

## 📌 18. Prototype이란? Prototype Chaining은?

JavaScript에서 모든 객체는 자신의 부모 역할을 하는 객체와 연결되어 있습니다.

이때 객체는 부모 객체의 프로퍼티와 메서드를 상속받아 사용할 수 있는데, 이때 사용되는 것이 프로토타입입니다.

프로토타입은 객체를 생성할 때마다 자동으로 생성되며, **proto**라는 숨겨진 프로퍼티에 부모 객체의 참조가 저장됩니다.

예를 들어, Object.create() 메서드로 객체를 생성하면 인자로 전달된 객체를 부모로 하는 자식 객체가 생성되고, 자식 객체의 `__proto__` 프로퍼티에 부모 객체의 참조가 저장됩니다.

<br>

프로토타입 체인(Prototype Chaining)은 객체의 프로퍼티나 메서드를 사용하려고 할 때 해당 객체에서 찾지 못하면 자동으로 `__proto__` 프로퍼티에 저장된 부모 객체에서 찾는 과정을 말합니다.

이러한 과정을 통해 상속 개념을 구현할 수 있습니다.

이렇게 Prototype 객체가 연결된 체인 형태로 연결되어 있으므로 Prototype Chain이라고 부릅니다.

Prototype Chaining의 장점은 상속을 통한 코드 재사용이 용이해진다는 것입니다.

그러나 Prototype 체인이 길어질수록 성능 문제가 발생할 수 있습니다.

또한, Prototype 객체의 프로퍼티나 메소드를 수정하는 경우, 해당 객체를 상속하는 모든 객체에 영향을 미치므로 주의해야 합니다.

<br>

## 📌 19. forEach와 Map의 차이점은?

forEach와 map은 자바스크립트의 배열 객체 메서드로서, 각 요소에 대한 반복적인 작업을 수행하는 데 사용됩니다.

그러나 두 메서드 간에는 중요한 차이점이 있습니다.

### forEach

forEach는 배열의 각 요소에 대해 주어진 함수를 호출하고, 반환값이 없습니다.

즉, 기존 배열을 변경하지 않습니다. 이러한 이유로 forEach는 배열의 각 요소를 반복하면서 어떤 작업을 수행하고자 할 때 유용합니다.

### map

반면, map은 배열의 각 요소에 대해 주어진 함수를 호출하여 그 결과로 새로운 배열을 반환합니다.

이렇게 반환된 새 배열은 기존 배열과 같은 길이를 가지며, 각 요소의 값은 주어진 함수에 따라 변경됩니다.

이러한 이유로 map은 배열을 변경하지 않고 새로운 배열을 생성하고자 할 때 유용합니다.

<br>

## 📌 20. 화살표 함수와 일반함수의 차이점

1. 문법적 차이점

화살표 함수는 function 키워드 대신 => 기호를 사용합니다.

매개변수가 하나일 경우 괄호를 생략할 수 있습니다.

함수 몸체가 하나의 표현식일 경우 중괄호와 return 키워드를 생략할 수 있습니다.

2. this 바인딩 차이점

일반 함수에서는 함수를 호출한 객체를 this로 바인딩합니다.

하지만 화살표 함수에서는 함수가 생성될 때 this가 상위 스코프의 this와 같이 바인딩됩니다.

따라서, 일반 함수에서는 this를 동적으로 결정하지만, 화살표 함수에서는 정적으로 결정됩니다.

3. 생성자 함수로 사용할 수 없음

화살표 함수는 생성자 함수로 사용할 수 없습니다. 따라서, 객체를 생성하거나 prototype 프로퍼티를 가질 수 없습니다.

4. arguments 객체의 차이점

화살표 함수는 arguments 객체를 가지지 않습니다. 따라서, arguments 객체를 사용해야 하는 경우에는 일반 함수를 사용해야 합니다.

5. 반환 값의 암묵적 반환 차이점

화살표 함수에서는 함수 몸체가 하나의 표현식일 경우 중괄호와 return 키워드를 생략할 수 있습니다. 이 경우, 표현식의 결과가 함수의 반환 값이 됩니다.
