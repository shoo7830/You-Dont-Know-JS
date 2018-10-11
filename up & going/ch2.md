# You Don't Know JS: Up & Going
# 2장 자바스크립트 속으로

이전 장에서는 변수, 루프, 조건부 및 함수와 같은 프로그래밍의 기본 구성 요소를 소개했습니다. 물론 표시 된 모든 코드는 자바스크립트로 작성되었습니다. 하지만 이 장에서는 JS 개발자로서 떠오르기 위해 알아야 할 사항에 집중하고자 합니다.

이 장에서 이어지는 *YDKJS* 서적까지 완전히 탐구되지는 않을 개념들을 소개 할 것입니다. 이 장을 이 시리즈의 나머지 부분에서 자세히 다루는 주제의 개요로 생각할 수 있습니다.

특히 자바스크립트를 처음 사용하는 사람이라면 여러 번 개념과 코드 예제를 검토하는 데 상당한 시간을 할애해야합니다. 좋은 기초는 벽돌과 타일이 누적 된 것이므로 전체 내용을 즉시 이해하고 첫 번째에서 이해할 것이라고 기대하지 마세요.

자바스크립트를 깊게 배우는 당신의 여정은 여기서부터 시작입니다.

**참고:** 첫 장에서도 말했듯이 이 장을 읽고 읽으면서 코드 전부를 직접 실행해야 합니다. 이 글의 일부는이 글을 쓰는 시점에서 최신 버전의 JavaScript (일반적으로 JS 규격의 공식 명칭 인 ECMAScript의 제 6 판에서는 "ES6"이라고 함)에 도입 된 기능을 사용한다는 점을 알아 두십시오. 이전 ES6 이전 브라우저를 사용하는 경우 코드가 작동하지 않을 수 있습니다. 최신 브라우저 (예 : Chrome, Firefox 또는 IE)의 최신 업데이트를 사용해야합니다.

## 값과 유형

1장에서 주장한 것 처럼 자바스크립트는 변수 유형이 없는 값 유형을 가집니다. 사용 가능한 기본 제공 유형은 다음과 같습니다:

* `문자열`
* `숫자`
* `부울`
* `null` 과 `undefined`
* `객체`
* `심볼` (ES6에서 새로 추가)

자바스크립트는 값을 검사하고 어떤 유형인지 알려주는 `typeof` 연산자를 제공합니다:

```js
var a;
typeof a;				// "undefined"

a = "hello world";
typeof a;				// "문자열"

a = 42;
typeof a;				// "숫자"

a = true;
typeof a;				// "부울"

a = null;
typeof a;				// "객체" -- 이상한, 버그

a = undefined;
typeof a;				// "undefined"

a = { b: "c" };
typeof a;				// "객체"
```
`typeof` 연산자의 반환 값은 항상 6 중 하나입니다 (ES6의 경우 7 개 - "심볼"유형) 문자열 값입니다. 즉, `typeof "abc"`는 `문자열`이 아니라 `"문자열"`을 반환합니다.

이 스니펫에서는 변수 `a`가 모든 다른 유형의 값을 보유하고 있으며 표면상의 모습에도 불구하고 `typeof a`는 "`a`의 유형"을 요구하지 않고 "`a`의 현재 값의 유형"을 요구합니다. 자바스크립트에는 값에만 유형이 있습니다. 변수는 그 값에 대한 단순한 컨테이너입니다.

`typeof null`은 `"null"`을 반환 할 때 `"객체"`를 잘못 반환하기 때문에 흥미로운 사례입니다.

**경고:** 이것은 JS의 오래된 버그이지만 결코 고칠 수 없는 버그입니다. 웹에서 코드가 너무 많으면 버그에 의존하기 때문에 버그를 수정하면 더 많은 버그가 발생합니다!

또한 `a = undefined`에 유의하십시오. 우리는 명시적으로 `a`를 `undefined`로 설정하고 있지만 스니펫 맨 위에 있는 행에 `var a;`와 같이 아직 값이 설정되지 않은 변수와 동작상의 차이는 없습니다. 변수는 값을 반환하지 않는 함수와 `void` 연산자를 사용하여 여러 가지 다른 방법으로이 "undefined"값 상태가 될 수 있습니다.

### 객체

`객체` 유형은 복합 유형의 값을 나타내며, 각 속성은 유형의 자체 값을 보유하는 특성 (위치 지정)을 설정할 수 있습니다. 이것은 아마도 모든 자바스크립트에서 가장 유용한 값 유형 중 하나 일 것입니다.

```js
var obj = {
	a: "hello world",
	b: 42,
	c: true
};

obj.a;		// "hello world"
obj.b;		// 42
obj.c;		// true

obj["a"];	// "hello world"
obj["b"];	// 42
obj["c"];	// true
```

이 `obj` 값을 시각적으로 생각하는 것이 도움이 될 수 있습니다:

<img src="fig4.png">

속성은 *점 표기법* (obj.a) 또는 *대괄호 표기법* (obj [ "a"])으로 액세스 할 수 있습니다. 점 표기법은 짧고 일반적으로 읽기가 쉽기 때문에 가능한 경우 선호됩니다.

대괄호 표기법은 `obj [ "hello world!"]`와 같이 특수 문자가 있는 속성 이름을 가진 경우 유용합니다. 이러한 속성은 대괄호 표기법을 통해 액세스 할 때 대개 *키*라고합니다. `[]` 표기법에는 변수 (다음에 설명 됨) 또는 `문자열` *리터럴* ( `".."`또는 `".."`으로 묶어야 함)이 필요합니다.

물론 대괄호 표기법은 속성 / 키에 액세스하려고하지만 이름이 다른 변수에 저장되는 경우 유용합니다:

```js
var obj = {
	a: "hello world",
	b: 42
};

var b = "a";

obj[b];			// "hello world"
obj["b"];		// 42
```

