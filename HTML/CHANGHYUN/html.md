# HTML
## HTML이란
- HyperText Markup Language

## 기본문법
### DOCTYPE
  - 자신이 작성한 html코드가 어떤 표준을 따르는 HTML이 작성되었는지 선언해주는 역할

### Tag
  - head tag와 body태그 모두 html 태그로 감싸주어야한다.

#### Body
p
  - 단락을 표현. 줄바꿈간격이 고정.
  - css라는 별도의 언어에서 P tag를 통한 띄어지는 간격을 조절할 수 있음.

b
  - 줄바꿈
  - 내용이 없는 tag로 "<"br">"명령을 쓴 후 "<"/br">"을 사용할 필요가 없음.
  - 단락을 표현할떄는 "<"br">"보다는 "<"p">"로 표현하는 것이 더 좋음.

img
  - 이미지를 추가하는 tag
  - width=""속성을 통해 ""안의 숫자만큼의 픽셀 크기로 변경.
  - height=""속성을 통해 ""안의 숫자만큼 픽셀 크기로 변경. 하지만 원래비율이 있으므로 바뀔 수 있음.
  - 위 속성중 하나만 한다면 해당 넓이나 높이만큼 지정이 됨과 동시에 해당 이미지의 비율에 맞게 나머지 속성은 조절.
  - alt=""속성을 통해 이미지가 꺠지거나 없어졌을때 깨진 표시와 함께 alt의 속성값이 표시.
  - title="" 속성을통해 이미지에 커서를 올려두었을때 도움말이 출력.

table
  - 표를 나타내주는 tag
  1. 항목 하나하나를 "td" tag로 묶기
  2. 같은행들끼리 "tr" tag를 통해 그룹화
  3. 표로 표현할 항목들을 "table" tag로 감싸기
  - table tag에 속성으로 border="숫자" 를 통해 테두리 생성.
  - 요즘에는 이쁘게 꾸미기위해 border 속성 보다css를 이용
  - 레이아웃 구조를 구성하기위해 사용하기도 했음. 
  - 요즘은 css를 통해 구성.
  
  - thead
    - 각데이터들의 제목 "th"를 사용히면 다른 항목들에 비해 진하게 표현
  
  - tbody
    - 표의 본문
  
  - tfoot
    - 표에서 가장 아래쪽
  
  - 병합
      - rowspan="숫자" tag를 통해 행(세로)병합
      - colspan="숫재" tag를 통해 열(가로)병합
    
form
  - 로그인, 글작성등을 통해 글자 입력등을 할때 사용.
  - 어디 있는 서버로 전송할 것인지 <form> tag의 action="url주소"속성을 통해 전송.
  - input tag를 통해 박스(컨트롤) 생성
  - type="text" 속성을 통해 글자 입력가능
  - type="password" 속성을 통해 글자 입력시 *로 표현
  - type="submit" 속성을 통해 서버로 전송하는 버튼 생성.
  - 각각의 박스(컨트롤)를 구분하기 위해 속성 name=""을 통한 이름 설정. 
  - 사용자가 사이트를 열었을때 컨트롤 안에 어떤 특정 문자가 적기 위해 value="문자열"속성을 사용.
    - "textarea" tag를 통해 여러줄을 입력받을 수 있는 컨트롤 생성
    - cols="숫자" rows="숫자" 속성을 통해 숫자갯수 지정가능.
    - "textarea" tag 사이에 문자를 적으면 기본값으로 출력됌.
     
select
  - dropdown list를 생성하는 tag
  - "option" tag를 통해 dropdownlist의 선택지 생성
  - value="문자열" 속성을 통해 실제 전송되는 값을 설정 할 수 있음.
  - multiple 속성을 통해 다중선택을 할수있게함. -> 사용자는 ctrl 키를 통해 다중선택 가능.

radio, checkbox
  - 사용자들로 하여금 하나를 선택하여 제출할 수 있게 함
  - input type="radio"를 사용하여 사용자가 선택할 수 있는 radio버튼 생성.
  - 각각 만들게 되면 복수 선택이 가능한데 name="문자열" 속성을 통해 이름이 같다면 하나만 선택이 가능.
  - 즉, name=""이 같은 radio버튼 끼리 그룹화.
  - value="문자열" 속성을 통해 전송시 실제 전송되는 값을 설정.
  - 기본적으로 선택되었으면 하는 항목에 checked 속성을 통해 미리 체크 가능

checkbox
  - 사용자들로 하여금 복수개를 선택하여 제출할 수 있게함.
  - input type="checkbox" 를 사용하여 사용자가 선택할 수 있는 checkbox 생성.
  - name="문자열" 속성이 같아도 여러개 중복선택이 가능.
  - 기본적으로 선택되었으면 하는 항목에 checked 속성을 통해 미리 체크 가능

button
  - input type="button와 같은 tag는 자바스크립트와 같은 언어를 배웠을때 활용
  - input tyep="reset" 버튼을 통해 사용자가 입력하였던것을 초기화 가능.

hidden field
  - 눈에 보이지않지만 서버로 무언가를 보내야할때 사용.
  - input type="hidden" name="문자" value="문자" tag를 사용

label
  - markup laguage로써 알려주기 위해 사용.
  - 무언가의 이름표임을 정확히 기술.
  - label for="문자" tag를 이용한뒤 input id="문자" tag를 사용한다면 
  - label tag로 감싸진 항목이 input tag의 label임을 명시할 수 있음. 
  - label tag안에 input tag를 포함시킴으로써 명시 가능.
  - 사용성이 높아지는 효과.

method
  - 기본적으로 id와 pwd를 서버로 전송하다보면 url에 사용자가 입력한 ID와 PWD가 노출되는 경우가 있음.
  - 이는 get 방식을 통한 서버와의 통신으로, url에 정보를 담음.
  - 따라서 form tag에 method="post" 속성을 이용한다면 url에 아무런 정보도 붙지 않음.
  - 즉, url을 통한 데이터 전송이아닌 다른 방식으로 전송.

파일 업로드
  - input type="file"을 이용하면 파일을 선택할 수 있음.
  - 이때 form tag에 action="url주소", method="전송방식", enctype="multipart/formd-data"속성이 필요.


li
  - list태그안에 다른태그가 존재할 수 있음.
  - 태그 중첩이 가능.
    - ul
      - unordered list
      - 순서가 없는 리스트
    - ol
      - ordered list
      - 순서가 있는 리스트


#### Head
title
  - 타이틀에 해당하는 내용이 탭에 표시

meta
  - 글씨가 깨지지않도록 해줌
