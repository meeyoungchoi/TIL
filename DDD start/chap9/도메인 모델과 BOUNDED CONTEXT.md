## 도메인 모델과 경계

- 하위 도메인 마다 같은 용어라도 의미가 다르고 같은 대상이라도 지칭하는 용어가 다를 수 있다
- 한개의 모델로 모든 하위 도메인을 표현하려는 시도는 올바른 방법이 아니다
- 모델은 특정 컨텍스트에서 완전한 의미를 갖는다
- 서로 구분되는 경계를 갖는 컨텍스트를 DDD에서는 BOUNDED CONTEXT라고 부른다
- 예) 같은 제품이라도 카탈로그 컨텍스트와 재고 컨텍스트에서 제품의 의미가 서로 다르다

### BOUNDED CONTEXT

- 한개의 BOUNDED CONTEXT에서 여러 하위 도메인을 포함다더라도 하위 도메인마다 구분되는 패키지를 갖도록 구현해야 한다
- 그래서 모델이 서로 섞이지 않아 하위 도메인 마다 BOUNDED CONTEXT를 갖는 효과를 낼 수 있다

### BOUNDED CONTEXT의 구현

- BOUNDED CONTEXT는 도메인 기능을 사용자에게 제공하는데 필요한 표현 영역 , 응용 서비스, 인프라 영역 등을 모두 포함한다
- 도메인 모델의 데이터 구조가 바뀌면 DB 테이블 스키마도 함께 변경해ㅑㅇ 하므로 해당 테이블도 BOUNDED CONTEXT에 포함된다

### BOUNDED CONTEXT 간 통합

- 마이크로서비스와 BOUNDED CONTEXT
- 마이크로서비스는 애플리케이션ㅇ르 작은 서비스로 나누어 개발하는 아키텍처 스타일이다
- 개발 서비스를 독립된 프로세스로 실행하고 각 서비스가 REST API나 메시징을 사용하여 통신하는 구조를 갖는다
- 마이크로서비스의 특징은 BOUNDED CONTEXT와 잘 어울린다
- BOUNDED CONTEXT를 마이크로서비스로 구현하면 컨텍스트별로 모델이 분리된다
- 마이크로서비스 마다 프로젝트를 생성하므로 BOUNDED CONTEXT 마다 프로젝트를 만들게 된다
- 별로 프로세스로 개발한 BOUNDED CONTEXT는 독립적으로 배포하고 모니터링하고 확장할 수 있게 마이크로서비스가 도와준다

### BOUNDED CONTEXT 간 관계

- 컨텍스트 맵
- 컨텍스트 맵은 시스템의 전체 구조를 보여준다
- 하위 도메인과 일치하지 않는 BOUNDED CONTEXT를 찾아 모데인에 맞게 BOUNDED CONTEXT를 조절하고 사업의 핵심 도메인을 위해 조직 역량을 어떤 BOUNDED CONTEXT에 집중할 지 파악하는데 도움을 준다