# axios

### 사용법
1. get방식, 파라미터 x
```javascript
// front
const result = axios.get('/getBoard').data;
// back
app.get('/getBoard', (req, res) => {
  const { params } = req;
})
```

2. get방식, 파라미터 o
 - get방식에서 파라미터를 포함하여 보내기 위해 {withCredentials: true} 설정을 추가한다.
 - withcross-site Access-Control 요청이 필요한 경우 withCredentials 값을 true로 설정한다.
 - 서버와 클라이언트 도메인이 다를 경우 쿠키 전송이 되지 않는 것을 방지하기 위해 사용한다.
```javascript
// front
const result = axios.get('/getBoard', {params: {seq: 1}}, {withCredentials: true})
// back
app.get('/getBoard', (req, res) => {
  const { query } = req;
});
```

3. post방식, 파라미터 o
- express 미들웨어에서 JSON 형태의 request를 받아 parse 해주기 위해 server.js에 ```app.use(express.json());``` 를 추가해주어야 한다.
 ```javascript
// front
axios.get('/writeBoard', {title: '제목', content: '내용'})
.then((res) => {
})
.catch((err) => {
});
// back
app.post('/writeBoard', (req, res) => {
  const { body } = req;
});
 ```