**참고:** 자바스크립트 `객체`에 대한 자세한 내용은 이 시리즈의 *this & 객체 프로토타입* ,특히 3 장을 참조하십시오.

자바스크립트 프로그램에서 일반적으로 상호 작용 할 수 있는 몇 가지 다른 값 유형이 있습니다. 그것은 *배열*과 *함수*입니다. 그러나 적절한 기본 제공 유형이 아니라 특수 유형의 `객체` 유형인 하위 유형과 더 비슷하게 생각해야합니다.

#### 배열

배열은 특히 명명된 속성/키가 아닌 숫자로 인덱싱 된 위치에 있는 값(모든 유형의 값을)을 보유하는 `객체`입니다.
예: 

```js
var arr = [
	"hello world",
	42,
	true
];

arr[0];			// "hello world"
arr[1];			// 42
arr[2];			// true
arr.length;		// 3

typeof arr;		// "object"
```

**참고 :** JS와 마찬가지로 0에서 시작되는 언어는 배열에서 첫 번째 요소의 인덱스로 0을 사용합니다. 

`arr`을 시각적으로 생각하는 것이 도움이 될 수 있습니다.

<img src="fig5.png">

배열은 특수한 객체이기 때문에 (`typeof`가 의미하는) 자동으로 업데이트되는 `length` 속성을 포함하여 속성을 가질 수도 있습니다.

이론적으로 자신의 명명 된 속성을 가진 일반 `객체`로 배열을 사용하거나 객체를 사용할 수 있지만 배열과 비슷한 숫자 속성 (`0`, `1` 등) 만 지정할 수 있습니다. 그러나 이것은 일반적으로 각 유형의 부적절한 사용으로 간주됩니다.

가장 자연스러운 방법은 수치 적으로 지정된 값에 배열을 사용하고 명명 된 속성에 `객체`를 사용하는 것입니다.

#### 함수

JS 프로그램 전체에서 사용할 다른 `객체` 하위 유형은 함수입니다:

```js
function foo() {
	return 42;
}

foo.bar = "hello world";

typeof foo;			// "function"
typeof foo();		// "number"
typeof foo.bar;		// "string"
```
다시 말하지만, 함수는 `객체`의 하위 유형입니다. `typeof`는 `"function"`을 반환합니다. 이는 `함수`가 기본 유형임을 나타내며 따라서 속성을 가질 수 있지만 일반적으로 제한된 경우에만 (`foo.bar`와 같은) 함수 객체 속성을 사용합니다.

**참고:** JS 값과 유형에 대한 자세한 내용은 이 시리즈의 *유형과 문법*의 처음 두 장을 참조하십시오.

### 내장 메서드

방금 살펴본 내장 유형 및 하위 유형은 매우 강력하고 유용한 속성 및 메서드로 표시되는 비헤이비어를 포함합니다.

예:

```js
var a = "hello world";
var b = 3.14159;

a.length;				// 11
a.toUpperCase();		// "HELLO WORLD"
b.toFixed(4);			// "3.1416"
```

`a.toUpperCase()`를 호출 할 수있는 "방법"은 값에 존재하는 메서드보다 훨씬 복잡합니다.

간단히 말해, 원시 `문자열` 유형과 쌍을 이루는 일반적으로 "원시"라고하는 `String` (대문자 `S`) 객체 래퍼 형식이 있습니다. 프로토타입에 `toUpperCase()` 메서드를 정의하는 것은 이 객체 래퍼입니다.

속성이나 메서드 (예 : 이전 스니펫의 `a.toUpperCase()`)를 참조하여 `"hello world"`와 같은 원시 값을 `객체`로 사용하는 경우 JS는 자동으로 값을 객체 래퍼 사본 (표지 아래에 숨김)에 "밀어넣습니다".

`문자열` 값은 `String` 객체로 래핑 할 수 있고 `숫자`는 `Number` 객체로 래핑 할 수 있으며 `부울`은 `Boolean` 객체로 래핑 할 수 있습니다. 대부분의 경우, 값의 객체 래퍼 형식을 걱정하거나 직접 사용할 필요가 없습니다. 모든 경우에 기본 값 형식을 선호하고 자바스크립트가 나머지 부분을 처리합니다.

**참고:** JS 네이티브 및 "boxing"에 대한 자세한 내용은 이 시리즈의 *유형과 문법* 3장을 참조하십시오. 객체의 프로토타입을 더 잘 이해하려면 이 시리즈의 *this와 객체 프로토타입* 5장을 참조하십시오.

### 값의 비교

JS 프로그램에서 *평등*과 *불평등*의 두 가지 주요 유형을 비교해야합니다: 모든 비교 결과는 비교되는 값 유형에 관계없이 엄격하게 `부울` 값 (`true` 또는 `false`)입니다.

#### 강제 변환

1 장에서 강제 변환에 대해 간략하게 이야기했지만 여기에서 다시 살펴 보겠습니다.

강제 변환은 자바스크립트에서 두 가지 형태로 제공됩니다 : *명시적* 및 *암시적*입니다. 명시적 강제 변환은 코드에서 한 유형에서 다른 유형으로의 변환이 발생한다는 것을 분명히 볼 수 있으며, 암시적 강제 변환은 유형 변환이 다른 조작의 부작용이 아닌 것으로 더 많이 발생할 수있는 경우입니다.

강제 변환이 놀라운 결과를 가져올 수있는 명확한 장소가 있다는 사실 때문에 "강제 변환은 악"과 같은 감정을 들었을 것입니다. 아마 언어가 그들을 놀라게 할 때보다 개발자들에게 좌절감을 불러 일으킬만한 것은 없을 것입니다.

