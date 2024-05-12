# LocalStorage, SessionStorage

### LocalStorage란?
- 로컬에 도메인 별로 지속되는 storage
- 시간제한이 없고, 브라우저가 종료되도 죽지 않는다.
- 값을 지우려면 직접 지워줘야한다.

### 사용 방법
```javascript
// 값 저장하기
localStorage.test = '';
localStorage.setItem('', '');
// 값 불러오기
localStorage.test;
localStorage.getItem('');
localStorage.getItem(); // 전체 값 불러오기
// 값 삭제하기
localStorage.removeItem('');
localStorage.clear();
```

### SessionStorage란? 
- 세션(프로세스, 탭, 브라우저)가 종료될 때까지 지속되는 storage
- 같은 브라우저라도 다른 탭일 경우 데이터가 공유되지 않는다.(다른 브라우저일 경우도 마찬가지이다.)
- 여기서 session이 의미하는 것은 가장 작은 단위인 탭단위를 의미한다.

### 사용 방법
```javascript
// 값 저장하기
sessionStorage.setItem('', '');
// 값 불러오기
sessionStorage.getItem('');
// 값 삭제하기
sessionStorage.removeItem('');
sessionStorage.clear();
```
