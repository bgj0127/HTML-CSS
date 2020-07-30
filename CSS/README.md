# What I Learned?

[NightBowl](https://bgj0127.github.io/HTML-CSS/CSS/Night/index.html)   
*그때그때 배운 CSS를 기록합니다. 따라서 특정 속성에 대한 내용이 완전하지 않을 수 있습니다.*

### background-attachment 

* 배경 이미지의 스크롤 여부를 정하는 속성
  * **scroll** : 선택한 요소와 같이 움직인다. 내용을 스크롤하면 배경 이미지는 스크롤되지 않는다.
  * **fixed** : 움직이지 않는다.
  * **local** : 선택한 요소와 같이 움직입니다. 내용을 스크롤하면 배경 이미지도 스크롤된다.
  * **initial** : 기본값으로 설정한다. (기본값 : scroll)
  * **inherit** : 부모 요소의 속성값을 상속받는다.

### background: linear-gradient( color , color )

* 그라데이션 지정

### overflow

* 내용이 요소의 크기를 벗어났을 때 처리 속성
  * **visible** : 기본 값. 넘칠 경우 컨텐츠가 상자 밖으로 보여진다.
  * **hidden** : 넘치는 부분은 잘려서 보여지지 않는다.
  * **scroll** : 스크롤바가 추가되어 스크롤 할 수 있다.(가로, 세로 모두 추가)
  * **auto** : 컨텐츠 량에 따라 스크롤바를 추가할지 자동으로 결정됩니다.

### opacity 

* 요소의 불투명도를 설정한다. 1에 가까울수록 불투명해진다.

### animation 

* **animation** : (이름)
* 하위 속성
  * **animation-delay** : 엘리먼트가 로드되고 나서 언제 애니메이션이 시작될지 지정한다.
  * **animation-direction** : 애니메이션이 종료되고 다시 처음부터 시작할지 역방향으로 진행할지 지정한다.
  * **animation-duration** : 한 싸이클의 애니메이션이 얼마에 걸쳐 일어날지 지정한다.
* **linear** : animation-timing-function의 속성으로 애니메이션 효과가 처음부터 끝까지 일정한 속도로 진행된다.

### transition

* transition 속성을 사용하여 정해진 시간 동안 요소의 속성값을 부드럽게 변화시킬 수 있다.
  * transition : 해당 요소에 추가할 CSS 스타일 전환 효과를 설정한다. 추가할 전환 효과가 지속될 시간을 설정한다.
  * transition-delay : 전환 효과가 나타나기 전까지의 지연 시간을 설정한다.
  * transition-duration : 전환 효과가 지속될 시간을 설정한다.
  * transition-property : 요소에 추가할 전환 효과를 설정한다.
  * transition-timing-function : 전환 효과의 시간당 속도를 설정한다.

#### @keyframes를 이용하여 애니메이션의 중간상태 기술하기

* 퍼센트로 나타낸다. 0%는 애니매이션이 시작된 시점을 의미하고 100%는 애니메이션이 끝나는 시점을 의미한다. 

### clip

* 요소의 특정 부분만 나오도록 할 수 있다.

  * auto : 요소의 모든 부분이 나온다.
  * shape : 특정 부분이 나오도록 한다.
  * initial : 기본값으로 설정한다.(auto)
  * inherit : 부모 요소의 속성값을 상속받는다.

  특정 부분만 나오게 할 때는 다음과 같은 코드로 나타낸다.

  ``````css
  rect( <top>, <right>, <bottom>, <left> )
  ``````

  * top : 위를 기준으로 **시작하는** 위치
  * right : 왼쪽을 기준으로 **끝나는** 위치
  * bottom : 위를 기준으로 **끝나는** 위치
  * left : 왼쪽을 기준으로 **시작하는** 위치

* **clip-path** - 기존의 clip 속성은 직사각형만 가능했다면 이 속성은 여러 형태의 도형을 적용할 수 있다. 

### masking

* 
