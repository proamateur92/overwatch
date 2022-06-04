# overwatch
html, css 실습을 위한 오버워치 프로젝트

<br>

> 참고 repository https://github.com/ParkYoungWoong/overwatch-hero-selector-vanilla/blob/master/main.css

<br>

> <br>
> - 컨테이너 중앙으로 안옴 - block형태, width값이 있으면 margin: 0 auto로 정렬 가능 <br>
> - 이미지 크기 조절 못함 - img를 감싸는 div의 길이 정의, img의 비율과 길이 또한 정의 <br>
> - 플렉스 정렬 예쁘게 안됨 - max-width를 적절하게 사용한다. <br>
> - 오버워치 로고 안나옴 - 당시 문제점이 무엇인지 모르겠다. <br>
> <br>

<br>

margin 요소의 외부 여백을 지정하는 단축 속성
0 외부 여백 없음
auto 브라우저가 여백을 계산

margin: 10px 20px 30px
-> 20px은 좌우를 의미한다.

<br> 

box-sizing

content-box 요소 내용으로 크기 계산
border-box 요소의 내용 + padding + border로 크기 계산
-> 요소에서 지정한 width, height 길이만큼으로 변경

border, padding => 좌우 길이

<br>

overflow 요소의 크기 이상으로 내용이 넘쳤을 때, 보여짐을 제어하는 단축 속성
-> visible 
-> hidden 넘친 내용을 잘라냄
-> scroll
-> auto 넘친 부분만 스크롤 바, 넘치지 않은 부분은 스크롤 바를 나타내지 않는다.

overflow-x x축으로 넘치는 부분 체크
overflow-y y축으로 넘치는 부분 체크

<br>

display
-> block 상자 요소
-> inline 글자 요소
-> inline-block 글자 + 상자 요소
-> none 화면에서 사라짐

<br>

opacity
-> .5 (50%)

<br>

line-height font의 위치는 line-height의 세로 중앙 정렬이 된다.
-> ex) line-height: 2
-> ex) line-height: 200%
; font-size의 2배 

<br>

text-indent
text-outdent

<br>

div {
  width: 200px;
  height: 200px;
  background-image: url('https://cdn.pixabay.com/photo/2021/12/04/04/44/woman-6844349_1280.jpg');
  background-size: 100px;
  background-repeat: no-repeat;
  background-position: center;
}

cover 비율 유지, 요소의 더 넓은 너비에 맞춤
cotain 비율 유지, 요소의 더 짧은 너비에 맞춤
background-attachment - 요소의 배경 이미지 스크롤 특성 
-> scroll: 기본 값. 이미지가 요소를 따라서 같이 스크롤
-> fixed: 이미지가 뷰포트에 고정. 같이 스크롤 X.

<br>

postion 요소 위치 지정 기준
relative 요소 자신 기준
absolute 부모 요소 기준
fixed 뷰포트 기준

<br>

요소의 쌓임이 정해지는 규칙 - 1 ~ 3의 우선순위를 가진다.
1. position값이 있으면 위에 쌓인다.
2. z-index 값이 높을 수록 위에 쌓인다.
3. html구조가 나중에 명시되어 있으면 해당 요소는 위에 쌓인다.

z-index 요소의 쌓임 정도 지정
기본값은 0이다.

absolute, fixed -> display가 block으로 변경된다.

<br>

flex
display: flex, inline-flex

flex-grow
flex-shirnk
flex-basis

기본값은 strech -> 요소가 늘어날 수 있을만큼 최대한 늘린다.
justify-content
align-content
align-items

flex-basis 공간 배분 전 기본 너비 
-> 요소의 content에 관계없이 크기 지정하기
px, em, rem 등으로 지정

요소의 전환(시작과 끝) 효과를 지정하는 단축 속성
transition: 속성명 지속시간 타이밍함수 대기시간

<br>

transition-property
-> all: 모든 속성에 적용
-> 속성이름: 전환 효과를 사용할 속성 이름 명시

div {
  width: 100px;
  height: 100px;
  background-color: royalblue;
  transition: 
  // 여러 속성 명시 가능
    width .5s,
    background-color 2s;
}

div:hover {
  width: 300px;
  background-color: orange;
}

<br>

2D 변환 함수

이동
translate(x, y)
translateX(x)
tnraslateY(y)

크기
scale(x, y)

회전
rotate(degree)

기울임
skewX(x)
skewY(y)

<br>

3D 변환 함수

원근법
perspective(n)

회전 
rotateX(x)
roteatY(y)

transform: perspective(500px) rotateX(45deg)

perspective: 600px; -> 관찰 대상의 부모
transform: perspective(600px) -> 관찰 대상

3D 변환으로 회전된 요소의 뒷면 숨김 여부
backface-visibility
-> visible
-> hidden
