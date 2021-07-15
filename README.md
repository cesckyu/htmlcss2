###
> https://github.com/ministori-yonsei/green_07

> https://codepen.io/ministori-yonsei/pen/VwbabLW?editors=1000 

### 단축키
주석 달기 : Ctrl + /

# 프론트 엔드 개발

## 클라이언트-서버 시스템(모델)

> 클라이언트-서버 시스템은 복잡한 네트워크 연결중 양 끝단에 연결된 사용자와 공급자의 관계를 의미함
> 
> 클라이언트 : 사용자가 사용하는 디바이스 또는 디바이스에서 실행되는 어플리케이션
> 
> Ex) 웹브라우저
> 
> 서버 : 데이터, 네트워크 서비스가 공급되는 디바이스 또는 디바이스에서 실행되는 서버소프트웨어
> 
> Ex) 아파치 서버

## HTML 기본 개념

> HTML - Hyper Text Markup Language
> 
> 웹페이지에 구성 요소를 표시하는 언어 (Markup , 표시만 하고 끝 동작x 제어x)
> 
> 구성 요소 : 콘텐츠, 구조
> -> 콘텐츠를 표시, 구조 

## HTML 기본구조

`(backtick)

```
<!DOCTYPE html>
<html>
  <head></head>
  <body></body>
</html>
```

- DOCTYPE : html문서 타입
- html : html 영역 표시
- head : 해당 웹페이지의 부연설명, 부가정보가 포함
- body : 웹페이지의 콘텐츠를 표시하는 영역

## HTML 요소 기본 개념

### 요소 문법

```
<starttag>contents</endtag>
```

### 포함관계

> 요소의 영역안에 다른 요소를 포함하는 관계
> 
> 직계 포함하는 요소 : 부모(parent)요소
> 
> 직계 포함되는 요소 : 자식(child)요소
> 
> 직계가 아닌 포함하는 요소 : 조상(ancestor)요소
> 
> 직계가 아닌 포함되는 요소 : 자손(descendant)요소

### Empty element(빈 요소)

> 시작태그만 있고 종료 태그가 없는 요소


### HTML 속성(Attribute)

> html element에 대해 추가정보(이동경로, 파일명...)를 제공
> 시작태그에 입력
> 형식 : 속성이름 = "속성값"

### HTML로 표현할수 있는 콘텐츠(웹페이지에서 표현할수 있는 콘텐츠)

> 텍스트 콘텐츠
> 
> 멀티미디어 콘텐츠
>  - 이미지
>  - 비디오
>  - 오디오

### 제목 요소(Heading Element)
> h1 ~ h6(h : heading)

### 단락 요소(Paragraph Element)
> p : Paragraph

> hr : horizontal rules
> - 단락을 구분하는 수평선을 표시
> 빈요소

> br : Line Break
> - 같은 단락안에서 강제 줄바꿈
> 빈요소

### 하이퍼링크 요소(Hyper Link Element)
> a : anchor

```
<a href="url">링크텍스트</a>
```

> href : hyper text reference - 이동하고자 하는 목적이 위치/경로를 표시하는 속성
> - url(Uniform Resource locator) : 이동하고자하는 목적지의 위치/경로 값

### 목록 요소(List Element)
> 순서있는/순서없는 목록
> 
> ol(Ordered List), ul(Unordered List), li(List Item)

> 설명목록
> 
> 주제와 설명이 한 세트로 구성되는 목록
> 
> dl(Description List), dt(Description Term), dd(Description Data)

### Table Element(https://www.tablesgenerator.com/html_tables)
> table, thead, tbody, tfoot, tr, th, td, caption

```
<table>
  <caption></caption>
  <thead>
    <tr>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td></td>
    </tr>
  </tbody>
  <tfoot>
    <tr>
      <td></td>
    </tr>
  </tfoot>
</table>
```

> table : table의 영역을 설정
> 
> thead, tbody, tfoot : table 데이터의 그룹을 표시
> 
> tr(table row) : 행
> 
> th(table head) : 제목 칸(셀)
> 
> td(table data) : 데이터 칸(셀)
> 
> caption : 테이블의 제목,설명

### Image element
> img(image)
> attribute : src(source), alt(alternative)

```
<img src="image.jpg" alt="image">
```

> img 태그를 사용할 때 src, alt 속성은 반드시 사용해야 함

### Video Element

> attrubute
> - controls : 비디오 컨트롤 버튼 표시
> - loop : 비디오 반복 재생
> - muted : 음소거
> - autoplay : 자동재생(항상 muted와 같이 사용)

### 절대경로/상대경로

> 절대경로 : 콘텐츠 파일을 불러오고자 하는 HTML 페이지가 어떤 위치에 있던 동일하게 찾아올수 있도록 자세하게 표시하는 경로
> 상대경로 : 콘텐츠 파일을 불러오고자 하는 HTML 페이지의 위치를 기준으로 콘텐츠 파일의 위치를 표시하는 경로

```
<img src="https://w3schools.com/images/picture.jpg">

