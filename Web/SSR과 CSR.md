### SSR: Server Side Rendering

<p align='center'><img src='https://user-images.githubusercontent.com/85447054/196355037-227f1e8a-3700-4ea7-a5c8-a7e9d96af688.png' width='600'></p>

  - 서버로부터 요청해서 받은 내용을 브라우저에 화면에 표시하는 것.
  - 장점
    - 랜더링 속도가 향상됨에 따라 사용자가 웹 페이지 접속 시 바로 볼 수 있습니다.
    - SEO에 최적화가 되어 있습니다.
  - 단점
    - 서버 부하가 CSR보다 상대적으로 많습니다.
    
### CSR: Client Side Rendering

<p align='center'><img src='https://user-images.githubusercontent.com/85447054/196355055-89258ef0-4043-4945-8a63-41064b75cfb7.png' width='600'></p>

  - 페이지의 내용을 클라이언트(브라우저)에서 그리는 것.
  - 장점
    - 컴포넌트 정의와 재사용에 용이합니다.
    - 서버에 부하가 줄어듭니다.
    - 사용자에게 부드러운 UX를 줄 수 있습니다.(사용자 친화적)
  - 단점
    - 초기 HTML가 빈 페이지(초기 렌더링 시간 소요).
    - SEO에 불리합니다.
      - 클라이언트에서 페이지를 그리는 만큼, 초기 HTML이 빈 페이지인데, 웹 페이지의 경우 홈쇼핑 같이 상업적인 성격을 갖고 있기 때문에 이처럼 검색 엔진 최적화에 불리하다면 큰 단점으로 올 것입니다.
    
> Next.Js SSR일까요?
  - Next.js는 React에서 SSR을 도와주는 라이브러리입니다.

  - 완전히 SSR은 아닌 것으로 알고 있습니다.(추가적으로 알아보는 과정이 필요함.)
  - SSR과 CSR의 혼합형태로 hydration이라는 기법을 통해서 SSR의 장점과 CSR의 장점을 모두 가지고 가는 프레임워크입니다.
