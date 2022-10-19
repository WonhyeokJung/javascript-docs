# Frontend 코드 기록

## 목차

1. [기재된 기술](#기재된-기술)
2. [CSS](#CSS)
   1. [Selector](#Selector)
   2. [CSS Property](#CSS-Property)
3. [JavaScript](#JavaScript)

## 기재된 기술

<img src="https://img.shields.io/badge/-PHP-yellow?logo=PHP&logoColor=#777BB4"> <img src="https://img.shields.io/badge/-Laravel-critical?logo=LARAVEL&logoColor=white"> <img src="https://img.shields.io/badge/-Bootstrap-blueviolet?logo=Bootstrap&logoColor=white"> <img src="https://img.shields.io/badge/-jQuery-important?logo=jQuery&logoColor=white"> <img src="https://img.shields.io/badge/-JavaScript-green?logo=JavaScript&logoColor=white"> <img src="https://img.shields.io/badge/-HTML5-blue?logo=HTML5&logoColor=white"> <a href="https://developer.mozilla.org/ko/docs/Learn/Getting_started_with_the_web/CSS_basics"><img src="https://img.shields.io/badge/-CSS3-gray?logo=CSS3&logoColor=white"></a> <img src="https://img.shields.io/badge/-Python-white?logo=Python&logoColor=blue"> <img src="https://img.shields.io/badge/-Vue.js-red?logo=Vue.js">

## Markdown

### Style Guide

>  https://arcticicestudio.github.io/styleguide-markdown/rules/

1. File Naming: kebab-case

### Link와 띄어쓰기

Link의 경우 기본적으로 이렇게 연결한다.
```markdown
## 목차
1. [목차](#목차)
2. [안녕하세요? 반갑습니다.](#안녕하세요?)
## 안녕하세요? 반갑습니다.
- 이하 [주소](https://www.google.com)를 참조하세요.
```

하지만 `안녕하세요? 반갑습니다`처럼 띄어쓰기가 있는 경우, 깃허브 README.md에서 정상적으로 작동하지 않는다. 띄어쓰기의 경우는 `%20` 혹은 `-`으로 표시해주어야 정상작동한다.
**목차 등의 link에선 `-`(dash)의 경우가 대체로 오류가 없음**

### 이미지 주소의 경우

이미지 같은 경우 기본적으로 이와 같이 작성한다.
```markdown
- bad
![devToolsEx3](./README.assets/devToolsEx3.png)
```

하지만 위 예시처럼 현재 경로(`.\`)를 표시하는 경우, 깃허브에선 이미지를 인식하지 못한다. 현재 경로를 작성하지 않는 경우 마크다운, 깃허브 양쪽에서 정상 인식하므로 현재 경로 표시는 회피하도록 하자.
```markdown
- good
![devToolsEx3](README.assets/devToolsEx3.png)
```



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

### Safari

애플의 웹 브라우저 사파리는 대단한 완성도를 자랑하는데 덕분에 크롬에서는 잘 실행되는 여러 css가 사파리에선 제대로 적용되지 않는 경우가 매우 자주 생긴다. 그를 대비해서 사파리에서만 일어나는 온갖 버그를 이곳에 정리한다.

가장 좋은 해결책은 크롬을 쓰게 유도하는 것이고 사파리는 폐기해버리는 것임을 항상 유의하자.

#### will-change와 filter: drop-shadow()

폰트어썸의 아이콘을 이용할 경우 기존에는 아래와 같은 방법으로 아이콘 뒤에 그림자를 줄 수 있었다.

```css
.fas-bookmark {
  color: orange;
  text-shadow: rgb(241, 157, 199) 1px 0 10px;
}
```

하지만 Vue3 / Nuxt3를 활용하거나, 최신 폰트어썸을 활용하면 `text-shadow`를 인식하지 않아 아래와 같은 방식으로 다르게 작성해야 한다.

```css
.fa-heart:hover {
  -webkit-filter: drop-shadow(rgb(209, 48, 48) 0px 0 0.5rem);
  	filter: drop-shadow(rgb(209, 48, 48) 0px 0 0.5rem);
}
```

위와 같은 경우엔 문제가 발생하지 않지만, 화면이 렌더링 된 후 코드에 의해 화면의 크기가 변경되는 경우 사파리에선 하나의 문제가 발생한다.

다음과 같은 코드를 작성했다고 가정하자.

```css
  .fa-heart:hover {
    color: rgba(237, 119, 102, 1);
    -webkit-filter: drop-shadow(rgb(209, 48, 48) 0px 0 0.5rem);
      filter: drop-shadow(rgb(209,48,48) 0px 0 0.5rem);
    -webkit-transform: scale(1.125, 1.125);
      transform: scale(1.125, 1.125);
    -webkit-transition: -webkit-transfrom .5s;
      transition: transform .5s;
  }
```

사파리에서 실행하면 어떻게 될까?

<img src="./assets/css-safari-will-change1.png" alt="css-safari-will-change1" style="zoom: 67%;" />

이처럼 `drop-shadow`에서 리사이징이 일어나 모자이크처럼 네모난 테두리가 생기며 쉐도우가 짤리게 된다.

이런 경우 활용할 수 있는 것이 `will-change` Property이다. `will-change`프로퍼티는 브라우저에게 어떤 요소(element)를 변경할 지 힌트를 주는 역할을 하는데,

```css
.fa-heart:hover {
  /* ... */
  will-change:filter;
}
```

위처럼 `filter`에서 사이즈 변경을 하도록 지정해주면 사파리에서도 위와 같은 문제 없이 잘 사용할 수 있다.

다만 `filter`는 치명적인 단점이 있는데 성능을 크게 저하시킬 수 있다는 문제점이 있다는 것이다. 따라서 많은 곳에 남발하는 것은 금물이고, 더이상 필요없는 경우 JavaScript 등을 이용하여 제거해 주는 것이 좋다.

```javascript
document.querySeletor('.fa-heart').style.willChange = 'auto';
function removeHint() {
  this.style.willChange = 'auto';
}
```

항상 정답은 사파리 사용을 막고 크롬을 사용하게 하는 것임을 명심하자.



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

   

#### CSS Property 기술 추천 순서(Properties Order Convention)



1. 기본 가이드
   1. **Layout Properties** (position, float, clear, display, box-sizing)
   2. **Box Model Properties** (width, height, margin, padding,)
   3. **Visual Properties** (color, background, border, box-shadow, box-color)
   4. **Typography Properties** (font-size, font-family, text-align, text-transform)
   5. **Misc Properties** (cursor, overflow, z-index)

2. 예제
   ```css
   el {
     display: ;
     list-style: ;
     float: ;
     position: ;
     clear: ;
     box-sizing: ;
     
     width: ;
     min-width: ;
     max-width: ;
     height: ;
     
     margin: ;
     margin-top: ;
     margin-right: ;
     margin-bottom: ;
     margin-left: ;
     
     padding: ;
     
     border: ;
     border-radius: ;
     box-color: ;
     box-shadow: ;
     background: ;
     
     color: ;
     font: ;
     font-family: ;
     font-size: ;
     line-height: ;
     font-weight: ;
     text-indent: ;
     text-transform: ;
     text-decoration: ;
     letter-spacing: ;
     word-spacing: ;
     white-space: ;
     text-align: ;
     vertical-align: ;
     
     overflow: ;
     cursor: ;
     z-index: ;
     transition: ;
     animation: ;
   }
   ```

3. Mozilla 제안 순서
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

4. Naver
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

### 가운데 정중앙 정렬

```css
div {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

### @media query의 선언 방법

미디어 쿼리는 디바이스 / 화면 크기 등에 따라 여러 가지 옵션을 줄 수 있는 등 CSS에서 자주 사용하는 요소이나 CSS에서 적용 순서 등에 민감하게 반응하여 제대로 적용되지 않는 경우가 잦다. 그를 대비해서 적용 순서/방법을 기재하고자 한다.

800px의 화면에 무언가를 적용해보자고 가정하자.

```css
@media screen and (max-width: 800px) {
  .foo {
    display: none;
  }
}
```

만약에 이미 작성된 프로퍼티를 오버라이딩 하고 싶다면 이렇게 할 수 있다.

```css
@media screen and (max-width: 800px) {
  .foo {
    display: none !important;
  }
}
```

하지만 알다시피 `!important`를 남발하는 것은 CSS 설계에 치명적인 영향을 줄 수 있어 다른 방식을 사용하는 것이 좋다. 다른 방식은 아래와 같다.

1. 클래스명 중복 사용
   ```css
   @media screen and (max-width: 800px) {
     /* class foo && class foo */
     .foo.foo {
       display: none;
     }
   }
   ```

2. CSS는 탑 다운 방식으로 코드를 읽는다.
   위에서부터 아래로 읽어 가므로, 아래의 것을 우선적용한다.(즉, 중첩시엔 가장 마지막 것을 읽는다.)

   ```css
   /* bad */
   @media screen and (max-width: 800px) {
     .foo {
       display: none;
     }
   }
   .foo {
     display: block;
   }
   ```

   ```css
   /* good */
   .foo {
     display: block;
   }
   @media screen and (max-width: 800px) {
     .foo {
       display: none;
     }
   }
   ```

   그러므로, 모바일 이외의 기기 등에서 `min-width` 등을 이용한 최솟값을 주지 않고 `max-width`로만 범위를 구분 짓고자 할 경우 이렇게 할 수 있다.

   ```css
   @media only screen and (max-width: 960px) {
     
   }
   @media only screen and (max-width: 768px) {
     
   }
   @media only screen and (max-width: 640px) {
     
   }
   ```

   반대의 경우는 역순으로 올라가야 한다.(최솟값을 기준으로 하니까!)

   ```css
   @media only screen and (min-width: 320px) {}
   @media only screen and (min-width: 480px) {}
   @media only screen and (min-width: 640px) {}
   ```

   물론 둘을 동시에 줘서 범위를 주는 것도 현명하다.

   ```css
   @media only screen and (max-width: 320px) {}
   @media only screen and (min-width: 320px) and (max-width: 480px) {}
   @media only screen and (min-width: 480px) and (max-width: 640px) {}
   /* ... */
   @media only screen and (min-width: 960px) {}
   ```

   

3. 중첩된 CSS 선택자의 사용시 그 이상 중첩하여 선언한다.
   1번과 유사한 경우인데, 2개 이상의 선택자(Selectors)를 이용하여 CSS를 주었을 때, 그 수 이상을 중첩해서 CSS 선택자를 주어야 정상적으로 중첩한다.

   ```css
   .container .foo {
     display: block;
   }
   @media screen and (max-width: 800px) {
     .container .foo {
       display: none;
     }
     /* or */
     body .container .foo {
       display: none;
     }
   }
   ```

   

## JavaScript

### Style Guide

> https://github.com/arcticicestudio/styleguide-javascript

#### Rules by identifier type

1. Package names
   - lowerCamelCase
2. File names
   - kebab-case
3. Class names
   - UpperCamelCase
4. Method names
   - lowerCamelCase
5. Enum names(상수값의 열거형)
   - UpperCamelCase(===PascalCase)
   
   - ```javascript
     const Season = {
       SPRING: 'spring',
       SUMMER: 'summer',
       AUTUMN: 'autumn',
       WINTER: 'winter'
     }
     
     Object.freeze(Season)  // 변경 방지
     ```
   
   - 
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
  

### Promise

#### 등장배경

기존의 콜백 패턴은 두 가지의 치명적인 단점을 갖고 있었다.

1. 콜백 지옥(Callback hell)

   ```typescript
   const get = (url:string, successCallback:Function, failure:Function) => {
     const xhr = new XMLHttpRequest();
     xhr.open('GET', url);
     xhr.send();
     
     xhr.onload = () => {
       if (xhr.status === 200) {
         successCallback(JSON.parse(xhr.response));
       }
     }
   }
   ```

   Rest API를 이용해서 데이터를 가져올 때, 비동기 함수를 이용하게 되므로 마찬가지로 태스크 큐에 들어가 있어 **처리 결과를 외부로 반환이 불가능**한데, 이 처리 결과를 보통 콜백 함수를 주어 처리하게 된다. 하지만 위의 GET 요청의 결과를 이용해 계속 GET 요청을 발생시키면 이와 같은 콜백 지옥이 발생하게 된다.

   ```javascript
   get(url, a => {
     get(url+`/${a}`, b => {
       get(url+`/${b}`, c => {
         console.log(c);
       })
     })
   })
   ```

   

2. 에러 처리의 어려움

   ```javascript
   try {
     setTimeout(() => { throw new Error('error!') }, 1000)
   } catch(e) {
     // 캐치가 불가능.
     console.error(e)
   }
   ```

   이와 같은 비동기 콜백패턴 에러 처리 방식이 있다고 가정하자. 위 로직에서 에러는 발생하지 않는다. 에러는 호출자(caller) 방향으로 전달되는데, setTimeout 내부의 함수는 setTimeout이 부르는 것이 아닌, **이벤트 루프에 의해서 태스크 큐에서 콜스택이 전부 빈 후 이동**하게 된다. 따라서, 에러가 발생했을 때 이미 setTimeout은 정상적으로 실행되어 코드에는 문제가 발생하지 않는다.

위와 같은 문제를 해결하기 위해 등장한 것이 바로, ES6의 Promise이다.

#### 개요

Promise는 ES6에서 도입된 **표준 빌트인 객체**이다.
Promise 생성자 함수는 비동기 처리를 수행할 콜백 함수를 인수로 전달 받는데, 이 콜백 함수는 `resolve`와 `reject`함수를 인수로 전달받는다.

```javascript
const promise = new Promise((resolve, reject) => {
  if (...) resolve('Hello world!');
  else reject('You cannot go');
})
```



```javascript
const condition = true;
const promise = new Promise((resolve, reject) => {
  if (condition) {
    resolve('성공');
  } else {
    reject('실패');
  }
});

promise
	.then((res) => {
  console.log(res);
})
	.catch((err) => {
  console.error(err);
})
	.finally(() => {
  console.log('무적권')
})

// result
// '성공'
// '무적권'
```

- 콜백함수 내부에서 비동기 처리를 수행한 후, 비동기 처리가 성공하면 `resolve`함수에 결과를 인수로 전달하여 호출하고, 실패하면 `reject`함수에 결과를 인수로 전달하여 호출하게 된다.
- new Promise는 바로 실행되지만, 결과값은 .then / .catch 메서드 실행시 받을 수 있다.
  즉, 실행은 즉시 하지만 결과값은 나중에 받는 객체이다.

#### 상태

반환하는 Promise에는 세가지 진행 상태가 있는데,각각  `pending`, `fulfilled`, `rejected`이다.

- `pending`: 기본 상태. 비동기 처리가 진행되지 않으면 계속 pending 상태를 유지한다.

- `settled`: fulfilled와 rejected는 settled 상태에 속하는데, pending이 아닌 비동기 처리가 수행된 상태를 의미하며, settled 상태가 된 경우 다른 상태로의 변경은 불가능하다.

  - `fulfilled`: 처리 성공. resolve 함수를 호출해 값을 반환하면 fulfilled 상태로 변경된다.

  - `rejected`: 처리 실패. reject 함수를 호출해 값을 반환하면 rejected 상태로 변경된다.

예제를 통해 결과를 봐보자.

```typescript
const fulfilled:Promise<any> = new Promise((resolve, reject) => resolve('성공'));
console.log(fulfilled); // Promise{ <fulfilled>: '성공' }
```

```typescript
const rejected:Promise<any> = new Promise((resolve, reject) => reject(new Error('Error occured')));
console.error(rejected); // Promise{ <rejected>: Error: error occurred }
```



#### 후속 처리(Prototype Methods)

앞에서 콜백 패턴이 콜백 함수로 후속 처리를 했던 것처럼, Promise도 Promise의 처리 결과를 사용하기 위해 후속 처리를 해야하는데, 이를 위해 후속 처리 메서드 `then`, `catch`, `finally`를 가지고 있다.

**Promise.prototype.then**

then 메서드는 두개의 콜백함수를 인수로 전달받고, 아래 두 개의 콜백함수는 인수로 Promise의 처리 결과를 전달받는다.

1. Promise가 fulfilled 상태(resolve 함수가 호출된 상태)가 된 경우 호출되는 첫번째 콜백 함수
2. Promise가 rejected 상태(reject 함수가 호출된 상태)가 된 경우 호출되는 두번째 콜백 함수

위 두 콜백함수는 **핸들러 함수**로, **비동기적으로 처리**되는 것에 유의한다.

```javascript
// fulfilled
// return Promise { <fulfilled>: undefined }
new Promise(resolve => resolve('fulfilled'))
	.then(res => console.log(res), err => console.log(err))

// Error: rejected
// return Promise { <fulfilled>: undefined }
new Promise((resolve, reject) => reject(new Error('rejected')))
	.then(res => console.log(res), err => console.error(err))
```

then 메서드는 언제나 **Promise를 반환**한다. then 메서드가 프로미스를 반환한 경우 그 값을 그대로, 아닌 경우 그 값을 암묵적으로 resolve 또는 reject하여 반환한다.

**Promise.prototype.catch**

catch 메서드는 한개의 콜백함수를 인수로 전달받고, 그 콜백함수는 Promise의 처리결과를 인수로 전달받는다. catch는 프로미스가 rejected 상태인 경우에만 작동한다.

```javascript
new Promise((_, reject) => reject(new Error('rejected')))
	.catch(err => console.error(err))
```

then메서드와 마찬가지로 언제든지 **프로미스를 반환**한다.

**Promise.prototype.finally**
finally 메서드는 fulfilled, rejected 결과와 상관없이 **무조건 한번 호출**되며, 한개의 콜백 함수를 인수로 전달받는다. 따라서, Promise 상태와 상관없이 공통적으로 수행해야 할 처리 내용이 있을 때 유용하다.
위 두 가지 메서드와 마찬가지로 항상 **프로미스를 반환**한다.

```javascript
fetch('https://jsonplaceholder.typicode.com/posts/1')
	.then(res => res.json())
	.then(res => console.log(res))
	.catch(err => console.error(err))
	.finally(() => console.log('finally it\'s done'))
```

#### 에러 처리

에러처리는 위에서 보았듯이 `.then`혹은 `.catch` 메서드에서 처리할 수 있지만, 기본적으로 `.catch` 메서드를 사용한다. `.then`의 두 번째 콜백 함수는 첫 번째 콜백 함수에서 발생한 에러를 캐치하지 못하기 때문이다.

```javascript
// Promise { <rejected>: TypeError: console.blah is not a function }
new Promise((resolve, reject) => resolve('hello world'))
	// console.blah 에러처리 불가능
	.then((res) => console.blah(res), err => console.error('에러발생'));
```

`.catch`를 `.then`메서드 이후 호출한 경우, `.then`내에서 발생한 에러도 전부 캐치할 수 있다.

```javascript
// 에러발생
// return Promise { <fulfilled>: undefined } console.log가 리턴되어 이값이 전달됨.
new Promise((resolve, reject) => resolve('hello world'))
	.then((res) => console.blah(res))
	.catch(err => console.error('에러발생'));
```



#### 프로미스 체이닝

위에서 설명했듯이, `.then / .catch / .finally` 후속 처리 메서드는 기본적으로 **프로미스를 반환**하고, 반환한 값이 프로미스가 아니더라도 암묵적으로 **settled된 프로미스 객체**로 변경하여 반환하기 때문에, 결과값을 다시 후속 처리하고 싶다면 이어서 `.then`을 사용하면 된다.

```javascript
promise
  .then((res) => {
    return new Promise((resolve, reject) => {
      resolve(res);
    });
  })
  .then((res2) => {
    console.log(res2); // res2 === resolve(res);
    return new Promise((resolve, reject) => {
      resolve(res2);
    });
  })
  .then((res3) => {
    console.log(res3); // res3 === resolve(res2);
  })
  .catch((err1) => {
    console.error('err1', err1);
  	return new Promise((resolve, reject) => {
      reject(err1);
    });
  })
	
```

콜백 지옥은 더이상 발생하지 않지만, 결국 **프로미스도 콜백 패턴을 사용**하므로 사실 가독성이 뛰어난 편은 아니다. 이 문제는 ES8에서 도입된 async/await를 통해 해결할 수 있다. 지금은 간단하게 예제만 살펴보자.

```javascript
function getUser(url) {
  return new Promise((resolve, reject) => {
    fetch(url)
    	.then(res => res.json())
    	.then(res => resolve(res))
    	.catch(err => reject(err))
    	.finally(() => console.log('finally it\'s done'));
  })
}

const url = 'https://jsonplaceholder.typicode.com';
(async () => {
  const { userId } = await getUser(`${url}/posts/30`);
  // 취득한 id 정보로 유저 검색
  const res = await getUser(`${url}/users/${userId}`);
  console.log(res);
})();
```

위처럼 필요한 정보를 변수에 할당하여 깔끔하게 볼 수 있다.

#### 정적 메서드(Static Methods)

주로 생성자 함수로 사용되는 Promise지만 **함수도 객체**이므로 메서드를 가질 수 있다. 메서드는 총 5가지가 있다. 이후 Promise.any[ES12(EcmaScript 2021)기준]가 추가되어 총 6가지로 늘었다.

**Promise.resolve**

인수로 전달받은 값을 래핑하여 resolve된 프로미스 객체로 생성하기 위해서 사용한다.

```javascript
function returnPromiseResolve() {
  return Promise.resolve({ name: 'abc' });
}

const foo = returnPromiseResolve();
console.log(foo); // Promise { <fulfilled> { name: 'abc' } }
foo.then(console.log); // { name: 'abc' }
```

아래의 예제와 동일하게 동작한다.

```javascript
function returnPromiseResolve() {
  return new Promise(resolve => resolve({ name: 'abc' }));
}
```

**Promise.reject**

인수로 전달받은 값을 래핑하여 reject된 프로미스 객체로 생성하기 위해서 사용한다.

```javascript
function returnPromiseReject() {
  return Promise.reject(new Error('경고, 경고'));
}

const foo = returnPromiseReject();
foo.catch(console.error); // Error: 경고, 경고
```

아래의 예제와 동일하게 동작한다.

```javascript
function returnPromiseReject() {
  return new Promise((_, reject) => reject(new Error('경고, 경고')));
}
```

**Promise.all**

```javascript
Promise.all(iterable);
```

여러 개의 비동기 처리를 병렬 처리할 때 사용한다. 아래의 예제를 보자.

```javascript
const req1 = () => new Promise(resolve => setTimeout(() => resolve(1), 3000));
const req2 = () => new Promise(resolve => setTimeout(() => resolve(2), 2000));
const req3 = () => new Promise(resolve => setTimeout(() => resolve(3), 1000));

const res = [];
req1()
	.then(r => {
  	res.push(r);
  	return req2();
	})
	.then(r => {
  	res.push(r);
  	return req3();
	})
	.then(r => {
  	res.push(r);
  	console.log(res); // 약 6초
	})
```

순차적으로 처리하기 때문에, 약 6초 정도가 걸린다. 하지만 위 세개의 비동기 처리는 서로 의존성이 없고 개별적으로 수행된다. 개별적으로 따로 `.then`을 사용할 수도 있겠지만 그럼 코드가 이유없이 길어지게 되므로 이럴 때 사용하는 것이 병렬 처리를 위한 Promise.all이다.

```javascript
Promise.all([req1(), req2(), req3()])
	.then(console.log) // 약 3초 소요
```

Promise를 요소로 갖는 배열 등의 이터러블을 인수로 받는다. **하나라도 reject가 되면 즉시 종료**(`.catch`실행)하며, **전부 fulfilled**가 된 경우 모든 처리 결과를 배열에 다시 담아 새로운 Promise를 반환한다.

```javascript
const promise1 = Promise.resolve('즉시 해결1');
const promise2 = Promise.resolve('즉시 해결2');
const promise3 = Promise.reject('즉시 거절');
Promise.all([promise1, promise2, promise3])
  .then((result) => {
    console.log(result); // promise3이 없었다면, ['즉시 해결1', '즉시 해결2']
  })
  .catch((error) => {
    console.error(error); // 즉시 거절 
  });
```

전달받은 이터러블의 요소가 프로미스가 아닌 경우, 암묵적으로 Promise.resolve 메서드를 통해 프로미스로 래핑한다.

```javascript
Promise.all([1,2,3]) // Promise { <fulfilled>: Array(3) };
	.then(res => console.log(res)) // [1, 2, 3], 리턴값은 Promise { <fulfilled>: undefined }
```

**Promise.race**

Promise.all과 다른 것은 동일하지만 **가장 먼저 settled(fulfilled/rejected)**상태가 된 프로미스의 처리 결과를 다시 resolve/reject하는 새로운 프로미스를 반환한다.

```javascript
const promise1 = Promise.resolve('즉시 해결1');
const promise2 = Promise.resolve('즉시 해결2');
const promise3 = Promise.reject('즉시 거절');
Promise.race([promise1, promise2, promise3]) // Promise { <fulfilled>: '즉시 해결' };
  .then((result) => {
    console.log(result); // '즉시 해결1'
  })
  .catch((error) => {
    console.error(error); 
  });
```

```javascript
const req1 = () => new Promise(resolve => setTimeout(() => resolve('즉시 해결1'), 3000));
const req2 = () => new Promise(resolve => setTimeout(() => resolve('즉시 해결2'), 2000));
const req3 = () => new Promise((resolve, reject) => setTimeout(() => reject(new Error('즉시 거절')), 1000));
Promise.race([req1(), req2(), req3()])
  .then(res => console.log(res))
  .catch(err => console.error(err)); // Error: 즉시 거절
```

**Promise.any**

`Promise.any`와 비슷하지만 가장 먼저 **fulfilled**된 프로미스를 반환한다. 프로미스가 아닌 객체를 인수로 전달한 경우, 동기적으로 fulfilled된 프라미스를 반환한다.

만약 모든 결과가 rejected된 경우 혹은 빈 iterable객체를 전달할 경우 **AggregateError 객체**(여러 개의 에러가 발생한 경우 하나의 에러로 치환하여 반환한다.)를 반환한다.

```javascript
// Promise 객체로 이루어진 배열
const req1 = () => new Promise(resolve => setTimeout(() => resolve('즉시 해결1'), 3000));
const req2 = () => new Promise(resolve => setTimeout(() => resolve('즉시 해결2'), 2000));
const req3 = () => new Promise((resolve, reject) => setTimeout(() => reject(new Error('즉시 거절')), 1000));
Promise.any([req1(), req2(), req3()])
	.then(res => console.log(res)) // 즉시 해결 2
	.catch(err => console.error(err));
```

```javascript
// Promise 객체가 아닌 값으로 이루어진 배열
Promise.any([1, 2, 3])
	.then(res => console.log(res)) // 1
	.catch(err => console.error(err));
```



```javascript
// Promise rejected 객체로 이루어진 배열
Promise.any([req3()])
  .then(res => console.log(res))
  .catch(err => console.error(err)); // [AggregateError: All promises were rejected]
```

```javascript
// 빈 iterable 객체
Promise.any([])
  .then(res => console.log(res))
  .catch(err => console.error(err)); // [AggregateError: All promises were rejected]
```

**Promise.allSettled**

Promise 객체를 담은 iterable 객체를 인수로 받아, **settled(fulfilled/rejected)**된 결과를 배열에 담아 전달한다. `Promise.all`과 달리 rejected가 발생하더라도 멈추지 않는다. 만약 Promise 객체가 아닌 값을 전달한다면 암묵적으로 resolve된 프로미스 객체를 반환한다.

- fulfilled: `{ status: fulfilled, value: ... }`
- rejected: `{ status: rejected, reason: ... }`

```javascript
Promise.allSettled([1, 2, 3])
  .then(res => console.log(res))
  .catch(err => console.error(err));
/**
	[
		{ status: 'fulfilled', value: 1 },
		{ status: 'fulfilled', value: 1 },
		{ status: 'fulfilled', value: 1 }
	]
*/
```

```javascript
const req1 = () => new Promise(resolve => setTimeout(() => resolve('즉시 해결1'), 3000));
const req2 = () => new Promise((resolve, reject) => setTimeout(() => resolve('즉시 해결2'), 2000));
const req3 = () => new Promise((resolve, reject) => setTimeout(() => reject(new Error('즉시 거절')), 1000));
Promise.allSettled([req1(), req2(), req3()])
  .then(res => console.log(res))
  .catch(err => console.error(err));
/**
  [
    { status: 'fulfilled', value: '즉시 해결1' },
    { status: 'fulfilled', value: '즉시 해결2' },
    {
      status: 'rejected',
      reason: Error: 즉시 거절
          at Timeout._onTimeout (./foo.js:3:77)
          at listOnTimeout (node:internal/timers:559:17)
          at processTimers (node:internal/timers:502:7)
    }
  ]
*/
```

빈 객체를 인수로 전달한 경우, 그대로 빈 객체를 반환한다.

```javascript
Promise.allSettled([])
	.then(res => console.log(res)) // []
	.catch(err => console.error(err));
```



#### 마이크로태스크 큐

비동기 함수는 태스크 큐에 들어가는 것으로 알고 있지만, 프로미스의 후속 메서드(`.then`, `.catch`, `.finally`)는 마이크로태스크 큐라는 별도의 큐를 사용한다. 콜백 함수나 이벤트 핸들러가 임시 저장된다는 점은 동일하지만 **마이크로태스크 큐는 태스크 큐보다 우선**해서 콜 스택에 들어간다. 즉, `콜스택 → 마이크로태스크큐 → 태스크큐`순으로 실행된다.

```javascript
setTimout(() => console.log(1), 0);

Promise.resolve()
	.then(() => console.log(2))
	.then(() => console.log(3));
// 1, 2, 3 순일 것 같지만...
// return 2 3 1
```



---

### Shorthand Properties

단축(축약) 속성명은 객체의 Key와 Value가 같을 떄 사용할 수 있다.

```javascript
let a = "foo"
let obj = {
  a: a
}
// Shorthand Properties
let obj = { a } // { a: a }와 동일
```

### Function & Method

#### 함수 구성

자바스크립트의 함수는 객체 타입의 값이다. 따라서 함수 리터럴로 생성할 수 있다.

```javascript
// 함수 리터럴
function () { ... }
// 풀어쓰면...
function FUNCTION_NAME(parameter1, parameter2...) {
  return;
}
```

함수명(fucntion name)은 생략할 수 있다. 이름이 있는 함수의 경우 기명함수(named function), 이름이 없는 함수의 경우 무명/익명 함수(anonymous function)이라고 한다.

기명 함수의 경우, **함수 내부에서만 참조가 가능**한 식별자이다.

```javascript
// named function
function add(x, y) {
  return x + y;
}

// anonymous function
function (x, y) {
  return x + y;
}

// 함수 내부에서만 참조 가능
(function bar() { console.log('bar') });
bar(); // ReferenceError: bar is not defined
```

### 함수 정의

1. 함수 선언문(function declaration)
   ```javascript
   function add(x, y) {
     return x + y;
   }
   ```

   함수 선언식은 함수명을 이용해 암묵적으로 식별자를 생성한다. 그래서 식별자의 선언 없이도 함수의 참조, 호출이 가능하다.

   ```javascript
   // 암묵적인 식별자 생성
   var add = function add(x, y) {
     return x + y;
   }
   ```

   함수 선언식에서는 **함수 호이스팅(function hoisting)**이 발생한다.

   ```javascript
   add(2, 5); // 7
   function add(x, y) {
     return x + y;
   }
   ```

2. 함수 표현식(function expression)
   함수는 일급객체이므로 함수 리터럴로 생성한 함수 객체를 변수에 할당할 수 있다.

   ```javascript
   // 함수 표현식에선 함수 이름을 생략하는 것이 일반적이다.
   const add = function (x, y) {
     return x + y;
   }
   ```

   함수선언문과 다르게 변수 호이스팅이 일어나므로, 함수 선언 이전에 함수를 사용하는 것은 불가능하다.

3. Function 생성자 함수(Function constructor function)
   빌트인 함수인 Function 생성자 함수를 이용하여 함수 객체를 선언하는 방식이다.

   ```javascript
   let add = new Function('x', 'y', 'return x + y;');
   console.log(add(2, 5)); // 7
   ```

   **클로저**를 생성하지 않아 보통 사용하지 않는다.

   ```javascript
   let add1 = (function() {
     var a = 10;
     return function (x, y) {
       return x + y + a;
     }
   }());
   console.log(add1(1, 2)) // 13;
   
   let add2 = (function () {
     var a = 10;
     return new Function('x', 'y', 'return x + y + a;');
   }());
   
   console.log(add2(1, 2)) // ReferenceError: a is not defined;
   ```

4. 화살표 함수(arrow function)

   ES6에서 도입되었으며, 화살표를 활용하여 간단하게 함수를 정의할 수 있다.

   ```javascript
   const add = (x, y) => x + y;
   add(2, 5); // 7
   ```

   화살표 함수는 생성자 함수로 사용할 수 없으며, 별도의 this를 갖지 않아 **자신의 상위 스코프**의 this를 this로 참조한다. 더불어, prototype 프로퍼티가 없으며 arguments 객체를 생성하지 않는다.

   ```javascript
   const Foo = () => {};
   new Foo(); // TypeError: Foo is not a constructor
   Foo.hasOwnProperty('prototype') // false
   
   ```

   

#### 메서드(method)

### Hoisting

> 자바스크립트의 모든 선언문에서는 호이스팅이 발생한다. 호이스팅은 변수 혹은 함수를 선언하기 전에 호출하는 경우 마치 코드의 선두로 끌어진 것처럼 실행되는 자바스크립트의 특징이다.

- 원인
  자바스크립트는 **런타임 실행 환경 이전에 모든 변수/함수 선언문을(var, let, const, function, function*, class) 먼저 실행**하기 때문에 호이스팅이 발생한다.

**Variable Hoisting**

- var

  > var는 몇가지 문제점을 가지고 있어 기본적으로 사용하지 않는 것을 전제로 하지만, 어떤 문제점을 갖고 있는 지 살펴보도록 하자.

  1. 호이스팅의 발생
     var에서 발생하는 호이스팅은 자동으로 **undefined**를 할당하여 디버깅을 어렵게 한다.

     ```javascript
     console.log(foo);  // undefined. 호이스팅 중 변수에 undefined를 할당한다.
     
     var foo = 30;
     console.log(foo);  // 30
     ```

  2. 변수의 중복 선언 허용 및 함수 레벨 스코프
     var로 선언한 변수는 함수의 코드 블록만을 지역 스코프로 인정하는 함수 레벨 스코프(Function level scope, Function scope)를 따라, 예상치 못한 값 변경의 위험성이 높다.

     ```javascript
     console.log(x); // undefined
     var x = 10; // 선언과 초기화를 동시에 해서 값을 할당하였다고 해도, 선언문과 할당문을 2개의 문으로 구분해서 실행하기 때문에 선언문 전엔 undefined가 할당되어 있다.
     if (true) {
       var x = 20; // 중복선언
     }
     console.log(x); // 20
     ```

- let

  > ES6에서 도입된 let은 블록 레벨 스코프(Block level scope, Block scope)를 따르며, 호이스팅이 발생하지 않는 것처럼 동작한다.

  1. 호이스팅의 발생
     let에서도 호이스팅은 발생하지만, 호이스팅이 발생하지 않는 것처럼 동작한다. 이는 let은 **선언 단계와 초기화 단계가 나뉘어** 동작하기 때문이다.

     ```javascript
     console.log(foo); // ReferenceError: foo is not defined. 일시적 사각 지대(TDZ)에 있다.
     
     let foo; // 변수 선언문에 도달했을 때 initialization을 시작한다. foo = undefined;
     console.log(foo); // undefined
     foo = 21; // assignment. 재할당(reassignment)도 가능하다.
     console.log(foo); // 21
     ```

     let의 호이스팅은 `선언 단계 [일시적 사각 지대(TDZ, Temporal Dead Zone)] 초기화 단계 - 할당 단계`로 이루어져 있는데, 변수가 선언된 코드 줄에 도달했을 때 초기화를 실행하고 그 전에는 변수를 끌어올려 선언만 해두기 때문에, 선언문에 도달할 때까지 코드를 참조할 수 없는 일시적 사각 지대가 생긴다. 즉, 코드 선언문에 도달하기까지는 코드를 불러올 수 없기 때문에 코드의 안정성이 향상된다.

     **호이스팅 미발생의 증명**

     ```javascript
     let foo = 1; // 전역변수
     {
     	console.log(foo); // ReferenceError : Cannot access 'foo' before initialization
       let foo = 2; // 지역변수
     }
     ```

     만약 호이스팅이 발생하지 않았다면, `console.log(foo)`는 당연히 전역변수인 foo의 값 1을 불러왔어야 했지만, 참조에러를 발생시키고 있다. 이는 지역변수의 foo에서 호이스팅이 발생했음을 증명한다.

  2. 변수 중복 선언 금지
     변수의 중복 선언은 `SyntaxError`를 발생시킨다.

     ```javascript
     let a = 123;
     // 같은 스코프 내에서 중복 선언을 허용하지 않는다.
     let a = 456; // SyntaxError: Identifier 'a' has already been declared;
     ```

  3. 블록 레벨 스코프
     오직 함수 블록만 지역 스코프(local scope)로 인정했던 var와 달리 let으로 선언한 변수는 모든 코드 블록(함수, 조건문, 반복문, try/catch문 등)을 지역 스코프로 인정하는 블록 레벨 스코프(Block level scope, Block scope)를 따른다.

     ```javascript
     let foo = 1; // 전역 변수
     {
       let foo = 2; // 지역 변수
       let bar = 3; // 지역 변수
     }
     console.log(foo); // 1
     console.log(bar); // referenceError: bar is not defined
     ```




### export의 두가지 방식

1. `export default` 방식

   ```javascript
   // 함수, 클래스
   export default function foo() {}
   export default class bar() {}
   
   // 변수
   const abc = 'something';
   export default abc;
   
   // 불러오기
   import foo from 'SOMEWHERE';
   import bar from 'SOMEWHERE';
   import abc from 'SOMEWHERE';
   ```

2. export 방식
   ```javascript
   export const abc = {};
   // 동시 export
   const foo = {};
   const bar = function () {}
   export { foo, bar }
   
   // import
   import { abc, foo, bar } from 'SOMEWHERE';
   ```


### SSR - Cookie와 CSR - localStorage

서버사이드 렌더링의 경우 localStorage를 활용할 수 없다. localStorage는 browser에만 있기 때문. 따라서 cookie를 사용하는 편이 좋다.



### Document Height

화면의 높이를 구하는 방식에는 대표적으로 세 가지가 있다.

1. `window.scrollY`: 현재 화면의 최상단 지점의 Y좌표를 반환한다.(기본값 0)
2. `document.documentElement.clientHeight`: 스크롤에 상관없이 현재 화면의 높이를 반환한다.
3. `document.documentElement.scrollHeight`: 스크롤까지 포함한 화면 전체의 높이를 반환한다.

위의 세 가지는 화면의 맨 하단에 도달했을 때 1 + 2 === 3이 성립한다.(현재 화면 제일 높은 지점 좌표 + 현재 화면 높이 === 스크롤 포함한 전체 화면 높이)

즉, 스크롤이 화면의 가장 하단에 도달한 경우,
 `window.scrollY + document.documentElement.clientHeight === docuemnt.documentElement.scrollHeight`이다.

만약 스크롤 최하단보다 100px 정도 높은 높이를 가지고 있다면,
`window.scrollY + document.documentElement.clientHeight === document.documentElement.scrollHeight - 100`이 성립하는 것이다.

### IntersectionObserver

#### IntersectionObserver Interface

IntersectionObserver 인터페이스는 대상 요소와 그 상위 요소 혹은 최상위 도큐먼트인 viewport와의 교차 영역의 변화를 비동기적으로 감지한다.

IntersectionObserver는 두가지의 매개변수를 갖는다.

```javascript
const io = new IntersectionObserver(callback[, options]);
```

**callback**

callback은 callback 함수를 칭하며, callback함수는 2개의 매개변수 entries와 observer를 갖는다.

관찰할 Target이 등록되거나, 가시성(Visibility)에 변화가 생기면 호출된다.

```javascript
(entries, observer) => { ... }
```

- `entries`: 루트 요소와 타겟 요소의 트랜지션 순간을 묘사하는(즉, **교차 상태**를 표현) `IntersectionObserverEntry` 인스턴스의 Array

  ```javascript
  let callback = (entries, observer) => {
    entries.forEach(entry => {
      // Each entry describes an intersection change for one observed
      // target element:
      //   entry.boundingClientRect 관찰 대상의 사각형 정보(DOMRectReadOnly)
      //   entry.intersectionRatio 관찰 대상의 교차한 영역 정보(DOMRectReadOnly)
      //   entry.intersectionRect 관찰 대상의 교차한 영역 백분율(intersectionRect 영역에서 boundingClientRect 영역까지 비율, Number)
      //   entry.isIntersecting 관찰 대상의 교차 상태(Boolean)
      //   entry.rootBounds 지정한 루트 요소의 사각형 정보(DOMRectReadOnly)
      //   entry.target 관찰 대상 요소(Element)
      //   entry.time 변경이 발생한 시간 정보(DOMHighResTimeStamp)
    });
  };
  ```

  

- `observer`: 콜백을 실행한 `IntersectionObserver` 자신을 참조

**options**(Optional)

options는 intersectionobserver가 호출되는 상황을 조작할 수 있으며, 3가지 필드를 갖는다.

- root: 기본값은 브라우저의 `viewport`이며, root값이 지정되지 않거나, null일 때 사용된다. observe 중인 대상 객체가 보이는 기준을 어디로 할 지 정의한다. 반드시 Target의 조상 요소여야 한다.
- rootMargin: root container의 바깥에 여백을 주어 그만큼 Root 범위를 `확장하거나 축소`한다. `css margin`과 같이 4단계로 설정이 가능하며, `px`혹은 `%`로 설정이 가능하다. 기본값은 `0px 0px 0px 0px`, 단위 입력은 필수이다.
  - TOP, RIGHT, BOTTOM, LEFT /  `10px 30px 30px 10px`
  - TOP, (LEFT, RIGHT) BOTTOM /  `10px 20px 10px`
  - (TOP, BOTTOM), (LEFT, RIGHT) / `30px 20px`
  - (TOP, BOTTOM, LEFT, RIGHT) / `-25px`
- threshold: Observer가 실행되기 위해 Target의 가시성이 얼마나 필요한 지 적용한다. 기본값은 Array: [0]이지만, Number 타입의 단일 값으로도 작성 가능하다.
  - `0`: 타겟의 가장자리 픽셀이 Root 범위를 교차하는 순간(타겟의 가시성이 0%일 때) 실행
  - `0.5`: 타겟의 가시성  50%일 때 실행.
  - `[0, 0.25, 1]`: 타겟의 가시성이 0%, 25%, 100%일 때 모두 실행.

**Methods**

- `observe`: 대상 요소의 관찰을 시작한다.
- `unobserve`: 대상 요소의 관찰을 중지한다. 관찰 중이지 않은 요소를 지정한 경우 아무 동작도 하지 않는다.
- `disconnect`: 인스턴스가 관찰하는 모든 요소의 관찰을 중지한다.
- `takeRecords`: 현재 IntersectionObserver의 IntersectionObserverEntry 객체의 배열을 반환

#### Infinite Scroll

인피니트 스크롤은 과거에는 `windows.addEventListener('scroll', callback)`을 사용했지만, 현재는 `IntersectionObserver`를 주로 사용한다.

**예제**

```vue
<template>
  <div class="index-container">
    <TheProfileCard></TheProfileCard>
    <PostForm v-if="!!user" />
    <PostCard v-for="p in mainPosts" :key="p.id" :post="p" />
    <!-- mouse wheel 인식 위해 1px -->
    <div ref="observe" style="height: 1px;" />
  </div>
</template>

<script>
definePageMeta({
  middleware: [() => { console.log('inline') }]
})
import PostCard from '~/components/ThePostCard.vue';
import PostForm from '~/components/ThePostForm.vue';
import TheProfileCard from '~/components/TheProfileCard.vue';
import { useUsersStore } from '~/stores/users';
import { usePostsStore } from '~/stores/posts';
export default {
  name: 'IndexView',
  components: { PostCard, PostForm, TheProfileCard },
  setup() {
    const name = 'Nuxt';
    const usersStore = useUsersStore();
    const postsStore = usePostsStore();
    const user = computed(() => usersStore.state.me.nickname || usersStore.state.me.email);
    const mainPosts = computed(() => postsStore.state.mainPosts);
    const observe = ref(null);
    onMounted(() => {
      const { $trigger } = useNuxtApp();
      $trigger('endLoading');

      const options = {
        root: null,
        threshold: 0
      }
      const io = new IntersectionObserver((entries, observer) => {
        entries.forEach((entry) => {
          // 현재 교차상태가 true인 경우
          if (entry.isIntersecting) {
            // 현재 보던 옵저버 해제
            observer.unobserve(entry.target);
            // 새로 추가전 로딩 구현
            postsStore.loadPosts();
            const items = document.querySelectorAll('.postcard-container');
            // 새 옵저버 추가
            io.observe(observe.value);
          }
        })
      }, options);
      io.observe(observe.value);
    });

    return {
      user,
      mainPosts,
      name,
      observe
    }
  },
}
</script>

```

**예제2/3 공통설정**

```javascript
// main.js
import { createApp } from 'vue'
import App from './App.vue';
import axios from "axios";

const app = createApp(App);
app.provide('axios', axios);
app.mount('#app');

```



**예제2(Promise 활용)**

```vue
<template>
  <div id="app">
    <div v-cloak class="photos">
      <div v-for="photo in photos"
        :key="photo.id"
        class="photo">
      <div class="photo__title">{{ photo.title }}</div>
      <div :style="`background-image: url(${photo.url});`"
        :class="{ loaded: photo.imageLoaded }"
        class="photo__image"></div>
      </div>
    </div>
    <div id="scroll-observer"
          v-if="showScrollObserver"
          ref="scrollObserver">
      <!-- 상시 작동중 -->
      <div class="lds-ring"><div></div><div></div><div></div><div></div></div>
    </div>
  </div>
</template>

<script setup>
  import { ref, inject } from 'vue';
  let photos = ref([]);
  let length = ref(4);
  let showScrollObserver = ref(true);
  let scrollObserver = ref(null);
  const axios = inject('axios');
  /**
   * @summary 사진을 가져옵니다.
   * @param {number} start - 가져올 사진의 시작 포인트
   * @param {number} limit - 가져올 사진의 개수
   * @return {Promise} - 비동기 실행을 위한 Promise 객체
  */
  function fetchPhotos (start = 1, limit = 1) {
    return new Promise(resolve => {
      const photosToFetch = []
      for (let i = start; i < start + limit; i += 1) {
        photosToFetch.push(axios(`https://jsonplaceholder.typicode.com/photos/${i}`));
      }

    Promise.all(photosToFetch)
      .then(photos => {
        return photos.map(photo => {
          return {
            ...photo.data,
            imageLoaded: false
          }
        })
      })
        .then(fetchedPhotos => {
          photos.value.push(...fetchedPhotos)
          photos.value.forEach(photo => {
          // 사진 로드를 대기
          const image = new Image();
          image.src = photo.url;
          image.onload = () => {
            photo.imageLoaded = true
          }
        });
        resolve(true);
    });
    });
  }
  /**
   * @summary Intersection Observer를 초기화합니다.
  */
  function initIntersectionObserver () {
    const io = new IntersectionObserver((entries, observer) => {
      entries.forEach(entry => {
        // 요소(#scroll-observer)의 가시성이 확보되면..
        if (entry.isIntersecting) {
          fetchPhotos(length.value);
          // For next photo
          increasePhotoLength();
          // unused var 회피용 observer 무의미한 호출
          observer;
        }
      });
      }, {
      // 로딩 애니메이션이 보이지 않게 가져오기를 수행할 수 있도록..
      // rootMargin: '0px 0px 400px 0px'
      rootMargin: '0px 0px 0px 0px',
      threshold: 1
    })
    io.observe(scrollObserver.value);
  }
    /**
     * @summary 가져올 사진의 시작 포인트를 증가시킵니다.
    */
  function increasePhotoLength () {
    length.value += 1
    console.log(length.value)
  }

  // init
  fetchPhotos(1, length.value)
    .then(() => {
    initIntersectionObserver()
  })
  // For next photo
  increasePhotoLength()
</script>

<style>
  .photos {
    padding: 30px;
  }

  .photos .photo {
    margin-bottom: 40px;
  }
  .photos .photo__title {
    font-size: 18px;
    font-weight: 700;
    margin-bottom: 10px;
    color: #444;
    line-height: 1.4;
  }
  .photos .photo__image {
    width: 100%;
    height: 250px;
    border-radius: 10px;
    overflow: hidden;
    background-position: center;
    background-repeat: no-repeat;
    background-size: cover;
  }
  .photos .loaded {
    animation: jello 1s;
  }

  #scroll-observer {
    height: 200px;
    display: flex;
    justify-content: center;
    align-items: center;
  }

  /* For Vue */
  [v-cloak] {
    display: none;
  }

  /* Loader */
  .lds-ring {
    display: inline-block;
    position: relative;
    width: 64px;
    height: 64px;
  }
  .lds-ring div {
    box-sizing: border-box;
    display: block;
    position: absolute;
    width: 51px;
    height: 51px;
    margin: 6px;
    border: 6px solid #fff;
    border-radius: 50%;
    animation: lds-ring 1.2s cubic-bezier(0.5, 0, 0.5, 1) infinite;
    border-color: #F86C06 transparent transparent transparent;
  }
  .lds-ring div:nth-child(1) {
    animation-delay: -0.45s;
  }
  .lds-ring div:nth-child(2) {
    animation-delay: -0.3s;
  }
  .lds-ring div:nth-child(3) {
    animation-delay: -0.15s;
  }
  @keyframes lds-ring {
    0% {
      transform: rotate(0deg);
    }
    100% {
      transform: rotate(360deg);
    }
  }
  
  @keyframes jello {
  11.1% {
    transform: none
  }
  22.2% {
    transform: skewX(-12.5deg) skewY(-12.5deg)
  }
  33.3% {
    transform: skewX(6.25deg) skewY(6.25deg)
  }
  44.4% {
    transform: skewX(-3.125deg) skewY(-3.125deg)
  }
  55.5% {
    transform: skewX(1.5625deg) skewY(1.5625deg)
  }
  66.6% {
    transform: skewX(-0.78125deg) skewY(-0.78125deg)
  }
  77.7% {
    transform: skewX(0.390625deg) skewY(0.390625deg)
  }
  88.8% {
    transform: skewX(-0.1953125deg) skewY(-0.1953125deg)
  }
  100% {
    transform: none
  }
</style>

```

**예제2(심플(image onload 처리등 생략) Async/Await 활용)**

```vue
<script setup>
  import { ref, inject } from 'vue';
  let photos = ref([]);
  let length = ref(4);
  let showScrollObserver = ref(true);
  let scrollObserver = ref(null);
  let loading = ref(null);
  const axios = inject('axios');

  async function fetchPhotos(start = 1,limit = 1) {
    try {
      if (length.value > 10) {
        if (loading.value) loading.value.classList.remove('on-loading');
        setTimeout(() => {
          if (loading.value) loading.value.classList.add('on-loading');
        }, 3000);
        return;
      }
      if (loading.value) loading.value.classList.remove('on-loading');
      for (let i = start; i < start + limit; i++) {
        const { data } = await axios(`https://jsonplaceholder.typicode.com/photos/${i}`);
        photos.value.push(data);
      }
      if (loading.value) loading.value.classList.add('on-loading');
    } catch(err) {
      console.log(err)
    }
  }

  /**
   * @summary Intersection Observer를 초기화합니다.
  */
  function initIntersectionObserver () {
    const io = new IntersectionObserver((entries, observer) => {
      entries.forEach(entry => {
        // 요소(#scroll-observer)의 가시성이 확보되면..
        if (entry.isIntersecting) {
          fetchPhotos(length.value);
          // For next photo
          increasePhotoLength();
          // unused var 회피용 observer 무의미한 호출
          observer;
        }
      });
      }, {
      // 로딩 애니메이션이 보이지 않게 가져오기를 수행할 수 있도록..
      // rootMargin: '0px 0px 400px 0px'
      rootMargin: '0px 0px 0px 0px',
      threshold: 1
    })
    io.observe(scrollObserver.value);
  }
    /**
     * @summary 가져올 사진의 시작 포인트를 증가시킵니다.
    */
  function increasePhotoLength () {
    length.value += 1
    console.log(length.value)
  }

  // init
  fetchPhotos(1, length.value)
    .then(() => {
    initIntersectionObserver()
  })
  // For next photo
  increasePhotoLength()
</script>
```



### Array

#### Methods

- Array.from()
  유사 배열 객체(array-like object)나 반복 가능한 객체(iterable object)를 얕게 복사해 새로운`Array` 객체를 만든다.
  
  ```javascript
  Array.from(arrayLike[, mapFn[, thisArg]]);
  ```
  
  - `arrayLike`

    배열로 변환하고자 하는유사 배열 객체나 반복 가능한 객체.

  
  - `mapFn`(Optional)
  
    배열의 모든 요소에 대해 호출할 맵핑 함수.
  

  - `thisArg`(Optional)
  
    `mapFn` 실행 시에 `this`로 사용할 값.
  
  예시
  
  ```javascript
  Array.from('foo'); // Array ['f', 'o', 'o'];
  Array.from([1, 2, 3], x => x + x); // Array [2, 4, 6];
  ```
  

#### 이차원 배열의 생성

```typescript
// 먼저 fill로 값을 채우고, map 함수로 값(새 array)를 추가하는 것에 유의.
let dp:Array<Array<number>> = new Array(nums.length).fill(0).map(x => new Array(nums.length).fill(0));
// num type의 배열 type의 배열
let dp:number[][] = Array.from(new Array(nums.length), x=> new Array(nums.length).fill(0));
```

#### 빈 배열 생성 후 각종 다양한 값을 넣어 초기화 하기

`fill()`을 이용해 값을 초기화하지 않으면, `map()`의 사용이 불가능함에 유의한다.

```typescript
// length 길이의 배열 생성 후, fill()로 empty => undefined로 초기화 후, 값 적용
const arr:Array<any> = new Array(length:number).fill().map(() => ({
  foo: 'something',
  bar: Math.floor(Math.random() * (10**13))
}));
```

### 기타

#### 프로토타입 메서드와 정적 메서드의 차이

프로토타입 메서드는 **생성자 함수**의 인스턴스를 생성한 후 호출할 수 있으며, 정적 메서드는 인스턴스를 생성하지 않아도 호출할 수 있는 메서드이다.

## TypeScript

### Non-null assertion operator

변수 뒤에 `!`을 붙여 null 혹은 Undefined가 아님을 확신한다.

## Node.js

### 논 블로킹 기법

자바스크립트에는 동시 실행이 가능한 작업(동기)과 동시 실행이 불가능한 작업(비동기)이 있다. 함수를 예로 들어보자.

```javascript
function longTask() {
  // ...A task that takes long time..
  console.log('done');
}
console.log('start');
longTask();
console.log('finish');
```

```javascript
// result
'start'
'done'
'finish'
```

이처럼 실행 컨테스트가 콜스택에 들어가 실행중인 `longTask()`함수 때문에 finish는 훨씬 먼저 끝낼 수 있음에도 오랜 시간을 기다려야 한다.
이럴 때 사용하는 것이 **다른 코드의 실행을 막는 것을 방지**하는 논 블로킹 기법이다.

1. setTimeout
   세트타임아웃은 기본적으로 설정된 시간을 대기(최소 지연시간 4ms)한 후 **태스크 큐**로 보내지고 콜스택이 빌 때까지 기다리기 때문에, 동기적 실행 순서와는 관련이 없다. 그래서 setTimeout(callback, 0)을 이용하면 논 블로킹한 순서로 실행이 가능하다.

   ```javascript
   function longTask() {
     // ...A task that takes long time..
     console.log('done');
   }
   console.log('start');
   setTimeout(longTask(), 0);
   console.log('finish');
   ```

   ```javascript
   // result
   'start'
   'finish'
   'done'
   ```

   

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

### 기본 사용 방법

#### 다운로드

#### 업로드

1. `git add PATH`: 커밋할 내용을 스테이지에 올린다.

```bash
git add . // 현재 경로 내 전체 디렉토리/파일
git add ./components/ // components 디렉토리 내 전체 디렉토리/파일
```

2. `git commit -m 'MESSAGE'`
3. `git push REMOTE_NAME BRANCH_NAME`

### Git Add를 취소할 때

`git reset HEAD`

### Git 초기 생성시 파일을 추가하여(LICENSE, README 등) 에러가 났을 때 대처 방법

```bash
git pull <remote_name> <branch_name> --allow-unrelated-histories
```

- 초기 파일들과 새로 올릴 파일들을 서로 다른 프로젝트로 구분하기 때문에(처음에 pull한 저장소 파일에 코드를 작성하지 않았다면), 병합이 불가능하도록 설정되어 있어 이를 허용해주어야 한다.

### Style Guide

1. Repo Name
   kebab-case



### Fork와 Pull request

Vue와 같은 대형 프로젝트에 참여한다고 할 때, 모든 개발자를 maintainer나 developer로 추가하는 것은 매우 어려울 것이다. 이런 경우, repository(원격 저장소, 이하 레포)를 Fork한 후, 수정사항을 pull request를 보내 merge를 요청하는 방식으로 개발이 많이 이루어진다.

1. Fork
   원하는 github 레포 페이지에 들어가 **clone이 아닌** Fork(우측 상단 star 옆에 아이콘이 있다.)를 통해서 내 고유의 레포를 생성한다. 이 때, 레포 네임은 자유롭게 지정이 가능하지만 되도록이면 기존 레포 이름을 따른다.

2. Fork한 저장소를 Local로 Clone
   Fork한 후 내 레포 목록을 봐보면 Fork한 레포가 추가되어 있다. 이는 내 고유한 리포지토리로, 개인적으로 생성한 레포처럼 사용할 수 있다.

   ```bash
   git clone <Forked Repository URL>
   ```

3. 루트 저장소 Remote 설정(Optional)
   레포를 clone한 경우, origin이란 remote명으로 내 레포가 연결되어 있다. 가능하다면, 포크한 원본 저장소도 연결해 두는 것이 좋으나 필수는 아니다.

   ```bash
   # add remote
   git remote add <REMOTE_NAME> <Root Repository URL(원본 저장소 URL)>
   ```

4. Branch 생성
   꼭 Fork한 대형 프로젝트가 아니더라도, 자신이 맡은 개발파트에 따라 branch를 생성하거나, dev 등 단계에 따라 branch를 생성하는 것은 흔한 일이다.
   예를 들면, 업데이트 버전 개발을 master branch에서 진행 중인데, 특정 코드에서 버그가 일어나 그 코드를 수정해야 하는 경우, master branch에 다같이 올리게 되면 현재 개발 중인 코드까지 전부 올라가는 불상사가 생기게 된다.(물론 `git add ./PATH`로 특정 파일만 올릴 수 있긴 하지만..) 이런 불상사를 대비하기 위해 독립적으로 branch를 생성해 특정 작업을 따로 시행하게 된다.

   ```bash
   git branch # Branch list
   git branch <Branch name> # create branch
   git checkout # check current branch
   git checkout <Branch name> # change branch
   git checkout -b <Branch name> # create&change branch
   ```

5. 코드 작업
   기존에 하던 것처럼 코드를 작업하되, **브랜치 변경을 잊지 말아야 한다.**

   ```bash
   git add ./${PATH}
   git commit -m 'message'
   git push <REMOTE_NAME(default: origin)> <BRANCH_NAME>
   
   ```

6. Compare & Pull Request
   커밋과 푸쉬를 완료한 후, 내 레포로 돌아가보면 변경한 사항이 반영되어 있고, 그에 따라 `Compare & pull request`	버튼이 생긴 것을 볼 수 있다. 이를 클릭하고 이 요청에 대한 설명을 작성한다.(제목은 보통 커밋 메세지를 그대로 계승한다.)
   윗 메뉴에서 풀 리퀘스트를 요청할 브랜치를 선택하고, 대상 브랜치를 원본 저장소에서 선택한 후 Pull request를 생성한다.

7. Merge
   관리자 측에서 코드를 확인 후, Merge 여부를 결정한다.

8. Merge 이후 동기화 및 Branch 삭제
   `3. 루트 저장소 Remote 설정(Optional)`에서 루트 저장소를 굳이 연결한 이유가 여기에 있는데, 루트 저장소를 pull받아 merge된 내용을 동기화하기 위함이다(pull시 브랜치 선택 주의할 것!). 이후 merge를 완료한 branch를 삭제한다.

   ```bash
   # pull original repo
   git pull <ORIGINAL_REPO_REMOTE_NAME>
   # delete branch
   git branch -d <BRANCH_NAME>
   ```

#### Commit을 잘못한 경우

Pull Request를 *closed*한 후 다시 작성할 수도 있겠지만, **Merge전에 바로 수정하는 방법**이 있다.

일단 수정이 필요한 부분을 먼저 수정한 후,
```bash
git add .
# 최신 커밋 덮어쓰기
# message는 필수가 아니며, 작성하지 않을 시 기존 커밋 메세지를 계승한다.
git commit --amend -m 'message'
# -f : force
git push -f <REMOTE_NAME> <BRANCH_NAME>
```

위와 같은 과정을 거치면 pull request에 들어가 있는 내 commit이 변경된 것을 볼 수 있다.



## NPM

- 개발자용 Package 설치
  ```bash
  npm i -D 'PACKAGE_NAME'
  ```


### 구버젼 패키지 확인

```bash
npm outdated
```

- 업데이트
  ```bash
  npm update
  ```

  

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

### Fetch Data

Vue3의 data-fetching 방법 중 대표적인 몇 가지를 소개한다. 

1. Fetch API(요즘은 미사용하는 추세)
   ```vue
   <script>
   export default {
     setup() {
       const result = ref(null);
       
       fetch('URL')
       	.then(res => res.json())
       	.then(data => result.value = data);
     }
   }
   </script>
   ```

2. axios(fetch를 써야한다면 대신 axios를 사용한다.)
   ```vue
   <script>
     export default {
       setup() {
         const result = ref(null);
         axios.get('URL')
         	.then(data => result.value = data);
         return { result }
       }
     }
   </script>
   ```

3. async/await
   ```vue
   <script setup>
     const result = ref(null);
     onMounted(async () => {
       result.value = await axios.get('URL');
     });
   </script>
   
   <!-- 혹은, 이와 같은 방법도 가능하다. -->
   <!-- Child.vue -->
   <script>
   	async setup() {
       const result = await axios.get('URL');
       return { result }
     }
   </script>
   <!-- Parent.vue -->
   <template>
   	<Suspense>
     	<template #default>
   			<Child />
   		</template>
   		<template #fallback>
   			<div>loading...</div>
   		</template>
     </Suspense>
   </template>
   ```

4. Composable(일반 / CacheMap 이용한 결과 저장)
   ```javascript
   import { ref, computed, reactive } from 'vue';
   import axios from 'axios';
   export const useFetch = (url, config = {}) => {
     const data = ref(null);
     const response = ref(null);
     const error = ref(null);
     const loading = ref(false);
   
     const fetch = async () => {
       loading.value = true;
       try {
         const result = await axios.request({
           url,
           ...config
         });
         response.value = result;
         data.value = result.data;
       } catch (err) {
         error.value = err;
       } finally {
         loading.value =false
       }
     }
   
     !config.skip && fetch();
   
     return { response, error, data, loading, fetch }
   }
   
   // cache로 fetchData 저장해두기
   const cacheMap = reactive(new Map());
   
   export const useFetchCache = (key, url, config) => {
     const info = useFetch(url, { skip: true, ...config });
   
     const update = () => cacheMap.set(key, info.response.value);
     const clear = () => cacheMap.set(key, undefined);
   
     const fetch = async () => {
       try {
         await info.fetch();
         update();
       } catch {
         clear();
       }
     }
   
     const response = computed(() => cacheMap.get(key));
     const data = computed(() => response.value?.data);
   
     if (response.value === null) fetch();
     
     return { ...info, fetch, data, response, clear };
   }
   ```


### 스크롤 위치 기억하기

전 페이지로 돌아갔을 때 맨 위로 이동하는 경우 원래 보던 페이지를 다시 찾아야 하는 불편함이 있다.

#### Nuxt

현재 Nuxt3 RC9에선 전부 제대로 동작하지 않는다.

1. vue-router options 설정

   `scrollBehavior`는 **HTML5 History mode**에서만 동작한다.

   경로: `~/app/router.options.ts`

   ```typescript
   import { RouterConfig } from '@nuxt/schema';
   // vue-router options로 페이지 위치 기억하기
   export default <RouterConfig>{
     scrollBehavior(_to, _from, savedPosition) {
       console.log(savedPosition); // 페이지가 옮겨질 때 이전 페이지의 스크롤 위치를 기억해둔다.
       if (savedPosition) {
         return savedPosition;
       } else {
         // 좌측 상위 좌표값과 scroll-behavior 설정
         return { left: 0, top: 0, behavior: 'smooth' };
       }
     },
   };
   ```

   

2. 플러그인 설정

   1번을 단순히 플러그인에서 설정한 것으로 1번과 같이 따로 불러오지 않아도 자동으로 작동한다.
   경로 : `~/plugins/PLUGIN_NAME.js`

   ```javascript
   // ~/plugins/scroll-to.js
   export default defineNuxtPlugin((nuxtApp) => {
     nuxtApp.$router.options.scrollBehavior = async (to, from, savedPosition) => {
       if (to.path !== from.path && process.client) {
         if (savedPosition) {
           return savedPosition;
         } else {
           window.scrollTo(0, 0);
           // or
           return { left: 0, top: 0 };
         }
       }
     }
   })
   ```

3. Middleware 설정
   Middleware 내에서 scrollTo를 통해 값을 변경한다.
   경로: `~/middleware/MIDDLEWARE_NAME.global.js`

   ```javascript
   export default defineNuxtRouteMiddleware((to, from) => {
     if (to.path === from.path && process.client) {
       // 스크롤 top으로
       window.scrollTo(0, 0);
     }
   })
   ```

4. onMounted 내 설정
   onMounted에 설정하면, 페이지 뒤로 가기를 할 때 mounted가 동작하면서 scrollTo를 적용한다.

   ```vue
   <!-- pages/index.vue -->
   <template>
   </template>
   <script setup>
     import { useIndexStore } from '~/stores/index';
     const indexStore = useIndexStore();
     const { state } = storeToRefs(indexStore);
     onMounted(() => {
       setTimeout(() => {
         window.scrollTo(0, indexStore.state.scrollY || 0);
         // or
         window.scrollTo(0, state.scrollY || 0);
       })
     });
   </script>
   ```

   ```vue
   <!-- components/COMPONENT_NAME.vue -->
   <script setup>
     import { useIndexStore } from '~/stores/index';
     const indexStore = useIndexStore();
     onUnmounted(() => {
       indexStore.setScroll(scrollY);
     });
   </script>
   ```

   ```javascript
   export const useIndexStore = defineStore('index', () => {
     const state = reactive({
       scrollY: 0,
     })
     const setScroll = function (y) {
       state.scrollY = y;
     }
     return {
       state,
       setScroll
     }
   });
   ```

   

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


## VSCODE

- 같은 줄 내 같은 단어 선택 : `CTRL + D`
- 페이지 내 전체 같은 단어 선택: `CTRL + SHIFT + L`
- 설정 관련 주소창 `F1` 혹은 `CTRL + SHIFT + P`



## 추천사이트

https://learn.shayhowe.com/html-css/

VSCode 기본 설정

https://gwonsungjun.github.io/articles/2018-06/vscodeSetting