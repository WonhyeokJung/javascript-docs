# Frontend 코드 기록

## 목차

1. [기재된 기술](#기재된-기술)
2. [CSS](#CSS)
   1. [Selector](#Selector)
   2. [CSS Property](#CSS-Property)
3. [JavaScript](#JavaScript)

## 기재된 기술

<img src="https://img.shields.io/badge/-PHP-yellow?logo=PHP&logoColor=#777BB4"> <img src="https://img.shields.io/badge/-Laravel-critical?logo=LARAVEL&logoColor=white"> <img src="https://img.shields.io/badge/-Bootstrap-blueviolet?logo=Bootstrap&logoColor=white"> <img src="https://img.shields.io/badge/-jQuery-important?logo=jQuery&logoColor=white"> <img src="https://img.shields.io/badge/-JavaScript-green?logo=JavaScript&logoColor=white"> <img src="https://img.shields.io/badge/-HTML5-blue?logo=HTML5&logoColor=white"> <a href="https://developer.mozilla.org/ko/docs/Learn/Getting_started_with_the_web/CSS_basics"><img src="https://img.shields.io/badge/-CSS3-gray?logo=CSS3&logoColor=white"></a> <img src="https://img.shields.io/badge/-Python-white?logo=Python&logoColor=blue"> <img src="https://img.shields.io/badge/-Vue.js-red?logo=Vue.js">

## HTML

### Escape Sequence

HTML 상에서는 특수문자가 제대로 나타나지 않는 경우가 있다. 그런 경우를 대비하여 이스케이프 문자를 제공한다.

| 표현 문자 | 숫자 표현   | 문자 표현 | 설명          |
| --------- | ----------- | --------- | ------------- |
| -         | `&#00;-&#08;` | -         | 사용하지 않음 |
| space     | `&#09;`       | -         | 수평탭        |
| space | `&#10;` | - | 줄 삽입 |
| - | `&#11;-&#31;` | - | 사용하지 않음 |
| space | `&#32;` | - | 여백 |
| ! | `&#33;` | - | 느낌표 |
| " | `&#34;` | &quot; | 따옴표 |
| # | `&#35;` | - | 숫자기호 |
| $ | `&#36;` | - | 달러 |
| % | `&#37;` | - | 백분율 기호 |
| & | `&#38;` | &amp; | Ampersand |
| ' | `&#39;` | - | 작은 따옴표 |
| ( | `&#40;` | - | 왼쪽 괄호 |
| ) | `&#41;` | - | 오른쪽 괄호 |
| * | `&#42;` | - | 아스트릭 |
| + | `&#43;` | - | 더하기 기호 |
| , | `&#44;` | - | 쉼표 |
| - | `&#45;` | - | Hyphen |
| . | `&#46;` | - | 마침표 |
| / | `&#47;` | - | Solidus (slash) |
| 0 - 9 | `&#48;-&#57;` | - | 0부터 9까지 |
| : | `&#58;` | - | 콜론 |
| ; | `&#59;` | - | 세미콜론 |
| < | `&#60;` | &lt; | 보다 작은 |
| = | `&#61;` | - | 등호 |
| > | `&#62;` | &gt; | 보다 큰 |
| ? | `&#63;` | - | 물음표 |
| @ | `&#64;` | - | Commercial at |
| A - Z | `&#65;-&#90;` | - | A부터 Z까지 |
| [ | `&#91;` | - | 왼쪽 대괄호 |
| \ | `&#92;` | - | 역슬래쉬 |
| ] | `&#93;` | - | 오른쪽 대괄호 |
| ^ | `&#94;` | - | 탈자부호 |
| _ | `&#95;` | - | 수평선 |
| ` | `&#96;` | - | Acute accent |
| a - z | `&#97;-&#122;` | - | a부터 z까지 |
| { | `&#123;` | - | 왼쪽 중괄호 |
| \| | `&#124;` | - | 수직선 |
| } | `&#125;` | - | 오른쪽 중괄호 |
| ~ | `&#126;` | - | 꼬리표 |
| - | `&#127;-&#159;` | - | 사용하지 않음 |
|  | `&#160;` | &nbsp; | Non-breaking space |
| ¡ | `&#161;` | &iexcl; | 거꾸로된 느낌표 |
| ￠ | `&#162;` | &cent; | 센트 기호 |
| ￡ | `&#163;` | &pound; | 파운드 |
| ¤ | `&#164;` | &curren; | 현재 환율 |
| ￥ | `&#165;` | &yen; | 엔 |
| \| | `&#166;` | &brvbar; | 끊어진 수직선 |
| § | `&#167;` | &sect; | 섹션 기호 |
| ¨ | `&#168;` | &uml; | 움라우트 |
| ⓒ | `&#169;` | &copy; | 저작권 |
| ª | `&#170;` | &ordf; | Feminine ordinal |
| ≪ | `&#171;` | &laquo; | 왼쪽 꺾인 괄호 |
| ￢ | `&#172;` | &not; | 부정 |
| ­ | `&#173;` | &shy; | Soft hyphen |
| ? | `&#174;` | &reg; | 등록상표 |
| &hibar; | `&#175;` | &macr; | Macron accent |
| ° | `&#176;` | &deg; | Degree sign |
| ± | `&#177;` | &plusmn; | Plus or minus |
| ² | `&#178;` | &sup2; | Superscript two |
| ³ | `&#179;` | &sup3; | Superscript three |
| ´ | `&#180;` | &acute; | Acute accent |
| μ | `&#181;` | &micro; | Micro sign (Mu) |
| ¶ | `&#182;` | &para; | 문단기호 |
| · | `&#183;` | &middot; | Middle dot |
| ¸ | `&#184;` | &cedil; | Cedilla |
| ¹ | `&#185;` | &sup1; | Superscript one |
| º | `&#186;` | &ordm; | Masculine ordinal |
| ≫ | `&#187;` | &raquo; | 오른쪽 꺾인 괄호 |
| ¼ | `&#188;` | &frac14; | 4분의 1 |
| ½ | `&#189;` | &frac12; | 2분의 1 |
| ¾ | `&#190;` | &frac34; | 4분의 3 |
| ¿ | `&#191;` | &iquest; | 거꾸로된 물음표 |
| A | `&#192;` | &Agrave; | Capital A, grave accent |
| A | `&#193;` | &Aacute; | Capital A, acute accent |
| A | `&#194;` | &Acirc; | Capital A, circumflex accent |
| A | `&#195;` | &Atilde; | Capital A, tilde |
| A | `&#196;` | &Auml; | Capital A, dieresis or umlaut mark |
| A | `&#197;` | &Aring; | Capital A, ring (Angstrom) |
| Æ | `&#198;` | &AElig; | Capital AE diphthong (ligature) |
| C | `&#199;` | &Ccedil; | Capital C, cedilla |
| E | `&#200;` | &Egrave; | Capital E, grave accent |
| E | `&#201;` | &Eacute; | Capital E, acute accent |
| E | `&#202;` | &Ecirc; | Capital E, circumflex accent |
| E | `&#203;` | &Euml; | Capital E, dieresis or umlaut mark |
| I | `&#204;` | &Igrave; | Capital I, grave accent |
| I | `&#205;` | &Iacute; | Capital I, acute accent |
| I | `&#206;` | &Icirc; | Capital I, circumflex accent |
| I | `&#207;` | &Iuml; | Capital I, dieresis or umlaut mark |
| Ð | `&#208;` | &ETH; | Capital Eth, Icelandic |
| N | `&#209;` | &Ntilde; | Capital N, tilde |
| O | `&#210;` | &Ograve; | Capital O, grave accent |
| O | `&#211;` | &Oacute; | Capital O, acute accent |
| O | `&#212;` | &Ocirc; | Capital O, circumflex accent |
| O | `&#213;` | &Otilde; | Capital O, tilde |
| O | `&#214;` | &Ouml; | Capital O, dieresis or umlaut mark |
| × | `&#215;` | &times; | Multiply sign |
| Ø | `&#216;` | &Oslash; | width="130"Capital O, slash |
| U | `&#217;` | &Ugrave; | Capital U, grave accent |
| U | `&#218;` | &Uacute; | Capital U, acute accent |
| U | `&#219;` | &Ucirc; | Capital U, circumflex accent |
| U | `&#220;` | &Uuml; | Capital U, dieresis or umlaut mark |
| Y | `&#221;` | &Yacute; | Capital Y, acute accent |
| Þ | `&#222;` | &THORN; | Capital Thorn, Icelandic |
| ß | `&#223;` | &szlig; | Small sharp s, German (sz ligature) |
| a | `&#224;` | &agrave; | Small a, grave accent |
| a | `&#225;` | &aacute; | Small a, acute accent |
| a | `&#226;` | &acirc; | Small a, circumflex accent |
| a | `&#227;` | &atilde; | Small a, tilde |
| a | `&#228;` | &auml; | Small a, dieresis or umlaut mark |
| a | `&#229;` | &aring; | Small a, ring |
| æ | `&#230;` | &aelig; | Small ae diphthong (ligature) |
| c | `&#231;` | &ccedil; | Small c, cedilla |
| e | `&#232;` | &egrave; | Small e, grave accent |
| e | `&#233;` | &eacute; | Small e, acute accent |
| e | `&#234;` | &ecirc; | Small e, circumflex accent |
| e | `&#235;` | &euml; | Small e, dieresis or umlaut mark |
| i | `&#236;` | &igrave; | Small i, grave accent |
| i | `&#237;` | &iacute; | Small i, acute accent |
| i | `&#238;` | &icirc; | Small i, circumflex accent |
| i | `&#239;` | &iuml; | Small i, dieresis or umlaut mark |
| ð | `&#240;` | &eth; | Small eth, Icelandic |
| n | `&#241;` | &ntilde; | Small n, tilde |
| o | `&#242;` | &ograve; | Small o, grave accent |
| o | `&#243;` | &oacute; | Small o, acute accent |
| o | `&#244;` | &ocirc; | Small o, circumflex accent |
| o | `&#245;` | &otilde; | Small o, tilde |
| o | `&#246;` | &ouml; | Small o, dieresis or umlaut mark |
| ÷ | `&#247;` | &divide; | Division sign |
| ø | `&#248;` | &oslash; | Small o, slash |
| u | `&#249;` | &ugrave; | Small u, grave accent |
| u | `&#250;` | &uacute; | Small u, acute accent |
| u | `&#251;` | &ucirc; | Small u, circumflex accent |
| u | `&#252;` | &uuml; | Small u, dieresis or umlaut mark |
| y | `&#253;` | &yacute; | Small y, acute accent |
| þ | `&#254;` | &thorn; | Small thorn, Icelandic |
| y | `&#255;` | &yuml; | Small y, dieresis or umlaut mark |

참고 : https://mateam.net/html-escape-characters/

## CSS

### Selector

#### 선택자란?

```css
p {color: red; padding: 5px;}
Selector {Declaration (property: property-value);} <- Declaration block
```

#### 종류

| 선택자명                         | 선언방식       | 내용                                                  |
| -------------------------------- | -------------- | ----------------------------------------------------- |
| 전체 선택자(Universal Selector)  | * { }          | HTML 페이지 내부의 모든 태그                          |
| 태그 선택자(Type Selector)       | tag { }        | 태그명 선택                                           |
| 클래스 선택자(Class Selector)    | .className { } | .클래스명 / 중복 사용에 주로 이용. 글자색, 굵기 등    |
| 아이디 선택자(ID Selector)       | #id { }        | #아이디 / 요소 배치에 주로 이용                       |
| 복합 선택자(Combinator)          | E F            | 하위 선택자. 모든 F 요소                              |
|                                  | E > F          | 하위 선택자. 바로 아래 자식 F.                        |
| 형제 선택자(Sibling Combinators) | E+F            | 인접 형제 선택자. 같은 레벨 중 E 바로 다음에 오는 F만 |
|                                  | E-F            | 일반 형제 선택자. E 다음의 모든 동생 F.               |
|                                  |                |                                                       |
### CSS Property
#### Css Property style 적용 순서

**참고** [*CSS Triggers*](https://csstriggers.com/)

1. Styles

   - 브라우저가 객체에 적용할 스타일의 값을 계산, 재계산

2. Layout

   - 브라우저가 객체의 모양과 위치를 생성

   |             |             |                |              |
   | ----------- | ----------- | -------------- | ------------ |
   | position    | display     | overflow       | overflow-y   |
   | width       | height      | min-width      | min-height   |
   | padding     | margin      | border         | border-width |
   | top         | bottom      | left           | right        |
   | font        | font-family | font-size      | font-weight  |
   | white-space | line-height | vertical-align | float        |
   | clear       |             |                |              |

3. Paint

   - 브라우저가 객체 영역의 픽셀들을 채움

   |                  |                     |                   |                 |
   | ---------------- | ------------------- | ----------------- | --------------- |
   | color            | background          | visibility        | text-decoration |
   | background-image | background-position | background-repeat | background-size |
   | outline          | outline-color       | outline-style     | outline-width   |
   | border-radius    | border-style        | box-shadow        |                 |

4. Composite

   - 브라우저가 레이어(z-index)순서대로 객체를 화면에 그림

   |           |         |
   | --------- | ------- |
   | transform | opacity |

   

#### CSS Property 기술 추천 순서

1. Mozilla 제안 순서

   ```markdown
   1. display
   2. list-style
   3. position
   4. float
   5. clear
   6. width / height
   7. padding / margin
   8. border / background
   9. color / font
   10. text-decoration
   11. text-align / vertical-align
   12. white-space
   13. other text
   14. content
   ```

2. Naver

   ```markdown
   1. display
   2. overflow
   3. float
   4. position
   5. width / height
   6. padding / margin
   7. border
   8. background
   9. color/font
   10. animation
   ```



#### 기타 참고 사항

##### Transition 성능 향상

- Css Property style 적용 순서에 따르면, 'Layout' 속성을 바꾸면 'Paint', 'Composite' 순서를 거치기 때문에 **Reflow**성능 저하가 일어나고, 'Paint' 속성을 바꿀 경우 'Composite' 순서를 거치기 때문에 **Repaint** 성능 저하가 일어난다.
- 따라서 성능을 최대한 발휘하기 위해선, 'Composite' 속성만 변경하는 것이 최고이다.

**BAD**

```javascript
function prev() {
      position += 100;
      items.style.transition = 'left 0.3s ease-out';
      items.style.left = `${position}%`;
      curPos -= 1;

      if (curPos === 0) {
        isTransitionEnd = false;
      }
  }
```

**GOOD**

```javascript
function prev() {
      position += 100;
      items.style.transition = 'transform 0.3s ease-out';
      items.style.transform = `${position}%`;
      curPos -= 1;

      if (curPos === 0) {
        isTransitionEnd = false;
      }
  }
```



## JavaScript

### Style Guide

#### Rules by identifier type

1. Package names
   - lowerCamelCase
2. File names
   - kebab-case
3. Class names
   - UpperCamelCase
4. Method names
   - lowerCamelCase
5. Enum names
   - UpperCamelCase
6. Constant names
   - CONSTANT_NAME ( all uppercase letters with words separated by underscores)
7. Non-constant field names(static or otherwise)
   - lowerCamelCase
8. Parameter names
   - lowerCamelCase
     **Exception**: When required by a third-party framework, parameter names may begin with a `$`. This exception does not apply to any other identifiers (e.g. local variables or properties).
9. Local variable names
   - lowerCamelCase

#### css의 kebab-case를 사용할 경우

- 다음과 같은 코드가 있다고 하자.

```html
<!-- data-index는 예외임에 유의 -->
<div data-index="1" style="z-index:1">
hi
</div>
<!-- 자바스크립트에서 이를 활용하고 싶다면 어떻게 할까? -->
```
```javascript
// kebab-case는 자바스크립트에서 camelCase로 대체된다.
/* Wrong */
div.dataset.dataIndex  // data-data-index를 반환
div.style.z-index = 2;
/* Right */
div.dataset.index  // data-index 반환
div.style.zIndex = 99;
```

### Escape sequences

| Escape sequence                                              | Unicode code point                                           |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| `\0`                                                         | null character (U+0000 NULL)                                 |
| `\'`                                                         | single quote (U+0027 APOSTROPHE)                             |
| `\"`                                                         | double quote (U+0022 QUOTATION MARK)                         |
| `\\`                                                         | backslash (U+005C REVERSE SOLIDUS)                           |
| `\n`                                                         | newline (U+000A LINE FEED; LF)                               |
| `\r`                                                         | carriage return (U+000D CARRIAGE RETURN; CR)                 |
| `\v`                                                         | vertical tab (U+000B LINE TABULATION)                        |
| `\t`                                                         | tab (U+0009 CHARACTER TABULATION)                            |
| `\b`                                                         | backspace (U+0008 BACKSPACE)                                 |
| `\f`                                                         | form feed (U+000C FORM FEED)                                 |
| `\uXXXX` …where `XXXX` is exactly 4 hex digits in the range `0000`–`FFFF`; e.g., `\u000A` is the same as `\n` (LINE FEED); `\u0021` is "`!`" | Unicode code point between `U+0000` and `U+FFFF` (the Unicode Basic Multilingual Plane) |
| `\u{X}`…`\u{XXXXXX}` …where `X`…`XXXXXX` is 1–6 hex digits in the range `0`–`10FFFF`; e.g., `\u{A}` is the same as `\n` (LINE FEED); `\u{21}` is "`!`" | Unicode code point between `U+0000` and `U+10FFFF` (the entirety of Unicode) |
| `\xXX` …where `XX` is exactly 2 hex digits in the range `00`–`FF`; e.g., `\x0A` is the same as `\n` (LINE FEED); `\x21` is "`!`" | Unicode code point between `U+0000` and `U+00FF` (the Basic Latin and Latin-1 Supplement blocks; equivalent to ISO-8859-1) |



### This

> This는 나를 호출한 객체를 부르는 객체이며, 함수를 호출한 방법에 의해 결정된다.

- JavaScript의 This는 기본적으로 전역객체(window)를 가리킨다.(호출한 객체가 없는 경우)

  ```javascript
  console.log(this); // window
  ```

- 함수 호출 시, this는 window를 가리킨다.

  ```javascript
  var foo = function () {
      console.log(this);
  }
  
  function foo2() {
      console.log(this);
  }
  foo(); // window
  foo2(); // window
  // window.foo();
  ```

- 메서드 호출시(객체의 프로퍼티로 호출), this는 객체를 가리킨다.(객체의 속성처럼 .있을 시, . 앞의 것)

  ```javascript
  var foo = function () {
      console.log(this);
  }
  
  var obj = {
      foo: foo
  };
  
  obj.foo(); // obj
  ```

- 단, 메서드의 내부함수는 전역객체(window)를 가리킨다.

  ```javascript
  var value = 1;
  var obj = {
      value: 100,
      foo: function() {
          console.log(this, this.value);  // obj, 100
          function bar() {
              console.log(this, this.value);  // window, 1
          }
          bar();
      }
  }
  obj.foo();
  ```

- 메서드의 내부함수와 같이, 콜백함수는 전역객체(window)를 가리킨다.

  ```javascript
  let person = {
      name: 'jane doe',
      age: 20,
      hello: function () {
          setTimeout(function () {
              console.log(this);  // window
              console.log(this.name);  // undefined
              console.log(this.age);  // undefined
          }, 1000);
      },
  }
  
  person.hello(); // undefined
  ```

- 내부함수가 전역 객체를 가리키는 것은 **설계상의 오류**이며, 이를 회피하는 방법은 보통 아래와 같다.

  ```javascript
  // 1. That 선언
  var value = 1;
  var obj = {
      value: 100,
      foo: function() {
          var that = this;  // this === obj
          console.log(this)  // obj
          console.log(this.value)  // 100
          function bar() {
              console.log(this, this.value)  // window, 1
              console.log(that, that.value)  // obj, 100
          }
          bar();
      }  // foo end
  }  // obj end
  
  // 2. Bind 이용
  let obj = {
      name: 'jane doe',
      age: 20,
      foo: function() {
          setTimeout(function () {
              console.log(this, this.name, this.age);
          }.bind(this), 1000); // bind로 this === obj를 binding한다.
      }
  }
  obj.foo();
  
  // 3. 화살표 함수 이용(상위 스코프의 this를 참조한다.)
  var obj = {
      name: 'jane doe',
      foo: () => {
          console.log(this);  // window
      },
      hello: function() {
          setTimeout(() => {
              console.log(this);
          }, 1000);  // 외부 scope인 hello의 this가 가리키는 obj === this
      },
  }
  
  obj.hello();
  ```

- Bind 호출시, 메서드 호출과 같이 this는 호출한 객체를 가리킨다.

  - 단, Bind는 **단 한번**만 적용된다.

  ```javascript
  function foo() {
      console.log(this);
  }
  var obj = {
      name: 'jane doe'
  }
  var obj2 = {
      name: 'john doe'
  }
  
  var bar = foo.bind(obj);
  bar(); // obj
  var bar2 = bar.bind(obj2);
  bar2(); // obj, 한번만 적용되므로 obj2는 무시됨. 즉, 이중 바인드는 불가능하다.
  ```
  
- ES6에 새로 추가된 화살표 함수는 **자신을 포함하고 있는 외부 Scope**에서 This를 계승받는다.

  - 따라서, 화살표 함수는 **객체의 메서드 선언시** 사용하면 오류가 발생할 수 있어 **사용하지 않는다**.
  ```javascript
  var obj = {
    name: 'jane doe',
    foo: () => {
        console.log(this);  // window
    },
    hello: function() {
        setTimeout(() => {
            console.log(this);
        }, 1000);  // 외부 scope인 hello의 this가 가리키는 obj === this
    },
  }
  obj.hello();
  
  // 오류의 발생
  let person = {
      name: 'john doe',
      age: 20,
      foo: () => {
          console.log(this.name);  // undefined, 기대했던 person.name이 아니다!
          console.log(this);  // window
      }
  }
  person.foo();
  ```

- addEventListener의 경우도 똑같이 적용되므로, 화살표 함수의 사용은 지양하는 것이 좋다.

  ```javascript
  let btn = document.querySelector('button');
  btn.addEventListener('click', function() {
  console.log(this);  // 클릭시, btn
  })
  btn.addEventListener('click', () => {
  console.log(this);  // 클릭시, window
  })
  ```

- Strict Mode(엄격모드)에서는 호출한 객체가 없을 경우, this를 window가 아닌 **undefined**로 간주한다.
  Class와 Strict Mode에서는 자동으로 적용됨에 유의한다.
  
  ```javascript
  'use strict';
  function printThis() {
      console.log(this);
  }
  printThis();  // ~~~window~~~, undefined
  ```
  
  

## PHP, Laravel & blade

### 문법

| 코드                                       | 상세내용                                                     |  Vue   |
| :----------------------------------------- | :----------------------------------------------------------- | :----: |
| @if  @elseif @endif                        | if문                                                         |        |
| @foreach                                   | for문                                                        |        |
| @forelse @empty @endforelse                | @if와 @foreach의 결합문                                      |        |
| @include & @require('.blade.php의 파일명') | 코드를 불러와 적용시킨다.<br />include는 Error가 발생해도 코드를 실행하지만, require은 Fatal error를 일으켜 코드를 실행하지 않는다. |        |
| @extends                                   | 상속 / 상속한 위치에서 상속한 컴포넌트를 전체 출력한다.      | Props? |
| @section @endsection                       | 섹션 생성. @yield와 같이 쓰여 섹션 내용을 출력한다.          | $emit  |
| @yield                                     | 섹션을 출력할 때 사용하며, 보통 하위 컴포넌트에서 @section을 선언하고 @extends되는 상위 컴포넌트에 @yield를 사용하여 자식 컴포넌트를 부모 컴포넌트에 적용한다. | $emit  |
| @show                                      | section을 자식에게 상속하고 싶을 때 사용(@section @show) / 자식은 @parent 키워드로 불러온다. |        |
| @stack<br />@push                          | 별도의 css나 script 혹은 컨텐츠를 추가할 때 사용한다.<br />@push @endpush 내에 정의된 것을 불러오며, Section과 다른 점은 **하나의 뷰에 여러번 호출이 가능하다 **는 점이다. |        |

#### Route / Controller / View

1. Route
   - Define URL & connect Controller and View
   - `Route::<HTTP Methods>('/subpath/{Variable routing}', 'Closure Function/Controller@specific method') -> name('naming')`
2. Controller
   - Get data from Database & send to Template
   - Route list : `php artisan route:list`
   - 

#### compact()

- 개별 변수들을 가지고 하나의 배열을 생성하는 PHP 함수

  ```php
  $city  = 'San Francisco';
  $state = 'CA';
  $event = 'SIGGRAPH';
  
  $location_vars = ['city', 'state'];
  
  $result = compact('event', $location_vars);
  print_r($result);
  /*
  	Array
  	(
  		[event] => SIGGRAPH
  		[city] => San Francisco
  		[state] => CA
  	)
  */
  ```

  

## jQuery

- stop()의 사용 이유
  - 이벤트 버블링 방지 위함.
  - 애니메이션 등의 동작을 중지시킴.
  - 하나의 로직 내에서 두 번의 Stop이 실행되면 다른 animation을 중지시킬 수 있는 위험성이 있음.





## Git

### Semantic Commit Messages

- `feat`: (new feature for the user, not a new feature for build script)
  - `example`: [feat] ISSUE-001: add slider
- `fix`: (bug fix for the user, not a fix to a build script)
- `docs`: (changes to the documentation)
- `style`: (formatting, missing semi colons, etc; no production code change)
- `refactor`: (refactoring production code, eg. renaming a variable)
- `test`: (adding missing tests, refactoring tests; no production code change)
- `chore`: (updating grunt tasks etc; no production code change)



## Vue

### Re-rendering 방지

```vue
<template>
	<keep-alive>
    <!-- 선택 컴포넌트 바인딩 -->
  	<component :something="something" /></component>
  </keep-alive>
</template>
```

This is the general documentation for vue 3 slots: [vuejs.org/guide/components/slots.html](https://vuejs.org/guide/components/slots.html) and the render function documentation contains a bit about using slots as well [vuejs.org/guide/extras/render-function.html#rendering-slots](https://vuejs.org/guide/extras/render-function.html#rendering-slots) 



## 용어 정리

### JavaScript / Vue

- 논리(Logic) : 하나의 논리, 혹은 기능을 구성하는 단위로 보통 하나의 기능을 수행하는 함수를 지칭하는 경우가 많다.(func calculator() === Logic)
  ```javascript
  // 하나의 logic
  function calculator(num1: number | string, num2: number | string): void { ... }
  ```

  

- 매개변수(Parameter): 함수가 실행 시 전달받는 변수들이다.
  ```javascript
  function calculator(num1: number | string, num2): void { ... } // num1, num2 === Parameters
  ```

  

- 인자, 인수(Arguments): 함수 실행문에서 전달하는 매개변수.
  ```javascript
  calculator(1, 2) // 1, 2 === Arguments
  ```

- 컴포넌트(Component):  Vue Class로 생상된 하나의 Vue 객체 / createApp, app.component 등도 마찬가지로 컴포넌트를 생성한다.
  ```javascript
  new Vue({
    ...
  })
  ```

- 인스턴스(Instance): 보통 정의된 Class를 new로 생성한 것을 인스턴스라 하는데, 따라서 위처럼 생성된 Vue Component를 컴포넌트 인스턴스라고 부르기도 한다. 전역 / 지역에 따로 등록하여 사용도 가능하다.

  > vuejs.org의 Component Registration 참조

  ```javascript
  // 전역(global) 예시. main.js
  import { createApp } from 'vue'
  import App from './App.vue' // component instance
  createApp(App).mount('#app')
  ```

  ```javascript
  // 지역(local) 예시
  import { MyComponent } from 'COMPONENT_PATH/MyComponent.vue'
  export default {
    components: { MyComponent }
  }
  ```

- 구조 분해(Destructuring): 자바스크립트와 밀접한 개념으로,
  ```javascript
  // Obj 구조 분해 할당
  const x = {
    lastName: 'kim',
    firstName: 'amoogae'
  }
  
  let { lastName, firstName } = x
  ```

  ```vue
  <!-- vue 내부에선 directive 등에 사용이 가능하다. -->
  <Component v-slot:default="{ lastName, firstName }"></Component>
  ```

- 함수(Function)과 메서드(Methods): 메서드는 호출할 때 앞에 마침표(.)가 붙는다. 메서드는 클래스, 혹은 객체에 속해 있는 함수로 독립적이지 못하고 해당 객체/클래스에 종속적이다.
  ```javascript
  let foo = {
    getName: function (n) {
      const name = n ? n : 'kim';
      return name;
    }
  }
  foo.getName() // methods
  
  function bar() {
    
  }
  ```

  

## 추천사이트

https://learn.shayhowe.com/html-css/

VSCode 기본 설정

https://gwonsungjun.github.io/articles/2018-06/vscodeSetting