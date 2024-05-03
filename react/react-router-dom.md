# react-router-dom
### react-router란?
- React-Router는 각 url에 따라 선택된 데이터를 한개의 페이지에서 렌더링하여 보여주는 라이브러리이다.
- 리액트는 spa(single page application) 방식으로 새로운 페이지를 로드하지 않고 하나의 페이지안에서 필요한 데이터만을 가져온다.

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
    <Routes>
      <Route path='/' element={<App />}></Route>
      <Route path='/menu' element={<Menu />}></Route>
    </Routes>
  </BrowserRouter>
};

export default Router;
```

```javascript
// index.js
import Router from './Router';
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(
  <React.StrictMode>
    <Router></Router>
  </React.StrictMode>
);
```
