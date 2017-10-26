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


이러한 일반적인 상황에서 당신을 도울 수 있도록 자바스크립트는 때로는 값을 입력하여 일치하는 유형에 *암묵적으로* 강제합니다.

따라서 `==` 느슨한 equals 연산자를 사용하여 비교 `"99.99"== 99.99`를 만들면 자바스크립트는 왼쪽 `"99.99"`를 `숫자 99.99`로 변환합니다. 비교는 `99.99 == 99.99`가되는데, 이는 `참`입니다.

당신이 그 행동을 지배하는 규칙을 배우는 데 시간을 할애하지 않았다면 암묵적인 강제 변환은 혼란을 야기 할 수 있습니다. 대부분의 JS 개발자는 절대 사용하지 않으므로 암묵적인 강제가 혼란스럽고 예기치 않은 버그가 있는 프로그램에 피해를 입힙니다. 따라서 피해야합니다. 때로는 언어 디자인의 결함으로 불리기도 합니다.

그러나 암묵적인 강제 변환은 *배울 수 있는* 메커니즘이며, 또한 자바스크립트 프로그래밍을 중요하게 생각하는 사람이 *배워야합니다.* 규칙을 배운 후에 혼란 스러울뿐만 아니라 실제로 프로그램을 더 잘 만들 수 있습니다! 그 노력은 그만한 가치가 있습니다.

**참고 :** 강제 변환에 대한 자세한 내용은 이 책의 2 장과 이 시리즈의 *유형 및 문법* 4 장을 참조하십시오.

## Code Comments

The phone store employee might jot down some notes on the features of a newly released phone or on the new plans her company offers. These notes are only for the employee -- they're not for customers to read. Nevertheless, these notes help the employee do her job better by documenting the hows and whys of what she should tell customers.

One of the most important lessons you can learn about writing code is that it's not just for the computer. Code is every bit as much, if not more, for the developer as it is for the compiler.

Your computer only cares about machine code, a series of binary 0s and 1s, that comes from *compilation*. There's a nearly infinite number of programs you could write that yield the same series of 0s and 1s. The choices you make about how to write your program matter -- not only to you, but to your other team members and even to your future self.

You should strive not just to write programs that work correctly, but programs that make sense when examined. You can go a long way in that effort by choosing good names for your variables (see "Variables") and functions (see "Functions").

But another important part is code comments. These are bits of text in your program that are inserted purely to explain things to a human. The interpreter/compiler will always ignore these comments.

There are lots of opinions on what makes well-commented code; we can't really define absolute universal rules. But some observations and guidelines are quite useful:

* Code without comments is suboptimal.
* Too many comments (one per line, for example) is probably a sign of poorly written code.
* Comments should explain *why*, not *what*. They can optionally explain *how* if that's particularly confusing.

In JavaScript, there are two types of comments possible: a single-line comment and a multiline comment.

Consider:

```js
// This is a single-line comment

/* But this is
       a multiline
             comment.
                      */
```

The `//` single-line comment is appropriate if you're going to put a comment right above a single statement, or even at the end of a line. Everything on the line after the `//` is treated as the comment (and thus ignored by the compiler), all the way to the end of the line. There's no restriction to what can appear inside a single-line comment.

Consider:

```js
var a = 42;		// 42 is the meaning of life
```

The `/* .. */` multiline comment is appropriate if you have several lines worth of explanation to make in your comment.

Here's a common usage of multiline comments:

```js
/* The following value is used because
   it has been shown that it answers
   every question in the universe. */
var a = 42;
```

It can also appear anywhere on a line, even in the middle of a line, because the `*/` ends it. For example:

```js
var a = /* arbitrary value */ 42;

console.log( a );	// 42
```

The only thing that cannot appear inside a multiline comment is a `*/`, because that would be interpreted to end the comment.

You will definitely want to begin your learning of programming by starting off with the habit of commenting code. Throughout the rest of this chapter, you'll see I use comments to explain things, so do the same in your own practice. Trust me, everyone who reads your code will thank you!

