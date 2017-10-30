# You Don't Know JS: Up & Going
# 1장 프로그래밍 속으로

*You Don't Know JS* (*YDKJS*) 시리즈에 오신 것을 환영합니다.

*Up & Going*은 프로그래밍의 몇 가지 기본 개념을 소개합니다. -- 물론 우리는 자바스크립트(종종 약어로 JS)를 향하여 기울여야합니다. -- 그리고 이 시리즈의 나머지 타이틀에 접근하고 이해하는 방법에 대해 설명합니다. 특히 프로그래밍 또는/혹은 자바스크립트에 익숙해진 분들에게  당신이 얻고자 하는 *up and going* 을 이 책에서 간략하게 탐색할 것입니다. 

이 책은 매우 높은 수준에서 프로그래밍의 기본 원칙을 설명하기 시작합니다. 사전 프로그래밍 경험이 거의 없거나 전혀 없이 *YDKJS*를 시작하고 자바스크립트의 렌즈를 통해 프로그래밍을 이해하는 길을 시작할 수 있도록 돕기 위해 이 책들을 찾고 있는 경우가 대부분입니다.

제 1장은 *프로그래밍에 대해* 더 배우고 실습하고 싶은 것들에 대한 간략한 개요로 접근해야합니다. 또한 이 주제들을 더 깊이 파헤치는 데 도움이 될 수 있는 환상적인 프로그래밍 소개 리소스가 많이 있습니다. 이 장 이외에 이들로부터 배울 것을 권장합니다.

일반적인 프로그래밍 기본 사항에 익숙해지면 2장은 자바스크립트 프로그래밍의 익숙함을 안내하는데 도움이 됩니다. 2장에서는 자바스크립트에 대해 소개하지만, 포괄적인 가이드는 아닙니다. 나머지 *YDKJS* 서적은 무엇을 위한 것입니까!

자바스크립트에 익숙하다면, 먼저 *YDKJS*에서 기대할 수 있는 것을 간단히 엿볼 수 있는 3장을 확인한 다음, 바로 뛰어 들어보십시오!

## 코드

기초부터 시작해봅시다.

흔히 *소스 코드* 또는 *코드*라고 하는 프로그램은 수행 할 작업을 컴퓨터에 알려주는 특수 지침 세트 입니다. 일반적으로 코드는 텍스트 파일로 저장됩니다. 자바스크립트를 사용하면 브라우저 개발자 콘솔에 직접 코드를 입력 할 수도 있습니다. 곧 다룰 내용을 살펴 보겠습니다.

유효한 형식 및 명령어의 조합에 대한 규칙을 *컴퓨터 언어*라고 하며 *구문 분석*이라고도 하며 영어와 거의 같은 방식으로 철자를 쓰는 방법과 단어와 구두점을 사용하여 유효한 문장을 만드는 방법을 알려줍니다.

### 명령문

컴퓨터 언어에서 특정 작업을 수행하는 단어, 숫자 및 운영자 그룹이 *명령문* 입니다. 자바스크립트에서는 명령문이 다음과 같이 보일 수 있습니다:

```js
a = b * 2;
```

문자 `a`와 `b`는 *변수* (변수 참조)이며, 간단한 상자처럼 물건을 저장할 수 있습니다. 프로그램에서 변수는 프로그램에서 사용할 값(예: `42`)을 포함합니다. 값 그 자체에 대한 상징적인 placeholder 라고 생각하십시오. 

대조적으로, `2`는 변수 자체에 저장되지 않고 혼자 있기 때문에 *리터럴 값*이라고 하는 값 자체입니다.

`=` 과 `*` 문자는 *연산자* ("연산자" 참조)입니다. 할당 및 수학적 곱셈과 같은 값 및 변수를 사용하여 작업을 수행합니다.

자바스크립트의 대부분의 문장의 끝은 세미콜론(`;`)으로 끝납니다.

`a = b * 2;` 대략 컴퓨터에 변수 `b`에 저장된 현재 값을 얻고 그 값에 `2`를 곱한 다음 결과를 다시 다른 변수 `a`로 저장합니다. 

프로그램은 단지 프로그램 목적을 수행하는 데 필요한 모든 단계를 설명하는 많은 명령문의 모음입니다.

### 표현식

명령문은 하나 이상의 *표현식*으로 구성됩니다. 표현식은 변수 또는 값에 대한 참조이거나 연산자와 결합 된 변수 및 값의 집합입니다.

예:

```js
a = b * 2;
```

이 명령문에는 4개의 표현식이 있습니다:

* `2` 는 *리터럴 값 표현식*입니다.
* `b` 는 현재 값을 검색하는 *변수 표현식*입니다.
* `b * 2` 는 곱셈을 하는 것을 의미하는 *산술 표현식*입니다.
* `a = b * 2` 는 *대입 표현식*으로, `b * 2` 표현식의 결과를 변수 `a`에 대입하는 것을 의미합니다.  (할당에 대해서는 나중에 자세히 설명 함)

단독으로 사용되는 일반 표현식은 다음과 같이 *표현식 구문*이라고 합니다.

```js
b * 2;
```
이 표현 문은 일반적으로 프로그램 실행에 아무런 영향을 미치지 않기 때문에 매우 일반적이거나 유용하지 않습니다. `b`의 값을 검색하고 `2`를 곱한 다음 아무것도 하지 않습니다. 그 결과, 

보다 일반적인 표현식 문은 전체 표현식이 함수 호출 표현식이기 때문에 *호출 표현문*("함수" 참조)입니다.

```js
alert( a );
```

### 프로그램 실행

이러한 프로그래밍 구문 컬렉션은 컴퓨터에서 무엇을 해야한다고 말합니까? 프로그램은 *실행되어야* 하며, 또한 *프로그램 실행*이라고도 합니다.

`a = b * 2`와 같은 구문은 개발자가 읽고 쓰는 데 도움이 되지만 실제로 컴퓨터가 직접 이해할 수 있는 형식은 아닙니다. 따라서 컴퓨터의 특별한 유틸리티(*인터프리터* 또는 *컴파일러*)는 작성한 코드를 컴퓨터가 이해할 수 있는 명령으로 변환하는데 사용됩니다.

