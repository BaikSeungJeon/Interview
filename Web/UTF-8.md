### UTF-8이란
- 전세계 모든 문자를 동시에 표현할 수 있도록 만들어진 국제 표준 코드이다.
  - UTF-8을 본다면? '아하 언어와 관련이 있나 보다' 생각하면 된다.
- UTF-8은 유니코드라고도 불린다.
  - UTF-8 =/= 유니코드. 유니코드를 표현하기 위한 방법 중 하나일 뿐이다.
- 컴퓨터가 문자를 표기할 때 영어권 국가만 생각해 만들었기 때문에, 각 나라는 문자를 표현하기 위해 (속된 말로)꼼수를 부려야 했다.
  - 이를 인코딩이라고 한다.
    - 인코딩이란, 문자나 기호들의 집합을 컴퓨터에서 저장하거나, 통신 목적으로 사용할 경우에는 부호로 바꾸는 것을 의미(=부호화)
    - 반대로 부호화된 문자를 복원하는 것을 복호화라고 한다.
  - 근데 각 나라마다 전부 제각각 길을 걷다 보니 문제가 생겼다.
    - ‘이상한 글자가 보인다’, ‘한글이 깨져 보인다’ 등의 문제.
- 이를 위해 탄생한 게 유니코드이다.
- 그 중에서 UTF-8이 가장 힘을 받게 되고 세계 표준으로 인정 받고 있다.

---

2022.10.19.수 업데이트

### 아스키코드랑 유니코드랑 차이점

- 아스키코드(ASCII: American Standard Code for Information Interchange)란?
  - 아스키코드는 이름에 나와 있는 미국에서 정의한 표준화 한 부호 체계이다.
  - 그런데 아스키코드는 7비트 즉, 128개의 고유한 값만 사용한다.
  - 그렇기 때문에 이러한 아스키코드를 가지고 각 나라별 언어를 표현하기에 제한이 걸릴 수밖에 없었고,
  - 이를 해결하기 위해 유니코드가 탄생하게 된 것이다.


### 참고

[본인 벨로그](https://velog.io/@veklog/TIL-221018-%EB%AA%A9)<br>
[아스키(ASCII)코드와 유니코드(Unicode)의 이해](https://whatisthenext.tistory.com/m/103)