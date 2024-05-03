# react-router-dom
### react-router-dom이란?
- 

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
