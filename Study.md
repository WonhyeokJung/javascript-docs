# Frontend 코드 기록

## 목차

1. [기재된 기술](#기재된-기술)
2. [CSS](#CSS)
   1. [Selector](#Selector)
   2. [CSS Property](#CSS-Property)
3. [JavaScript](#JavaScript)

## 기재된 기술

  <img src="https://img.shields.io/badge/Framework-Bootstrap-blueviolet?logo=Bootstrap&logoColor=white"> <img src="https://img.shields.io/badge/-jQuery-important?logo=jQuery&logoColor=white"> <img src="https://img.shields.io/badge/Language-JavaScript-green?logo=JavaScript&logoColor=white"> <img src="https://img.shields.io/badge/Language-HTML5-blue?logo=HTML5&logoColor=white"> <a href="https://developer.mozilla.org/ko/docs/Learn/Getting_started_with_the_web/CSS_basics"><img src="https://img.shields.io/badge/StyleSheet-CSS3-lightgray?logo=CSS3&logoColor=white"></a> <img src="https://img.shields.io/badge/Language-Python-white?logo=Python&logoColor=blue"> <img src="https://img.shields.io/badge/Framework-Vue.js-green?logo=Vue.js"><img src="https://img.shields.io/badge/Tools-Github-blue?logo=github"><img src="https://img.shields.io/badge/Language-TypeScript-red?logo=typescript"><img src="https://img.shields.io/badge/Runtime-node.js-red?logo=node.js">

netlify, npm, postman, gitlab, docker, tailwind, mysql, mongodb, react

## Markdown

### Style Guide

>  https://arcticicestudio.github.io/styleguide-markdown/rules/

1. File Naming: kebab-case

### Link와 띄어쓰기

Link의 경우 기본적으로 이렇게 연결한다.
```markdown
## 목차
1. [목차](#목차)
2. [안녕하세요? 반갑습니다.](#안녕하세요?-반갑습니다.)
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

`\n` , `\t`

### 아스키 코드를 이용한 HTML 특수문자

HTML 상에서는 특수문자가 제대로 나타나지 않는 경우가 있다. 그런 경우를 대비하여 아스키 코드를 이용한 HTML 특수문자를 제공한다. 

```html
<!-- 예시 -->
<p class="text_indent0px font_size0_8em line_height1_325 margin_bottom1px margin_left0px margin_right0px sans_serif floatleft">E<span class="small_caps">VELYNE</span>&#9;</p>
```



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

### 기본 기능

| CSS Property | Explanation |
| ------------ | ----------- |
| line-height  | 줄 간격     |
|              |             |



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

위처럼 `filter` 프로퍼티에서 사이즈 변경을 하도록 지정해주면 사파리에서도 위와 같은 문제 없이 잘 사용할 수 있다.

다만 `filter`는 치명적인 단점이 있는데 성능을 크게 저하시킬 수 있다는 문제점이 있다는 것이다. 따라서 많은 곳에 남발하는 것은 금물이고, 더이상 필요없는 경우 JavaScript 등을 이용하여 제거해 주는 것이 좋다.

```javascript
document.querySeletor('.fa-heart').style.willChange = 'auto';
function removeHint() {
  this.style.willChange = 'auto';
}
```

항상 정답은 사파리 사용을 막고 크롬을 사용하게 하는 것임을 명심하자.

#### 크롬과 사파리의 fixed / body 바깥으로의 scroll 차이점 문제

상단에 navbar를 `position: fixed`로 주고 크롬과 사파리에서 각각 실행해보면, 크롬은 스크롤을 최상단에서 off the body로 스크롤을 더 올리면 fixed는 여전히 고정되고 body만 움직이지만, 사파리에선 **fixed가 같이 움직여** 상단이 노출되는 현상을 볼 수 있다. 이럴 때 사용할 수 있는 css 기술이 있다.

**top이 height 절대값보다 1px 작아야 제대로 적용됨에 주의**하자.

1. HTML에 가짜 div 삽입
   ```html
   <html>
     <body>
       <div style="height:1000px; background:#00BD9C; margin-top:-999px; position:fixed; width:100%;" />
     </body>
   </html>
   ```

2. css에 적용
   ```css
   html:before {
     content: '';
     position: fixed;
     width: 100%;
     height: 999px;
     top: -998px;
     background-color: #F7AF05;
   }
   ```

   

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

### 좌우 끝 정렬

```html
<!-- 방법1 grid -->
<div style="display: grid; grid-template-columns: 100px 100px; justify-content: space-between;">
  <div style="margin: 0;">안녕</div>
  <div>하세요</div>
</div>
<!-- 방법2 float left/right -->
<div>
  <h1 style="float: left; margin: 0;">Go Sox</h1>
  <p style="display: inline-block; float: right">Chicago White Sox fan page</p>
</div>
<!-- 방법3 flex -->
<head>
  <style>
  .flex-wrapper {
    display: flex;
    margin: 0 auto;
    /** height 필수 / width는 크기 조절용 **/
    width: 960px; 
    height: 100px;
    flex-wrap: nowrap;
    /** 가로, 세로 정렬. align-items는 높이가 없으면 적용이 안되므로 상위 컨텐츠 100% 크기 들어가도록 조정 **/
    justify-content: space-between;
    align-items: center;
  }
  </style>
</head>
<body>
	<header class="site-header">
  	<div class="container flex-wrapper">
    	<a class="site-title">Go Sox</a>
    	<p style="color: white;">Chicago White Sox fan page</p>
  	</div>
	</header>
</body>
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


### 중복 스크롤 방지(스크롤체이닝 방지)

페이지 내에 스크롤을 가진 요소가 여러개일때 하나의 스크롤이 끝나면 상위 요소의 스크롤을 내부에서 작동시키는 체이닝 현상이 발생할 수 있다. 이를 방지하기 위해 사용한다.(각 요소에서 자기 요소만 스크롤할 수 있게 한다.)

```css
body {
  overscroll-behavior-y: auto; /* default */
	overscroll-behavior-y: contain;
  overscroll-behavior-y: none;
}
```



### 특정 요소의 배경색만 투명하게 만들기

```css
element {
  background-color: transparent;
  /* or */
  background-color: rgba(0,0,0,0);
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

Node.js 환경에서는 `process.nextTick(() => { ... })`도 마이크로태스크 큐이다.

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

#### 함수 정의

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



### Module

#### ES6(EcmaScript2015) 이전

완성도가 아주 대단한 자바스크립트에 모듈이 없던 시절에 스크립트가 커지고 모듈의 필요성이 대두되면서 `AMD`나 `CommonJS`가 등장해 모듈을 불러왔다.

Node.js와 Express 프레임워크를 이용한 그 예시를 보자.

```json
// package.json
{
  "main": "app.js", // 실행시 최초 진입할 js 파일을 설정한다.
  "scripts": {
    "start": "nodemon app"
  },
 	"dependencies": {
    "express": "^4.18.2"
  },
  "devDependencies": {
    "nodemon": "^2.0.20"
  }
}
```

```javascript
// app2.js
const express = require('express');

const app = express();
process.env.PORT = 3001;
app.set('port', process.env.PORT || 3000);

// get요청
app.get('/', (req, res) => {
  // 단순 문자열
  // res.send('Hello, Express');
  // html 페이지
  res.sendFile(path.join(__dirname, '/index.html'));
});

app.listen(app.get('port'), () => {
  console.log(app.get('port'), '번 포트에서 서버가 실행중입니다.');
});

module.exports = {
  app
}

```

```javascript
// app.js 최초 실행 페이지.
const app = require('./app2'); // app2.js에서 만든 const app을 불러온다.
```

#### module.exports vs exports

- `module.exports`는 빈 객체를 참조한다.
- `exports`는 `module.exports`를 참조한다.

```javascript
// module.exports를 항상 참조하기 때문에, 객체를 수정하지 않고 생성/수정이 가능하다.
exports.[SOMTHING] = SOMETHING;
// 항상 새로운 객체가 할당되므로, 무한정 사용하기에는 부담이 있다.
module.exports = {
  SOMETHING,
};
// or
module.exports = () => {
  SOMETHING,
}
```

이후, `require`는 항상 `module.exports`를 리턴받아 사용한다.

#### import/export

`package.json`이 기본적으로 `CommonJS`를 베이스로 하고 있기 때문에, `ES module`타입인 `import/export`, `.mjs`등을 사용하려면 **type**을 설정해주어야 한다.

```javascript
{
 "type": "module", // ESModule을 인식하게 한다.
}
```

```javascript
// app2.js
import express from 'express';
import path from 'path';
import { fileURLToPath } from 'url';

const __filename = fileURLToPath(import.meta.url);
// dirname 설정
const __dirname = path.dirname(__filename);

const app = express();
// export default const app = express();
process.env.PORT = 3001;
app.set('port', process.env.PORT || 3000);

// get요청
app.get('/', (req, res) => {
  // 단순 문자열
  // res.send('Hello, Express');
  // html 페이지
  res.sendFile(path.join(__dirname, '/index.html'));
});

app.listen(app.get('port'), () => {
  console.log(app.get('port'), '번 포트에서 서버가 실행중입니다.');
});

export {
  app
}

// or
export default app;
```

```javascript
// webpack 사용시 .js 생략가능
import { app } from './app2.js';
// import app from './app2.js';
// 따로 부르지 않아도 자동인식한다.
```




#### export의 두가지 방식

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

### 프로젝트 기본 설정

타입스크립트는 기본적으로 자바스크립트에 기초하기 때문에, 자바스크립트의 변환이 필요하다. 이런 경우 기본적으로 필요한 설정을 알아보자.

#### package.json 생성

```bash
# 프로젝트 폴더 내 package.json 생성
$ npm init
```

```json
// package.json
{
  "name": "test",
  "version": "1.0.0",
  "description": "test",
  "main": "src/app.ts", // 패키지 실행시 시작파일을 설정한다. 예를 들면 누군가 내 모듈을 설치하고 require('test')를 한 경우, main에 지정한 module.exports가 반환된다. 즉, 모듈 내 모든 모듈의 시작점이다.
  "scripts": { // npm run test 등 스크립트별 실행할 명령어의 내용을 설정한다.
    "build": "tsc" // ts 파일 빌드
    "test": "echo \"Error: no test specified\" && exit 1",
    "push": "git pull origin master && git add . && git commit -m \'test\' && git push origin master" // git push 예시
  },
  "repository": {
    "type": "git",
    "url": "git+https:~.git"
  },
  "author": "WonhyeokJung",
  "license": "MIT",
  "bugs": {
    "url": "https://github.com/WonhyeokJung/[REPO]/issues"
  },
  "homepage": "https://~/#README",
  "dependencies": { // 의존성 모듈. 모듈은 모듈을 가질 수 있는 것이 노드 모듈의 특징이다.
  }
}
```

2. 의존성 모듈을 설치한다.

```bash
$ npm install typescript # Compiler 설치(tsc 명령어로 js로의 compile이 가능해진다.)
$ npm install -D ts-node # ts 파일을 바로 컴파일하여 실행하게 해줌
$ npm install @types/node # node에 사용되는 ts의 타입 정의를 가져온다.
```

3. package.json이 있는 root folder 혹은 root folder 내의 필요한 위치에 tsconfig.json을 생성

```json
// tsconfig.json
{
  "include": [], // 포함할 파일과 경로
  "exclude": [], // 제외할 파일과 경로
  "compilerOptions": { // 아주 다양하니 찾아볼것
    "target": "ES2021", // ES2021을 타켓으로 한 컴파일을 한다. 구 브라우저도 읽을 수 있는 es5설정 등을 사용할 수도 있다. 타켓에 맞게 언어가 변환되어 반환된다.(let이 없는 등)
    "lib": ["ES2021"], // 현재 내가 작성한 코드를 읽을 수 있는 라이브러리를 선택
    
    "module": "commonjs", // commonjs, esmodule 등이 있다. js에 require로 반환할 건지, import로 반환할건지 결정해준다
    "rootDir": "./src", // 원하는 루트 폴더
    "outDir": "dist", // 컴파일된 파일 저장 루트. 설정 안할 시 .js 파일 옆에 생성
    "declaration": "true" // d.ts 파일 생성
    "esModuleInterop": true, // commonjs가 import를 쉽게 하게 해준다.
    "forceConsistentCasingInFileNames": true, // Ensure that casing is correct in imports.
    "strict": true, // 엄격한 타입체크 옵션을 전부 true로 한다.
    "noImplicitAny": true, // any type이 암시되면 에러를 일으킴
  }
}
```

다음과 같이 커맨드 라인에 옵션을 주어 tsconfig.json 파일을 생성할 수도 있다.

```bash
$ tsc --init --rootDir src --outDir ./bin --esModuleInterop --lib ES2015 --module commonjs --noImplicitAny true
$ npx tsc --init --rootDir src --outDir ./bin --esModuleInterop --lib ES2015 --module commonjs --noImplicitAny true # typescript 설치 안한경우 npx 이용
```

json 식으로 파일을 생성하지 않은 경우, json 형식으로 내용을 확인하려면 아래의 커맨드를 입력하면 된다.

```bash
$ tsc [COMPILING_FILE_NAME] --target es6 --module commonjs --showConfig # showconfig로 확인
```

4. 설정한 소스폴더와 출력폴더 생성

```bash
$ mkdir src
$ mkdir dist # 사실 안해도 outdir은 자동생성된다.
```

5. `tsconfig.json` 이 있는 경로에서 컴파일 실행

```bash
$ tsc
# 혹은
$ tsc [FILE_PATH]/[FILE_NAME].ts # 특정파일 컴파일
```

6. 생성된 js 파일 실행

```bash
$ node [FILE_PATH]/[FILE_NAME].js
# 혹은
$ ts-node [FILE_PATH]/[FILE_NAME].js
$ npx ts-node [FILE_PATH]/[FILE_NAME].js
```



### Non-null assertion operator

변수 뒤에 `!`을 붙여 null 혹은 Undefined가 아님을 확신한다.

```typescript
let words = ['a', 'b', 'c', 'd', 'a', 'c', 'b'];
let res:Map<string, number> = new Map();
for (let i = 0; i < words.length; i++) {
  res.set(words[i], res.has(words[i]) ? res.get(words[i])! + 1 : 1);
}
console.log(res); // Map(4) { 'a' => 2, 'b' => 2, 'c' => 2, 'd' => 1 }
```

### Object의 key값에 String을 넣지 못할 때(TS7053)

> TS7053: Element implicitly has an 'any' type because expression of type 'string' can't be used to index type 'Object'.

타입스크립트에서는 이처럼 객체의 키값에 문자열을 사용하면 컴파일 에러를 발생시킨다.

```typescript
const obj:Object = {
  foo: 'hello',
  1000: 'X'
}
console.log(obj['foo']); // TS7053 compile error
```

이것은 타입스크립트의 [Index Signatures](https://www.typescriptlang.org/docs/handbook/2/objects.html#index-signatures)문제와 관련이 있다.

즉, 프로퍼티를 인덱스로 사용하는데, 이 때 인덱스의 타입이 정확히 정의되지 않아 에러가 발생하는 것이다.

이를 가능하게 하는 방법은 직접 타입 관련 설정을 하는 `Index Signature	`를 정의하는 것이다.

1. 타입 정의

```typescript
type objType = {
  [key: string]: string
}
// or
interface ObjType = {
  [key: string]: any
}
const obj:objType = {
  foo: 'hello',
  1000: 'X'
}
console.log(obj['foo'], obj['1000']);
```

2. Index Signatures 정의

```typescript
const obj:{ [key:string]:any } = {
  foo: 'hello',
  1000: 'X'
}
console.log(obj['foo'], obj['1000']);
```

3. Record<Keys, type> utility 사용([Record](https://www.typescriptlang.org/docs/handbook/utility-types.html#recordkeys-type)참조)

```typescript
// 3. Record<Keys, type> utility 사용
// Record는 오브젝트의 키와 밸류 타입 설정을 위해 사용된다.
const obj:Record<string, string> = {
  foo: 'hello',
  1000: 'X'
}
console.log(obj['foo'], obj['1000']);
```

4. Map 사용

```typescript
const obj = new Map();
obj.set('foo', 'hello');
obj.set('1000', 'X');
console.log(obj.get('foo'), obj.get('1000'));
```

### ?와 !의 사용

- `?`는 프로퍼티가 있다면(즉, if와 같다.) 지정해준 타입을 적용하고 없으면 ` undefined`로 인식한다.
- `!`는 해당 값이 `null`혹은 `undefined`가 아님을 선언한다.

위 두가지는 구조 분해 할당을 사용할 때 유용하게 사용할 수 있는데 그 예시를 보자.

```typescript
let foo: Array<{ y?: string, x?: string }> = [{ y: 'abc', x: 'def' }];
let { y, x } = foo.shift(); // TS2339: Property 'y' does not exist on type '{ y?: string | undefined; x?: string | undefined; } | undefined'
```

위와 같은 에러가 일어나는 이유는 두가지이다.

1. `y`와 `x`가 `undefined`일 가능성
2. `foo.shift()`가 `undefined`일 가능성

첫번째는 `?`를 지워줌으로써 해결이 가능하다.

```typescript
let foo: Array<{ y: string, x: string }> = [{ y: 'abc', x: 'def' }];
let { y, x } = foo.shift(); // TS2339: Property 'x' does not exist on type '{ y: string; x: string; } | undefined'. (첫번째는 해결이 되었다.)
```

두번째는 `!`를 이용하여 구조분해할당 대상 객체가 빈 객체가 아님을 명시해주면 된다.

```typescript
let foo: Array<{ y: string, x: string }> = [{ y: 'abc', x: 'def' }];
let { y, x } = foo.shift()!; // Error가 사라진다.
```

### Vue3 사용시 ref 객체의 타입설정(TS2740)

Vue3에선 반응형을 유지하기 위해 ref를 자주 사용하게 되는데, ref 객체를 선언했을때 타입을 지정하면 이와 같은 에러에 마주하게 된다.

```markdown
Type 'Ref<never[]>' is missing the following properties from type 'ItemsProps[]': length, pop, push, concat, and 28 more.ts(2740)
const items: ItemsProps[]
```

```html
<script lang="ts">
	import { ref, onMounted } from 'vue'
	export default {
    setup () {
      const items: Array<ItemsProps> = ref([])
    onMounted(() => {
      setTimeout(() => {
        items.value = [
          { body: 'Scoped Slots Guide', username: 'Evan You', likes: 20 },
          { body: 'Vue Tutorial', username: 'Natalia Tepluhina', likes: 10 }
        ]
      }, 2000)
    }
  }
	type ItemsProps = {
  	body: string,
  	username: string,
  	likes: number
	}
</script>
```

Ref 는 내가 선언한 변수가 반응성을 유지할 수 있게 해주는데, 위처럼 ref 함수를 사용하는 경우에는 변수에 직접 타입 설정을 하게 되면 ref가 정상적으로 작동하지 않게 된다. 그래서 따로 Ref 타입을 설정해 주어야 한다.

```html
<script lang="ts">
	import { ref, type Ref } from 'vue' // type Ref를 불러온다.
  export default {
    setup () {
      const items: Ref<Array<ItemsProps>> = ref([])
    }
  }
</script>
```

위처럼 작성하게 되면, 정상적으로 작동한다.

## Node.js

### 프로세스 종료하기

노드뿐만 아니라 프로세스가 작동 중인 포트가 있으면 전부 프로세스 종료가 가능하다.

**윈도우**

```bash
$ netstat -ano | findstr 포트
$ taskkill /pid 프로세스아이디 /f
```

예를 들어 포트가 3000이고 netstat -ano | findstr 3000을 수행한 결과의 프로세스 아이디가 12345였을 경우, taskkill /pid 12345 /f를 하면 해당 프로세스가 종료된다.

**맥/리눅스**

맥이나 리눅스 운영체제에서는 다음과 같은 방법으로 프로세스를 종료할 수 있다. 터미널에 다음 명령어를 입력한다.

```bash
$ lsof -i tcp:포트
$ kill -9 프로세스아이디
```

예를 들어 포트가 3000이고 lsof -i tcp:3000을 수행한 결과의 프로세스 아이디가 12345였을 경우, kill -9 12345를 하면 해당 프로세스가 종료된다.

### This

Node.js의 This는 브라우저와는 조금 다르다.

```javascript
console.log(this); // {}
console.log(this === module.exports); // true
console.log(this === exports); // true
function whatIsThis() {
  console.log('function', this === exports, this === global);
}
whatIsThis(); // 'function' false true
```

함수 선언문 내부의 This는 `global` 객체를 가리키고, 전역에서는 `module.exports(또는 exports)객체`를 가리킨다.

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

### Express

익스프레스는 Node.js 개발을 위한 웹 프레임워크이다. 요즘은 **디노(Deno)**가 대세로 떠오르고 있지만, 디노도 익스프레스를 베이스로 하여 개발되었으므로 익스프레스를 익혀두면 디노 사용법을 쉽게 익힐 수 있다.

- Package.json 설정
  ```javascript
  // package.json
  {
    "main": "app.js", // 실행시 최초 진입할 js 파일을 설정한다.
    "scripts": {
      "start": "nodemon app"
    },
   	"dependencies": {
      "express": "^4.18.2"
    },
    "devDependencies": {
      "nodemon": "^2.0.20"
    }
  }
  ```

- 선언

  ```javascript
  // app.js
  // ES6 이전
  const express = require('express');
  const app = express();
  // 현재 페이지가 ROOT 페이지가 아닌 경우
  module.exports = {
    app
  }
  
  // ES6 이후
  import express from 'express';
  import path from 'path';
  import { fileURLToPath } from 'url';
  
  const app = express();
  const __filename = fileURLToPath(import.meta.url);
  const __dirname = path.dirname(__filename);
  // 현재 페이지가 ROOT 페이지가 아닌 경우
  export {
  	app
  }
  export default app;
  ```

  

- 변수 세팅
  ```javascript
  app.set(KEY, VALUE);
  // sample
  process.env.PORT = 3000;
  app.set('port', process.env.PORT || 3000);
  ```

- REST API
  ```javascript
  // GET 요청 예시
  app.get('/', (req, res) => {
    // 단순 문자열
    // res.send('Hello, Express')!
    // html 페이지. 위치는 package.json에 설정된 최초실행파일 기준
    res.sendFile(path.join(__dirname, '/index.html'));
  }
  ```

- 서버 실행
  ```javascript
  app.listen(PORT_NUMBER, callback);
  // 예시
  app.listen(app.get('port'), () => {
    console.log(app.get('port'), '번 포트에서 서버가 실행중입니다.');
  });
  ```

#### next()

핸들러 함수의 next()는 다음 핸들러 혹은, 다음 라우트를 불러올 때 사용한다.

```javascript
app.[HTTP_METHOD]('/', handler[, handler, ...])
```

```javascript
import express from express;
const app = express();
app.get('/', (req, res, next) => {
  console.log('Hello!');
  next();
}, (req, res, next) => {
  console.log('다음 핸들러 함수로 next를 통해 왔습니다.');
});
```

이어지는 핸들러 함수가 없다면, 다음 라우트로 이동한다.

```javascript
app.get('/', (req, res, next) => {
  console.log('Hello!');
  next(); // 다음 핸들러 함수가 없다면, 다음 라우트로 이동한다.
});
app.get('/', (req, res, next) => {
  console.log('next 통해 다음 라우트로 왔습니다.');
});
```

`route`인수를 추가하면 다음 핸들러 함수로는 가지 않고, 다음 라우트를 불러온다.

```javascript
app.get('/', (req, res, next) => {
  console.log('start!');
  next('route');
}, (req, res, next) => {
  console.log('오지 않습니다.');
});

app.get('/', (req, res, next) => {
  console.log('여기로 옵니다.');
});
```

`next()`를 사용하지 않는 경우, `res.sendFile()`, `res.send()`등으로 사용자에게 응답을 전달해주어야 사용자가 무한로딩에 빠지지 않는다.

#### Middleware

미들웨어는 요청(req)과 응답(res)의 중간에 위치하여 요청과 응답을 제어하는 역할을 한다. 잘못된 요청이 들어오면 에러를 출력하거나 요청 혹은 응답을 조작하여 보내기도 한다.

미들웨어의 일반적인 사용법은 아래와 같다.

- 미들웨어는 위에서부터 아래로 실행된다.
- next()가 없으면 다음 미들웨어가 실행되지 않고, 웹페이지가 무한로딩에 빠져 계류한다.
- 그러므로, next()를 사용하지 않을 경우 res.send() 혹은 res.sendFile() 등으로 응답을 보내야 한다.(예를 들면, express.static 같은 정적 파일을 사용할 경우)

1. `app.use`의 사용
   가장 일반적인 방식으로 

   ```javascript
   // app.use('/PATH(optional)', [middleware, [middleware, ]])식으로 작성하면 된다.
   // '/PATH'로의 모든 요청(GET, POST, PUT, PATCH, DELETE)에서 실행
   // '/PATH' 생략시 모든 요청에서 실행
   app.use((req, res, next) => {
     console.log('모든 요청에 다 실행됩니다.');
     next();
   }, (req, res, next) => {
     console.log('여기 모든 요청에 이은 다음 요청이 next()를 통해 왔네요. next()를 통해 app.get으로 갈까요?');
     next();
   });
   ```

2. app.[HTTP METHOD]

   ```javascript
   // /PATH로 시작하는 get요청에서 실행
   // app.get('/PATH', [middleware, [middleware, ...]]) 식으로 작성하며, app.[post, put, patch, delete]()도 같다.
   app.get('/', (req, res, next) => {
     console.log('GET / 요청에서만 실행됩니다.');
     next();
   }, (req, res) => {
     throw new Error('에러는 에러 처리 미들웨어로 갑니다.');
   });
   ```

3. Errors

   ```javascript
   // 에러처리의 경우 4가지의 매개변수를 갖고 있다. 사용하지 않더라도 반드시 작성해야한다.
   // 별 다른 일이 없는 경우 가장 아래에 있는 것이 좋다.
   app.use((err, req, res, next) => {
     console.error(err);
     res.status(500).send(err.message);
   });
   ```

#### routes

##### routes 접속 전 middleware 직접 생성

기존의 미들웨어를 사용할 땐 아래와 같은 방식으로 했다.

```javascript
const express = require('express');
const app = express();
app.use(...); // middleware 사용
```

routes에 접속하기 전에 로그인 여부 같은 것을 검증해주는(해당 라우터에 입장할 권한이 있는 지 체크) middleware를 직접 생성하는 것도 가능하다. 아래의 예시를 보자.

```javascript
// routes/middlewares.js
exports.isLoggedIn = (req, res, next) => { // middleware들은 사실 내부적으로 (req, res, next) => { ... }의 구조를 취하고 있다.
  
};

exports.isNotLoggedIn = (req, res, next) => { 
  ... 
};
  
// 혹은
module.exports = {
  isLoggedIn: () => {},
  isNotLoggedIn: () => {}
}
// 로 설정한다. 우선권은 항상 module.exports가 높다.
```

```javascript
// routes/post.js
// HTML 요청 METHODS 내부에 넣으면 미들웨어로서 동작한다.()
const express = require('express');
const router = express.Router();
const { isLoggedIn } = require('./middlewares');

router.post('/', isLoggedIn, (req, res) => { // POST /post/

});
```



#### POST 요청과 보안

HTTP Methods 중 하나인 POST 요청시 흔히 **데이터가 숨겨져서 보내진다**라고 알고 있지만, 사실이 아니다. 요청 후 개발자 도구의 Network 탭에서 보낸 요청 주소를 확인해보면,

![httpmethod-post](./assets/httpmethod-post.png)

이처럼 보낸 데이터가 전부 공개되어 있다. 키를 숨겨 보안성을 높이는 것은 **https 프로토콜**을 사용해서 적용한다.

#### Application/JSON 데이터와 form action 받기

POST 요청 등으로 데이터를 보냈다고 가정하자.

```javascript
const express = require('express');
const app = express();

app.post('/', (req, res) => {
  console.log(req.body) // undefined??
})
```

분명, 데이터를 보냈고 네트워크 상에 payload에서 확인이 가능함에도 서버 쪽에서 받지 못한다.
이는 express의 문제인데, express는 기본적으로 JSON 데이터를 받지 못하기 때문이다. 코드를 아래와 같이 수정하면 정상적으로 확인이 가능하다.

```javascript
const express = require('exprss');
const app = express();

// 추가
// req.body에 json 데이터를 해석하여 넣어준다.
app.use(express.json());

app.post('/', (req, res) => {
  console.log(req.body) // 정상 출력
  res.status(201).json(data) // 함수 내부에서 데이터를 가져와 json으로 보낼 때
})
```

Form action으로 데이터를 전송하는 경우는 아래의 코드를 입력하면, 그 데이터를 해석하여 req.body에 반환해준다.

```javascript
app.use(express.urlencoded({ extended: false }));
```



### 자주 사용하는 패키지

Express와 결합하여 자주 사용하는 패키지들을 소개한다.

#### mysql2

```bash
$ npm install mysql2
```

MySQL과 Node.js를 연결해주는 컨트롤러 역할의 패키지이다.

#### sequelize

##### 기본 설정

```bash
$ npm install sequelize
$ npm install -D sequelize-cli
$ npx sequelize init # models, config, migrations 등 생성
```

그리고 자신의 DB와 일치하는 라이브러리를 선택해서 깔아준다.

```bash
# One of the following:
$ npm install --save pg pg-hstore # Postgres
$ npm install --save mysql2
$ npm install --save mariadb
$ npm install --save sqlite3
$ npm install --save tedious # Microsoft SQL Server
$ npm install --save oracledb # Oracle Database
```

자바스크립트 형식의 코드로 MySQL을 다루게 해주지만 완벽한 대체는 하지 못하여 로직이 깊은 코드를 짜는 경우 MySQL을 사용해야 한다.

```json
// config/config.json
{
  "development": {
    "username": "root",
    "password": "ROOT_PASSWORD",
    "database": "DB_NAME", // 원하는 db명
    "host": "127.0.0.1", // localhost
    "dialect": "mysql" // 사용 DB
  },
  "test": {
    "username": "root",
    "password": null,
    "database": "database_test",
    "host": "127.0.0.1",
    "dialect": "mysql"
  },
  "production": {
    "username": "root",
    "password": null,
    "database": "database_production",
    "host": "127.0.0.1",
    "dialect": "mysql"
  }
}
```

```javascript
// models/index.js
// 기본 인덱스 아래와 같이 수정
const Sequelize = require('sequelize');
const env = process.env.NODE_ENV || 'development';
const config = require(__dirname + '/../config/config.json')[env];
const db = {};

const sequelize = new Sequelize(config.database, config.username, config.password, config);

// DB 연결
db.User = require('./user')(sequelize, Sequelize);

Object.keys(db).forEach(modelName => {
  if (db[modelName].associate) {
    db[modelName].associate(db);
  }
});

db.sequelize = sequelize;
db.Sequelize = Sequelize;

module.exports = db;
```

```javascript
// user db 예시
// models/user.js
module.exports = (sequelize, DataTypes) => {
  const User = sequelize.define('User', { // table명은 users가 된다.(lowercase + 's')
    email: {
      type: DataTypes.STRING(40),
      allowNull: false,
      unique: true, // 중복금지
    },
    nickname: {
      type: DataTypes.STRING(20),
      allowNull: false,
    },
    password: {
      type: DataTypes.STRING(100),
      allowNull: false,
    }
  }, { // id, createdAt, updatedAt 자동 추가됨.
    charset: 'utf8mb4', // 이모티콘 허용 + 현재 utf8 사용시 표준이 utf8mb4로 적용.
    collate: 'utf8mb4_general_ci', // 한글 저장
  });
	// 관계 정의
  User.associate = (db) => {
    // 1:N relationship Parent table
    db.User.hasMany(db.Post); // hasMany는 추가되는 건 없지만 자신이 외래키로 들어가 있는 곳에서 로우를 가져올 수 있음.(즉, 양방향 불러오기를 가능하게 함.)
  };
  return User;
}
```

```javascript
// models/post.js
module.exports = (sequelize, DataTypes) => {
  const Post = sequelize.define('Post', { // table name => lowercase + 's' => posts
    content: {
      type: DataTypes.TEXT, // 정해진 길이 없는 글
      allowNull: false,
    }
  }, {
    charset: 'utf8mb4',
    collate: 'utf8mb4_general_ci',
  });

  Post.associate = (db) => {
    // 1:N Child table(Foreign Key 전달 받음 => User테이블에 속해있음.)
    db.Post.belongsTo(db.User); // User 테이블의 Id 추가해줌(Primary Key만 외래키가 될 수 있음에 주의.)
  }
  return Post;
}
```

```javascript
// app.js express 및 sequelize 연결
const express = require('express');
const db = require('./models'); // sequelize db

// 리눅스와 맥은 MySQL을 터미널 혹은 GUI에서 따로 실행해주는 것까지 해야 한다.
db.sequelize.sync(); // db 시작(MySQL). 만약 db 생성을 안한경우, $ npx sequelize db:create 먼저 실행한다.
// 무언가 꼬여서 안되는 경우 직접 DB를 삭제하고 다시 한다.
```

##### 1:N과 N:N 관계 설정



##### 이미지 저장

이미지는 보통 **이미지 서버를 따로 두어 이미지를 저장**하고, **저장된 주소를 DB에 저장**하는 방식을 사용한다. 그 이유는, 이미지는 보통 들어가면 바뀔 일이 거의 없고, 삭제할 일도 거의 없다. 즉, 저장하면 주로 읽기만을 하게 되고 읽을 때 이미지는 용량이 크기 때문에 DB에 직접 저장한 경우 무리가 가는 경우가 잦다. 그래서 보통 이미지를 대용량 파일 스토리지(File Storage, fs)에 넣고 cdn 등을 붙여 캐싱할 수 있게 해준다. 뿐만 아니라, DB 서버가 터질 것을 우려해 서버를 여러 개 만들어 둔다고 가정할 때 서버는 전체DB를 복제하므로  이미지를 DB에 저장해 둔 경우 차지하는 용량이 상당하여 쓸데없이 용량을 낭비할 수 있다.

##### Row CRUD

```javascript
app.post('/user', async (req, res, next) => {
  try {
    // create
    const newUser = db.[DB_NAME].create({
      id: req.body.id,
      password: req.body.password
    });
    // read
    const exUser = await db.User.findOne({
      // where 안쓰면 부분 집합도 다 조회된다.
      where: {
        id: req.body.id,
      }
    });
    if (exUser) {
      return res.status(403).json({
        errorCode: 1, // 커스텀 에러코드. 에러코드의 의미를 더 상세하게 쓰기 위해 사용.
        message: '이미 존재하는 이메일입니다.'
      })
    }
  } catch(err) {
    ...
  }
});
```

##### 마이그레이션(Migration)

sequelize에선 테이블 스키마가 업데이트되거나 새로운 컬럼 등을 추가해서 model가 변경되면, 마이그레이션을 통해 업데이트 해주어야 하는데 개발 과정에선 업데이트 없이 모든 데이터를 날리고 다시 테이블을 생성하는 방법이 있다.

```javascript
// app.js
const db = require('./models');
// sequelize 사용
db.sequelize.sync({ force: true }); // 서버 재시작시 모든 데이터를 지우고 새로 생성
// 무언가 꼬여서 안되는 경우 직접 DB를 삭제하고 다시 한다.
```

하지만, 이미 배포중인 서비스라면 모든 DB를 날릴 수는 없다. 그럴 때 사용하는 것이 마이그레이션이다.

```javascript
// models/user.js
// 추가하고 싶은 내용을 먼저 작성한다.
module.exports = (sequelize, DataTypes) => {
  const User = sequelize.define('User', {
    email: {
      type: DataTypes.STRING(40),
      allowNull: false,
      unique: true, // 1. 유니크키를 추가한다고 가정하자.
    },
    nickname: {
      type: DataTypes.STRING(20),
      allowNull: false,
    },
    password: {
      type: DataTypes.STRING(100),
      allowNull: false,
    }
  }, { // id, createdAt, updatedAt 자동 추가됨.
    charset: 'utf8mb4',
    collate: 'utf8mb4_general_ci', // 한글 저장
  });

  User.associate = (db) => {

  };
  return User;
}
```

다음으로, 마이그레이션 파일을 생성한다.

```bash
$ npx sequelize migration:create --name [MIGRATION_FILE_NAME]
```

```javascript
// migrations/[DATE_TIME_NOW]-[MIGRATION_FILE_NAME].js
'use strict';

/** @type {import('sequelize-cli').Migration} */
module.exports = {
  async up (queryInterface, Sequelize) {
    // 올릴 것을 작성하고
  },

  async down (queryInterface, Sequelize) {
    // 내릴 것을 작성한다.
  }
};
```

- CRUD 예시
  ```javascript
  'use strict';
  
  module.exports = {
    async up(queryInterface, Sequelize) {
      // update
      await queryInterface.changeColumn('Users', 'email', {
        type: Sequelize.DataTypes.STRING(40),
        allowNull: false,
        unique: true,
      });
    }
  }
  ```

이후, 마이그레이션을 적용한다.

```bash
# 선작성 선 마이그레이트 됨에 유의한다.
$ npx sequelize db:migrate --debug # 문제 발생시 상세 내용을 디버깅
$ npx sequelize db:migrate:undo # 최근 마이그레이트 취소
$ npx sequelize db:migrate:undo:all # 전부 취소
```



#### nodemon

```bash
$ npm i -D nodemon
# package.json
"script": {
	"dev": "nodemon app.js" # 원래 node app.js
}
```

기본적으로 코드를 수정한 경우 서버를 재시작해야 변경 사항이 적용되는데, 개발 중에는 큰 불편함을 야기한다. 이를 실시간 적용해주는 것이 노드몬이다.

#### cors

```bash
$ npm i cors
```

CORS(교차 출처 리소스 공유) 문제를 해결하기 위한 라이브러리이다. 보통 프론트와 백엔드 그리고 DB 서버가 구분되어 있는 프로그래밍 서버 구조상 같은 URI가 아닌 다른 URI에서 데이터를 요청하게 되는데, 무분별한 접근을 막기 위해 CORS로 접근을 제한하고 있다.

```javascript
// 사용 예제
const express = require('express');
const cors = require('cors');

const app = express();
// pre-flight (요청이 진입하기 전에, 보안을 위해 미리 허가된 요청인지 요구하는 경우가 있음. 요청에 헤더 등이 추가됐을 때 등이 있음.)
app.options([대상주소], cors({ origin: '허가할 출처 주소' }));
// 전체 주소, 전체 출처(요청) 주소 허용
app.options('*', cors());
// 특정
app.options('/login', cors({ origin: 'http://localhost:3000' }));

// 요청 내 사용
app.get('/login', cors({ [options] }), (req, res) => { ... });
```

#### morgan

요청과 응답에 대한 정보를 기록해준다.

- 설치 

  `npm install morgan`

- 사용

  ```javascript
  import morgan from 'morgan';
  // 보통 맨위에 선언한다.
  app.use(morgan([ARGUMENTS]));
  // 인수는 'dev', 'combined', 'short', 'tiny', 'common' 등이 있다.
  ```

- 결과

  ```bash
  # console / morgan('dev') 기준
  GET / 500 7.409 ms – 50
  [HTTP METHOD] [ADDRESS] [HTTP STATUS CODE] [RESPONSE TIME] [RESPONSE BYTE]
  ```

#### static

정적인 파일들을 제공하는 라우터 역할을 한다. 기본적으로 제공되기 때문에 따로 설치할 필요는 없다. 정적인 파일들을 알아서 제공해주어, `fs.readFile`등으로 따로 읽어올 필요가 없는 것이 장점이며, 요청 경로에 파일이 없는 경우 **알아서 next()**를 호출한다. 만약 파일을 발견했다면 다음 미들웨어는 실행하지 않는다.

- 사용

  ```javascript
  app.use([REQUEST_PATH], express.static([REAL_PATH]))
  app.use('/', express.static(path.join(__dirname, 'public')));
  ```

  함수의 인수에 정적인 파일들이 담겨 있는 폴더를 연결해주면 된다. 위의 예제에 따르면 `./public/css/style.css`파일은 `localhost:3000/css/style.css`로 접근이 가능하다.

#### body-parser

요청의 바디(req.body)에 있는 데이터를 해석해서 추출해주는 미들웨어다. 보통 `form data / AJAX 요청`을 처리한다. 기본적으로 **내장되어 있는 express.json()**등이 있어 설치가 필수는 아니다. 단, 멀티파트(*이미지, 동영상, 파일*)은 처리하지 못하므로 이 경우 **multer**모듈을 사용한다. 역시 내장되어 있어 따로 설치할 필요는 없다.

요청의 본문이 버퍼 데이터일 경우엔, Raw 형식 / 텍스트 형식일 경우에는 Text 형식을 해석할 수 있어야 하는데, 이 경우에는 따로 설치해서 사용해야 한다.

- 설치(Optional) 및 사용

  ```javascript
  // 설치
  npm i body-parser
  // 설치가 필요한 데이터 타입의 경우
  const bodyParser = require('body-parser'); 
  app.use(bodyParser.raw());
  app.use(bodyParser.text());
  ```

  

- 사용(내장모듈)

  ```javascript
  app.use(express.json()); // JSON 데이터 해석
  // extended true시 노드 내장 모듈인 querystring 아닌 qs 모듈(설치) 사용한다는 의미이다.
  app.use(express.urlencoded({ extended: false })); // urlencoded(주소 형식) 데이터 해석
  ```

바디-파서를 사용하면 `POST, PUT` 요청 등에서 필요했던 req.on('data', callback)으로 바디에 데이터를 붙인 후, req.on('end')로 스트림을 사용할 필요없이 내부적으로 스트림을 처리하여 **바로 req.body**에 데이터가 들어간다.

#### passport

패스포트는 세션 스토리지 등을 이용하여 인증정보를 저장하거나 사용자 인증 요청을 처리하는 라이브러리이다. 플러그인 형태로 구성되어 있어 특정 로그인 방식에 맞춰 여러 플러그인을 받아 사용할 수 있다.(passport-kakao 등)

**설치**

```bash
$ npm install passport passport-local cookie-parser express-session bcrypt
```

passport는 각 로그인 별 플러그인을 **Strategy**라고 표현하며, 각 전략 별로 플랜을 세워두고, 상황에 맞는 전략을 불러와서 로그인 시도를 하게된다.

**생성**

Root에 `passport/index.js`를 생성한다. passport directory는 필수는 아니지만, 폴더 구조를 명확히 하기 위해 생성하며, `index.js`는 passport 앱을 컨트롤하는 중앙장치라고 생각하면 된다. 

```javascript
// passport/index.js
const passport = require('passport');

module.exports = () => {
  passport.serializeUser(() => {
    
  });
  passport.deserializeUser(() => {
    
  });
};
```

이후 app.js에 import 후 기본 설정을 한다.

```javascript
// app.js
// 미들웨어
const passport = require('passport');
// 직접만든 모듈
const passportConfig = require('./passport');
// session에 저장 위함
const session = require('express-session');
// 쿠키 해석용
const cookie = require('cookie-parser');

app.use(cookie('cookiesecret'));
app.use(session({
  resave: false,
  saveUninitialized: false,
  secret: 'cookiesecret', // 세션 쿠키가 암호화되어 있는데, 암호화를 해제할 수 있는 키 역할을 한다.
  cookie: {
    maxAge: 600000, // 쿠키 수명 10분
    secures: true // https 사용
  }
}));
// 실행
app.use(passport.initialize());
// 세션 저장 허용
app.use(passport.session());
// 직접 만든 패스포트 파일 실행
passportConfig();

app.use(cors({ origin: 'http://localhost:3000', credentials: true })); // headers에 인증 정보를 패스하기 위한 credentials: true
```

이후 각 로그인 방식에 맞는 **전략(strategy)**를 생성한다. 예를 들면, 사이트에서 직접 가입 및 로그인을 한다면, passport-local을 이용해서 로그인하는 것이다.

아래의 예제는 로컬 로그인 전략 예제이다.

```javascript
// passport/local.js
const passport = require('passport');
// 비밀번호 암호화
const bcrypt = require('bcrypt');
// 로컬 전략 객체
const { Strategy: LocalStrategy } = require('passport-local');
// db(MySQL 사용)
const db = require('../models');

module.exports = () => {
  passport.use(new LocalStrategy({
    // body의 property를 넣어줌.
    usernameField: 'email', // req.body.email을 의미
    passwordField: 'password', // req.body.password을 의미
    session: true, // 세션 저장여부
    // passReqToCallback:false, // express의 req 접근 가능 여부
  }, async (email, password, done) => { // 위에서 넘겨준 필드가 들어와 있다.
    try { // 서버 정지 방지 위해 실무에선 try catch가 필수.(async, await 사용시)
      // 검사
      // db에서 email있는 지 확인
      const exUser = await db.User.findOne({
        where: {
          email,
        }
      });
  
      if (!exUser) {
        // 각 에러, 성공시 반환내용(성공하는 경우 없을 시 false 반환하기), 실패시 반환할 내용 작성
        return done(null, false, { reason: '존재하지 않는 사용자입니다.' });
      }
  		// 비밀번호 비교
      const result = await bcrypt.compare(password, exUser.password);
  
      if (result) {
        return done(null, exUser);
      } else {
        return done(null, false, { reason: '비밀번호가 틀립니다.' });
      } 
    } catch (err) {
      console.error(err);
      return done(err);
    }
  }));
}
```

**연결 및 사용**

먼저, `passport/index.js`에서 전략을 연결, 실행한다.

```javascript
// passport/index.js
const passport = require('passport');
const local = require('./local');
module.exports = () => {
  passport.serializeUser(() => {
    
  });
  passport.deserializeUser(() => {
    
  });
  
  // 연결, 실행
  local();
};
```

이제 local을 통해 직접 로그인을 해보자. `app.js`에 관련 내용을 작성할 것이다.

```javascript
// app.js
...
app.post('/user/login', async (req, res, next) => {
  try {
    /* 
    	1. passport.authenticate('local', callback)(req, res, next): localStrategy에 req, res, next를 인수로 전달하여 실행 
    	2. 실행 후 결과를 strategy의 done() 함수를 통해 (에러, 성공데이터, 실패정보) 세가지를 받아 콜백 함수를 부른다.
    	3. 단계를 거치며, localStrategy의 실행 결과에 따른 반환값에 맞는 상황을 다시 return한다.
    	4. 성공한 경우, req.login()을 실행하게 된다.
    */
    passport.authenticate('local', (err, user, info) => {
      // 에러 전송시 에러 처리
      if (err) {
        console.error(err);
        return next(err);
      }
      
      // 실패시 front의 실수이므로 next(err)이 아닌 이유를 send(없는 아이디, 잘못된 비밀번호)
      if (info) {
        return res.status(401).json({
          errorCode: 2,
          message: info.reason
        });
      }
      
      // 성공시
      /*
      	1. Middleware 조작으로 (app.use(passport.initialize())) req에 login, logout이라는 메서드가 추가됨.
      	2. login 메서드가 동작할 때 passport/index.js의 serializeUser를 불러 session에 사용자 정보를 저장.
      	3. session에 [임의의 key]: [serializeUser가 돌려준 done() 성공값을 value]로 저장하고, 이 값을 login함수가 쿠키[connect.sid]:[session key]식으로 넘겨준다.
      */
      return req.login(user, (err) => {
        // 에러가 있는 경우 err에 값이 담겨 오므로, 에러 처리를 해둔다.
        if (err) {
          console.error(err);
          return next(err);
        }
        // front로 사용자 정보 res.data로 넘겨주기
        return res.status(200).json(user);
      }); // app.use(passport.initialize());에서 추가된 req methods
    })(req, res, next); // 함수 실행
    
  } catch(err) {
    console.error(err);
    return next(err);
  } // catch
}); // app.post
```

그러면, 다시 `passport/index.js`로 돌아가 serializeUser와 deserializeUser를 마저 작성하자.

```javascript
const passport = require('passport');
const local = require('./local');
const db = require('../models');

module.exports = () => {
  /*
  	1. req.login()에 의해 호출
  	2. req.login의 첫번째 매개변수가 serializeUser 콜백함수의 첫번째 매개변수로 등록된다.
  	3-1. 콜백함수의 두번째 매개변수는 done()으로, 첫번째 매개변수가 전달한 값중 세션에 등록할 값을 선택한다.
  	3-2. 값을 세션(req.session.passport.user)에 저장한다.
  	4. 여기선 오직 user.id만 등록했는데, user.id는 db내 고유값이라 유저 조회가 용이하고 + 서버의 메모리 부담을 줄이기 위해선 저장 내용을 최대한 줄이는 것이 이득이기 때문이다.
  */
  passport.serializeUser((user, done) => {
    return done(null, user.id);
  });
  
  /*
  	0. 로그인 후의 모든 요청은 deserializeUser를 거치게 된다.
  	1. serializeUser의 콜백함수의 반환함수, done()의 두번째 인자였던 user.id가 deserializeUser의 콜백함수의 첫번째 인자로 전달된다.
  	2. DB에서 받아온 아이디를 통해 유저가 있는 지 확인하고, 해당 유저가 있으면 done()함수에 보내 req.user에 그 정보를 투입하고, req.isAuthenticated() === true로 만든다.
  */
  passport.deserializeUser( async (id, done) => {
    try {
      // 백엔드는 db접속을 최대한 적게 하는 것이 최우선 과제여서 나중엔 캐싱처리를 해준다.
      const user = await db.User.findOne({ attributes: ['email', 'nickname'], where: { id: id } });
      return done(null, user);
    } catch(err) {
      console.error(err);
      return done(err);
    }
  });
  // 로컬전략 연결, 실행
  local();
}
```

로그인을 완료했으면, 이후 사이트 접속시마다 deserializeUser가 작동한다. 이때의 처리는 아래 `프런트엔드에서의 요청`항목을 확인하고, 이제 로그아웃 구현을 알아보자. 로그아웃은 **반드시 콜백함수를 써야함**에 주의하자.

```javascript
// app.js
app.post('/logout', (req, res, next) => {
  if (req.isAuthenticated()) {
    // req.logout(callbak)은 반드시 콜백함수로 다음 동작을 지정해야 한다.
    req.logout(function (err) {
      if (err) {
        return next(err);
      }
      req.session.destroy(); // 세션 없애기, 선택사항
      return res.status(200).send('로그아웃 되었습니다.');
    });
  }
});
```

**프런트엔드에서의 요청**

요청을 할 시엔, 암호화된 정보를 전송 및 응답하고 이후 `req.user`에 유저 데이터를 받아오기 위해 반드시 `withCredentials: true` config를 전달해야 한다.(쿠키를 전송하고, 프런트로 쿠키를 내려받기 위함)
서버 측에선 위에도 설명했지만 `app.use(cors({ origin: 'http://localhost:3000', credentials: true }));`를 반드시 설정해둔다.

1. 로그인을 요청한다.
   ```javascript
   // api/index.js
   import axios from 'axios';
   
   const form = {
     baseUrl: 'URL/',
   }
   // withcredentials 항상 true 설정
   // axios.defaults.withCredentials = true;
   // 예시
   /** 
     axios.get(url, {
       headers: {},
       withCredentials: true,
     });
   
     axios.post(url, data: {}, {
       withCredentials: true,
     })
   */
   async function $_getApi(url, config) {
     const data = ref(null);
     const error = ref(null);
   
     try {
       const res = await axios.get(`${form.baseUrl}${url}/`, config);
       data.value = res.data;
     } catch (err) {
       if (process.dev) {
         console.error(err);
       }
       error.value = err;
     }
   
     return { data, error } 
   }
   
   async function $_postApi(url, reqData=null, config=null) {
     const data = ref(null);
     const error = ref(null);
   
     try {
       const res = await axios.post(`${form.baseUrl}${url}`, reqData, config);
       data.value = res.data;
     } catch (err) {
       if (process.dev) {
         console.error(err);
       }
       error.value = err?.response?.data ?? { errorCode: 0, message: '서버 상에 문제가 발생했습니다.'};
     }
     return { data, error };
   }
   
   export {
     $_getApi,
     $_postApi
   }
   
   // stores/users.js
   import * as api from '@/api';
   
   export const useUsersStore = defineStore('users', () => {
     const state = reactive({
       me: null,
     });
     // 로그인 요청
     async function login(payload) {
       const { data, error } = await api.$_postApi('user/login', {
         email: payload.email,
         password: payload.password,
       }, { withCredentials: true }); // withCredentials는 필수이다.
       if (error.value) {
         console.error(error.value);
         alert(error.value);
       }
       state.me = {
         email: data.value.email,
         nickname: data.value.nickname,
       };
       await router.push('/');
     }
     
     return {
       login,
     }
   }
   ```

2. 서버에서 로그인 요청을 받아 그 로직을 처리한다.(위에 작성해둔, app.post('/user/login')함수를 참조할 것)

3. 로그인 후에는 접속할 때마다 로그인이 되어 있는 지 확인하기 위한 요청을 보낸다.
   ```javascript
   // stores/users.js
   async function onCheckLoggedIn(payload) {
       try {
         // withCredentials 필수
         const { data, error } = await api.$_getApi('user', { withCredentials: true });
         if (error.value) {
           console.error(error.value);
           alert(error.value);
         }
         if (data.value) {
           state.me = {
             email: data.value.email,
             nickname: data.value.nickname,
           }
           return true;
         }
         return false;
       } catch (err) {
         console.error(err);
         return false;
       }
     }
   ```

4. 서버는 요청을 받아 로그인이 되어있는 지 확인해준다.
   ```javascript
   app.get('/user', (req, res, next) => {
     if (req.isAuthenticated()) { // 로그인 정보가 인증되어 있다면
       // deserializeUser에서 전달받는다.
       return res.status(200).json(req.user?.dataValues); // dataValues에 유저 정보가 저장되어 있다.
     }
     return res.status(204).send();
   });
   ```

   

**전체 과정 정리**

1. 프런트에서 로그인 정보를 담아 post요청을 보낸다.
2. `app.use(express.json())`혹은 `app.use(express.urlencoded({ extended: false }))`가 프런트에서 보낸 정보를 req.body에 담아준다.
3. `passport.authenticate([STRATEGY], callback)`가 설정한 전략을 실행하고, 해당 전략에서 `req.body`를 전달받아 로그인 정보를 체크해 검사하고, 결과에 맞게 `에러/성공/실패`를 보내준다.
4. `passport.authentiacte()`의 콜백함수로 돌아와서 보내온 결과가 에러 혹은 실패인 경우 그에 맞는 값을 반환하고, 성공한 경우 `req.login()`함수를 실행한다.
5. `req.login()` 이 `passport/index.js`의 serializeUser를 불러온다. serializeUser는 값을 세션에 저장하고, req.login()은 프런트엔드에 이를 다시 가공하여 쿠키로 내려보내준다.
6. 이후 오는 모든 요청에 deserializeUser함수가 동작해서 로그인 여부를 확인해준다.

#### 캐싱처리(redis)

passport 과정에서 session을 저장했던 메모리 방식은 정보가 서버에 들어가기 때문에 서버를 종료하면 정보가 날아가게된다. 그래서 이를 저장할 때는 `redis`라는 별도의 db를 이용한다.

#### 비밀번호 암호화

많은 방법이 있지만 대표적으로 `bcrypt, scrypt, pbkdf2` 등이 있다. 여기서는 bcrypt를 예시로 들어본다.
참고로, 프런트에서부터의 암호화를 하고 싶다면 `bcrypt-js`를 사용하거나, `https`적용으로 해결할 수 있다.

```bash
# 설치
$ npm install bcrypt
```

```javascript
// app.js
const bcrpyt = require('bcrypt');

app.post('/user', async (req, res, next) => {
  try {
    // 요청의 데이터 body에 포함.
    const hash = await bcrypt.hash(req.body.password, 12);
    const newUser = await db.User.create({
      email: req.body.email,
      password: hash, // 암호화 전송
      nickname: req.body.nickname,
    })
  } catch(err) {
    ...
  }
});
  
```

```javascript
// 패스워드 일치 확인 예제
module.exports = () => {
  passport.use(new LocalStrategy({
    usernameField: 'email',
    passwordField: 'password'
  }, async (email, password, done) => {
    try { // 서버 정지 방지 위해 실무에선 try catch가 필수.(async, await 사용시)
      const exUser = await db.User.findOne({
        where: {
          email,
        }
      });
  
      if (!exUser) {
        return done(null, false, { reason: '존재하지 않는 사용자입니다.' });
      }
  		// password 일치 확인
      const result = await bcrypt.compare(password, exUser.password);
  
      if (result) {
        return done(null, exUser);
      } else {
        return done(null, false, { reason: '비밀번호가 틀립니다.' });
      } 
    } catch (err) {
      console.error(err);
      return done(err);
    }
  }));
}
```



## Git

### Semantic Commit Messages(의미론적 커밋 메세지)

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

### Github Pages 정적 사이트 배포 예시

#### 기본 방법

Settings -> pages에서 deploy 설정을 레포지토리로 한 후, 배포할 index.html 파일이 있는 repo를 설정해 배포한다.
이와 같은 경우, 본 페이지는 [USERNAME].github.io / 그 외 레포는 [USERNAME].github.io/[REPO_NAME]으로 배포된다.

#### Github Actions를 이용할 때(Vite 예시)

1. `vite.config.js`의 `base`값을 적절하게 설정한다.

   커스텀 도메인 혹은 메인페이지(`[USERNAME].github.io`)에 배포시, `base`설정을 하지 않거나, `'/'`로 하면 된다.

   그 외 레포(`[USERNAME].github.io/[REPO_NAME]`)의 경우 `base`설정값을 `'/[REPO_NAME]/'`으로 지정한다.

2. github repo에서 settings - pages 설정으로 이동 후, 배포 방식을 `Github Actions`로 지정 후(혹은 github에서 추천 옵션으로 제공하는 `static HTML`을 선택하면 아래처럼 직접 작성이 아닌 몇가지 완성된 로직을 제공한다. 내 빌드환경과 일치하는지 확인 필수) 아래와 같이 설정한다.

   아래 설정은 npm을 이용한 기본 예시임에 주의하자.

   ```bash
   # Simple workflow for deploying static content to GitHub Pages
   name: Deploy static content to Pages
   
   on:
     # Runs on pushes targeting the default branch
     push:
       branches: ['master']
   
     # Allows you to run this workflow manually from the Actions tab
     workflow_dispatch:
   
   # Sets the GITHUB_TOKEN permissions to allow deployment to GitHub Pages
   permissions:
     contents: read
     pages: write
     id-token: write
   
   # Allow one concurrent deployment
   concurrency:
     group: 'pages'
     cancel-in-progress: true
   
   jobs:
     # Single deploy job since we're just deploying
     deploy:
       environment:
         name: github-pages
         url: ${{ steps.deployment.outputs.page_url }}
       runs-on: ubuntu-latest
       steps:
         - name: Checkout
           uses: actions/checkout@v4
         - name: Set up Node
           uses: actions/setup-node@v3
           with:
             node-version: 20
             cache: 'npm'
         - name: Install dependencies
           run: npm install
         - name: Build
           run: npm run build
         - name: Setup Pages
           uses: actions/configure-pages@v5
         - name: Upload artifact
           uses: actions/upload-pages-artifact@v3
           with:
             # Upload dist repository
             path: './dist'
         - name: Deploy to GitHub Pages
           id: deployment
           uses: actions/deploy-pages@v4
   ```

3. `npm run build`는 Vite 상에서 기본적으로 `/dist`디렉토리에 배포 파일을 생성하는데, **github actions**를 통해 build를 하는 경우, 파일 경로가 전부 기본적으로 `/dist/`로 형성된다.

   ```html
   <!doctype html>
   <html lang="en">
     <head>
       <meta charset="UTF-8" />
    		<!-- REPO명은 go-sox지만, 전부 /dist/로 주소가 형성되었다. -->   
       <link rel="icon" type="image/svg+xml" href="/dist/assets/go-sox-logo-CPUPgZ4t.png" />
       <meta name="viewport" content="width=device-width, initial-scale=1" />
       <title>Go Sox</title>
       <script type="module" crossorigin src="/dist/assets/index-BovFBprn.js"></script>
       <link rel="stylesheet" crossorigin href="/dist/assets/index-BaNrfgD2.css">
     </head>
     <body>
       <div id="app"></div>
     </body>
   </html>
   ```

4. 위 예시에서 이제 문제가 발생하는데, **github pages**는 주소를 `[USER_ID].github.io/[REPO_NAME]`으로 형성하는데, 위 href에선 `/dist/`로 형성되어 있어 REPO명이 아닌 dist 주소를 통해 불러오려고 해, **js/css 파일을 불러올 수 없다.**
   (정상적으로 불러올 수 있는 주소 예시는 `https://[USER_ID].github.io/[REPO_NAME]/[JS_FILE_NAME].js`와 같다.)

5. Github Actions는 일단 `.env`파일을 Branch에 올려도 **인식하지 못하며**, 그 이전에 보안상 .env 파일을 올리는 경우는 흔치 않다. 따라서 이를 해결해야 하는데, 이를 해결하는 방법에는 두가지가 있다.

   1. 로컬에서 배포 파일을 빌드 후, 빌드한 배포 파일을 배포하기
   2. Github Repo에서 Secret 키 형성 후 이를 사용해 Github Actions로 배포하기


##### 로컬에서 빌드 후, 빌드한 파일을 repo에 올려서 gh-pages에 배포하기

1. 개발 환경에서의 환경 변수와 배포 환경에서의 환경 변수를 구분하기 위해 `.env`파일 생성하기
   ```json
   // .env.production
   // 배포 환경에서의 기본 주소
   VITE_ASSET_PATH='/go-sox/'
   
   // .env.development
   // 개발 환경에서의 기본 주소
   VITE_ASSET_PATH='/'
   ```

2. 배포 파일의 `css, js`파일의 기본 경로 설정을 위해 `base`  키 설정하기
   ```typescript
   // vite.config.ts
   import { fileURLToPath, URL } from 'node:url'
   
   import { defineConfig, loadEnv } from 'vite'
   import vue from '@vitejs/plugin-vue'
   
   // https://vitejs.dev/config/
   export default defineConfig(({ command, mode }) => {
     const env = loadEnv(mode, process.cwd(), '')
     return {
       // mode에 따른 기본 route 변경(mode는 const env 통해 현재 모드를 읽어오게 된다. config 외부에선 import.meta.env로 확인 가능)
       base: env.VITE_ASSET_PATH,
       // webpack에서 지원하는 alias 기능.
       // @로 root directory 가리키게 설정. tsconfig.json에도 설정해야 vscode에서 @/ 인식함.
       plugins: [vue()],
       resolve: {
         alias: [
           { find:'@', replacement: fileURLToPath(new URL('./src', import.meta.url))},
           // asset directory 가리키기.
           { find:'@assets', replacement: fileURLToPath(new URL('./src/assets', import.meta.url)) }
         ]
       },
     }
   })
   
   ```

3. dist 파일을 함께 github에 업로드한다.
   ```bash
   cd dist/ # 빌드 형성된 폴더로 이동
   git add . -f # dist가 .gitignore에 있으면 force 필수
   git commit -m ''
   git push <remote> <branch>
   ```

4. Github Actions를 아래와 같이 설정한다.(기본 workflow에서 **build**를 제거함. 이미 로컬에서 build해서 올렸기 때문)
   ```yaml
   # Simple workflow for deploying static content to GitHub Pages
   name: Deploy static content to Pages
   
   on:
     # Runs on pushes targeting the default branch
     push:
       branches: ['master']
   
     # Allows you to run this workflow manually from the Actions tab
     workflow_dispatch:
   
   # Sets the GITHUB_TOKEN permissions to allow deployment to GitHub Pages
   permissions:
     contents: read
     pages: write
     id-token: write
   
   # Allow one concurrent deployment
   concurrency:
     group: 'pages'
     cancel-in-progress: true
   
   jobs:
     # Single deploy job since we're just deploying
     deploy:
       environment:
         name: github-pages
         url: ${{ steps.deployment.outputs.page_url }}
       runs-on: ubuntu-latest
       steps:
         - name: Checkout
           uses: actions/checkout@v4
         - name: Set up Node
           uses: actions/setup-node@v3
           with:
             node-version: 20
             cache: 'npm'
         - name: Install dependencies
           run: npm install
         - name: Setup Pages
           uses: actions/configure-pages@v5
         - name: Upload artifact
           uses: actions/upload-pages-artifact@v3
           with:
             # Upload dist repository
             path: '${{ github.workspace }}/dist/'
         - name: Deploy to GitHub Pages
           id: deployment
           uses: actions/deploy-pages@v4
   ```

   

##### Secret 키 형성으로 env 환경 변수 사용해서 배포하기

1. 배포 파일을 따로 build하지 않은 채로 일반적으로 repo에 업로드한다.

2. github REPO 페이지에서 `settings - security - secrets and variables - actions`로 이동해서, `New repository secret`을 클릭해 새 비밀을 생성한다.
   Name은 **VITE_KEY_NAME**(VITE이므로, VITE로 시작. 개발 환경에 맞게 수정할 것), Secret은 Value를 작성하되, `''`는 작성할 필요없다.

   ```json
   // 예시
   Name
   VITE_ASSET_PATH
   Secret
   /[REPO_NAME]/
   // repo명이 go-sox인 경우
   /go-sox/ O
   '/go-sox' X
   ```

3. 다음과 같이 시크릿을 적용해서 env를 불러오기 때문에 workflow에서 빌드가 가능해서 빌드 파일을 repo에 올릴 필요가 없다.
   ```yaml
   # Simple workflow for deploying static content to GitHub Pages
   name: Deploy static content to Pages
   
   on:
     # Runs on pushes targeting the default branch
     push:
       branches: ['master']
   
     # Allows you to run this workflow manually from the Actions tab
     workflow_dispatch:
   
   # Sets the GITHUB_TOKEN permissions to allow deployment to GitHub Pages
   permissions:
     contents: read
     pages: write
     id-token: write
   
   # Allow one concurrent deployment
   concurrency:
     group: 'pages'
     cancel-in-progress: true
   
   jobs:
     # Single deploy job since we're just deploying
     deploy:
       environment:
         name: github-pages
         url: ${{ steps.deployment.outputs.page_url }}
       runs-on: ubuntu-latest
       steps:
         - name: Checkout
           uses: actions/checkout@v4
         - name: Set up Node
           uses: actions/setup-node@v3
           with:
             node-version: 20
             cache: 'npm'
             
         - name: Install dependencies
           run: npm install
         - name: Build
           run: npm run build
           # 환경 변수 사용
           env:
             VITE_ASSET_PATH: ${{ secrets.VITE_ASSET_PATH }}
         - name: Setup Pages
           uses: actions/configure-pages@v5
         - name: Upload artifact
           uses: actions/upload-pages-artifact@v3
           with:
             # Upload dist repository
             path: '${{ github.workspace }}/dist/'
         - name: Deploy to GitHub Pages
           id: deployment
           uses: actions/deploy-pages@v4
   ```

   

#### Vue 예시

1. `vue.config.js`에서 `publicPath`혹은`baseUrl(구버젼)`을 설정하는데, **vite**와는 **다른 점**이 있다.

   ```javascript
   const { defineConfig } = require('@vue/cli-service')
   module.exports = defineConfig({
     // 아래처럼, 배포 시에는 주소를 다르게 설정해 주어야 하는데,
     // npm run build를 사용시 production 환경에 맞는 주소를 이어붙여서 빌드해 주는데,
     // 예를 들면 css의 src가 기본은 '/'이다가, 배포시엔 앞에 '/[원하는기본주소]/'를 붙여서 작성해주게 된다.
     // [GITHUB_ID].github.io/[REPO_NAME]에 배포한다고 했을 때, 이 레포명이 없으면 배포 후
     // src가 [GITHUB_ID].github.io/[REPO_NAME]/ 경로가 아닌
     // [GITHUB_ID].github.io/ 경로에서 찾게 되어 css, js 파일을 찾을 수 없기 때문에
     // 하얀 화면을 맞이하게 된다.
     // 즉, 빌드시엔 레포명을 추가해주어 빌드했기 때문에 정상적으로 css와 js 파일 로드가 가능해진다.
     publicPath: process.env.NODE_ENV === 'production' ? '/[REPO_NAME]/' : '/',
     transpileDependencies: true
   })
   ```

2. 설정에서 Pages -> Github Actions를 설정해준다. 설정에 들어가면 `staticHTML` 옵션을 기본적으로 제공해주는데, 이를 사용해서 `path`만 변경해줘도 된다.

   ```bash
   # Simple workflow for deploying static content to GitHub Pages
   name: Deploy static content to Pages
   
   on:
     # Runs on pushes targeting the default branch
     push:
     	# 사용하는 branch명
       branches: ["master"]
   
     # Allows you to run this workflow manually from the Actions tab
     workflow_dispatch:
   
   # Sets permissions of the GITHUB_TOKEN to allow deployment to GitHub Pages
   permissions:
     contents: read
     pages: write
     id-token: write
   
   # Allow only one concurrent deployment, skipping runs queued between the run in-progress and latest queued.
   # However, do NOT cancel in-progress runs as we want to allow these production deployments to complete.
   concurrency:
     group: "pages"
     # 중복 배포 등을 피하려면 true로 하면된다.
     cancel-in-progress: false
   
   jobs:
     # Single deploy job since we're just deploying
     deploy:
       environment:
         name: github-pages
         url: ${{ steps.deployment.outputs.page_url }}
       runs-on: ubuntu-latest
       steps:
         - name: Checkout
           uses: actions/checkout@v4
         - name: Setup Pages
           uses: actions/configure-pages@v4
           # 설정한 폴더 내의 내용을 하나의 압축파일로 만든다. 이를 이용해 배포속도를 높인듯?
         - name: Upload artifact
           uses: actions/upload-pages-artifact@v3
           with:
           	# vue의 경우 파일이 root/dist 폴더에 배포되어 root/dist 폴더로 설정했지만, 
           	# 개발환경에 맞게 변경해서 사용하면 된다.
             path: '${{ github.workspace }}/dist/'
         	# artifact 압축 파일을 전달받아 배포한다.
         - name: Deploy to GitHub Pages
           id: deployment
           uses: actions/deploy-pages@v4

#### Netlify CLI 예시

```bash
# Install the Netlify CLI
$ npm install -g netlify-cli

# Create a new site in Netlify
$ ntl init

# Deploy to a unique preview URL
$ ntl deploy
```



### Git Add를 취소할 때

`git reset HEAD`

### Git 오래된 커밋 없애기(Git Branch 새로 생성해서 옮기는 방식)

```bash
git checkout --orphan [TEMP_BRANCH_NAME] # git branch 생성
git add . # 저장소 add
git commit -m 'commit message' # commit
git branch -D [BRANCH_NAME] # old branch 삭제
git branch -m [BRANCH_NAME] # 새로 생성한 branch name 변경(master등 삭제한 기존 브랜치명)
git push -f origin [BRANCH_NAME] # force push
```



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

> [https://docs.npmjs.com/](https://docs.npmjs.com/)

- 개발자용 Package 설치
  ```bash
  npm i -D 'PACKAGE_NAME'
  ```

### 전역 패키지 경로

```bash
/usr/local/bin/lib/node_modules/ # macOS
```



### 구버젼 패키지 확인

```bash
npm outdated # 업데이트 가능 확인
```

- 업데이트
  ```bash
  npm update [package name(optional)] # update package to wanted version.
  ```

### 패키지 검색

```bash
npm search ${PACKAGE_NAME}
```

### 패키지 상세정보

```bash
npm info ${PACKAGE_NAME}
```



### Prefix 경로 확인

전역 npm_modules의 위치를 확인한다.

```bash
npm root -g
```

### 취약 패키지 확인

보안에 심각한 취약점을 가지고 있는 패키지를 확인한다.

```bash
npm audit
#  자동 수정
npm audit fix
```

### package-lock.json과 package.json

**package-lock.json**

내가 설치한 패키지들에도 사용하는 패키지들이 있을 수 있다. 이 패키지들의 버전과 의존 관계를 표현해 기록해 두는 역할을 한다.

**package.json**

내 패키지들에 관련된 정보와 의존성 등을 기록한 json파일이다.

### 인스톨 명령어

> https://docs.npmjs.com/cli/v8/commands/npm-install

```bash
# devDependencies에 패키지를 추가한다. npm build --production 혹은 npm install --production시 devDependencies의 패키지는 추가되지 않는다.
npm install package --save-dev === npm install package --D
# package.json에 패키지 추가. 기본 옵션으로 적용되어 있다.
npm install --save
# packge.json에 추가하지 않음.
npm install --no-save
# 기재한 version의 패키지 추가
npm install package@${version}
# 현재 워킹 디렉토리가 아닌 prefix 폴더에 추가(전역 설치)
# macOS의 경우
# /usr/local/lib/node_modules
# 윈도우의 경우
# c:\Users\%USERNAME%\AppData\Roaming\npm\node_modules
npm install -g === npm install --global# deprecated
sudo npm install --location=global # mac은 전역 설치시 관리자 권한이 필수다.
# package-lock.json에 의존하여 설치
# 더 엄격한 버젼 통제 가능.
npm ci
```

### package.json 모듈 전역 설치처럼 사용하기

```bash
npm [module name] ${commands}
```

### package.json 버젼관리

```bash
# 현재 패키지 및 모든 의존 패키지 버젼
npm version
# 현재 패키지 메이저 버젼 상승 / 하위 호환 불가능
npm version major # 0.1.1 => 1.0.0
# 현재 패키지 마이너 버젼 상승 / 메이저 버젼간 호환 가능한 수준의 업데이트
npm version minor # 1.0.1 => 1.1.0
# 현재 패키지 패치 버젼 상 / 기존 기능 버그 수정
npm version patch # 0.0.9 => 0.0.10
# deprecated 경고 메세지 출력. 자신의 패키지에만 적용 가능.
npm deprecate [package name] [version] [message]
```

```javascript
// 혹은 package.json
{
  "name": "test-package",
  "version": "0.0.1", // 직접 수정
  ...,
  },
}
```

```bash
npm install package@^1.4.6 # 1.4.6 <= ver < 2.0.0
npm install package@~4.18.2 # 4.18.2 <= ver < 4.19.0
npm install package@1.17.x # 1.17.0 <= ver < 1.18.0
npm install package@>1.1.1 # ver > 1.1.1 / >, >=, =, =<, <
npm install package@latest # latest version
npm install package@x # latest version
npm install package@next # latest version including alpha or beta ver.
```

### 로그인 및 개인정보 관리

```bash
npm adduser # 로그인
npm whoami # 로그인한 유저 확인
npm logout # adduser로 로그인한 유저 로그아웃
```

### 배포

```bash
npm publish # 자신이 생성한 패키지 배포
npm unpublish [package name]# 배포한 패키지 제거. 24시간 이내 배포한 패키지만 제거 가능
npm unpublish [package name] --force # 72시간 내 가능. 배포한 패키지 영구 삭제.
npm owner ls [package name] # 패키지명 소유자 확인
```

### 패키지 배포 예시

1. root 폴더 내 `npm init -y` 후 package.json 작성

   ```javascript
   {
     "name": "vuejs-slider",
     "version": "0.0.3",
     "description": "Simple Slider for Vue.js",
     "scripts": {},
     "keywords": [
       "slider",
       "vue",
       "carousel",
       "slide",
       "slideshow"
     ],
     "repository": {
       "type": "git",
       "url": "https://github.com/WonhyeokJung/vue-slider.git"
     },
     "author": {
       "name": "WonhyeokJung",
       "url": "https://WonhyeokJung.github.io"
     },
     "license": "MIT",
     "bugs": {
       "url": "https://github.com/WonhyeokJung/vue-slider/issues",
       "email": ""
     }
   }
   ```

2. 사용할 패키지명 중복 확인

   ```bash
   npm info <Package_Name>
   ```

3. terminal에서 npm 로그인

   ```bash
   npm login / npm whoami / npm logout
   ```

4. root 폴더 README.md / LICENSE / .gitinore 추가(Optional)

5. 배포 전 테스트(Optional)

   - 다른 폴더 생성후 `npm init / npm install <PACKAGE_PATH>`(package.json 있는 root 폴더) 실행
   - 이후 코드 정상작동 되는 지 확인

6. 배포

   ```bash
   npm publish
   ```

7. 사용

   ```bash
   npm install <PACKAGE_NAME> // 상위 예시의 경우 vuejs-slider
   ```

### npx?

보통 패키지를 전역이 아닌 프로젝트 별로 관리하는데, 이런 경우 명령어를 전역에서 사용하지 못하는 경우가 있다. 이런 경우를 대비해 `npx [명령어] ...` 형태로 코드를 입력하게 되면 지역에 설치한 패키지의 명령어를 전역에 설치한 것처럼 사용할 수 있게 된다.

### Github Actions 이용한 CI/CD 자동화

프로젝트가 커질수록 빌드와 배포가 오래 걸리는데, github actions를 이용하면 일종의 github 가상머신 내에서 자동으로 빌드와 배포를 구축할 수 있다. 아래의 예시는 간단하게 README.md 파일을 업데이트하는 예시이다.

1. 먼저 github repo에 들어가 **actions** 항목에서 yml 파일을 작성한다.

```yaml
# main.yml 명칭은 목적에 맞게 자유롭게 수정한다.
name: Update Readme
on: # pull, push 조건에 맞게 발생시 jobs 실행
  push:
    branches:
      - master
  pull_request:
  	branches:
  		- master
# on: [push]
jobs:
  build:
    runs-on: ubuntu-latest # 가상머신 환경
    steps: # 실행순서
      - uses: actions/checkout@master # 해당 레포에 접근할 수 있는 action
      # 특정 노드 버젼 설치, 필수는 아니며 없이도 npm 사용은 여전히 가능하다.
      - name: Use Node.js 16.x
        uses: actions/setup-node@v3
        with:
          node-version: 16.x
          cache: npm # npm, pnpm, yarn 등에서 선택 가능
      - run: npm ci # npm install과 달리 node_modules를 쓰지 않음. 다만 package_lock.json을 이용
      - name: Compile .ts file
        run: | # npx의 사용도 가능하다. 혹은 패키지로 typescript 설치 후 그냥 tsc도 가능하다.
          npx tsc
      - name: Update README.md
        run: |
          node tsBuild/update-readme.js
      - name: commit
        run: |
        # 여러개의 커맨드 실행도 가능하다.
          git add .
          git config --global user.name 'WonhyeokJung'
          git config --global user.email 'wonhyeok.contact@gmail.com'
          git commit -m '[docs] auto-update README.md'
      - name: push
        run: |
          git push
          

```

빌드가 필요한 경우, `Update README.md`부터를 아래의 코드처럼 구성해주면 된다.

```yaml
- run: npm run build
- name: deploy
	run: |
		deploy 명령어 실행..
```



### npm ci / npm install

npm install은 package_lock.json 파일을 생성하고, package.json 파일을 변경하면서 node_modules에 패키지들을 설치한다.

npm ci는 **package_lock.json** 파일을 참조하여 패키지를 설치하고 version 매칭에만 package.json을 활용한다. 따라서, `node_modules/`를 사용하지 않는 CI/CD 환경에서는 npm ci가 더 적합하며, 빠른 속도를 기대할 수 있다.

### npm audit fix --force 되돌리기

npm audit fix --force 시에 각 패키지 간에 의존성 문제를 강제로 해결하는데, 이걸 하는 경우 오히려 패키지 간의 의존성에 치명적인 문제가 발생하거나, 프로그램 상에 오류가 발생할 가능성이 있다. 이와 같은 경우를 대비해 **반드시 git에 미리 패키지를 업데이트하고 진행**하거나 npm audit fix --force를 진행하지 않는 것이 좋다. 보통 **npm update --force**를 진행한 경우, 치명적인 의존성 문제는 거의 해결되었을 가능성이 높기 때문이다. 어찌됐건 문제를 해결하는 방법은 아래와 같다.
```bash
$ git restore package-lock.json
$ git restore package.json
$ npm install
$ npm update [--force] [--legacy-peer-deps]
```

## Vue

### Vue3 Computed에 Parameter 투입하기

**고차함수(higher-order function)**, 즉 함수로 함수를 리턴하는 구조를 사용한다.

```vue
<script setup lang="ts">
  const arr = [
    {
      a: 'b',
      b: 'c'
    },
    {
      b: 'c',
      c: 'd'
    }
  ]
  // 일종의 이중함수처럼 형성된다
	const something = computed(() => (Param:string) => arr.filter((obj) => obj[Param]).length)
</script>
<template>
	<div>
    {{ soemthing('a') }}
  </div>
</template>
```



### Provide / Inject



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

### npm

- RC: rc(Release Candidate) 출시 직전 패키지.

## VSCODE

- 같은 줄 내 같은 단어 선택 : `CTRL + D`
- 페이지 내 전체 같은 단어 선택: `CTRL + SHIFT + L`
- 설정 관련 주소창 `F1` 혹은 `CTRL + SHIFT + P`



## MySQL

### 설치 및 저장된 경로

```bash
$ brew install mysql
$ brew cask install mysqlworkbench # 시각화 도구(콘솔로 진행할 시 불필요)
# 저장경로
/opt/homebrew/Celler/mysql
```

### 실행 및 보안설정

```bash
$ brew services [start/restart/stop] mysql # MySQL [시작/재시작/종료](백그라운드에서 계속 실행됨에 유의)
$ brew services list # 서비스 리스트
$ mysql_secure_installation # root 비밀번호 설정
```

### 접속

```bash
$ mysql -h localhost -u root -p # root 계정 접속
```

### 접속 후 비밀번호 변경

```mysql
mysql> ALTER user 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY [변경할 비밀번호];
```



### DB 생성

```mysql
# 접속 선행 필수
# SCHEMA === DATABASE 의미
CREATE SCHEMA `DB_NAME` DEFAULT CHARACTER SET UTF8MB4; # ; === 입력 완료 및 실행
```

### DB 확인

```mysql
mysql>SHOW DATABASES;
```

### DB 사용

```mysql
USE [DATABASE_NAME];
```

### 사용 중인 DB 확인

```mysql
SELECT DATABASE();
```

### DB 삭제

```mysql
DROP DATABASE `DB_NAME`;
```

### 테이블 생성

```mysql
# users 테이블 생성
CREATE TABLE nodejs.users (
  # id ~ created_at까지 columns 생성 / 각 컬럼 하나는 field라고 칭함.
  # 정수 / NULL 금지 / 자동 숫자 증가(즉, 아이디 += 1 부여)
  -> id INT NOT NULL AUTO_INCREMENT, # enter시 자동으로 -> 출력됨.(실행문이 안끝났음을 알림.)
  # 가변 길이 문자열(0~20) 고정 길이 CHAR() -> 길이 부족시 자동으로 공백 들어감.
  -> name VARCHAR(20) NOT NULL,
  # 정수(-2147483648~2147483647) / 음수 무시 
  -> age INT UNSIGNED NOT NULL,
  # -128부터 127까지의 정수. 1 또는 0 저장시 boolean
  -> married TINYINT NOT NULL,
  # 수백자 넘는 글자
  -> comment TEXT NULL,
  # 날짜(DATE) + 시간(TIME) / 현재시간 now() => CURRENT_TIMESTAMP도 같은 동작.
  -> created_at DATETIME NOT NULL DEFAULT now(),
  # 기본키. row를 대표하는 고유한 값.
  -> PRIMARY KEY(id),
  # 고유해야 하는 값(id 등) / INDEX 명(name_UNIQUE) / (컬럼 오름차순)
  -> UNIQUE INDEX name_UNIQUE (name ASC))
  # 테이블에 대한 보충 설명
  -> COMMENT = '사용자 정보'
  # 기본 문자열 인코딩
  -> DEFAULT CHARACTER SET = utf8mb4
  # 엔진(줄로 MyISAM, InnoDB 사용)
  -> ENGINE = InnoDB;
  
  # 그 외..
  # ZEROFILL 자릿수 고정. INT(4)에 1 할당시, 빈자리 0 자동입력 => 0001
```

```mysql
# 외래키를 가지는 테이블 comments 예시
mysql> CREATE TABLE nodejs.comments (
  -> id INT NOT NULL AUTO_INCREMENT,
  -> commenter INT NOT NULL, # 댓글 쓴 사용자 아이디
  -> comment VARCHAR(100) NOT NULL,
  -> created_at DATETIME NOT NULL DEFAULT now(),
  -> PRIMARY KEY(id),
  -> INDEX commenter_idx (commenter ASC),
  # CONSTRAINT [제약조건명]
  -> CONSTRAINT commenter
  # FOREIGN KEY [Field(Column)명]
  -> FOREIGN KEY (commenter) # commenter field는 외래키로 nodejs.users의 id(댓글작성자 아이디)를 사용할 것임을 선언.
  # REFERENCES [참고하는 Field(Column)명] => PRIMARY KEY여야 한다.
  -> REFERENCES nodejs.users (id)
  # 사용자 정보가 수정되거나 삭제된 경우 연결된 댓글도 삭제(CASCADE)
  -> ON DELETE CASCADE
  -> ON UPDATE CASCADE)
  -> COMMENT = '댓글'
  -> DEFAULT CHARSET=utf8mb4
  -> ENGINE=InnoDB;
```

### TABLE 확인

```mysql
SHOW TABLES;
```

### 특정 테이블 SCHEMA 확인

```mysql
DESC [TABLE_NAME];
```

### CRUD
#### 데이터 생성(Create)

```mysql
INSERT INTO [테이블명] ([컬럼1], [컬럼2], .. .) VALUES ([값1], [값 2], ...);
```

```mysql
mysql> INSERT INTO nodejs.users (name, age, married, comment) VALUES ('foo', 30, 0, 'Hi');
# 혹은 USE nodejs를 했다면
mysql> INSERT INTO users (name, age, married, comment) VALUES ('foo', 30, 0, 'Hi');
# commenter는 기본키를 참조하는 외래키이므로, 기본키 값이 일치하지 않거나 존재하지 않으면 에러가 발생한다.
mysql> INSERT INTO comments (commenter, comment) VALUES (1, 'foo의 댓글입니다.');
```

#### 테이블 내 데이터 조회(Read)

```mysql
SELECT [FIELD(COLUMN)_NAME] FROM [TABLE_NAME] WHERE [CONDITION];
```

```mysql
# 예시
mysql> SELECT name, married FROM users;
mysql> SELECT * FROM users; # 전체선택
mysql> SELECT * FROM users WHERE married = true AND age > 30;
# 나이 오름차순/내림차순 조회 / 출력 행수 설정 / 건너뛸 숫자(페이지네이션 등 활용)
mysql> SELECT * FROM users ORDER BY age ASC/DESC LIMIT 1 OFFSET 1;
```

#### 데이터 수정(Update)

```mysql
UPDATE [TABLE(FIELD)_NAME] SET [COLUMN_NAME = '바꿀 내용'] WHERE [CONDITION];
```

```mysql
# 예시
UPDATE nodejs.users SET comment = '코멘트 내용 변경해봅니다.' WHERE id = 1;
```

#### 데이터 삭제(Delete)

```mysql
DELETE FROM [TABLE(COLUMN)_NAME] WHERE [CONDITION]
```

```mysql
# 예시
mysql> DELETE FROM nodejs.users WHERE id = 2; # 위 예시 코멘트 예시에 따라 코멘트가 있는 경우 코멘트도 삭제.
```



## MongoDB

### 설치 및 저장경로

```bash
$ brew tap mongodb/brew
$ brew install mongodb-community
# 저장경로
/opt/homebrew/Celler/mongodb # 원본
/opt/homebrew/var/mongodb # Data Directory
/opt/homebrew/etc/mongod.conf # Configuration file(설정용)
/opt/homebrew/var/log/mongodb # Log directory
```

### 조회 및 실행

```bash
$ brew services list # 조회
$ brew services [start/restart/stop] mongodb-community # 실행/재실행/정지
$ mongo # < @6.0
$ mongosh # >= @6.0
```

### 관리자 계정 설정

```bash
# MongoDB
test> use admin # admin 전환
# root === 모든권한
db.createUser({ user: '이름', pwd: '비밀번호', roles: ['root'] }) # 계정추가
# 몽고디비 정지후
$ vim /opt/homebrew/local/etc/mongod.conf
# Vim에 추가
security:
  authorization: enabled
# Vim 종료 후
$ brew services start mongodb-community
$ mongosh admin -u [이름] -p [비밀번호] # 접속, WonhyeokJung
```

### 컴퍼스

몽고디비를 위한 GUI 도구로, 시각화 도구가 필요하지 않으면 사용할 필요는 없다.

### RDBMS와의 용어 비교

| MongoDB    | RDBMS    |
| ---------- | -------- |
| Database   | Database |
| Collection | Table    |
| Field      | Column   |
| Document   | Row      |
|            | Join     |

### DB 생성 및 조회

```
use [DB_NAME] # 생성
show dbs # 조회(컬렉션이 없으면 뜨지 않는다.)
```

### 컬렉션(MySQL의 테이블) 생성 및 조회

컬렉션을 따로 생성하지 않아도 몽고디비에서는 **다큐먼트(데이터, row)**를 삽입할 때  컬렉션이 없다면 컬렉션을 **자동으로 생성**해주지만, 컬렉션 생성이 가능하긴 하다.

```mysql
db.createCollection('users') # 생성
db.[COLLECTION_NAME].[insertOne, replaceOne]({ key:value, ... }) # 컬렉션 없을 시 자동 생성
show collections # 조회
```

### 다큐먼트(RDBMS의 row) CRUD

> 다큐먼트는 MySQL의 rows 즉, 데이터와 동일한 의미를 가진다.

MongoDB에서는 컬럼(Field)의 정의가 필요없다. 따라서, 자유롭다는 장점이 있지만 무엇이 들어올지 모른다는 단점도 있다.

#### Create(생성)

```mysql
# 다큐먼트 추가
> db.[COLLECTION_NAME].[insertOne, replaceOne]({ key:value, key:value, .... });
# 예시
> db.[COLLECTION_NAME].[insertOne, replaceOne]({ name: 'foo', age: 32, married: true, comment: '컬렉션 이름이 제멋대로여도 다 들어갑니다..', createdAt: new Date() });
# 관계 키 설정
# 1. 유저 조회 (_id 기본값)
> db.users.find({ name: 'foo' }, { _id: 1 })
> { "_id" : ObjectId("조회된아이디") } # 조회 결과
> db.comments.save({ commenter: ObjectId('조회된아이디'), comment: '안녕하세요. 댓글입니다.', createdAt: new Date() });
```

#### Read(조회)

```mysql
# 조회(조건/조건에 부합하는 다큐먼트 중 출력할 컬럼값/옵션)
db.[COLLECTION_NAME].find(query, projections, options);
# greater than 30(30세 초과), 혼인
db.comments.find({ age: { $gt:30 }, married: true })
# 그 외 $gt(초과), $gte(이상), $lt(미만), $lte(이하), $ne(같지 않음), $or(또는), $in(배열 요소 중 하나), $or 등이 있다.
db.users.find({ $or: [{ age: { $gt: 30 } }, { married: false }] }, { _id: 1, name: 1, age: 0}); # 아이디와 네임은 출력, 나이는 비출력 => Error. 포함과 제외를 혼용할 수 없음.(단, _id만 예외)
db.users.find({ $or: [{ age: { $gt: 30 } }, { married: false }] }, { _id: 1, name: 0, age: 0}) # 에러없이 잘 나온다.
# 정렬 1 오름차순, -1 내림차순
db.users.find({}, { _id: 0, name: 1, age: 1 }).sort({ age: -1 }) # 내림차순
# 조회할 숫자 설정
db.users.find({}, { _id: 0, name: 1, age: 1}).sort({ age: -1 }).limit(1);
# 특정 자료 개수 건너뛰기
db.users.find({}, { _id: 0, name: 1, age: 1 }).sort({ age: -1 }).limit(1).skip(1)
```

#### Update(수정)

```mysql
# 기본 형태
db.[COLLECTION_NAME].[updateOne, updateMany, bulkWrite]({ 대상 }, { 변경내용 });
# $set => 일부 필드만 수정하고자 할 때 / 없을 시 통째로 수정
db.users.[updateOne, updateMany, bulkWrite]({ name: 'foo' }, { $set: { comment: '변경해봅시다.' } });
```

#### Delete(삭제)

```mysql
# 기본형
db.[COLLECTION_NAME].[deleteOne, deleteMany, findOneAndDelete, or bulkWrite.]({ key:value }); # 지우고 싶은 값을 인수로.
```



## Mac

### Safari

#### 단축키

| 단축키                       | 상세설명                                     |
| ---------------------------- | -------------------------------------------- |
| Control + 왼쪽/오른쪽 화살표 | 화면 전환(전체 화면으로 사용중인 앱 있을 때) |
| Fn + backspace               | Delete                                       |



### 업데이트 후 터미널 명령어가 안될 때

git 등의 명령어가 실행되지 않을 경우가 있다. 이 때 터미널에 아래를 입력하여 설치해준다.

```bash
$ xcode-select --install
```



### Homebrew

#### 설치

```bash
$ /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
# 환경변수 설정
$ echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/<USER_ID>/.zprofile # 혹은 [>> ~/.zprofile]
# zsh 아닌 bash 사용시 환경변수 설정
$ echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.bash_profile
# 설정 후 실행
$ eval "$(/opt/homebrew/bin/brew shellenv)" # 현재 사용중인 쉘에 브루파일 경로 적용
# 이후 홈브루 사용 예제
$ brew install [PACKAGE_NAME] # formulae 설치
$ brew list # 설치 formulae 리스트
$ brew uninstall [PACKAGE_NAME] # 삭제
# Cask
$ brew install  --cask [APPLICATION_NAME]
$ brew list --cask # 설치 cask 리스트
$ brew uninstall --cask [APPLICATION_NAME] # 삭제
```

#### brew 업데이트

```bash
$ brew update
```

#### Formulae와 Cask 차이

- Formulae는 흔히 설치하는 npm 패키지처럼 터미널 인스톨 후 직접 사용할 수 있는 패키지들이다.
- Cask는 Chrome 등의 GUI 기반 어플리케이션을 brew를 통해 인스톨해서 사용하고자 할 때 사용한다.(dmg 기반 파일을 applications에 드래그앤 드롭해서 이용하기 싫은 경우 이용한다.)
  애플리케이션을 직접 찾아 이용하기 불편한 점이 있어 비추천한다.

#### 기본 패키지 설치 경로 및 기타 저장 경로

```bash
$ /opt/homebrew/Cellar
# 원본
/usr/local/Celler/ # 과거
/opt/homebrew/Celler/ # 현재
# Data Directory
/usr/local/var/ # 과거
/opt/homebrew/var/ # 현재
# Configuration file(설정용)
/usr/local/etc/ # 과거
/opt/homebrew/etc/ # 현재
# Log directory
/usr/local/var/log/ # 과거
/opt/homebrew/var/log/ # 현재
```

#### 원하는 패키지를 brew 전체 패키지 목록에서 찾기

```bash
$ brew search [PACKAGE_NAME]
```

#### 전역 설치 목록 보기

```bash
$ brew list
```

### Keyboard Shortcut

| 기능                  | 단축키                  |
| --------------------- | ----------------------- |
| 숨김 폴더 보기/숨기기 | Cmd + Shift + Period(.) |



### Terminal

#### 숨김파일 보기

```bash
ls -a
```

#### 환경 변수 설정

환경 변수는 mac의 경우 **Users/[USER_NAME]/**으로 이동하면 설정파일을 확인할 수 있는데, 그곳을 통해 설정을 진행할 수 있다.

내부에 있는 파일들의 내용을 간략히 알아보자.
```bash
node_repl_history	
Application 
Support
.npm
Applications
.CFUserTextEncoding
.npmrc # npm 설정
Desktop
.DS_Store
.nuxtrc
Documents
.Trash
.viminfo
Downloads
.bash_history # bash 콘솔에 입력했던 명령어 기록
.vscode
Library
.degit
.vuerc
Movies
.gitconfig # email, name 등 git config로 입력한 정보 저장
.yarnrc
Music
.lesshst
.zprofile # zsh 설정. 환경변수 설정을 여기에서 진행.
Pictures
.mongodb # mongodb 사용 기록
.zsh_history # zsh 콘솔에 입력했던 명령어 기록
Public
.mysql_history # MySQL 콘솔에 입력했던 명령어 기록
.zsh_sessions
node_modules
```



```bash
# Users/[USER_NAME]/
# bash의 경우
$ chsh -s /bin/bash # 기본 터미널로 bash 설정
$ vi ~/.bash_profile # 없을 시 파일 생성까지
# 혹은
$ vi ~/.bashrc

# zsh
$ chsh -s /bin/zsh # zsh 기본 터미널 설정
$ vi ~/.zshrc
# 혹은
$ vi ~/.zprofile

# 파일 열기
$ open [FILE_NAME]
# 설정 내용 작성 후 :wq!로 저장 후 종료.(vim 입력시)
# M1 이전
$ export PATH="$PATH:[/PATH(경로는 최상위(Macintosh HD) 기준)]" # 명령어(mongo) 등 입력시 명령어의 경로를 설정
# M1의 경우 export PATH가 작동하지 않을 수 있다. 이 경우는 설정파일에 아래의 코드를 작성한다.
$ eval "([경로 혹은 정해진 명령어] [사용 shell 등])"
# 혹은 커맨드 라인에 파일 작성 및 내용 입력까지 한번에 요청할 수 있다.
# 실행 'eval ~'의 내용을 >> [] 경로의 파일(없을 시 생성)에 작성한다.(예시는 홈브루)
$ echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> /Users/<USER_ID>/.zprofile # [>> ~/.zprofile]도 okay
# 설정파일 새로고침
$ source [FILE_NAME] # ~./zshrc, ~/.bashrc, etc.
```

### Vim

파일을 작성하거나 열 수 없는 파일의 내용을 변경할 때 이용한다.

```bash
$ vi ~/[FILE_NAME] # 생성 및 열기 / 현재 위치 기준
# 혹은
$ vim /[PATH] # 최상위 폴더(macintosh hd) 기준
```

vim으로 이동한 후 사용할 수 있는 명령어는 아래와 같다.

- `a`: 입력 모드(파일 내 내용 입력)
- `esc`: 명령어 모드
  - `:qa` 종료
  - `:wq!`저장 후 종료



## Pinia

피니아는 이해하기 쉬운 Store를 표방하며 나온 Vuex의 대안책이며 Vue.js 개발자가 공식으로 개발하는 Store입니다.

### 설치

```bash
# vue create [ProjectName] 완료 후
$ yarn add pinia
# or with npm
$ npm install pinia
```

### 적용

```javascript
// Vue 3, main.js
import { createApp } from 'vue'
import App from './App.vue'
import router from './router'
import store from './store'
import { createPinia } from 'pinia'

// createPinia의 경우, 반드시 router 호출 다음에 이루어져야 함에 유의한다.
createApp(App).use(store).use(router).use(createPinia()).mount('#app')

```

좀 더 구분이 잘 가는 적용을 하고 싶다면, 이와 같이 변수에 할당한다면 더 깔끔하게 볼 수 있다.

```javascript
import { createApp } from 'vue'
import { createPinia } from 'pinia'
import App from './App.vue'
import router from './router'
import store from './store'

const pinia = createPinia()
const app = createApp(App)

app.use(store)
app.use(router)
app.use(pinia)
app.mount('#app')
```



## Vite

https://vite-pwa-org.netlify.app/guide/

### Vite + Vue에 이미지 등 캐싱 적용하기

1. 다운로드
   ```bash
   npm create @vite-pwa/pwa@latest
   ```

2. 서비스 워커 등록
   ```typescript
   // vite.config.ts
   import { VitePWA } from 'vite-plugin-pwa'
   
   export default defineConfig({
     plugins: [
       VitePWA({
         injectRegister: 'auto',
         registerType: 'autoUpdate',
         workbox: {
           globPatterns: ['**/*.{js,css,html,ico,png,svg}']
         }
       })
     ]
   })
   ```

3. 원하는 파일 설정해서 할 때
   ```typescript
   import { fileURLToPath } from 'node:url'
   import { defineConfig, loadEnv } from 'vite'
   import { VitePWA } from 'vite-plugin-pwa'
   import vue from '@vitejs/plugin-vue'
   
   // https://vitejs.dev/config/
   export default defineConfig(({ command, mode }) => {
     const env = loadEnv(mode, process.cwd(), '')
     return {
       base: env.VITE_ASSET_PATH,
       plugins: [
         vue(),
         VitePWA({ 
           registerType: 'autoUpdate',
           injectRegister: 'auto',
           workbox: {
             // 이용자에게 캐시로 강제할 것.
             globPatterns: ['**/*.{js,css,ico,png,svg,jpg,jpeg}'],
             // index.html pattern에 없으면 에러 발생하는데, 그것 방지용
             navigateFallback: null,
           },
         })
       ],
       resolve: {
         alias: [
           { find:'@', replacement: fileURLToPath(new URL('./src', import.meta.url))},
           // asset directory 가리키기.
           { find:'@assets', replacement: fileURLToPath(new URL('./src/assets', import.meta.url)) }
         ]
       },
     }
   })
   
   ```




## .gitignore 적용 안될때

이미 ignore할 파일이 올라가 있는데 .gitignore에 새로 추가하는 경우 파일이 계속 올라가게 된다. 파일을 삭제 후 commit 한 후, 이후에 다시 파일을 추가해서 commit하면 적용되게 바뀐다.

## 추천사이트

https://learn.shayhowe.com/html-css/

VSCode 기본 설정

https://gwonsungjun.github.io/articles/2018-06/vscodeSetting