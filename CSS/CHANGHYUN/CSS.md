# CSS
## 1.선택자
###  1-1. tag 선택자
###  1-2. 클래스 선택자
    - html 태그에 class="설정할 class" 를 통해 class를 선언.<br>
  	css style태그 안에 '.설정한 class{}'를 이용하여 css를 적용.<br>
    Class는 같은 css를 적용해야하는 동일하거나 다른 html태그에 적용할 때 사용.
    
### 1-3. id 선택자
    -  html 태그에 id="설정할 id" 를 통해 id를 선언.<br>
	  css style태그 안에 '#설정한 id{}'를 이용하여 css를 적용.<br>
	  id는 1번 등장하였다면 중복되서 사용하면 안됨.
    
   - '*' : 모든 선택자
   - 'tag *' : 태그아래에 있는 모든 선택자
   - 'tag1 + tag2' : tag1옆에 있는 tag2 (tag1은 선택 안됨)
   - 'tag1 ~ tag2' : tag1옆에있는 tag2들모두(tag1은 선택 안됨)

### 1-4. 부모 자식 선택자
    1. ul li{}
        - 부모, 자손관계.<br>
	        ul태그 아래에 있는 li의 모든 태그에 적용.<br>
    2. ul>li{}, #id>li{}
        - 부모, 자식관계.<br>
          ul태그 또는 id를 가진 태그 바로 아래에 있는 li태그들에만 적용. <br>
          그아래에 추가적인 태그가 있다면 그것들에는 적용하지않음.<br>
    3. ul,ol{}
        - 동등한 위치에서 여러 태그에 같은 css를 적용할때 사용.<br>
        
  - 참고 링크:<[flukeout.github.io](https://flukeout.github.io/)>

###  1-5. 가상클래스 선택자
      - 'html태그:가상클래스선택자{}' 로 작성<br>
	    visited, hover, active,focus, first-child, onlt-child등이 있음.<br>
      
 - - - 
## 2.속성
### 2-1. font size
  * 단위(unit): px, em, rem
    - px: 폰트의 크기가 고정
    - em, rem: 브라우저의 설정을 바꾸면 폰트의 크기가 변경.
    - 요즘엔 rem이 잘 사용.
  
### 2-2. color
  * color, rgb, hex 방식사용.

### 2-3. text-align
  * center, left, right, justify등
 
### 2-4. font
    1. font family
      이를 속성으로하면 적은 value값들의 순서에 따라 유무를 판별후 사용.
      arial, verdana, "Helvetica Neue" 등
      또한 마지막에 sans-serif(장식X), serif(장식), monospace(고정폭) 등을 적음.
      
    2. font-weight
      value값을 bold로 설정하여 글꼴을 두껍게 만든다.
      
    3. line-height
      폰트간의 위아래 간격을 폰트사이즈의 몇배 설정할 것인지.
     
    4. font
      위에 사용한 font관련 속성들을 한번에 사용하려고할때 사용.
      font-style font-variant font-weight font-size/line-height font-family|caption|icon|menu|message-box|small-caption|status-bar|initial|inherit; 
		  다음과 같은 순서를 따름.
     
    5. webfont
      사용자의 컴퓨터에 없는 폰트를 웹을 통해 사용하고자할때 사용
      
 - - -
 ## 3. 상속
    - Css의 모든 속성이 상속되는건 아님.
    - 상속하지 않는 속성과 상속하는 속성.
  * 참고 자료 : <https://www.w3.org/TR/CSS21/propidx.html>

- - -

## 4. stylish
  * 다른사람이 제작한 css나 내가 사용하는 사이트에 내가 직접 css를 적용할 수 있는 chrome tool

- - -

## 5. Cascading
    - 브라우저, 사용자, 저자 모두가 같은 css를 하나의 웹에 적용하고자 할때, 브라우저<사용자<저자 와 같은 우선순위가 적용
    - tag, class, id, style attribute가 있을때는 tag<class<id<style 순으로 우선순위가 적용.
    - 같은 효과를 적용할때 나중에 선언된것이 우선순위.
    - !important 무조건적인 우선순위
   
- - -   
   
## 6. inline 과 block level
  * 이둘은 "display:"태그를 이용하여 설정할 수 있음.
    1. inline : 다른 태그들과 조화롭게 한줄에 포함되서 사용되어지는 태그
    2. block level : 혼자서 화면 전체를 사용하는 태그

- - -

## 7. box
### 7-1. border
    1. block level
    테두리 설정, 테두리는 박스모델의 기준점을 선정해줌.
    padding: 테두리와의 안의 요소간의 간격
    margin: 다른 박스모델간의 간격
    width: 해당 박스모델의 넓이 설정.
    height: 해당 박스모델의 높이 설정.
    
    2. inline
    padding, margin은 적용되는데 width값은 설정안됌.
    
### 7-2. box sizing
    width를 설정하면 요소 전체의 크기가 다른 것을 알 수 있음.
    이는 테두리의 크기를 고려하지않고 박스모델안의 요소의 전체 크기를 고려했기 때문.
    따라서 이를 수정하려면 boxsizing의 value값을 border-box로 변경하면 테두리를 고려하여 넓이를 설정.
    
### 7-3. margin 겹침현상
    - 인접해잇는 두개의 박스모델간 두 박스모델중 더 큰 margin값만 두 박스모델 사이에 적용
    - 부모와 자식간의 관계, 부모태그에 시각적으로 아무런 효과를 설정하지않는다면, 부모태그와 자식태그의 margin값중 더 큰 margin값만 적용
    - 인접해잇는 두개의 박스모델간 두 박스모델중 두개의 박스모델 모두 아무런 시각적 효과가 설정되어있지않다면 두 모델의 magin값중 더 큰 margin값만 적용
    
- - -

## 8.Position
  * html의 태그들이 어디에 위치할 것인가에 대한 것.
### 8-1. relative
    position="" 속성 안에 value값으로 relative 설정. 부모에대해 상대적으로 변경가능.
    left(우선),right, top(우선), bottom와 같은 offset 설정가능
    relative를 설정하지 않을 시 offset 적용안됌.
    각요소들의 기본적으로 css의 포지션이 고정값에있음.(static)

### 8-2. ststic
    기본 값
    
### 8-3. absolute
    절대 포지션
    부모에대해 상대적으로가 아닌 html또는 다른 태그를 기준으로 position을 변경하고 싶을 때 사용.
    offset은 기본값으로 원래 위치인 부모에대해 상대적일때의 위치로 가짐.
    position의 값을 absolute로 설정 시, 더이상 해당 태그는 부모의 소속이아님.
    부모 태그들 중 realtive값이 있다면,static인 부모들은 무시하다가 static이 아닌 부모가 나타나면 그 부모의 위치를 기준으로 offset을 설정.
    width와 hight를 따로 설정하지 않으면, 요소안의 컨텐츠 크기만큼만 설정.
    
### 8-4. fixed
    화면자체에 위치시켜 스크롤로 부터 독립적.
    width와 hight를 따로 설정하지 않으면, 요소안의 컨텐츠 크기만큼만 설정.
    position의 값을 fixed로 설정 시, 더이상 해당 태그는 부모의 소속이아님.
    
- - -

## 9. flex
  * 레이아웃. container역할을 하는 태그와 item역할을 하는 태그로 구성.
  * 부모에게 display속성에 flex값을 설정.
    1. container
    display:flex설정
	  flex-direction으로 수직또는 수평설정
    
    2. item
    flex-basis를 통해 기본크기 설정
    flex-grow; 1을 통해 전체크기를 1/item 크기로 각 item태그들이 차지.
    -> 하지만 하나의 태그에만 flex-grow를 설정한다면 '각 태그들의 grow값/전체 각 태그들의 grow합'만큼의 크기를 차지하게됌.
    flex-shrink: 0을 통해 전체적인 화면의 크기가 줄때, 해당 속성이 설정된 태그는 크기가 안줄어들고 나머지 만 줄어듬.
    -> item이 특정한 basis값을 가지고 있을때,basis값보다 전체 적인 화면이 줄어들때 어느것을 더 줄이고 안줄일지 결정하게 함.
  * 클래스값이 같은 여러개의 태그중 2번째 클래스에 대해서만 css를 설정하고 싶을 때, ".class이름:th-child(2){}"로 설정가능.

- - -

## 10. flex
    1. column-count: 숫자;
      숫자 만큼의 단락이 나눠짐
      
    2. column-width: px;
    최소 px만큼 표현할 수 있는 크기가 되면 단락을 나눔
    
    3. column-gap: px;
    단락간의 간격 크기를 조정.
    
    4. column-rule-style: solid
    단락간 구분선 설정
    
    5.  column-rule-width, column-rule-color;
    단락 구분선의 크기와 색 설정.
    
- - -

## 11. media query
  * 미디어의 상태에 따른 디자인 설정, 반응형 웹.
    1.  @media(" "){}
    - width:숫자 -> 전체 화면이 해당 숫자에 해당할때 적용할 css
    - max-width:숫자 -> 전체 화면이 해당 숫자보다 작을때 적용할 css
    - min-width:숫자 -> 전체 화면이 해당 숫자보다 클때 적용할 css
    - * <meta name="viewport" content="width=device-width, initial-scale=1.0"> 를 통해 모바일에서도 적용가능.

## 12. float
  * 이미지를 삽입할때 조금더 자연스럽게 삽입하기위함.
  * 레이아웃을 잡을때 사용했음. 요즘은 flex가 대두되고 있긴함.

### 12-1. 이미지 삽입
    float 속성을 통해 이미지 공간을 제외한 부분에 글을 넣을 수 있음.
    clear을 통해 flaot 무시 가능.
 
### 12-2. holy grail layout
    실습
   
- - -

## 13. backhround
  * 배경이미지나 색을 지정하는것.
	- background-color
	- background-image:url('url주소');
	- color와 이미지가 함께온다면 이미지가 앞쪽으로 옴.
	- transparent라는 투명값(이미지가 없는 부분)이 없다면 backgroundcolor는 적용이 안됌.
	- 이미지가 반복적으로 나옴. 이때 background-repeat:no reapet;을 사용하면 1번만 나옴
	- 스크롤시 background는 고정되게한다면: background-attachment:fixed를 사용하면됌
	- background-size를 통해 background의 크기를 지정할 수 있음.
	- cover와 contain의 차이가있는데 두 기능모두 이미전체를 사용, 하지만 cover는 조금 짤리더라도 이미지가 설정한화면에 다보이게 되는속성. 
	- contain은 주어진 화면크기 width나 height에 맞춰서 화면비율을 고수하고 전체를 다 보이게해줌.	
	- 이미지의 위치설정- background-position을 통해 가능.center,bottom과 같은 속성을 통해 사용.
	- (우리클론코딩할 naver 이미지 해보라고 해도될듯 이거실습으로)
	 
  * 참고 자료:<https://caniuse.com/>

- - -

## 14. filter
    포토샵의 기능들이 코드화. 
    복수의 필터 결합도 가능.
    image, iframe, video, text등에 적용 가능하다.
    grayscale(%)-흑백효과
    blur(px)-흐림효과
    가상클래스 선택자와 혼합사용 가능하다.

- - -

## 15. blend
   * 이미지와 이미지를 겹쳐놨을때 서로다른색상의 차이.
 
- - -

## 16. transform
	대상의 크기,회전,비틀기 등을 진행. 
	scaleX(수),scaleY(수), scale(x,y): x축,y축으로 확대또는 축소
	transform은 2번사용시, 가장 나중에 입력한것만 적용.
	여러 효과를 적용할떄, 나열을 통한 적용.
	
  * 참고자료: <[codepen.io](https://flukeout.github.io/)>

- - -

## 17. transition
	전환, css의 여러 효과들이 변경되었을때 그 변환을 부드럽게 해주는 효과.
	transition-property: all 모든 효과에 대해 변화가 일어났을떄 전환이 일어남 이라는뜻
	transition-property:transform transform변화에만 transition적용.
	여러 효과를 적용하고 싶을때 한꺼번에 할때는 띄어쓰기를 통해 나열하면 가능.
	transition-duration: s(초) 효과 변경 소요시간 설정
	trasition: all 1s 모든 효과 전환에 대해 1초소모.

- - -

## 18. link & import
  * 만약 1000개의 파일에 있는 css를 모두 수정해야한다면 너무 많은 노력과 시간이 필요함.
  * css적으로 중복되는 부분이있다면, 유지보수, 사용자가사용하는데 있어 많은 자원이 필요.
	1. 별도의파일을 만듬. ex) style.css
	2. 중복되는 부분을 style.css파일에 입력
	3. 각 html파일들에 <link rel="stylesheet" href="style.css">을 입력
	4. link의 href라는 파일을 다운 받고, 해당 파일을 css문법으로 해석하여 html에 적용해줌.
  * "<style>"이라는 태그안에서 @import url("경로") 를 통해 css파일을 불러온느것도 가능.
  * link는 html태그로 로드, import는 css파일안에서 다른 css를 로드할떄 사용.
	
- - -

## 19. preprocesssor
  * 문법, 문법에 따라 작성한코드를 css로 변환기(컴파일러).
	
- - -
	
## 20. fontello
	  특정 문자가 특정 이미지로 표현하게 하는 법.
	  백터 기반 폰트.
	  여러 아이콘 사용 가능.
	  ->thenounproject에 다양한 픽토그램존재.
	
- - -

## 21. Button
	다양한 디자인 버튼.
	콤보박스는 JS가 필요함.
	
- - -

## 22. OVERFLOW_taekit (속성)
  * 컨텐츠가 블록을 넘어감`
	1. hidden: 넘은 부분은 안보여줌.
	2. scroll: 가로와 세로에 스크롤.
	3. scroll-x,scroll-y:를 통해 가로 축또는 세로축에 스크롤 설정.
	4. auto: 가로가 넘치는지 세로가 넘치는지 에따라 자동으로 스크롤 생성.
	
- - - 
	
## 23. clear_taekit(속성)
	페이지 범람
	float을 사용하면 margin이 없어짐. 즉, 텍스트와 이미지가 함께 공존 할 수 있음.
	없어진 margin영역에 대응하기 위해 clear사용.
	역할: float으로 인해 없어진 margin영역을 무시하고 올라가지 않도록 처리해준다.
	margin은 사라지지만 다른요소가 없어진 마진을 채우지 않음.
	
	clearfix, clear라는 속성으로 레이아웃을 바로잡는 속성
	범람을 막고싶은 요소::after{
	content:
	display="block"
	clear:"both"
	}

