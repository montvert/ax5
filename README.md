# ax5 새로운 JS UI 라이브러리

## link
- [API테스터] (http://ax5.io)
- [API JSDOC] (http://ax5.io/jsdoc)

# 시작에 앞서
이 프로젝트는 제이쿼리를 이용하지 않고 독립적으로 자바스크립트 UI라이브러리를 구현하기 위한 프로젝트 입니다. 이렇게 제작된 UI라이브러리가 더욱 높게 멀리 전파되게 하는 것이 우리의 소망입니다.

## ax5가 추구하는 목표
1. **코드의 독립성**<br/>
JS UI가 어떠한 라이브러리의 의존없이 구동해야 하면서 또한 모든 라이브러리와 호환될 수 있어야 합니다. <br/><br/>
2. **UI의 확장성** <br/> 
UI를 위한 CSS 박스모델정의를 연구하여 연구자료를 공개하여 많은 사람들이 UI를 확장할 수 있게 합니다.<br/><br/>
3. **사용자의 편의성** <br/> 
만들어진 UI라이브러리가 보다 쉽게 사용 될 수 있도록 기존 스크립트 바인딩방식 외에 webcomponent방식을 지원합니다.<br/><br/>

## 커미터를 위한 가이드
### 폴더 설명
- [api-test] 제작된 메소드등을 테스트 하는 코드 모음입니다. 코드 테스트 함수를 만들어 자동화 처리 하고 추후에 테스트 결과를 서버로 저장하여 로그를 쌓을 생각합니다.
- [jsdoc] 폴더에 위치한 gruntfile.js가 src폴더안에 있는 jsdoc주석을 추출하여 API문서를 만들어 냅니다. 개발할 때는 고려하지 않고 배포시에 확인 합니다.
- [plugin] 외부에서 제작된 라이브러리등을 담아두는 곳 입니다.
- [pub] src코드를 압축하여 배포용으로 저장합니다. 이때 버전별로 파일을 생성합니다.
- [samples] 소스코드 레벨로 설명서를 작성하는 공간입니다. ax5 폴더아래에 html파일을 만들어 두면 (이때 head는 선언하지 않고 내용만 코딩하면) samples/Gruntfile.js에서 samples/index.html 에 만들어냅니다. (watch 를 실행하면 편집될 때 마다 자동 퍼블리시 합니다.) 추후에 정리하여 데모페이지로 활용하고 디자인도 한번에 처리 합니다.
- [src] 실제 소스 코드가 있는 공간입니다.
- [ui] less/css파일을 담아두는 공간입니다. 추후 이 아래에 theme가 폴더별로 담기게 됩니다.

### [src]
ax5.js는 ax5-polyfill.js + ax5-core.js + ax5-xhr.js + ax5-ui.js의 합친파일입니다. 
>개발시에는 헤드에 개밸파일별로 import하여 개발테스트 하고 커밋합니다. ax5.js에 직접 작업하고 커밋하면 여러사람이 고생하게 됩니다.

**개발은 반드시 ax5-core, xhr, ui에 하고 커밋합니다.*<br/>
**[주의!!] ax5.js파일을 푸시해도 머지하지 않습니다.**

### Pull Request
포크한 소스를 풀리퀘 하실 때에는 다음 그림에서와 같이 왼쪽의 브랜치를 alpha로 선택하여 풀리퀘스트 해주시면 감사하겠습니다.

![pullrequest](http://ax5.io/samples/images/pullrequest.png)

[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/tom-axisj/ax5/trend.png)](https://bitdeli.com/free "Bitdeli Badge")