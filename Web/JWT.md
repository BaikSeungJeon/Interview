## JWT

### JWT(Json Web Token)란
  - **Json 포맷을 이용**하여 사용자에 대한 속성을 저장하는 Claim 기반의 **Web Token**
  
### JWT 특징 ([출처](https://velopert.com/2389))
  - 수많은 프로그래밍 언어에서 지원
    - JWT 는 C, Java, Python, C++, R, C#, PHP, JavaScript, Ruby, Go, Swift 등 **대부분의 주류 프로그래밍 언어에서 지원**된다.
  - 자가 수용적 (self-contained) 
    - JWT 는 **필요한 모든 정보를 자체적**으로 지니고 있습니다.
    - 또한 **토큰이 검증됐다는것 을 증명**해주는 **signature를 포함**하고있습니다.
  - 쉽게 전달 될 수 있다
    - **JWT 는 자가수용적**이므로, **두 개체 사이에서 손쉽게 전달** 될 수 있습니다. 웹서버의 경우 HTTP의 헤더에 넣어서 전달 할 수도 있고, URL 의 파라미터로 전달 할 수도 있습니다.

### JWT 구조
<img src='https://user-images.githubusercontent.com/85447054/196369853-82998866-2686-433e-8dfd-c0e799c79acc.png' width='600'>

#### Header
- type: 토큰의 타입 지정
- alg: 해싱 알고리즘 지정

#### Payload
- 토큰에 담을 정보가 들어있다.
- name/value 한 쌍으로 이뤄진 claim이 존재
- claim의 세 분류
  - 등록된 (registered) 클레임
  - 공개 (public) 클레임
  - 비공개 (private) 클레임

#### Signature
- 헤더의 인코딩과 정보의 인코딩을 합친 후, 비밀키로 해쉬하여 생성
