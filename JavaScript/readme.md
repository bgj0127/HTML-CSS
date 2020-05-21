*JavaScript*

<script  src="file.js"></script> 의 형태로 html 코드에 넣는다.

가장 좋은 방법은 <head>안에 <script  defer  src="file.js"></script> 이다.

defer를 사용하게 된다면 파싱 중 defer를 만나면 자바스크립트를 다운만 받고 html 파싱을 끝까지 한 후 다운로드 된 자바스크립트 파일을 실행시킨다.

use strict은 바닐라 자바스크립트로 개발을 할 때, 선언하지 않은 변수를 사용할 수 없게 막아준다.
