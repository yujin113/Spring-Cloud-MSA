# Spring-Cloud-MSA

### API Gateway Service
- 사용자의 라우팅 설정에 따라 각 엔드포인트로 클라이언트 대신해서 요청하고, 응답을 받으면 다시 클라이언트에 전달해주는 proxy 역할
- 시스템의 내부 구조는 숨기고, 외부의 요청에 대해 적절한 형태로 가공해서 응답할 수 있다는 장점
- 클라이언트는 직접 microservice를 호출하지 않고, gateway만 상대 -> 변경작업이 훨씬 수월해짐
<br>

### Spring Cloud에서 microservice끼리의 통신 방법
1. RestTemplate
2. Feign Client
<br>

### Netflix Zuul
- API gateway 역할, Routing 기능
- SpringBoot 2.4에서 Maintenanace 상태 (더이상 지원 x)
- Spring Cloud Gateway 사용 권장
<br>

### Spring Cloud Gateway
- gateway 서비스, rounting 서비스 구현
- 비동기 처리가 가능하다
- Tomcat이 아닌 Netty라는 비동기 내장 서버가 작동됨

---
### Spring Cloud Gateway - Filter 적용
<img width="1330" alt="image" src="https://github.com/yujin113/Spring-Cloud-MSA/assets/73515587/7fdc2e97-0dfc-4bb3-93c6-f8ae6c42f2f7">

- Gateway는 클라이언트로부터 요청 정보를 받고, Predicate 영역에서 요청에 대한 조건을 분기한다. (요청 정보가 들어오면 어떤 것인지 판단하는 역할)
- PreFilter, PostFilter를 작성해서 요청 정보를 구성할 수 있다.
작성 방법은 두 가지 : Property, Java code