일부 컴퓨터 언어의 경우 이 명령 변환은 대개 프로그램이 실행될 때마다 한 줄씩 위에서부터 차례대로 수행되며 일반적으로 코드 *해석*이라고 합니다.

다른 언어의 경우 변역은 코드 *컴파일*이라고 미리 수행되며, 그래서 프로그램이 나중에 *실행*될 때 실행 중인 것은 실제로 이미 컴파일 된 컴퓨터의 명령어입니다. 

일반적으로 자바스크립트 소스코드는 실행될 때마다 처리되므로 자바스크립트가 *해석된다*고 주장합니다. 그러나 그것은 정확하지 않습니다. 자바스크립트 엔진은 실제로 프로그램을 즉시 *컴파일* 한 다음 컴파일 된 코드를 즉시 실행합니다.

**참고:** 자바스크립트 컴파일에 대한 자세한 내용은 이 시리즈의 *Scope & Closures* 처음 두 장을 참조하십시오.

## 직접 해보기

이 장에서는 모든 프로그래밍 개념을 간단한 코드 스니펫으로 소개 할 것이며, 모두 자바스크립트로 작성됩니다.(분명히!)

충분히 강조할 수 는 없지만, 이 장을 살펴 보면서 몇 번에 걸쳐 시간을 할애해야 할 수도 있습니다. 코드를 직접 입력하여 이러한 개념을 연습해야 합니다. 가장 쉬운 방법은 가장 최신 버전의 브라우저(Firefox, Chrome, IE 등)에서 개발자 도구 콘솔을 여는 것입니다.