## Variables

Most useful programs need to track a value as it changes over the course of the program, undergoing different operations as called for by your program's intended tasks.

The easiest way to go about that in your program is to assign a value to a symbolic container, called a *variable* -- so called because the value in this container can *vary* over time as needed.

In some programming languages, you declare a variable (container) to hold a specific type of value, such as `number` or `string`. *Static typing*, otherwise known as *type enforcement*, is typically cited as a benefit for program correctness by preventing unintended value conversions.

Other languages emphasize types for values instead of variables. *Weak typing*, otherwise known as *dynamic typing*, allows a variable to hold any type of value at any time. It's typically cited as a benefit for program flexibility by allowing a single variable to represent a value no matter what type form that value may take at any given moment in the program's logic flow.

JavaScript uses the latter approach, *dynamic typing*, meaning variables can hold values of any *type* without any *type* enforcement.

As mentioned earlier, we declare a variable using the `var` statement -- notice there's no other *type* information in the declaration. Consider this simple program:

```js
var amount = 99.99;

amount = amount * 2;

console.log( amount );		// 199.98

// convert `amount` to a string, and
// add "$" on the beginning
amount = "$" + String( amount );

console.log( amount );		// "$199.98"
```

The `amount` variable starts out holding the number `99.99`, and then holds the `number` result of `amount * 2`, which is `199.98`.

The first `console.log(..)` command has to *implicitly* coerce that `number` value to a `string` to print it out.

Then the statement `amount = "$" + String(amount)` *explicitly* coerces the `199.98` value to a `string` and adds a `"$"` character to the beginning. At this point, `amount` now holds the `string` value `"$199.98"`, so the second `console.log(..)` statement doesn't need to do any coercion to print it out.

JavaScript developers will note the flexibility of using the `amount` variable for each of the `99.99`, `199.98`, and the `"$199.98"` values. Static-typing enthusiasts would prefer a separate variable like `amountStr` to hold the final `"$199.98"` representation of the value, because it's a different type.

Either way, you'll note that `amount` holds a running value that changes over the course of the program, illustrating the primary purpose of variables: managing program *state*.

In other words, *state* is tracking the changes to values as your program runs.

Another common usage of variables is for centralizing value setting. This is more typically called *constants*, when you declare a variable with a value and intend for that value to *not change* throughout the program.

You declare these *constants*, often at the top of a program, so that it's convenient for you to have one place to go to alter a value if you need to. By convention, JavaScript variables as constants are usually capitalized, with underscores `_` between multiple words.

Here's a silly example:

```js
var TAX_RATE = 0.08;	// 8% sales tax

var amount = 99.99;

amount = amount * 2;

amount = amount + (amount * TAX_RATE);

console.log( amount );				// 215.9784
console.log( amount.toFixed( 2 ) );	// "215.98"
```

**Note:** Similar to how `console.log(..)` is a function `log(..)` accessed as an object property on the `console` value, `toFixed(..)` here is a function that can be accessed on `number` values. JavaScript `number`s aren't automatically formatted for dollars -- the engine doesn't know what your intent is and there's no type for currency. `toFixed(..)` lets us specify how many decimal places we'd like the `number` rounded to, and it produces the `string` as necessary.

The `TAX_RATE` variable is only *constant* by convention -- there's nothing special in this program that prevents it from being changed. But if the city raises the sales tax rate to 9%, we can still easily update our program by setting the `TAX_RATE` assigned value to `0.09` in one place, instead of finding many occurrences of the value `0.08` strewn throughout the program and updating all of them.

The newest version of JavaScript at the time of this writing (commonly called "ES6") includes a new way to declare *constants*, by using `const` instead of `var`:

```js
// as of ES6:
const TAX_RATE = 0.08;

var amount = 99.99;

// ..
```

Constants are useful just like variables with unchanged values, except that constants also prevent accidentally changing value somewhere else after the initial setting. If you tried to assign any different value to `TAX_RATE` after that first declaration, your program would reject the change (and in strict mode, fail with an error -- see "Strict Mode" in Chapter 2).