강제 변환은 악의도 아니고 놀라운 것도 아닙니다. 실제로 유형 강제 변환을 사용하여 작성할 수있는 대부분의 경우는 매우 현명하고 이해할 수 있으며 코드의 가독성을 *향상*시키는 데 사용될 수도 있습니다. 그러나 우리는 그 논쟁을 더 이상하지 않을 것입니다 - 이 시리즈의 *유형 및 문법* 4 장은 모든 면을 다룹니다.

다음은 *명시적* 강제 변환의 예입니다: 

```js
var a = "42";

var b = Number( a );

a;				// "42"
b;				// 42 -- 숫자!
```

그리고 다음은 *암시적* 강제 변환의 예입니다:

```js
var a = "42";

var b = a * 1;	// "42" 암시적으로 여기에 42 강제 변환

a;				// "42"
b;				// 42 -- 숫자!
```

#### 진실과 거짓

1장에서 우리는 값의 "진실"과 "거짓" 성질을 간략하게 언급하였습니다: `부울`이 아닌 값이 `부울`로 강요될 때 각각 `참`인지 `거짓`인지 되나요?

자바스크립트의 "거짓"값의 구체적인 목록은 다음과 같습니다:

* `""` (빈 문자열)
* `0`, `-0`, `NaN` (유효하지 않은 `숫자`)
* `null`, `undefined`
* `false`

이 "거짓"목록에 없는 모든 값은 "진실"입니다. 다음은 그 몇 가지 예입니다.:

* `"hello"`
* `42`
* `true`
* `[ ]`, `[ 1, "2", 3 ]` (배열)
* `{ }`, `{ a: 42 }` (객체)
* `function foo() { .. }` (함수)

`부울`이 아닌 값은 실제로 부울로 강제 변환되는 경우이 "진실"/ "위증"강제 변환에만 이어지는 것을 기억하는 것이 중요합니다.

#### 동등

네 개의 동등연산자가 있습니다: `==`, `===`, `!=`, `!==` 입니다. The `!` 양식은 물론 대칭인 "동등하지 않은"  버전입니다. *비 동등성*을 *불평등*과 혼동해서는 안됩니다.

`==`과 `===`의 차이점은 일반적으로는 `==`는 값의 동등성을 검사하고 `===`는 값과 동등성을 모두 확인 한다는 것을 특징으로 합니다. 그러나 이것은 정확하지 않습니다. 그것들을 특성화 하는 적절한 방법은 `==`는 강제 변환과 함께 가치 동등 을 검사하고 `===`는 강압을 허용하지 않고 가치 동등을 검사하는 것입니다. 이러한 이유로 "엄격한 동등" 이라고 종종 부릅니다.

`==`는 느슨한 동등 비교에 허용된 암시적 강제변환을 고려하고 `===` 엄격한 동등에서는 허용되지 않습니다.

```js
var a = "42";
var b = 42;

a == b;			// true
a === b;		// false
```

`a == b` 비교에서 JS는 유형이 일치하지 않다는 것을 알아차리고 형식이 일치할 때까지 하나 또는 두 개의 값을 다른 유형으로 강제 변환하는 일련의 단계를 거치며 간단한 값의 동등성을 확인할 수 있습니다.

그것에 대해 생각한다면, `a == b` 가 강요를 통해 `진실`을 줄 수 있는 두 가지 가능한 방법이 있습니다. 비교가 `42 == 42`로 끝나거나 `"42" == "42"`가 될 수 있습니다. 어떤가요?

답: `"42"`는 `42`가 되어 `42 == 42`로 비교됩니다. 간단한 예제에서 최종 결과가 동일하므로 프로세스가 어떤 방식으로 진행되는지는 중요하지 않습니다. 그러나 더 복잡한 경우에, 이 뿐만 아니라 비교의 최종 결과에 매우 중요하지만, 또한 당신을 위해 *무엇을* 이 결과에서 얻기 위해 매우 중요합니다.


`a === b`는 강제 변환이 허용되지 않으므로 `false`를 생성합니다.그래서 단순 값 비교는 분명히 실패합니다. 많은 개발자들은 `===`이 더 예측가능하다고 느끼기 때문에 `==`에서 벗어나 항상 해당 양식을 사용해야 한다고 옹호합니다. 나는 이 견해가 매우 근시안적이라고 생각합니다. 나는 `==` 이 *작동하는 법을 배우기 위해 시간을 들이면*, 당신의 프로그램을 돕는 강력한 도구라고 믿습니다.

