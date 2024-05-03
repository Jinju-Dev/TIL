# ES6 문법 적용 시
### "type": "module" 해줘야하는 이유?
 - commonJs 방식에서 ES6문법을 사용할때 package.json 에서 "type": "module"을 적용해주어야한다.
 - __dirname, __filename은 CommonJs 문법이므로 ES6 문법을 사용한다면 직접 선언해주어야 한다.

### __dirname 이란?
 - 현재 파일이 위치한 폴더의 절대경로를 알려주는 환경 변수
 - "__"는 자바스크립트에서 기본적으로 정의된 변수에 붙는다.
```javascript
import path from 'path';
const __dirname = path.dirname(__filename);
``` 

### __filename 이란?
 - 현재 파일명을 알려주는 환경 변수 
```javascript
import { fileURLToPath } from 'url';
const __filename = fileURLToPath(import.meta.url);
```

---

# import/export

## [ Common JS 문법 ] 
#### 전체
```javascript
// import
const mdl = require('mdl.js');

// export
module.esports = {}
```
#### 개별
```javascript
// import
exports.mdl1 = '';
exports.mdl2 = {};
exports.mdl3 = () => {};

// export
const {mdl1, mdl2, mdl3} = require('mdl.js');
```
## [ ES6 문법 ]
#### 전체
```javascript
// import
import mdl from 'mdl.js';

// export
export default mdl;
```
### 개별
```javascript
// import
// 1. 
export const mdl1 = '';
export const mdl2 = {};
export const mdl3 = () => {};
// 2. 
export {mdl1, mdl2, mdl3};

// export
// 1. 
import {mdl1, mdl2, mdl3} from 'mdl.js';
// 2. 
import * as mdlObj from 'mdl.js';
```