By the way, that kind of "protection" against mistakes is similar to the static-typing type enforcement, so you can see why static types in other languages can be attractive!

**Note:** For more information about how different values in variables can be used in your programs, see the *Types & Grammar* title of this series.

## Blocks

The phone store employee must go through a series of steps to complete the checkout as you buy your new phone.

Similarly, in code we often need to group a series of statements together, which we often call a *block*. In JavaScript, a block is defined by wrapping one or more statements inside a curly-brace pair `{ .. }`. Consider:

```js
var amount = 99.99;

// a general block
{
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

This kind of standalone `{ .. }` general block is valid, but isn't as commonly seen in JS programs. Typically, blocks are attached to some other control statement, such as an `if` statement (see "Conditionals") or a loop (see "Loops"). For example:

```js
var amount = 99.99;

// is amount big enough?
if (amount > 10) {			// <-- block attached to `if`
	amount = amount * 2;
	console.log( amount );	// 199.98
}
```

We'll explain `if` statements in the next section, but as you can see, the `{ .. }` block with its two statements is attached to `if (amount > 10)`; the statements inside the block will only be processed if the conditional passes.

**Note:** Unlike most other statements like `console.log(amount);`, a block statement does not need a semicolon (`;`) to conclude it.

## Conditionals

"Do you want to add on the extra screen protectors to your purchase, for $9.99?" The helpful phone store employee has asked you to make a decision. And you may need to first consult the current *state* of your wallet or bank account to answer that question. But obviously, this is just a simple "yes or no" question.

There are quite a few ways we can express *conditionals* (aka decisions) in our programs.

The most common one is the `if` statement. Essentially, you're saying, "*If* this condition is true, do the following...". For example:

```js
var bank_balance = 302.13;
var amount = 99.99;