**팁** 일반적으로 키보드 단축키 또는 메뉴 항목을 사용하여 개발자 콘솔을 시작할 수 있습니다.
자주 사용하는 브라우저에서 콘솔을 시작하고 사용하는 방법에 대한 자세한 내용은 "개발자 도구 콘솔 완전정복"(http://blog.teamtreehouse.com/mastering-developer-tools-console)을 참조하십시오. 한 번에 여러 행을 콘솔에 입력하려면 `<shift> + <enter>`를 사용하여 다음 행으로 이동하십시오. `<enter>`만 실행하면 콘솔은 방금 입력한 모든 것을 실행합니다.

콘솔에서 코드를 실행하는 프로세스에 익숙해지십시오. 먼저 브라우저에서 빈 탭을 열어 보시기 바랍니다. 주소 표시 줄에 `about:blank`를 입력하면 됩니다. 방금 언급한 바와 같이 개발자 콘솔이 열려 있는지 확인하십시오.

이제 코드를 입력하고 실행방법을 확인하십시오:

```js
a = 21;

b = a * 2;

console.log( b );
```
앞의 코드를 Chrome의 콘솔에 입력하면 다음과 같은 결과가 나타납니다.

<img src="fig1.png" width="500">

어서 해보세요. 프로그래밍을 배우는 가장 좋은 방법은 코딩을 시작하는 것입니다!

### 출력

이전 코드에서 `console.log(..)`를 사용했습니다. 간단히 말하면, 그 코드 라인이 무엇을 의미하는지 살펴 보겠습니다.

짐작할 수 있겠지만 개발자 콘솔에서 텍스트(사용자에게 *출력*)를 인쇄하는 방법입니다. 그 구문에는 우리가 설명해야 할 두가지 특징이 있습니다.

먼저, `log( b )` 부분을 함수 호출이라고 합니다. ("함수" 참조) 우리는 `b` 변수를 그 함수에 건네주고, b의 값을 받아서 콘솔에 출력 할 것을 요구합니다.

두번째로, `콘솔` 파트는 `log(..)`함수가 있는 객체 참조입니다. 우리는 객체와 그 속성을 2장에서 자세히 다룹니다.

출력을 생성하는 또 다른 방법은 `alert(..)`문을 실행 하는 것입니다.
예:

```js
alert( b );
```
이를 실행하면 출력을 콘솔에 출력하는 대신 `b` 변수의 내용이 있는 "OK" 상자가 나타납니다. 그러나 `console.log(..)`를 사용하면 브라우저 인터페이스를 방해하지 않고 즉지 많은 값을 출력 할 수 있기 때문에 일반적으로 `alert(..)`을 사용하는 것보다 콘솔에서 프로그램 코딩 및 실행에 대해 배우게 됩니다.

이 책에서는 `console.log(..)`를 사용하여 출력합니다.

### 입력

출력물에 대해 논의하는 동안 *입력*(예: 사용자로부터 정보 수신)에 대해 궁금할 수 있습니다.

가장 일반적인 방법은 HTML 페이지가 입력할 수 있는 사용자에게 텍스트 상자와 같은 양식 요소를 표시한 다음 JS를 사용하여 해당 값을 프로그램의 변수로 읽는 것입니다.

그러나 이 책 전체에서 수행 할 작업과 같은 간단한 학습 및 데모용 입력을 얻는 더 쉬운 방법이 있습니다. `prompt(..)` 내장함수를 사용하십시오.

```js
age = prompt( "Please tell me your age:" );

console.log( age );
```
짐작할 수 있듯이, `prompt(..)`에 전달하는 메시지 - 이 경우, "나이를 적어주세요: "가 팝업에 출력됩니다.

이것은 다음과 비슷합니다.

<img src="fig2.png" width="500">

"OK"를 클릭하여 입력 텍스트를 제출하면 입력한 값이 `age`변수에 저장되고 `console.log(..)`와 함께 *출력*된다는 것을 알 수 있습니다:

<img src="fig3.png" width="500">

기본적인 프로그래밍 개념을 배우는 동안 간단하게 하기 위해 이 책의 예제는 입력 할 필요가 없습니다. 그러나 이제 `prompt(..)`를 사용해 보았습니다. 자신에게 도전하고 싶다면 예제를 탐색할 때 입력을 시도해도 됩니다.

## 연산자

연산자는 변수와 값에 대한 작업을 수행하는 방법입니다. 이미 두 개의 연산자 `*`, `=`를 보았습니다. 

`*` 연산자는 수학적 곱셈을 수행합니다. 충분히 간단합니다. 그렇죠?
The `*` operator performs mathematic multiplication. Simple enough, right?

`=` 동등 연산자는 *할당*에 사용됩니다. -- 먼저 `=`의 *오른쪽* (소스 값)에 있는 값을 계산 한 다음 *왼쪽*(목표 변수)에 넣습니다.

**경고:** 이것은 지정을 지정하는 이상한 역순처럼 보일 수 있습니다. `a = 42` 대신에 일부는 순서를 뒤집어서 소스 값이 왼쪽에 있고 목표 변수가 오른쪽에 있는  `42 -> a`(유효하지 않은 자바스크립트!)와 같은 것을 선호 할 수 있습니다. 불행히도 `a = 42` 주문형 및 유사 변형은 현대 프로그래밍 언어에 널리 보급되어 있습니다. 부자연스럽다고 느낄 경우 마음에 그 주문을 연습하면서 시간을 들여 익숙해지십시오.

고려사항:

```js
a = 2;
b = a + 1;
```

여기서는 변수에 `2` 값을 할당합니다. 그런 다음 변수 (여전히 `2`)의 값을 가져 와서 결과 값 `1`을 `3`으로 만든 다음 그 값을 변수 `b`에 저장합니다.

기술적으로 연산자는 아니지만 모든 프로그램에서 키워드 `var`가 필요합니다. 변수를 *선언*(일명 *생성*)하는 주요 방법입니다. ("변수"참조) 

변수를 사용하기 전에 항상 변수를 이름으로 선언해야합니다. 그러나 각 *범위*에 대해 한 번만 변수를 선언하면 됩니다. ("스코프" 참조) 필요할 때마다 여러 번 사용할 수 있습니다. 

예:

```js
var a = 20;

a = a + 1;
a = a * 2;

console.log( a );	// 42
```
다음은 자바스크립트에서 가장 일반적인 연산자 중 일부입니다:

* 할당: `a = 2`의 경우에서와 같이 `=`.
* 사칙연산: `a * 3`의 경우에서와 같이`+` (더하기), `-` (빼기), `*` (곱하기), `/` (나누기).
* 복합 할당: `a++` (`a = a + 1`와 동일)의 경우에서와 같이 `+=`, `-=`, `*=`, `/=` 수학 연산과 대입 연산자를 결합하는 복합 연산자입니다.
* 객체 속성 액세스: `console.log()`의 경우에서와 같이 `.`

  객체는 속성이라는 특정 명명된 위치에세서 다른 값을 보유하는 값입니다. `obj.a`는 `a`라는 속성을 가진 `obj`라는 객체 값을 의미합니다.

  객체는 속성이라는 특정 명명된 위치에서 다른 값을 보유하는 값입니다. `obj.a`는 `a`라는 속성을 가진 `obj`라는 객체 값을 의미합니다. 속성은 `obj["a"]`로 엑세스 할 수도 있습니다. 2장을 참조하십시오.

* 동등: `a == b` 의 경우에서와 같이 `==` (느슨한 equals), `===` (엄격한 equals), `!=` (느슨한 not-equals), `!==` (엄격한 not-equals)

  "값과 유형", 2장을 참조하십시오.

* 비교: `a <= b` 의 경우에서와 같이 `<` (보다 작다), `>` (보다 크다), `<=` (작거나 같다), `>=` (크거나 같다)

   "값과 유형", 2장을 참조하십시오.

* 논리:  `&&` (and), `||` (또는), `a || b`는 `a` *또는* `b`를 선택합니다. 

  이 연산자는 `a` *또는* `b`가 참인 것과 같이 복합 조건부 ("조건부" 참조)를 표현하는 데 사용됩니다.

**참고:** 여기에 언급되지 않은 연산자에 대한 자세한 내용과 적용 범위는 Mozilla Developer Network (MDN)의 "표현식 및 연산자"를 참조하십시오. (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Expressions_and_Operators).

## 값과 유형

전화 상점 직원에게 전화 비용이 얼마인지 묻는다면 그들은 "99, 99.99"라고 말합니다. 전화 번호는 실제 숫자로 표시되며, 그것을 사기 위해 (세금을 더 지불해야합니다.) 이 전화기 중 두 대를 사고 싶다면 기본 가격으로 199.98 달러를 얻으려면이 값을 두 배로 늘리는 정신적 인 수학을 쉽게 할 수 있습니다.

같은 직원이 다른 비슷한 전화를 선택하면, 그러나 그것은 "무료"(아마도 액면 그대로 받아들이지 말라고 손짓.)라고 말하면서, 그들은 당신에게 숫자를주지 않고, 당신의 기대 비용 ($ 0.00)의 또 다른 표현 - 단어 "무료"를 말합니다.

나중에 전화에 충전기가 포함되어 있는지 물어 보면 그 대답은 "예"또는 "아니오"중 하나 일 수 있습니다.

매우 유사한 방식으로, 프로그램에서 가치를 표현할 때, 당신은 그 값으로 무엇을 할 계획인지에 따라 다른 표현을 선택하게됩니다.

이러한 값에 대한 다양한 표현을 프로그래밍 용어로 *유형*이라고합니다. 자바스크립트에는 *원시* 변수라는 기본 값이 있습니다:

* 계산을 해야 할 때 `숫자`가 필요합니다.
* 화면에 값을 인쇄해야 할 때 `문자열` (하나 이상의 문자, 단어, 문장)이 필요합니다.
* 프로그램에서 결정을 내려야 할 때는 `부울` (`true` 또는 `false`)이 필요합니다.

소스 코드에 직접 포함 된 값을 *리터럴*이라고합니다. `문자열` 리터럴은 큰 따옴표 `"..."`또는 작은 따옴표 ( '...')로 둘러싸여 있습니다. 유일한 차이점은 문체 선호입니다. `숫자` 및 `부울` 리터럴은 그대로 표현됩니다 (예 : `42`, `true` 등).

고려사항:

```js
"I am a string";
'I am also a string';

42;

true;
false;
```

`문자열` / `숫자` / `부울` 값 유형 이외에도 프로그래밍 언어가 *배열*, *객체*, *함수* 등을 제공하는 것이 일반적입니다. 이 장과 다음 장에서 가치와 유형에 대해 더 많이 다룰 것입니다.

### 유형 간 변환

`숫자`가 있지만 화면에 인쇄해야하는 경우 값을 `문자열`로 변환 해야하며 자바스크립트에서는 이 변환을 "강제 변환"이라고합니다. 마찬가지로 누군가가 전자 상거래 페이지의 양식에 일련의 숫자를 입력하면 해당 `문자열`이지만, 그 값을 사용하여 수학 연산을 수행해야하는 경우 `숫자`로 *변환*해야합니다.

자바스크립트는 *유형* 간에 강제로 강제 변환하는 여러 가지 기능을 제공합니다. 

예:

```js
var a = "42";
var b = Number( a );

console.log( a );	// "42"
console.log( b );	// 42
```

그림과 같이 `Number (..)` (내장 함수)를 사용하면 다른 형식에서 `숫자` 형식으로 *명시적으로* 변환 할 수 있습니다. 그것은 아주 간단해야합니다.

그러나 논쟁의 여지가 있는 주제는 *암시적* 강제 변환이 필요한 동일한 유형이 아닌 두 값을 비교하려고 할 때 일어나는 일입니다.

문자열 `"99.99"`와 숫자 `99.99`를 비교할 때 대부분의 사람들은 그들이 동등하다는 것에 동의 할 것입니다. 하지만 정확히 똑같지는 않습니까? 두 가지 다른 표현, 즉 두 가지 *유형*에서 동일한 값입니다. 당신은 그들이 "느슨하게 동등하다"고 말할 수 있겠습니까?


이러한 일반적인 상황에서 당신을 도울 수 있도록 자바스크립트는 때로는 값을 입력하여 일치하는 유형에 *암시적으로* 강제합니다.

따라서 `==` 느슨한 equals 연산자를 사용하여 비교 `"99.99"== 99.99`를 만들면 자바스크립트는 왼쪽 `"99.99"`를 `숫자 99.99`로 변환합니다. 비교는 `99.99 == 99.99`가되는데, 이는 `참`입니다.

당신이 그 행동을 지배하는 규칙을 배우는 데 시간을 할애하지 않았다면 암시적인 강제 변환은 혼란을 야기 할 수 있습니다. 대부분의 JS 개발자는 절대 사용하지 않으므로 암시적인 강제가 혼란스럽고 예기치 않은 버그가 있는 프로그램에 피해를 입힙니다. 따라서 피해야합니다. 때로는 언어 디자인의 결함으로 불리기도 합니다.

그러나 암시적인 강제 변환은 *배울 수 있는* 메커니즘이며, 또한 자바스크립트 프로그래밍을 중요하게 생각하는 사람이 *배워야합니다.* 규칙을 배운 후에 혼란 스러울뿐만 아니라 실제로 프로그램을 더 잘 만들 수 있습니다! 그 노력은 그만한 가치가 있습니다.

**참고 :** 강제 변환에 대한 자세한 내용은 이 책의 2 장과 이 시리즈의 *유형 및 문법* 4 장을 참조하십시오.

## 코드 주석

전화 매장 직원은 새로 출시 된 휴대 전화의 기능이나 회사에서 제공하는 새로운 계획에 대한 메모를 적어 둘 수 있습니다. 그것은 고객이 읽을 수있는 것이 아닙니다. 그럼에도 불구하고 이 메모는 직원이 고객에게 무엇을 말해야 하는지를 문서화함으로써 직원이 자신의 업무를 더 잘 수행 할 수 있도록 도와줍니다.

코드 작성에 대해 배울 수있는 가장 중요한 교훈 중 하나는 컴퓨터에만 해당되는 것이 아니라는 것입니다. 코드는 컴파일러와 마찬가지로 개발자에게 더 많은 것은 아니지만 모든 비트만큼이나 중요합니다.

당신의 컴퓨터는 *컴파일*에서 오는 기계 코드, 일련의 이진 0과 1만을 염려합니다. 당신이 쓸 수있는 거의 무한한 숫자의 프로그램이 있습니다. 같은 프로그램을 만들어 낼 수 있습니다. 프로그램 문제를 작성하는 방법에 대한 선택은 당신 뿐 아니라 다른 팀원에게도 중요합니다.

올바르게 작동하는 프로그램을 작성하는 것뿐만 아니라 검사 할 때 의미가있는 프로그램을 작성해야합니다. 변수에 대한 올바른 이름 ("변수"참조)과 함수 ("함수"참조)를 선택하면 많은 노력을 기울일 수 있습니다.

그러나 또 다른 중요한 부분은 코드 주석입니다. 이것들은 순수하게 인간에게 설명하기 위해 삽입되는 텍스트입니다. 인터프리터 / 컴파일러는 항상 이러한 주석을 무시합니다.

잘 설명 된 코드를 작성하는 것에 대한 많은 의견이 있습니다. 우리는 절대적 보편 규칙을 실제로 정의 할 수 없습니다. 그러나 일부 관찰 및 가이드 라인은 매우 유용합니다:

* 주석이 없는 코드는 차선책입니다.
* 주석이 너무 많으면 (예를 들어, 한 줄에 하나씩) 아마도 잘못 작성된 코드의 표시 일 것입니다.
* 주석은 *무엇*이 아니라 *왜*를 설명해야합니다. 특히 혼란스럽다면 그것들은 선택적으로 *어떻게*를 설명할 수 있습니다.

자바스크립트에서는 한 줄 주석과 여러 줄 주석 두 가지 주석 유형이 있습니다.

고려사항:

```js
// This is a single-line comment

/* But this is
       a multiline
             comment.
                      */
```

`//` 한 줄짜리 주석은 단일 문장 바로 위에 주석을 달거나 줄의 끝 부분에 주석을 넣을 때 적합합니다. `//` 뒤에 오는 줄의 모든 내용은 줄 끝까지의 주석으로 처리됩니다 (따라서 컴파일러에서 무시됩니다). 한 줄짜리 주석 안에 무엇이 나타날 수 있는지는 아무런 제한이 없습니다.

고려사항:

```js
var a = 42;		// 42 is the meaning of life
```

`/ * .. * /` multiline 주석은 주석에 여러 줄의 설명을 할 수 있다면 적절합니다.

다음은 여러 줄 주석의 일반적인 사용법입니다:

```js
/* The following value is used because
   it has been shown that it answers
   every question in the universe. */
var a = 42;
```

또한 줄의 중간에 있더라도 줄의 아무 곳에 나 나타날 수 있습니다. `* /`는 끝나기 때문입니다. 
예:

```js
var a = /* arbitrary value */ 42;

console.log( a );	// 42
```
여러 줄 주석문 안에 나타날 수없는 유일한 것은 주석을 끝내기 위해 해석되기 때문에 `* /`입니다.

코드를 주석하는 습관으로 시작하여 프로그래밍 학습을 시작하고 싶을 것입니다. 이 장이 나머지 부분에서는 주석을 사용하여 사물을 설명하는 것을 볼 수 있습니다. 나를 믿으십시오, 당신의 코드를 읽는 모든 사람들은 당신에게 감사할 것입니다.

## 변수

대부분의 유용한 프로그램은 프로그램 진행 과정에서 변경될 때 값을 추적해야 하며 프로그램의 의도 된 작업이 요구하는 다른 작업을 수행해야 합니다.

프로그램에서 그 일을 하는 가장 쉬운 방법은 *변수*라는 심볼 컨테이너에 값을 할당하는 것입니다. 이 컨테이너의 값은 필요에 따라 시간이 지남에 따라 *달라질* 수 있습니다.

일부 프로그래밍 언어에서는 `숫자` 또는 `문자열`과 같은 특정 유형의 값을 보유할 변수 (컨테이너)를 선언합니다. *정적 유형 지정* 또는 *유형 강제*는 일반적으로 의도하지 않은 값 변환을 방지하여 프로그램 정확성에 대한 이점으로 인용됩니다.

다른 언어는 변수 대신 값의 유형을 강조합니다. *동적 유형 지정*이라고도 하는 *약한 유형 지정*을 사용하면 변수가 언제든지 모든 유형의 값을 보유할 수 있습니다. 그것은 일반적으로 하나의 변수가 값 유형을 막론하고 값을 나타낼 수 있게 하여 프로그램 유연성을 위한 이점으로 인용되며 프로그램의 논리 흐름에서 주어진 순간에 걸릴 수 있습니다.

자바스크립트는 후자의 방식인 *동적 유형 지정* 을 사용합니다. 즉, 변수는 *유형* 적용 없이 모든 *유형*의 값을 보유할 수 있습니다.

앞서 언급했듯이 우리는 `var` 문을 사용하여 변수를 선언합니다. 선언에 다른 *유형* 정보가 없다는 것을 알 수 있습니다. 이 간단한 프로그램을 생각해보십시오:

```js
var amount = 99.99;

amount = amount * 2;

console.log( amount );		// 199.98

// convert `amount` to a string, and
// add "$" on the beginning
amount = "$" + String( amount );

console.log( amount );		// "$199.98"
```
`amount` 변수는 `99.99`를 갖고 있는 채로 시작하여 `amount * 2`, `199.98`의 `숫자` 결과를 갖게 됩니다.

첫 번째 `console.log(..)` 명령은 *암시적으로* `숫자` 값을 `문자열`로 강제 변환하여 출력하여 인쇄합니다.

그런 다음 명령문 `amount = "$" + String(amount)`는 *명시적으로* `199.98` 값을 `문자열`로 강제 변환하고 시작 부분에 `"$"`문자를 추가합니다. 이 시점에서 `amount`는 이제 문자열 값 `"$199.98"`을 보유하므로 두 번째 `console.log(..)`문은 이를 인쇄하기 위해 강제 변환 할 필요가 없습니다.

자바스크립트 개발자는 `99.99`, `199.98`, `"$199.98"`값 각각에 대해 `amount`변수를 사용할 수 있는 유연성에 주목합니다. 정적 유형 열광자는 amount 유형이 다른 유형이기 때문에 금액의 최종 `"$ 199.98"` 표현을 유지하기 위해 `amountStr`과 같은 별도의 변수를 선호합니다.

어느 쪽이든, `amount`는 프로그램의 과정에서 변화하는 실행 가치를 지니고 있으며 변수의 주된 목적을 보여줍니다. 그것은 프로그램 *상태*를 관리합니다.

즉, *상태*는 프로그램이 실행될 떄 값의 변경을 추적합니다.

변수의 또 다른 일반적인 용도는 값 설정을 중앙 집중화하는 것입니다. 변수를 값으로 선언하고 해당 값이 프로그램 전체에서 *변경되지 않도록* 하는 경우 더 일반적으로 *상수*라고 합니다.

이러한 *상수*는 종종 프로그램 상단에 선언되므로 필요한 경우 한 자리에서 값을 변경하는 것이 편리합니다. 일반적으로 상수로 사용되는 자바스크립트 변수는 대문자로 되어 있으며 여러 단어 사이에 밑줄이 `_` 있습니다.

다음은 어리석은 예입니다:

```js
var TAX_RATE = 0.08;	// 8% sales tax

var amount = 99.99;

amount = amount * 2;

amount = amount + (amount * TAX_RATE);

console.log( amount );				// 215.9784
console.log( amount.toFixed( 2 ) );	// "215.98"
```

**참고:** `console.log(..)`가 콘솔 값에서 객체 속성으로 엑세스 되는 함수 `log(..)` 와 비슷한 방식으로 `toFixed(..)` 는 숫자 값에서 액세스할 수 있는 함수입니다. 자바스크립트 `숫자`는 자동으로 달러 형식으로 지정되지 않습니다. 엔진은 의도가 무엇인지 알지 못하며 통화 유형이 없습니다. `toFixed(..)`는 소수점 이하 자리수를 지정하고 필요에 따라 `문자열`을 생성합니다.

`TAX_RATE` 변수는 관행에 의해서만 *일정합니다.* 이 프로그램에는 특별한 변화가 일어나지 않습니다. 그러나 도시가 판매 세율을 9 %로 인상하면, `TAX_RATE` 할당 값을 한 곳에서 `0.09`로 설정하여 프로그램 전체에서 `0.08`의 값을 여러 번 발견하고 모두 업데이트하는 대신 프로그램을 쉽게 업데이트 할 수 있습니다.

이 글을 쓰고있는 시점의 최신 버전의 자바스크립트 (일반적으로 "ES6")에는 `var` 대신 `const`를 사용하여 *상수*를 선언하는 새로운 방법이 포함되어 있습니다:

```js
// as of ES6:
const TAX_RATE = 0.08;

var amount = 99.99;

// ..
```

상수는 변경되지 않은 값을 가진 변수와 마찬가지로 유용합니다. 단, 상수는 초기 설정 이후 실수로 다른 값을 변경하는 것을 방지합니다. 첫 번째 선언 후에 다른 값을 `TAX_RATE`에 할당하려고하면 프로그램이 변경을 거부합니다. (strict mode에서는 오류와 함께 실패합니다 - 2 장의 "Strict Mode"참조)

그런데 실수에 대한 그런 종류의 "보호"는 정적 타이핑 유형 강제와 비슷하므로 다른 언어의 정적 유형이 왜 매력적인지 알 수 있습니다!

**참고:** 변수에서 다른 값을 프로그램에서 사용하는 방법에 대한 자세한 내용은 이 시리즈의 *유형 및 문법* 제목을 참조하십시오.

## 블록

전화 상점 직원은 새 전화를 구입할 때 일련의 단계를 수행하여 결제를 완료해야 합니다.

마찬가지로, 코드에서 종종 일련의 명령문을 그룹으로 묶어야합니다. 우리는 종종 블록이라고 부릅니다. 자바스크립트에서 *블록*은 중괄호 쌍 `{ .. }` 안에 하나 이상의 명령문을 래핑하여 정의됩니다. 

고려사항:

```js
var amount = 99.99;

// a general block
{
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

이러한 종류의 독립실행형 `{ .. }` 일반 블록은 유효하지만 JS 프로그램에서 일반적으로 볼 수 있는 것은 아닙니다. 일반적으로 블록은 `if` 문("조건부" 참조) 또는 루프("루프" 참조)와 같은 다른 제어문에 첨부됩니다. 

예: 

```js
var amount = 99.99;

// is amount big enough?
if (amount > 10) {			// <-- block attached to `if`
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

다음 절의 `if` 문을 설명하지만, 두 개의 명령문이있는 `{..}` 블록은 `if (amount> 10)`에 첨부됩니다. 조건부가 통과하는 경우에만 블록 내부의 명령문이 처리됩니다.

**참고:** `console.log(amount);`와 같은 대부분의 다른 명령문과는 달리, 블록 명령문은 이를 종결하기 위해 세미콜론(`;`)이 필요하지 않습니다.

## 조건문

"9.99 달러에 구입하신 화면 보호 장치를 추가하고 싶습니까?" 도움이 되는 전화 상점 직원이 귀하에게 결정을 요청했습니다. 그리고 그 질문에 대답하기 위해 지갑이나 은행 계좌의 현재 *상태*를 먼저 확인해야 할 수도 있습니다. 그러나 분명히 이것은 단순한 "예 또는 아니오"질문 일뿐입니다.

프로그램에서 *조건문* (일명 결정)을 표현할 수있는 몇 가지 방법이 있습니다.

가장 일반적인 것은 `if` 문입니다. 근본적으로 말하면, "이 조건이 사실*이라면*, 다음을 수행하십시오 ...". 
예 :

```js
var bank_balance = 302.13;
var amount = 99.99;

if (amount < bank_balance) {
	console.log( "I want to buy this phone!" );
}
```

`if` 문은 `true` 또는 `false`로 처리 할 수있는 괄호 `()` 사이의 표현식을 필요로합니다. 이 프로그램에서는 표현 `amount < bank_balance`를 제공했습니다. 실제로 `bank_balance` 변수의 양에 따라 `true` 또는 `false`로 평가됩니다.

`else` 절로 불리는 조건이 참이 아니면 대안을 제공 할 수도 있습니다. 

고려사항:

```js
const ACCESSORY_PRICE = 9.99;

var bank_balance = 302.13;
var amount = 99.99;

amount = amount * 2;

// can we afford the extra purchase?
if ( amount < bank_balance ) {
	console.log( "I'll take the accessory!" );
	amount = amount + ACCESSORY_PRICE;
}
// otherwise:
else {
	console.log( "No, thanks." );
}
```

여기 `amount < bank_balance`가 `true` 인 경우, `"내가 액세서리를 가져갈 것입니다!"`라고 인쇄 할 것입니다. 우리 `amount` 변수에 `9.99`를 추가하십시오. 그렇지 않으면, `else` 절은 우리가 정중하게 `"아니, 고마워."`라고 대답 할 것이라고 말합니다. 그리고 `amount`를 변경하지 않고 끝날 것입니다.

이전에 "값 및 유형"에서 논의했듯이 이미 예상 유형이 아닌 값은 종종 해당 유형으로 강제 변환됩니다. `if` 문은 `부울`을 기대하지만, 이미 `부울`이 아닌 무언가를 전달하면 강제 변환이 발생합니다.

자바스크립트는 `부울`로 강요 될 때 `false`가 될 때 `0`및 `""`와 같은 값을 포함하기 때문에 "거짓"으로 간주되는 특정 값의 목록을 정의합니다. "거짓" 목록에 없는 다른 값은 자동으로 "진실"입니다. `부울`로 강요 될 때 그것은 `true` 입니다. 진리 값에는 `99.99`와 `"무료"`같은 것이 포함됩니다. 자세한 내용은 2 장의 "참과 거짓"을 참조하십시오.

*조건문*은 `if` 이외의 다른 형식으로 존재합니다. 예를 들면, `switch` 문은 일련의 `if..else` 문에 대한 줄임말로 사용할 수 있습니다 (2 장 참조). 루프 ( "루프"참조)는 *조건문*을 사용하여 루프를 계속 진행할지 또는 중지할지 결정합니다.

**참고:** *조건문*의 테스트 표현식에서 암시적으로 발생할 수있는 강제 변환에 대한 자세한 내용은 이 시리즈의 *유형 및 문법* 4 장을 참조하십시오.

## 루프

바쁜 시간에는 전화 상점 직원과 통화해야하는 고객을위한 대기자 명단이 있습니다. 그 목록에 여전히 사람들이 있지만, 그녀는 다음 고객에게 계속해서 봉사해야합니다.

특정 조건이 실패 할 때까지 일련의 동작을 반복합니다. 즉, 조건이 유지되는 동안 만 반복하는 것은 프로그래밍 루프의 작업입니다. 루프는 다른 형태를 취할 수 있지만 모두 기본 동작을 만족시킵니다.

루프는 테스트 조건과 블록 (일반적으로 `{..}`과 같이)을 포함합니다. 루프 블록이 실행될 때마다 이를 *반복*이라고합니다.

예시는 `while` 루프 및 `do..while` 루프 양식은 조건이 더 이상 `true`가 아닌 것으로 판단될 때까지 명령문 블록을 반복하는 개념을 보여줍니다:

```js
while (numOfCustomers > 0) {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
}

// versus:

do {
	console.log( "How may I help you?" );

	// help the customer...

	numOfCustomers = numOfCustomers - 1;
} while (numOfCustomers > 0);
```

이러한 루프 간의 유일한 차이점은 조건부가 첫 번째 반복 전에 (`while`) 또는 첫 번째 반복 후에 (`do..while`) 테스트되는지 여부입니다.

두 가지 형태 중 하나라도 조건부 테스트가 `false`면 다음 반복이 실행되지 않습니다. 즉, 조건이 처음 `false`이면 `while` 루프는 실행되지 않지만 `do..while` 루프는 처음 실행됩니다.

때로는 `0`에서 `9` (10 개의 숫자)와 같은 특정 숫자 세트를 계산하는 의도 된 목적을 위해 루핑합니다. 값이 0 인 `i`같은 루프 반복 변수를 설정하고 각 반복마다 `1` 씩 증가시켜 이를 수행 할 수 있습니다.

**경고:** 다양한 역사적 이유로 프로그래밍 언어는 거의 항상 0부터 시작합니다. `1`대신에 `0`으로 시작하는 것을 의미합니다. 그 사고 방식에 익숙하지 않다면 처음에는 매우 혼란스러울 수 있습니다. 0으로 시작하는 계산을 연습할 시간을 가지십시오.

루프 내에서 묵시적인 `if`문이 있는 것처럼 조건은 각 반복에서 테스트됩니다.

자바스크립트의 `break`문을 사용하여 루프를 멈출 수 있습니다. 또한 `break` 매커니즘없이 영원히 돌아갈 수 있는 루프를 만드는 것은 너무나 쉽습니다.

설명해 보겠습니다:

```js
var i = 0;

// a `while..true` loop would run forever, right?
while (true) {
	// stop the loop?
	if ((i <= 9) === false) {
		break;
	}

	console.log( i );
	i = i + 1;
}
// 0 1 2 3 4 5 6 7 8 9
```

**경고:** 이것은 반드시 루프에 사용하려는 실용적인 형식은 아닙니다. 여기서는 설명의 목적으로 만 제시되었습니다.

 `while` 하는 동안 (또는 `do..while`) 수동으로 작업을 수행 할 수 있지만 그 목적을 위해 `for` 루프라고하는 또 다른 구문 형식이 있습니다:

```js
for (var i = 0; i <= 9; i = i + 1) {
	console.log( i );
}
// 0 1 2 3 4 5 6 7 8 9
```
보다시피, 두 경우 모두 조건식 루프 형태의 처음 10회 반복 (`0`부터 `9`까지 `i`값) `i <= 9`는 `true`입니다.  그러나 `i`의 값이 `10`이면 `false`가 됩니다.

`for` 루프에는 초기화 절 (`var i=0`), 조건부 테스트 절 (`i <= 9`), 업데이트 절 (`i = i + 1`) 이라는 세 개의 절이 있습니다. 따라서 루프 반복 횟수를 세는 경우, `for`가 이해하기 쉽고 더 간단한 형식입니다.

암시적 조건 테스트는 모든 속성이 처리되었는지 여부와 같은 객체의 속성 (2 장 참조)과 같이 특정 값을 반복하기 위한 다른 특수한 루프 양식이 있습니다. "조건이 실패 할 때까지 루프"개념은 루프의 형식에 관계없이 유지됩니다.

## 함수

전화 상점 직원은 아마도 세금 및 최종 구매 금액을 계산하기 위해 계산기를 들고 다니지 않습니다. 그것은 한 번 정의하고 반복해서 사용해야하는 작업입니다. 가능성은 회사에 "기능들"이 내장 된 계산대 (컴퓨터, 태블릿 등)가 있습니다.

비슷하게, 프로그램은 반복적으로 반복적으로 반복하는 대신(말장난!) 코드의 작업을 재사용 가능한 부분으로 분해하려고 합니다. 이를 수행하는 방법은 `함수`를 정의하는 것입니다.

함수는 일반적으로 이름으로 "호출"할 수있는 코드의 명명 된 섹션이며 그 안에있는 코드는 매번 실행됩니다.

고려사항:

```js
function printAmount() {
	console.log( amount.toFixed( 2 ) );
}

var amount = 99.99;

printAmount(); // "99.99"

amount = amount * 2;

printAmount(); // "199.98"
```

함수는 선택적으로 인수 (일명 매개 ​​변수) - 전달한 값을 취할 수 있습니다. 또한 값을 선택적으로 반환 할 수도 있습니다.

```js
function printAmount(amt) {
	console.log( amt.toFixed( 2 ) );
}

function formatAmount() {
	return "$" + amount.toFixed( 2 );
}

var amount = 99.99;

printAmount( amount * 2 );		// "199.98"

amount = formatAmount();
console.log( amount );			// "$99.99"
```

함수 `printAmount (..)`는 `amt`라고 부르는 매개 변수를 취합니다. `formatAmount()` 함수는 값을 반환합니다. 물론 동일한 기능에서 두 기술을 결합 할 수도 있습니다.

함수는 여러 번 호출 할 계획 인 코드에 자주 사용되지만 한 번만 호출 할 계획이라 할지라도 관련 코드 비트를 명명 된 컬렉션으로 구성하는 데 유용 할 수 있습니다. 

고려사항: 

```js
const TAX_RATE = 0.08;

function calculateFinalPurchaseAmount(amt) {
	// calculate the new amount with the tax
	amt = amt + (amt * TAX_RATE);

	// return the new amount
	return amt;
}

var amount = 99.99;

amount = calculateFinalPurchaseAmount( amount );

console.log( amount.toFixed( 2 ) );		// "107.99"
```

`calculateFinalPurchaseAmount(..)`는 한 번만 호출되지만 별도의 명명 된 함수로 동작을 구성하면 로직을 사용하는 코드가 만들어집니다 (`amount = calculateFinal ...` 문). 함수에 더 많은 구문이 포함되어 있다면 이 점은 더욱 분명해질 것입니다.

### 스코프

전화 상점 직원에게 매장에서 판매하지 않는 전화 모델을 요청하면 원하는 전화를 판매 할 수 없습니다. 그녀는 매장의 인벤토리에 있는 전화에만 액세스 할 수 있습니다. 찾고 있는 전화를 찾을 수 있는지 알아보기 위해 다른 상점을 방문해야합니다.

프로그래밍에는이 개념의 용어 인 *스코프* (기술적으로 *렉시컬 스코프* 라고 함)가 있습니다. 자바스크립트에서는 각 함수가 자체 범위를 가져옵니다. 스코프는 기본적으로 변수의 모음 일뿐만 아니라 변수가 이름으로 어떻게 액세스되는지에 대한 규칙입니다. 해당 함수 내의 코드만 해당 함수의 *스코프* 변수에 액세스 할 수 있습니다.

변수 이름은 동일한 스코프 내에서 고유해야합니다. 서로 다른 `a` 변수가 두 개씩 나란히 있을 수 없습니다. 그러나 동일한 변수 이름 `a` 가 다른 범위에 나타날 수 있습니다.

```js
function one() {
	// this `a` only belongs to the `one()` function
	var a = 1;
	console.log( a );
}

function two() {
	// this `a` only belongs to the `two()` function
	var a = 2;
	console.log( a );
}

one();		// 1
two();		// 2
```

Also, a scope can be nested inside another scope, just like if a clown at a birthday party blows up one balloon inside another balloon. If one scope is nested inside another, code inside the innermost scope can access variables from either scope.

Consider:

```js
function outer() {
	var a = 1;

	function inner() {
		var b = 2;

		// we can access both `a` and `b` here
		console.log( a + b );	// 3
	}

	inner();

	// we can only access `a` here
	console.log( a );			// 1
}

outer();
```

Lexical scope rules say that code in one scope can access variables of either that scope or any scope outside of it.

So, code inside the `inner()` function has access to both variables `a` and `b`, but code in `outer()` has access only to `a` -- it cannot access `b` because that variable is only inside `inner()`.

Recall this code snippet from earlier:

```js
const TAX_RATE = 0.08;

function calculateFinalPurchaseAmount(amt) {
	// calculate the new amount with the tax
	amt = amt + (amt * TAX_RATE);

	// return the new amount
	return amt;
}
```

The `TAX_RATE` constant (variable) is accessible from inside the `calculateFinalPurchaseAmount(..)` function, even though we didn't pass it in, because of lexical scope.

**Note:** For more information about lexical scope, see the first three chapters of the *Scope & Closures* title of this series.

## Practice

There is absolutely no substitute for practice in learning programming. No amount of articulate writing on my part is alone going to make you a programmer.

With that in mind, let's try practicing some of the concepts we learned here in this chapter. I'll give the "requirements," and you try it first. Then consult the code listing below to see how I approached it.

* Write a program to calculate the total price of your phone purchase. You will keep purchasing phones (hint: loop!) until you run out of money in your bank account. You'll also buy accessories for each phone as long as your purchase amount is below your mental spending threshold.
* After you've calculated your purchase amount, add in the tax, then print out the calculated purchase amount, properly formatted.
* Finally, check the amount against your bank account balance to see if you can afford it or not.
* You should set up some constants for the "tax rate," "phone price," "accessory price," and "spending threshold," as well as a variable for your "bank account balance.""
* You should define functions for calculating the tax and for formatting the price with a "$" and rounding to two decimal places.
* **Bonus Challenge:** Try to incorporate input into this program, perhaps with the `prompt(..)` covered in "Input" earlier. You may prompt the user for their bank account balance, for example. Have fun and be creative!

OK, go ahead. Try it. Don't peek at my code listing until you've given it a shot yourself!

**Note:** Because this is a JavaScript book, I'm obviously going to solve the practice exercise in JavaScript. But you can do it in another language for now if you feel more comfortable.

Here's my JavaScript solution for this exercise:

```js
const SPENDING_THRESHOLD = 200;
const TAX_RATE = 0.08;
const PHONE_PRICE = 99.99;
const ACCESSORY_PRICE = 9.99;

var bank_balance = 303.91;
var amount = 0;

function calculateTax(amount) {
	return amount * TAX_RATE;
}

function formatAmount(amount) {
	return "$" + amount.toFixed( 2 );
}

// keep buying phones while you still have money
while (amount < bank_balance) {
	// buy a new phone!
	amount = amount + PHONE_PRICE;

	// can we afford the accessory?
	if (amount < SPENDING_THRESHOLD) {
		amount = amount + ACCESSORY_PRICE;
	}
}

// don't forget to pay the government, too
amount = amount + calculateTax( amount );

console.log(
	"Your purchase: " + formatAmount( amount )
);
// Your purchase: $334.76

// can you actually afford this purchase?
if (amount > bank_balance) {
	console.log(
		"You can't afford this purchase. :("
	);
}
// You can't afford this purchase. :(
```

**Note:** The simplest way to run this JavaScript program is to type it into the developer console of your nearest browser.

How did you do? It wouldn't hurt to try it again now that you've seen my code. And play around with changing some of the constants to see how the program runs with different values.

## Review

Learning programming doesn't have to be a complex and overwhelming process. There are just a few basic concepts you need to wrap your head around.

These act like building blocks. To build a tall tower, you start first by putting block on top of block on top of block. The same goes with programming. Here are some of the essential programming building blocks:

* You need *operators* to perform actions on values.
* You need values and *types* to perform different kinds of actions like math on `number`s or output with `string`s.
* You need *variables* to store data (aka *state*) during your program's execution.
* You need *conditionals* like `if` statements to make decisions.
* You need *loops* to repeat tasks until a condition stops being true.
* You need *functions* to organize your code into logical and reusable chunks.

Code comments are one effective way to write more readable code, which makes your program easier to understand, maintain, and fix later if there are problems.

Finally, don't neglect the power of practice. The best way to learn how to write code is to write code.

I'm excited you're well on your way to learning how to code, now! Keep it up. Don't forget to check out other beginner programming resources (books, blogs, online training, etc.). This chapter and this book are a great start, but they're just a brief introduction.

The next chapter will review many of the concepts from this chapter, but from a more JavaScript-specific perspective, which will highlight most of the major topics that are addressed in deeper detail throughout the rest of the series.
