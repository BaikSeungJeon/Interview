### Array, Set란?

- Array는 데이터가 연속적인 메모리에 저장된 형태로 각 데이터를 인덱스 값으로 접근 할수가 있는 **Indexed collections입니다.**

- Set는 중복되지 않는 데이터가 모여있는 형태이고 삽입 순서대로 요소를 순회할 수 있습니다. **Keyed Collection**

</br>

### 실제 속도 테스트

[stackoverflow에서 array,set 속도를 실험한 내용](https://stackoverflow.com/questions/39007637/javascript-set-vs-array-performance)

> 💡 테스트는 요소가 10,000개 들어있는 작은테스트와 100,000가 있는 큰 테스트로 나뉨

1. 요소 추가 테스트 : array에 push를 쓰는 것이 set에 add를 쓰는것보다 4배 빨랐습니다.(요소의 개수와는 상관없었습니다)

2. 순회 테스트 : for문으로 array를 순회하는것이 for…of 문을 사용하는 set보다 2~4배가량 빨랐습니다.

3. 요소 제거 테스트 : for문과 splice를 이용해 array에서 요소를 제거하고, for...of와 delete를 이용해 set에서 요소를 제거 작은 테스트에서는 set이 array에 비해 세 배 정도 빨랐으나(2.6ms vs 7.1ms), 큰 테스트에서는 무려 23배 차이가 났습니다. (83.6ms vs 1955.1ms)

> 💡 요소를 제거할 때는 set으로 연산하는것이 빠르고 그외에는 array가 더빠릅니다.

</br>

하지만 중복되지않은 Array를 만들고싶으면  기존 방식은 매우 큰 오버헤드를 발생시킵니다.

간단하게 진행한 실험에서, 10,000개의 요소를 가진 배열에 15개의 요소를 추가하는 데,

요소를 추가하기 전에 추가 하려는 값이 배열에 들어있는지 확인해서 중복값은 스킵하는 과정을 추가했습니다.

이 실험은 74ms가 걸렸다. 그러나 동일 조건에서 set.add(value)를 했을 때는 고작 9ms 걸렸습니다.
