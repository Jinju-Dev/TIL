## [ Common JS 문법 ] 
### 전체
```
// import
const mdl = require('mdl.js');

// export
module.esports = {}
```
### 개별
```
// import
exports.mdl1 = '';
exports.mdl2 = {};
exports.mdl3 = () => {};

// export
const {mdl1, mdl2, mdl3} = require('mdl.js');
```
## [ ES6 문법 ]
### 전체
```
// import
import mdl from 'mdl.js';

// export
export default mdl;
```
### 개별
```
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
