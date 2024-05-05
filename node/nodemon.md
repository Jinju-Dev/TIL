# nodemon
  ### nodemon이란?
  - 서버 코드를 수정 시 자동적으로 재실행을 도와주는 node.js 라이브러리 이다.
  - 코드를 수정하고 재실행 해주지 않아도 되는 장점이 있다.

 ### nodemon 설치 및 실행
  - 전역 설치
```npm install -g nodemon```
  - 지역 설치(전역설치를 주로 사용할 것 같다.)
```npm install --save-dev nodemon```
  - 실행
``` nodemon '파일명'```

### nodemon 설치 후 실행이 안될 때 
1. powershell 관리자 모드로 실행
2. ```Set-ExecutionPolicy Unrestricted``` 입력 후 ```y``` 입력
