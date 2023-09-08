#### API Gateway Service
- 사용자의 라우팅 설정에 따라 각 엔드포인트로 클라이언트 대신해서 요청하고, 응답을 받으면 다시 클라이언트에 전달해주는 proxy 역할
- 시스템의 내부 구조는 숨기고, 외부의 요청에 대해 적절한 형태로 가공해서 응답할 수 있다는 장점
- 클라이언트는 직접 microservice를 호출하지 않고, gateway만 상대 -> 변경작업이 훨씬 수월해짐
<br>

#### Spring Cloud에서 microservice끼리의 통신 방법
1. RestTemplate
2. Feign Client
<br>

#### Netflix Zuul
- API gateway 역할, Routing 기능
- SpringBoot 2.4에서 Maintenanace 상태 (더이상 지원 x)
- Spring Cloud Gateway 사용 권장
<br>

#### Spring Cloud Gateway
- gateway 서비스, rounting 서비스 구현
- 비동기 처리가 가능하다