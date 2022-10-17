## GLSB의 정의와 특이점

> GSLB(Global Server Load Balancing)
> 이름만 보면 얼핏 업그레이드된 로드 밸런싱 형태라고 생각할 수 있지만, 이름과는 다르게 DNS 서비스의 발전된 형태이다.(물론 LB 역할을 하긴 하지만 근본적으론 DNS형태라 보면 좋을 것 같다
> </br>
> 출처:  [코딩스타트 :: 네트워크 - GSLB(Global Server Load Balancing)란?](https://coding-start.tistory.com/339)

> DNS 레코드를 추가하는 방식의 부하 분산과 L4/L7 스위치를 이용한 GSLB의 가장 큰 차이는 '서버 헬스체크'를 하느냐 안 하느냐 입니다. 
> 헬스체크를 하지 않을 경우 해당 서버가 장애가 나서 접속이 불가능해도, 해당 내용을 모르고 네임 서버가 접속할 수 없는 서버의 IP 주소를 알려주죠. 사용자에게는 서버를 찾을 수 없다는 메시지가 나가게 되겠죠. GSLB는 다릅니다. 서버의 헬스 체크가 지속해서 이루어지기 때문에 특정 위치에 있는 서버로 접속이 어려우면 다른 위치의 서버 IP를 배포합니다. 헬스 체크를 통해 다른 쪽 서버 상태를 파악하기 때문에 접속 불가능한 곳으로 사용자를 안내하지 않습니다. 
> <br>
> [Global server load balancing (GSLB) 다 쓰는 이유가 있는 구성](https://smashingpumpkins.tistory.com/entry/Global-server-load-balancing-GSLB-%EB%8B%A4-%EC%93%B0%EB%8A%94-%EC%9D%B4%EC%9C%A0%EA%B0%80-%EC%9E%88%EB%8A%94-%EA%B5%AC%EC%84%B1)


## 출처 및 참고
- [코딩스타트 :: 네트워크 - GSLB(Global Server Load Balancing)란?](https://coding-start.tistory.com/339)
- [Global server load balancing (GSLB) 다 쓰는 이유가 있는 구성](https://smashingpumpkins.tistory.com/entry/Global-server-load-balancing-GSLB-%EB%8B%A4-%EC%93%B0%EB%8A%94-%EC%9D%B4%EC%9C%A0%EA%B0%80-%EC%9E%88%EB%8A%94-%EA%B5%AC%EC%84%B1)
- [효율적인 부하 분산 라우팅을 위한 GSLB 기술 활용 - ZDNet korea](https://zdnet.co.kr/view/?no=00000010055390)
- [로드 밸런싱(SLB, Server Load Balancing) 기본 개념](https://incredible-larva.tistory.com/entry/%EC%84%9C%EB%B2%84-%EB%A1%9C%EB%93%9C-%EB%B0%B8%EB%9F%B0%EC%8B%B1SLB-Server-Load-Balancing-%EA%B8%B0%EB%B3%B8-%EA%B0%9C%EB%85%90)
