- ### Redux
    - Flux 디자인 패턴을 따르고 있으며 기본적으로 순수 함수 형태이기 때문에 test 코드를 짜기 쉽습니다.
    - 상태 관리에서 불변성 유지가 매우 중요하며 상태를 읽기전용으로 취급합니다.
    Immutable.js 와 같은 라이브러리가 쓰이기도 합니다.
    - 개념에 대한 이해가 선행되어야 하고, 여러 라이브러리를 함께 사용하는 경우가 있기 때문에 러닝 커브가 높은 편입니다.
    - 액션을 하나 추가하는데, 작성 필요한 부분이 많고, 컴포넌트와 스토어를 연결하는 필수적인 부분들이 있어 코드양이 많아질 수 있습니다.
- ### Mobx
    - Redux에 비해서 간결하고 깔끔한 구조를 가지고 있으며 보일러 플레이트 코드를 덜 작성해도 됩니다.
    - State의 불변성 유지를 위해 노력하지 않아도 됩니다. Redux에서는 state의 불변성 유지를 위해 여러 라이브러리를
    사용하기도 하는데, Mobx에서는 그러지 않아도 됩니다.
- ### Recoil
    - Recoil은 context API 기반으로 구현된 함수형 컴포넌트에서만 사용할 수 있는 페이스북에서 만든 라이브러이입니다.
    - redux, mobx에 비해서 매우 간단한 구조를 가지고 있습니다.
    - 업데이트가 거의 이루어지지 않고 있습니다.
    2022-10-09 기준으로 나온 지 몇 년이 지났지만 0.7.5버전이 최신버전입니다.
- ### Context API
    - Context API는 자체적으로 상태 관리를 하는 기능은 없습니다. useState나 useReducer을 사용해서 상태 관리를 할 수 있게끔 만들 수 있습니다.
    - Context API는 최적화가 하기 어렵습니다. 다만 프로젝트가 작은 경우에는 로직의 복잡도를 생각했을 때, Redux 등의 라이브러리와의 trade-off로서 생각할 수 있습니다.
    - 컴포넌트에서 만약 Context의 특정 값을 의존하는 경우, 해당 값 말고 다른 값이 변경 될 때에도 컴포넌트에서는 리렌더링이 발생하게 된다고 합니다.
    - 따라서 관심사의 분리가 무척 중요하다고 합니다.

- ### 참고할만한 사이트
    - [리덕스 잘 쓰고 계시나요? - 리디주식회사 RIDI Corporation](https://ridicorp.com/story/how-to-use-redux-in-ridi/)