<img src="images/picture.jpg">

<img src="../images/picture.jpg">

root 상대경로
<img src="/images/picture.jpg">
```
> root를 특정 폴더로 정하는 방법??????????????????????????????????????????????????


### Block/Inline Element
> 화면에 표시되는 형태를 기준으로 구분하는 방식

> Block Element
> 
> - 화면에 줄바꿈되어 표시되는 요소
> 
> - 항상 사용가능한 전체 너비를 차지함
> 
> Inline Element
> 
> - 화면에 줄바꿈되지 않고 나란히 표시되는 요소
> 
> - 인라인요소에 포함된 콘텐츠의 너비만큼만 차지함
> 
> div(division) / span
> - 단순 영역구분 요소(Container Element)


### 폼 요소

> input, button

```
<input type="text">

<input type="password">

<input type="button" value="이름">
<input type="submit" value="이름">
<input type="reset" value="이름">

<button type="button">이름</button>
<button type="submit">이름</button>
<button type="reset">이름</button>
```

### 인터넷 주소체계

> IP address : 192.168.0.1
> 
> Domain address : https://www.naver.com
> 
> - 기본주소(IP) => 의미있는 영어단어로 변환 : 도메인 주소
> - 도메인 + 경로주소 => URL 
> 
> ex) www.naver.com/images/picture.jpg 

# CSS

> - Cascading Style Sheets
> - Cascading : 나중에 선언한 것이 최종 반영되는 CSS 특징

> CS Syntax (문법)
> 
> - selector(선택자) 와 declaration block(선언블록)으로 구성
> - 선언블록은 { } 안의 여러 선언을 포함
> - 각 선언에는 property와 value로 구성


```
h1 {color:blue; font-size:21px;}
```

Internal 웬만해선 사용 x


JS는 CSS 컨트롤이 불가하여 Inline으로 제어

### class, ID

> HTML element에 대해서 이름을 지정해줄 때 사용하는 attibute
> 
> class
> 
> - 여러개의 HTML element에 같은 클래스 이름을 사용할 수 있음
> 
> - 한 개의 HTML element에 여러개의 클래스 이름을 사용할 수 있음
> 
> id
> 
> - id 이름은 HTML 문서내에서 고유해야함(한 개만 존재)\
> 
> - 한 개의 HTML element에 한 개의 id 이름만 사용할 수 있음 

> ! ID는 고유해야함 
> : ID도 중복 가능은 함 but, 논리적 문제 발생(서버에서 정확한 곳에만 데이터를 보내지 못함)
> : 서버개발에서 id 사용 많음

```
<div class="box box1 box2"></div>
<div class="box box1 box2"></div>
<div class="box box1 box2"></div>

