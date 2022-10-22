### 트리쉐이킹(Tree Shaking)

번들의 크기를 줄이거나, 번들링 시간을 줄이기 위해 **불필요한 코드를 제거**하는 모습을 '나무를 흔든다'는 행동에 묘사해 명명한 단어입니다.

> 그럼 트리쉐이킹은 어느 시점에 진행하면 좋나요?

#### 트리쉐이킹 적용 지점

```js
import utils from 'utils-lib';

let count = 0;

const handlePlus = (a) => {
  count += a	
};

utils.parseResult(handlePlus(5));
```

위에서 사용하는 메서드는 utils의 parseResult() 메서드 하나 뿐입니다. parseResult() 메서드 하나를 사용하기 위해 객체 전부를 불러온 상황인데요. 여기서 **사용하지 않는 모듈을 흔들면(트리 쉐이킹)** 다음과 같이 작성이 가능합니다.

```js
import { parseResult } from 'utils-lib'

let count = 0;

const handlePlus = (a) => {
  count += a
};

parseResult(handlePlus(5);
```

이처럼 가끔 거대한 객체를 <code>default export</code> 하여 <code>import</code> 해 오고 그 안에서 필요한 메서드를 꺼내 사용하는 경우가 있는데요. 필요한 부분만 <code>named export</code> 하여 <code>import</code> 한다면, 트리쉐이킹을 통해 번들 사이즈를 줄일 수 있다고 합니다. 