if (amount < bank_balance) {
	console.log( "I want to buy this phone!" );
}
```

The `if` statement requires an expression in between the parentheses `( )` that can be treated as either `true` or `false`. In this program, we provided the expression `amount < bank_balance`, which indeed will either evaluate to `true` or `false` depending on the amount in the `bank_balance` variable.

You can even provide an alternative if the condition isn't true, called an `else` clause. Consider:

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

Here, if `amount < bank_balance` is `true`, we'll print out `"I'll take the accessory!"` and add the `9.99` to our `amount` variable. Otherwise, the `else` clause says we'll just politely respond with `"No, thanks."` and leave `amount` unchanged.

As we discussed in "Values & Types" earlier, values that aren't already of an expected type are often coerced to that type. The `if` statement expects a `boolean`, but if you pass it something that's not already `boolean`, coercion will occur.

JavaScript defines a list of specific values that are considered "falsy" because when coerced to a `boolean`, they become `false` -- these include values like `0` and `""`. Any other value not on the "falsy" list is automatically "truthy" -- when coerced to a `boolean` they become `true`. Truthy values include things like `99.99` and `"free"`. See "Truthy & Falsy" in Chapter 2 for more information.

*Conditionals* exist in other forms besides the `if`. For example, the `switch` statement can be used as a shorthand for a series of `if..else` statements (see Chapter 2). Loops (see "Loops") use a *conditional* to determine if the loop should keep going or stop.

**Note:** For deeper information about the coercions that can occur implicitly in the test expressions of *conditionals*, see Chapter 4 of the *Types & Grammar* title of this series.

## Loops

During busy times, there's a waiting list for customers who need to speak to the phone store employee. While there's still people on that list, she just needs to keep serving the next customer.

Repeating a set of actions until a certain condition fails -- in other words, repeating only while the condition holds -- is the job of programming loops; loops can take different forms, but they all satisfy this basic behavior.

A loop includes the test condition as well as a block (typically as `{ .. }`). Each time the loop block executes, that's called an *iteration*.

For example, the `while` loop and the `do..while` loop forms illustrate the concept of repeating a block of statements until a condition no longer evaluates to `true`:

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

The only practical difference between these loops is whether the conditional is tested before the first iteration (`while`) or after the first iteration (`do..while`).

In either form, if the conditional tests as `false`, the next iteration will not run. That means if the condition is initially `false`, a `while` loop will never run, but a `do..while` loop will run just the first time.

Sometimes you are looping for the intended purpose of counting a certain set of numbers, like from `0` to `9` (ten numbers). You can do that by setting a loop iteration variable like `i` at value `0` and incrementing it by `1` each iteration.

**Warning:** For a variety of historical reasons, programming languages almost always count things in a zero-based fashion, meaning starting with `0` instead of `1`. If you're not familiar with that mode of thinking, it can be quite confusing at first. Take some time to practice counting starting with `0` to become more comfortable with it!

The conditional is tested on each iteration, much as if there is an implied `if` statement inside the loop.

We can use JavaScript's `break` statement to stop a loop. Also, we can observe that it's awfully easy to create a loop that would otherwise run forever without a `break`ing mechanism.

Let's illustrate:

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

**Warning:** This is not necessarily a practical form you'd want to use for your loops. It's presented here for illustration purposes only.

While a `while` (or `do..while`) can accomplish the task manually, there's another syntactic form called a `for` loop for just that purpose:

```js
for (var i = 0; i <= 9; i = i + 1) {
	console.log( i );
}
// 0 1 2 3 4 5 6 7 8 9
```

As you can see, in both cases the conditional `i <= 9` is `true` for the first 10 iterations (`i` of values `0` through `9`) of either loop form, but becomes `false` once `i` is value `10`.

The `for` loop has three clauses: the initialization clause (`var i=0`), the conditional test clause (`i <= 9`), and the update clause (`i = i + 1`). So if you're going to do counting with your loop iterations, `for` is a more compact and often easier form to understand and write.

There are other specialized loop forms that are intended to iterate over specific values, such as the properties of an object (see Chapter 2) where the implied conditional test is just whether all the properties have been processed. The "loop until a condition fails" concept holds no matter what the form of the loop.

## Functions

The phone store employee probably doesn't carry around a calculator to figure out the taxes and final purchase amount. That's a task she needs to define once and reuse over and over again. Odds are, the company has a checkout register (computer, tablet, etc.) with those "functions" built in.

Similarly, your program will almost certainly want to break up the code's tasks into reusable pieces, instead of repeatedly repeating yourself repetitiously (pun intended!). The way to do this is to define a `function`.

A function is generally a named section of code that can be "called" by name, and the code inside it will be run each time. Consider:

```js
function printAmount() {
	console.log( amount.toFixed( 2 ) );
}

var amount = 99.99;

printAmount(); // "99.99"

amount = amount * 2;

printAmount(); // "199.98"
```

Functions can optionally take arguments (aka parameters) -- values you pass in. And they can also optionally return a value back.

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

The function `printAmount(..)` takes a parameter that we call `amt`. The function `formatAmount()` returns a value. Of course, you can also combine those two techniques in the same function.

Functions are often used for code that you plan to call multiple times, but they can also be useful just to organize related bits of code into named collections, even if you only plan to call them once.

Consider:

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

Although `calculateFinalPurchaseAmount(..)` is only called once, organizing its behavior into a separate named function makes the code that uses its logic (the `amount = calculateFinal...` statement) cleaner. If the function had more statements in it, the benefits would be even more pronounced.

### Scope

If you ask the phone store employee for a phone model that her store doesn't carry, she will not be able to sell you the phone you want. She only has access to the phones in her store's inventory. You'll have to try another store to see if you can find the phone you're looking for.

Programming has a term for this concept: *scope* (technically called *lexical scope*). In JavaScript, each function gets its own scope. Scope is basically a collection of variables as well as the rules for how those variables are accessed by name. Only code inside that function can access that function's *scoped* variables.

A variable name has to be unique within the same scope -- there can't be two different `a` variables sitting right next to each other. But the same variable name `a` could appear in different scopes.

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
