### 함수 선언식
- 어디서든 호출이 가능하다.

```js
// 함수 선언식
hi();

function hi(){
  console.log('hi');
}

// hi
```

### 함수 표현식 & 화살표 함수
- 함수를 생성한 코드 아래에서 호출이 가능하다.
- 화살표 함수와 호이스팅이 동일하다.

```js
// 함수 표현식
hello();

const hello = function {
  console.log('hello');
}

// Uncaught SyntaxError: Unexpected token '{' at
```
```js
// 화살표 
bye();

const bye = () => {
  console.log('bye');
}

// Uncaught ReferenceError: Cannot access 'bye' before initialization at
```
