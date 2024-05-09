# react-router
### react-router란?
- React-Router는 각 url에 따라 선택된 데이터를 한개의 페이지에서 렌더링하여 보여주는 라이브러리이다.
- 리액트는 spa(single page application) 방식으로 새로운 페이지를 로드하지 않고 하나의 페이지안에서 필요한 컴포넌트만 가져와서 다른 페이지를 나타내는 방식을 지원한다.
- ** 라우팅: 사용자가 요청한 url에 따라 해당 url에 맞게 페이지를 보여주는 것을 뜻한다.

### 설치
```npm install react-router-dom```

### 설정
```javascript
// Router.js
import {BrowserRouter, Routes, Route} from 'react-router-dom';
import App from './App';
import menu from './Menu';

const Router = () => {
  <BrowserRouter>
    <Routes> // 여러 라우터를 감싸서 그 중 url이 일치하는 하나의 라우터를 렌더링 한다.
      <Route path='/' element={<App />}></Route> // 각 path: 경로, element: 컴포넌트 지정한다.
      <Route path='/menu' element={<Menu />}></Route>
    </Routes>
  </BrowserRouter>
};

export default Router;
```

### 기능

#### Link
- 새로운 페이지를 불러오는 것을 막고 History API를 통해 브라우저 주소의 경로만 바꾸는 기능이 내장되어 있다.
- a태그를 사용하면 새로운 페이지를 불러오므로 사용하지 않도록 한다.

```javascript
import Link from 'react-router-dom'
<Link to='/경로'></Link>
```

#### useNavigate 
- 다른 페이지로 이동할 때 사용한다.

```javascript
import useNavigate from 'react-router-dom'

const 최상위함수 = () => { // 최상위 함수에서 사용해야한다.
  const navigate = useNavigate();
  navigate('/경로'); // 원하는 경로로 이동
  navigate(-1); // 이전 페이지로 이동
}
```

#### useParams
- url의 동적인 파라미터 정보(url parameter)를 가져올 수 있다.

```javascript
// call
import Link from 'react-router-dom';
<Link to={`/Board/${board.seq}`}></Link>
```
```javascript
// router
<Route path={`/Board/:seq`} element={<Board />}></Link>
```
```javascript
// getParam 
import useParams from 'react-router-dom'
const { seq } = useParams();
```


