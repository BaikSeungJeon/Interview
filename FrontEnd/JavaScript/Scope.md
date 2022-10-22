## TIL 2022 10 22

### 스코프(Scope)

#### 스코프

단순 번역으로 '범위'를 의미하는 이것은 개발 언어로 '변수에 접근할 수 있는 범위', '함수의 범위'를 의미합니다. 

자바스크립트에는 다음의 스코프가 존재하는데요.
- 전역 스코프
- 지역 스코프

```js
var a = 1; // 전역 스코프

function ex() { // 지역(함수) 스코프
  var a = 2;
  console.log(a);
}

ex(a); // 2
console.log(a); // 1
```

#### 스코프 체인

내부 함수에서 외부 함수는 접근이 가능하지만, 외부 함수에서 접근이 불가능 합니다. 내부 함수에서 변수를 호출하고 변수가 없으면 한 단계 올라가 바깥 스코프에서 찾고, 이렇게 계속 찾아 올라가 전역 스코프까지 도달하게 되는데요. 이런 것을 **스코프 체인**이라고 부릅니다


```js
var a = 1; // 전역 스코프

function ex() { // 지역(함수) 스코프
  console.log(a);
}

ex(a); // 1
```

<code>함수 ex</code> 안에 변수 <code>var a = 2;</code>를 지운 후 함수를 호출하면, 내부에 변수 a가 없다고 해서 <code>error</code>를 출력하는 것이 아닌, 그 위로 올라가 최종적으로 전역 변수에 닿아 <code> 1</code>를 출력하는 것을 볼 수 있습니다. 이러한 현상을 스코프 체인이라고 합니다.

#### 함수 스코프 / 블록 스코프

이처럼 전역 스코프와 지역 스코프를 함수로 나누는 기준을 **함수 스코프**라고 하는데요. 자바스크립트는 이 함수 스코프가 디폴트입니다. 하지만 함수 스코프 말고 블록<code>{ }</code>을 기준으로도 나눌 수 있는데요. 이를 **블록 스코프**라고 합니다.

<code>var</code>는 함수 스코프를 유효 범위로, <code>let</code>, <code>const</code>는 블록 스코프를 유효 범위로 합니다.

```js
var x = 0;
{
  var x = 1; // 재할당
  console.log(x); // 1
}

console.log(x);   // 1

// ES6 이후 let, const 추가로 let을 사용하여 블록 스코프 사용이 가능합니다.
let y = 0;
{
  let y = 1;
  console.log(y); // 1
}

console.log(y);   // 0
```

```js
function solution(s) {
  for(var i = 0; i < 10; i++){
    ...
  }
  
  console.log(i); // 10
}
```

```js
function solution(s) {
  for(let i = 0; i < 10; i++){
    ...
  }
  
  console.log(i); // ReferenceError
}
```
