# express 기능

### app.use()란?
- express 앱에서 항상 실행되는 미들웨어 역할이다.
- 지정된 요청에 따라 로직을 수행할 수 있다.
- 요청 url 상관없이 앱이 요청을 수신할 때 마다 매번 실행 할 수 있다.(모든 요청에 공동 로직을 처리하기 위해 사용한다.)

### 사용 방법
```javascript
// 모든 요청에 대한 핸들링
app.use((req, res, next) => {
});
// 특정 요청에 대한 핸들링
app.use(path, (req, res, next) => {
});
```

### app.listen()란?
- 원하는 포트에 서버를 오픈할 수 있다.

### 사용 방법
```javascript
app.listen(port, () => {
});
```
