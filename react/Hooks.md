# Hooks
## Hooks란?
- 함수 컴포넌트에서 React state와 생명주기 기능(lifecycle features)을 연동, 연결(hook info) 해주는 함수이다.
- 클래스형 컴포넌트의 문제점들을 해결하기위해 등장했다.

### useSate
- 함수형 컴포넌트에서 상태 값을 관리하게 한다.
- setBoard를 통해 board값을 변경하게되면 렌더링이 다시 일어난다.
```javascript
import useState from 'react';
const [board, setBoard] = useState({}); 
```

### useEffect
- 어떤 Effect를 발생시키고 싶을 때 사용한다.
- ** Effect는 명령형 함수 또는 타이머, 로깅, 변형, sideEffect 등을 발생시키는 함수를 말한다.
- useEffect에 전달된 함수는 렌더링이 완료된 후에 실행되거나, 어떤 값이 변경됐을 때 실행되도록 할 수 있다.
```javascript
import {useEffect, useState} from 'react';

const BoardDetail = () => {
  const [board, setBoard] = useState({});

  const getBoard = async () => {
    const result = (await axios.get(`/getBoard/${seq}`));
    setBoard(result.data[0]);
  };

  useEffect(() => {
    getBoard();
  }, []);
};
```
