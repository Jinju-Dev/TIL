# express-session

### express-session 이란?
- Express.js 프레임워크에서 사용자 세션 데이터를 관리하고 유지할 수 있는 방법을 제공하는 미들웨어이다.

### 설치
```npm i express-session```

### 세팅
```javascript
import session from 'express-session'

app.use(session({
  secure: true, // 보안을 위한 https으로 통신하기 위해 추가
  secret: 'keyboard cat', // id 값 
  resave: false, // 세션 데이터가 변화가 있을 때에만 저장(true일 경우 계속 저장)
  saveUninitialized: true, // 세션이 필요하기 전까지는 세션을 구동하지 않음(false일 경우 세션을 구동)
}));
```

### 사용 방법
- 값추가
``` req.session.isLogined(추가할 변수) = true(추가할 값);```
- session 삭제
``` req.session.destroy();```