우리는 여기 `==` 에서 강제 변환이 어떻게 작용하는지에 대한 핵심적인 모든 세부 사항을 다루지 않을 것입니다.
매우 감각적이지만, 조심해야할 몇 가지가 있습니다. 
정확한 규칙을 보려면 ES5 사양의 11.9.3 절 (http://www.ecma-international.org/ecma-262/5.1/)을 참조하시면 
이 메커니즘을 둘러싼 모든 부정적인 과대 광고와 비교해서 이 메커니즘이 얼마나 단순한 지 놀랄 것입니다. 

많은 세부 사항을 몇 가지 간단한 요점으로 요약하려면, 다양한 상황에서 `==` 또는 `===`를 사용할지를 알 수 있도록 도와줄 것입니다. 여기에 간단한 규칙이 있습니다.

* 비교의 값 (일명 측)이 `true` 또는 `false` 값일 수 있는 경우 `==` 피하고 `===` 사용.
* 비교의 어느 값이 이러한 특정 값 (`0`, `""`또는 빈 배열) 일 경우 `==`를 피하고 `===`를 사용.
* 다른 *모든* 경우에는 `==`를 사용하는 것이 안전합니다. 안전 할 뿐만 아니라 대부분의 경우 코드 가독성을 향상시키는 방식으로 단순화합니다.

이 규칙들이 부각 되려면 코드에 대해 비판적으로 생각하고 동등을 위해 비교되는 변수를 통해 어떤 종류의 값이 올 수 있는지에 대해 생각해야 합니다.
값에 대해 확신 할 수 있고 `==`가 안전하다면 사용하십시오! 값에 대해 확실하지 않으면 `===`를 사용하십시오. 그것은 간단합니다.

`!=` 같지않다의 형식은 `==`와 짝을 이루고 `!==` 형식은 `===`와 짝을 이룹니다. 
방금 논의한 모든 규칙과 관찰은 이러한 비동등간 비교를 위해 대칭적으로 유지됩니다.

`객체` (`함수` 및 `배열` 포함)와 같은 두 가지 비 기본 값을 비교하는 경우 `==` 및 `===` 비교 규칙에 특히 주의해야 합니다.
이러한 값은 실제로 참조에 의해 유지되므로 `==` 및 `===` 비교는 참조가 일치하는지 여부를 단순히 확인하고 기본 값에 대해서는 아무것도 확인하지 않습니다.

For example, `array`s are by default coerced to `string`s by simply joining all the values with commas (`,`) in between. You might think that two `array`s with the same contents would be `==` equal, but they're not:

예를 들어 `배열`은 모든 값 사이에 쉼표 (,)로 결합하여 기본적으로 `문자열`로 강제 변환됩니다. 
같은 내용을 가진 두 개의 `배열`은 `==`,  동등할 것이라고 생각할 수도 있지만 그렇지 않습니다.

```js
var a = [1,2,3];
var b = [1,2,3];
var c = "1,2,3";

a == c;		// true
b == c;		// true
a == b;		// false
```

**참고:** `==` 동등 비교 규칙에 대한 자세한 내용은 ES5 사양 (11.9.3 단원)을 참조하고 이 시리즈의 *형식과 문법* 4장을 참조하십시오. 
값 대 참조에 대한 자세한 내용은 2 장을 참조하십시오.

#### 부등

`<`,`>`, `<=`, `>=` 연산자는 부등호에 사용되며 사양에서 "관계형 비교" 라고합니다.
일반적으로 `숫자`와 같이 비교할 수 있는 값과 함께 사용됩니다. `3 < 4`를 이해하는 것은 쉽습니다.

그러나 JavaScript `문자열` 값은 일반적인 알파벳 규칙 ( `"bar" < "foo"`)을 사용하여 부등을 비교할 수도 있습니다

강제는 어떤가요? 
`==` 비교 (똑같은 것은 아니지만!)와 비슷한 규칙이 부등호 연산자에 적용됩니다.
특히 "엄격한 동등", `===` 과 같은 방식으로 강제를 허용하지 않는  "엄격한 부등" 연산자는 없습니다.

고려사항:

```js
var a = 41;
var b = "42";
var c = "43";

a < b;		// true
b < c;		// true
```

여기서 어떻게 되나요?
ES5 사양의 11.8.5 절에서는 `<` 비교에서 두 값이 모두 `문자열` 인 경우 `b < c`와 같이 비교가 사전식 (알파벳순으로 사전과 유사 함)으로 되어 있다고 말합니다.
그러나 하나 또는 둘 다 `문자열`이 아니고 `a < b` 인 경우 두 값이 모두 `숫자`로 강요되며 일반적인 숫자 비교가 발생합니다.

The biggest gotcha you may run into here with comparisons between potentially different value types -- remember, there are no "strict inequality" forms to use -- is when one of the values cannot be made into a valid number, such as:

잠재적으로 다른 값 유형 간의 비교를 통해 여기까지 갈 수있는 가장 큰 문제는 -- 기억하십시오. 사용할 "엄격한 부등" 양식이 없습니다. --  다음 중 하나의 값을 유효한 숫자로 만들 수 없는 경우입니다:

```js
var a = 42;
var b = "foo";

a < b;		// false
a > b;		// false
a == b;		// false
```

잠깐, 어떻게 그 세 가지 비교가 모두 `false` 일 수 있습니까?
`b` 값은 `<` 및 `>` 비교에서 "유효하지 않은 숫자 값" `NaN`으로 강제 변환되기 때문에 `NaN`이 다른 값보다 크지도 작지도 않습니다.

`==` 비교는 다른 이유로 실패합니다. `a == b`는 `42 == NaN` 또는 `"42"== "foo"`로 해석되면 실패 할 수 있습니다. 전자는 사실입니다.

**참고:** 부등 비교 규칙에 대한 자세한 내용은 ES5 사양의 섹션 11.8.5를 참조하고 이 시리즈의 *유형과 문법* 4 장을 참조하십시오.

## 변수

자바스크립트에서 변수 이름 (함수 이름 포함)은 유효한 *식별자*여야합니다.
Unicode와 같은 비 전통적 문자를 고려할 때 식별자의 유효한 문자에 대한 엄격하고 완전한 규칙은 조금 복잡합니다.
그러나 일반적인 ASCII 영숫자 문자만 고려하면 규칙은 간단합니다.

식별자는 `a`-`z`, `A`-`Z`, `$` 또는 `_`로 시작해야합니다. 그런 다음 해당 문자와 ​​숫자 `0`-`9`를 더할 수 있습니다.
일반적으로 변수 식별자와 동일한 규칙이 속성 이름에 적용됩니다.
그러나 특정 단어는 변수로 사용할 수 없지만 속성 이름으로 사용하면 좋습니다. 이 단어는 "예약어"라고하며 JS 키워드 (`for`, `in`, `if` 등)는 물론 `null`, `true` 및 `false`도 포함됩니다.

**참고 :** 예약어에 대한 자세한 내용은 이 시리즈의 *유형 및 문법* 부록 A를 참조하십시오.

### 함수 범위

현재 함수 범위에 속하는 변수를 선언하려면 `var` 키워드를 사용하고 함수 외부의 최상위 수준에 있는 경우 전역 범위를 선언합니다.

#### 호이스팅

어떤 `var`가 스코프 내부에 나타날 때마다, 그 선언은 전체 스코프에 속하고 어디에서나 액세스 할 수 있습니다.
비유적으로 이 동작은 `var` 선언이 개념적으로 둘러싸고 있는 범위의 맨 위로 이동 될 때 *호이스팅*이라고 부릅니다. 
기술적으로이 프로세스는 코드가 컴파일되는 방식에 의해 보다 정확하게 설명되지만 지금은 그 세부 사항을 건너 뛸 수 있습니다.

고려사항:

```js
var a = 2;

foo();					// works because `foo()`
						// declaration is "hoisted"

function foo() {
	a = 3;

	console.log( a );	// 3

	var a;				// declaration is "hoisted"
						// to the top of `foo()`
}

console.log( a );	// 2
```

**경고:** `var` 선언보다 범위 내에서 변수를 사용하기 위해 가변적인 *호이스팅*에 의존하는 것은 일반적이지 않으며 좋은 생각이 아닙니다.
*호이스트* 함수 선언을 사용하는 것이 훨씬 더 일반적이며 받아 들여집니다. 공식 선언 전에 나타나는 `foo()` 호출과 마찬가지로 호이스트 함수 선언을 사용하는 것이 일반적입니다.

#### Nested Scopes

When you declare a variable, it is available anywhere in that scope, as well as any lower/inner scopes. For example:

```js
function foo() {
	var a = 1;

	function bar() {
		var b = 2;

		function baz() {
			var c = 3;

			console.log( a, b, c );	// 1 2 3
		}

		baz();
		console.log( a, b );		// 1 2
	}

	bar();
	console.log( a );				// 1
}

foo();
```

Notice that `c` is not available inside of `bar()`, because it's declared only inside the inner `baz()` scope, and that `b` is not available to `foo()` for the same reason.

If you try to access a variable's value in a scope where it's not available, you'll get a `ReferenceError` thrown. If you try to set a variable that hasn't been declared, you'll either end up creating a variable in the top-level global scope (bad!) or getting an error, depending on "strict mode" (see "Strict Mode"). Let's take a look:

```js
function foo() {
	a = 1;	// `a` not formally declared
}

foo();
a;			// 1 -- oops, auto global variable :(
```

This is a very bad practice. Don't do it! Always formally declare your variables.

In addition to creating declarations for variables at the function level, ES6 *lets* you declare variables to belong to individual blocks (pairs of `{ .. }`), using the `let` keyword. Besides some nuanced details, the scoping rules will behave roughly the same as we just saw with functions:

```js
function foo() {
	var a = 1;

	if (a >= 1) {
		let b = 2;

		while (b < 5) {
			let c = b * 2;
			b++;

			console.log( a + c );
		}
	}
}

foo();
// 5 7 9
```

Because of using `let` instead of `var`, `b` will belong only to the `if` statement and thus not to the whole `foo()` function's scope. Similarly, `c` belongs only to the `while` loop. Block scoping is very useful for managing your variable scopes in a more fine-grained fashion, which can make your code much easier to maintain over time.

**Note:** For more information about scope, see the *Scope & Closures* title of this series. See the *ES6 & Beyond* title of this series for more information about `let` block scoping.

## Conditionals

In addition to the `if` statement we introduced briefly in Chapter 1, JavaScript provides a few other conditionals mechanisms that we should take a look at.

Sometimes you may find yourself writing a series of `if..else..if` statements like this:

```js
if (a == 2) {
	// do something
}
else if (a == 10) {
	// do another thing
}
else if (a == 42) {
	// do yet another thing
}
else {
	// fallback to here
}
```

This structure works, but it's a little verbose because you need to specify the `a` test for each case. Here's another option, the `switch` statement:

```js
switch (a) {
	case 2:
		// do something
		break;
	case 10:
		// do another thing
		break;
	case 42:
		// do yet another thing
		break;
	default:
		// fallback to here
}
```

The `break` is important if you want only the statement(s) in one `case` to run. If you omit `break` from a `case`, and that `case` matches or runs, execution will continue with the next `case`'s statements regardless of that `case` matching. This so called "fall through" is sometimes useful/desired:

```js
switch (a) {
	case 2:
	case 10:
		// some cool stuff
		break;
	case 42:
		// other stuff
		break;
	default:
		// fallback
}
```

Here, if `a` is either `2` or `10`, it will execute the "some cool stuff" code statements.

Another form of conditional in JavaScript is the "conditional operator," often called the "ternary operator." It's like a more concise form of a single `if..else` statement, such as:

```js
var a = 42;

var b = (a > 41) ? "hello" : "world";

// similar to:

// if (a > 41) {
//    b = "hello";
// }
// else {
//    b = "world";
// }
```

If the test expression (`a > 41` here) evaluates as `true`, the first clause (`"hello"`) results, otherwise the second clause (`"world"`) results, and whatever the result is then gets assigned to `b`.

The conditional operator doesn't have to be used in an assignment, but that's definitely the most common usage.

**Note:** For more information about testing conditions and other patterns for `switch` and `? :`, see the *Types & Grammar* title of this series.

## Strict Mode

ES5 added a "strict mode" to the language, which tightens the rules for certain behaviors. Generally, these restrictions are seen as keeping the code to a safer and more appropriate set of guidelines. Also, adhering to strict mode makes your code generally more optimizable by the engine. Strict mode is a big win for code, and you should use it for all your programs.

You can opt in to strict mode for an individual function, or an entire file, depending on where you put the strict mode pragma:

```js
function foo() {
	"use strict";

	// this code is strict mode

	function bar() {
		// this code is strict mode
	}
}

// this code is not strict mode
```

Compare that to:

```js
"use strict";

function foo() {
	// this code is strict mode

	function bar() {
		// this code is strict mode
	}
}

// this code is strict mode
```

One key difference (improvement!) with strict mode is disallowing the implicit auto-global variable declaration from omitting the `var`:

```js
function foo() {
	"use strict";	// turn on strict mode
	a = 1;			// `var` missing, ReferenceError
}

foo();
```

If you turn on strict mode in your code, and you get errors, or code starts behaving buggy, your temptation might be to avoid strict mode. But that instinct would be a bad idea to indulge. If strict mode causes issues in your program, almost certainly it's a sign that you have things in your program you should fix.

Not only will strict mode keep your code to a safer path, and not only will it make your code more optimizable, but it also represents the future direction of the language. It'd be easier on you to get used to strict mode now than to keep putting it off -- it'll only get harder to convert later!

**Note:** For more information about strict mode, see the Chapter 5 of the *Types & Grammar* title of this series.

## Functions As Values

So far, we've discussed functions as the primary mechanism of *scope* in JavaScript. You recall typical `function` declaration syntax as follows:

```js
function foo() {
	// ..
}
```

Though it may not seem obvious from that syntax, `foo` is basically just a variable in the outer enclosing scope that's given a reference to the `function` being declared. That is, the `function` itself is a value, just like `42` or `[1,2,3]` would be.

This may sound like a strange concept at first, so take a moment to ponder it. Not only can you pass a value (argument) *to* a function, but *a function itself can be a value* that's assigned to variables, or passed to or returned from other functions.

As such, a function value should be thought of as an expression, much like any other value or expression.

Consider:

```js
var foo = function() {
	// ..
};

var x = function bar(){
	// ..
};
```

The first function expression assigned to the `foo` variable is called *anonymous* because it has no `name`.

The second function expression is *named* (`bar`), even as a reference to it is also assigned to the `x` variable. *Named function expressions* are generally more preferable, though *anonymous function expressions* are still extremely common.

For more information, see the *Scope & Closures* title of this series.

### Immediately Invoked Function Expressions (IIFEs)

In the previous snippet, neither of the function expressions are executed -- we could if we had included `foo()` or `x()`, for instance.

There's another way to execute a function expression, which is typically referred to as an *immediately invoked function expression* (IIFE):

```js
(function IIFE(){
	console.log( "Hello!" );
})();
// "Hello!"
```

The outer `( .. )` that surrounds the `(function IIFE(){ .. })` function expression is just a nuance of JS grammar needed to prevent it from being treated as a normal function declaration.

The final `()` on the end of the expression -- the `})();` line -- is what actually executes the function expression referenced immediately before it.

That may seem strange, but it's not as foreign as first glance. Consider the similarities between `foo` and `IIFE` here:

```js
function foo() { .. }

// `foo` function reference expression,
// then `()` executes it
foo();

// `IIFE` function expression,
// then `()` executes it
(function IIFE(){ .. })();
```

As you can see, listing the `(function IIFE(){ .. })` before its executing `()` is essentially the same as including `foo` before its executing `()`; in both cases, the function reference is executed with `()` immediately after it.

Because an IIFE is just a function, and functions create variable *scope*, using an IIFE in this fashion is often used to declare variables that won't affect the surrounding code outside the IIFE:

```js
var a = 42;

(function IIFE(){
	var a = 10;
	console.log( a );	// 10
})();

console.log( a );		// 42
```

IIFEs can also have return values:

```js
var x = (function IIFE(){
	return 42;
})();

x;	// 42
```

The `42` value gets `return`ed from the `IIFE`-named function being executed, and is then assigned to `x`.

### Closure

*Closure* is one of the most important, and often least understood, concepts in JavaScript. I won't cover it in deep detail here, and instead refer you to the *Scope & Closures* title of this series. But I want to say a few things about it so you understand the general concept. It will be one of the most important techniques in your JS skillset.

You can think of closure as a way to "remember" and continue to access a function's scope (its variables) even once the function has finished running.

Consider:

```js
function makeAdder(x) {
	// parameter `x` is an inner variable

	// inner function `add()` uses `x`, so
	// it has a "closure" over it
	function add(y) {
		return y + x;
	};

	return add;
}
```

The reference to the inner `add(..)` function that gets returned with each call to the outer `makeAdder(..)` is able to remember whatever `x` value was passed in to `makeAdder(..)`. Now, let's use `makeAdder(..)`:

```js
// `plusOne` gets a reference to the inner `add(..)`
// function with closure over the `x` parameter of
// the outer `makeAdder(..)`
var plusOne = makeAdder( 1 );

// `plusTen` gets a reference to the inner `add(..)`
// function with closure over the `x` parameter of
// the outer `makeAdder(..)`
var plusTen = makeAdder( 10 );

plusOne( 3 );		// 4  <-- 1 + 3
plusOne( 41 );		// 42 <-- 1 + 41

plusTen( 13 );		// 23 <-- 10 + 13
```

More on how this code works:

1. When we call `makeAdder(1)`, we get back a reference to its inner `add(..)` that remembers `x` as `1`. We call this function reference `plusOne(..)`.
2. When we call `makeAdder(10)`, we get back another reference to its inner `add(..)` that remembers `x` as `10`. We call this function reference `plusTen(..)`.
3. When we call `plusOne(3)`, it adds `3` (its inner `y`) to the `1` (remembered by `x`), and we get `4` as the result.
4. When we call `plusTen(13)`, it adds `13` (its inner `y`) to the `10` (remembered by `x`), and we get `23` as the result.

Don't worry if this seems strange and confusing at first -- it can be! It'll take lots of practice to understand it fully.

But trust me, once you do, it's one of the most powerful and useful techniques in all of programming. It's definitely worth the effort to let your brain simmer on closures for a bit. In the next section, we'll get a little more practice with closure.

#### Modules

The most common usage of closure in JavaScript is the module pattern. Modules let you define private implementation details (variables, functions) that are hidden from the outside world, as well as a public API that *is* accessible from the outside.

Consider:

```js
function User(){
	var username, password;

	function doLogin(user,pw) {
		username = user;
		password = pw;

		// do the rest of the login work
	}

	var publicAPI = {
		login: doLogin
	};

	return publicAPI;
}

// create a `User` module instance
var fred = User();

fred.login( "fred", "12Battery34!" );
```

The `User()` function serves as an outer scope that holds the variables `username` and `password`, as well as the inner `doLogin()` function; these are all private inner details of this `User` module that cannot be accessed from the outside world.

**Warning:** We are not calling `new User()` here, on purpose, despite the fact that probably seems more common to most readers. `User()` is just a function, not a class to be instantiated, so it's just called normally. Using `new` would be inappropriate and actually waste resources.

Executing `User()` creates an *instance* of the `User` module -- a whole new scope is created, and thus a whole new copy of each of these inner variables/functions. We assign this instance to `fred`. If we run `User()` again, we'd get a new instance entirely separate from `fred`.

The inner `doLogin()` function has a closure over `username` and `password`, meaning it will retain its access to them even after the `User()` function finishes running.

`publicAPI` is an object with one property/method on it, `login`, which is a reference to the inner `doLogin()` function. When we return `publicAPI` from `User()`, it becomes the instance we call `fred`.

At this point, the outer `User()` function has finished executing. Normally, you'd think the inner variables like `username` and `password` have gone away. But here they have not, because there's a closure in the `login()` function keeping them alive.

That's why we can call `fred.login(..)` -- the same as calling the inner `doLogin(..)` -- and it can still access `username` and `password` inner variables.

There's a good chance that with just this brief glimpse at closure and the module pattern, some of it is still a bit confusing. That's OK! It takes some work to wrap your brain around it.

From here, go read the *Scope & Closures* title of this series for a much more in-depth exploration.

## `this` Identifier

Another very commonly misunderstood concept in JavaScript is the `this` identifier. Again, there's a couple of chapters on it in the *this & Object Prototypes* title of this series, so here we'll just briefly introduce the concept.

While it may often seem that `this` is related to "object-oriented patterns," in JS `this` is a different mechanism.

If a function has a `this` reference inside it, that `this` reference usually points to an `object`. But which `object` it points to depends on how the function was called.

It's important to realize that `this` *does not* refer to the function itself, as is the most common misconception.

Here's a quick illustration:

```js
function foo() {
	console.log( this.bar );
}

var bar = "global";

var obj1 = {
	bar: "obj1",
	foo: foo
};

var obj2 = {
	bar: "obj2"
};

// --------

foo();				// "global"
obj1.foo();			// "obj1"
foo.call( obj2 );		// "obj2"
new foo();			// undefined
```

There are four rules for how `this` gets set, and they're shown in those last four lines of that snippet.

1. `foo()` ends up setting `this` to the global object in non-strict mode -- in strict mode, `this` would be `undefined` and you'd get an error in accessing the `bar` property -- so `"global"` is the value found for `this.bar`.
2. `obj1.foo()` sets `this` to the `obj1` object.
3. `foo.call(obj2)` sets `this` to the `obj2` object.
4. `new foo()` sets `this` to a brand new empty object.

Bottom line: to understand what `this` points to, you have to examine how the function in question was called. It will be one of those four ways just shown, and that will then answer what `this` is.

**Note:** For more information about `this`, see Chapters 1 and 2 of the *this & Object Prototypes* title of this series.

## Prototypes

The prototype mechanism in JavaScript is quite complicated. We will only glance at it here. You will want to spend plenty of time reviewing Chapters 4-6 of the *this & Object Prototypes* title of this series for all the details.

When you reference a property on an object, if that property doesn't exist, JavaScript will automatically use that object's internal prototype reference to find another object to look for the property on. You could think of this almost as a fallback if the property is missing.

The internal prototype reference linkage from one object to its fallback happens at the time the object is created. The simplest way to illustrate it is with a built-in utility called `Object.create(..)`.

Consider:

```js
var foo = {
	a: 42
};

// create `bar` and link it to `foo`
var bar = Object.create( foo );

bar.b = "hello world";

bar.b;		// "hello world"
bar.a;		// 42 <-- delegated to `foo`
```

It may help to visualize the `foo` and `bar` objects and their relationship:

<img src="fig6.png">

The `a` property doesn't actually exist on the `bar` object, but because `bar` is prototype-linked to `foo`, JavaScript automatically falls back to looking for `a` on the `foo` object, where it's found.

This linkage may seem like a strange feature of the language. The most common way this feature is used -- and I would argue, abused -- is to try to emulate/fake a "class" mechanism with "inheritance."

But a more natural way of applying prototypes is a pattern called "behavior delegation," where you intentionally design your linked objects to be able to *delegate* from one to the other for parts of the needed behavior.

**Note:** For more information about prototypes and behavior delegation, see Chapters 4-6 of the *this & Object Prototypes* title of this series.

## Old & New

Some of the JS features we've already covered, and certainly many of the features covered in the rest of this series, are newer additions and will not necessarily be available in older browsers. In fact, some of the newest features in the specification aren't even implemented in any stable browsers yet.

So, what do you do with the new stuff? Do you just have to wait around for years or decades for all the old browsers to fade into obscurity?

That's how many people think about the situation, but it's really not a healthy approach to JS.

There are two main techniques you can use to "bring" the newer JavaScript stuff to the older browsers: polyfilling and transpiling.

### Polyfilling

The word "polyfill" is an invented term (by Remy Sharp) (https://remysharp.com/2010/10/08/what-is-a-polyfill) used to refer to taking the definition of a newer feature and producing a piece of code that's equivalent to the behavior, but is able to run in older JS environments.

For example, ES6 defines a utility called `Number.isNaN(..)` to provide an accurate non-buggy check for `NaN` values, deprecating the original `isNaN(..)` utility. But it's easy to polyfill that utility so that you can start using it in your code regardless of whether the end user is in an ES6 browser or not.

Consider:

```js
if (!Number.isNaN) {
	Number.isNaN = function isNaN(x) {
		return x !== x;
	};
}
```

The `if` statement guards against applying the polyfill definition in ES6 browsers where it will already exist. If it's not already present, we define `Number.isNaN(..)`.

**Note:** The check we do here takes advantage of a quirk with `NaN` values, which is that they're the only value in the whole language that is not equal to itself. So the `NaN` value is the only one that would make `x !== x` be `true`.

Not all new features are fully polyfillable. Sometimes most of the behavior can be polyfilled, but there are still small deviations. You should be really, really careful in implementing a polyfill yourself, to make sure you are adhering to the specification as strictly as possible.

Or better yet, use an already vetted set of polyfills that you can trust, such as those provided by ES5-Shim (https://github.com/es-shims/es5-shim) and ES6-Shim (https://github.com/es-shims/es6-shim).

### Transpiling

There's no way to polyfill new syntax that has been added to the language. The new syntax would throw an error in the old JS engine as unrecognized/invalid.

So the better option is to use a tool that converts your newer code into older code equivalents. This process is commonly called "transpiling," a term for transforming + compiling.

Essentially, your source code is authored in the new syntax form, but what you deploy to the browser is the transpiled code in old syntax form. You typically insert the transpiler into your build process, similar to your code linter or your minifier.

You might wonder why you'd go to the trouble to write new syntax only to have it transpiled away to older code -- why not just write the older code directly?

There are several important reasons you should care about transpiling:

* The new syntax added to the language is designed to make your code more readable and maintainable. The older equivalents are often much more convoluted. You should prefer writing newer and cleaner syntax, not only for yourself but for all other members of the development team.
* If you transpile only for older browsers, but serve the new syntax to the newest browsers, you get to take advantage of browser performance optimizations with the new syntax. This also lets browser makers have more real-world code to test their implementations and optimizations on.
* Using the new syntax earlier allows it to be tested more robustly in the real world, which provides earlier feedback to the JavaScript committee (TC39). If issues are found early enough, they can be changed/fixed before those language design mistakes become permanent.

Here's a quick example of transpiling. ES6 adds a feature called "default parameter values." It looks like this:

```js
function foo(a = 2) {
	console.log( a );
}

foo();		// 2
foo( 42 );	// 42
```

Simple, right? Helpful, too! But it's new syntax that's invalid in pre-ES6 engines. So what will a transpiler do with that code to make it run in older environments?

```js
function foo() {
	var a = arguments[0] !== (void 0) ? arguments[0] : 2;
	console.log( a );
}
```

As you can see, it checks to see if the `arguments[0]` value is `void 0` (aka `undefined`), and if so provides the `2` default value; otherwise, it assigns whatever was passed.

In addition to being able to now use the nicer syntax even in older browsers, looking at the transpiled code actually explains the intended behavior more clearly.

You may not have realized just from looking at the ES6 version that `undefined` is the only value that can't get explicitly passed in for a default-value parameter, but the transpiled code makes that much more clear.

The last important detail to emphasize about transpilers is that they should now be thought of as a standard part of the JS development ecosystem and process. JS is going to continue to evolve, much more quickly than before, so every few months new syntax and new features will be added.

If you use a transpiler by default, you'll always be able to make that switch to newer syntax whenever you find it useful, rather than always waiting for years for today's browsers to phase out.

There are quite a few great transpilers for you to choose from. Here are some good options at the time of this writing:

* Babel (https://babeljs.io) (formerly 6to5): Transpiles ES6+ into ES5
* Traceur (https://github.com/google/traceur-compiler): Transpiles ES6, ES7, and beyond into ES5

## Non-JavaScript

So far, the only things we've covered are in the JS language itself. The reality is that most JS is written to run in and interact with environments like browsers. A good chunk of the stuff that you write in your code is, strictly speaking, not directly controlled by JavaScript. That probably sounds a little strange.

The most common non-JavaScript JavaScript you'll encounter is the DOM API. For example:

```js
var el = document.getElementById( "foo" );
```

The `document` variable exists as a global variable when your code is running in a browser. It's not provided by the JS engine, nor is it particularly controlled by the JavaScript specification. It takes the form of something that looks an awful lot like a normal JS `object`, but it's not really exactly that. It's a special `object,` often called a "host object."

Moreover, the `getElementById(..)` method on `document` looks like a normal JS function, but it's just a thinly exposed interface to a built-in method provided by the DOM from your browser. In some (newer-generation) browsers, this layer may also be in JS, but traditionally the DOM and its behavior is implemented in something more like C/C++.

Another example is with input/output (I/O).

Everyone's favorite `alert(..)` pops up a message box in the user's browser window. `alert(..)` is provided to your JS program by the browser, not by the JS engine itself. The call you make sends the message to the browser internals and it handles drawing and displaying the message box.

The same goes with `console.log(..)`; your browser provides such mechanisms and hooks them up to the developer tools.

This book, and this whole series, focuses on JavaScript the language. That's why you don't see any substantial coverage of these non-JavaScript JavaScript mechanisms. Nevertheless, you need to be aware of them, as they'll be in every JS program you write!

## Review

The first step to learning JavaScript's flavor of programming is to get a basic understanding of its core mechanisms like values, types, function closures, `this`, and prototypes.

Of course, each of these topics deserves much greater coverage than you've seen here, but that's why they have chapters and books dedicated to them throughout the rest of this series. After you feel pretty comfortable with the concepts and code samples in this chapter, the rest of the series awaits you to really dig in and get to know the language deeply.

The final chapter of this book will briefly summarize each of the other titles in the series and the other concepts they cover besides what we've already explored.