<div id="title1"></div>
<div id="title2"></div>
<div id="title3"></div>
```

### Naming (표기 방식)

- 한 단어로 Naming 하는 것은 한계가 있기 때문에, 여러 단어로 Naming 필요
- 단어와 단어 사이 구분 필요하나, 일반 문서처럼 띄어쓰기로 구분 불가.
- 따라서, 단어와 단어 사이를 기호나 규칙으로 띄어쓰지 않고 구분하는 방법을 '표기방식'이라 함
-
> 표기방식 종류
> - Snake case(underbar/underscore) : gnb_list_item => file/folder 에 사용
> - Kebab case(hyphen/dash) : gnb-list-item => HTML의 id/class 에 사용
> - Camel case : gnbListItem => javascript 변수/함수 이름 정할 때 사용
> - Pascal case : GnbListItem => javascript의 class 이름 지정 시 사용

> 참고
> - 코딩 컨벤션 : 조직별로 네이밍 규칙을 갖고 있음
> - 프로그래밍에서는 snake, kebab 사용 X
> - 파이썬에서는 snake case 사용
> - 객체 지향 언어는 class 개념이 있음

>   - 프론트엔드 자동화 툴
>   - CSS 전처리기 (ex) Sass, Less, Stylus)
>   - : Sass 에서 Snake case (ex: gnb-list-item) 사용해야 &- 


> 

> OOCSS 이론
> - 모든 태그에 이름 부여하여 대상화

### Reset CSS


### 컬러 모드
> - RGB : 가산 혼합
> - CMYK : 감산 혼합 Cyan, Magenta, Yellow, Key Plate(Black)

> 색 표현 범위
> - 1bit : 최소단위
> - 8bit = 1byte : 정보 표현의 최소 단위
> - RGB 색상 표현 : 각 1 byte 씩 총 3 byte(24bit)로 표현(트루컬러)
> - RGB 색상 표현 값
>   - 16진수 : #0FAB78
>   - 10진수 : (255, 100, 121) ※숫자범위 : 0~255

### Text CSS

> color
> - value : #000000(black), #ffffff(white) rgb(255, 255, 255)(white)
> text-align : left, center, right, justify;
> text-decoration : underline, line-through, overline, none;
> text-indent : 50px(들여쓰기), -50px(내어쓰기)
> letter-spacing : 3px, -3px(사이가 좁아짐)
> line-height : 24px or 1.6
> word-spacing
> white-space : nowrap (줄바꿈 없애기)\

### Font CSS

> font-family : 'Times New Roman' (띄어쓰기가 있는 경우 ''로 묶어 하나임을 의미), Times, serif;
> - font fallback : 렌더링 시 폰트가 없는 경우 다른 폰트로 대비
> - web safe : 웹 페이지가 표시될 때 의도한 폰트가 제대로 보이도록 선택
> - web font : 사용자 클라이언트가 아아닌 서버에서 폰트를 찾도로 하는 방법
> - google font : 웹 폰트를 사용하도록 도와주는 서비스
> - 눈누 : 한글 웹폰트 서비스
> font-weight : normal(regular:400), bold(700);
> font-size : 20px;
> font-style : italic

### Box Model
> HTML Element에는 기본 영역이 존재하며, 여기에 CSS 요소를 적용할 수 있음
> - Content 영역
> - padding / border / margin

### width / height

> width
> - 기본 속성 : Block 요소는 부모요소에 맞춰지며, Inline 요소는 자식요소에 맞춰짐
> height
> - 기본 속성 : Block, Inline 모두 자식요소에 맞춰짐 
> 단위
> - px : 지정된 수치값으로 고정
> - % : 부모요소 기준 일정 비율로 크기 정해짐
>   - Block 요소는 가로길이 px, % 적용 가능하나, 세로는 % 적용이 되지 않음(가능한 방법은 있음)
>   - Inline 요소의 경우 px, % 단위 적용 불가

### Padding

> 축약표현
> - padding: 20px; : 모든 방향
> - padding: 20px 30px; : top/bottom right/left
> - padding: 20px 30px 40px : top right/left bottom
> - padding: 10px 20px 30px 40px : top right bottom left

### Margin

> Margin Collapse 마진 겹침
> - 위아래로 연이어 박스가 배치될 때 큰 수치의 margin만 표시됨

### border

> border

> width, style, color
> top, right, bottom, left

```
border : 1px solid #fff;    4방향
 
border-top : 1px solid #fff; 

-> *색이 같을 때 축약 가능 #aa5500 = #a50
```

### 박스 모델 크기 계산

> width/height, pading, border, margin는 모두 별개 요소

> Ex) 박스 전체너비가 300px이고 padding이 20px, border 1px, margin 30px라면
```
div{
  padding : 20px;
  border : 1px solid #fff;
  margin : 30px;
  width : ???? = 258px;
}
```

> box-sizing: border-box; (기본값 : content-box) 설정 시

```
  padding : 20px;
  border : 1px solid #fff;
  margin : 30px;
  width : 300px;
  box-sizing: border-box;
}
```

### Block, Inline에 박스모델 적용
> Block : 박스모델의 모든 요소가 적용 가능 Inline : 박스모델의 width/height, 상하 margin 이 제대로 적용되지 않음

### Display 속성

> 박스(영역)의 block, inline 속성을 변형

> display : inline -> 박스 속성 inline으로 변형
> display : block -> 박스 속성 block으로 변형
> display : inline-block -> inline, block 두 가지 특징 가짐

### 가로 배치 방법

- float
- flex
- grid
-
## Float
> 박스를 띄워 좌우 배치
> float : left, right => 부모요소 왼/오른쪽 기준으로 배치

> float 배치 시 위아래 인접 박스들이 위로 올라감
> 
> 하단 인접 박스에 clear : both 설정 시 위로 올라가지 않음
> 
> but, float 박스는 계속 떠 있는 상태이므로, margin 적용 문제가 발생

> - 해결책 : float 박스를 <div>(부모)로 감싸주고, 
  
  float박스 아래에 <div>박스 추가 후 clear: both 적용
  
  float 박스 외 위아래 인접 박스들은 float 박스 부모요소와 인접관계가 되기 때문에 float과 상관 없어짐
  
```
  <div class="float-parent"
       <div class="float-box"> Text</div>
       <div class="clearfix"></div>
  </div>
 CSS
 .float-box{
 float: left;
 }
    
 .clearfix{
 clear: both;
 }
  
 

### 가상 클래스(Pseudo Class)

> 선택자(요소)의 상태를 정의

> 여러 요소 중 특정 요소를 지정


상태 정의

a:link{
  color:red;
  }
  
 a:visited{
 color:blue;
 }
 
 
### 가상 요소(Pseudo Element)

> HTML에 직접 입력하는 것이 아닌 CSS에서 렌더링 시 생성되는 가상 요소

```
div::before{
  content: "Hello World";
  }
  
div::after{
  content: "";
  display: block;
  width:100px;
  height:30px;
  }
```

### 투명도

> Transparent
> Opacity
> alpha
