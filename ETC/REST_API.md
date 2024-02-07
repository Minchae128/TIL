> *개인적인 학습을 위해 작성한 내용입니다. 옳은 내용만 작성하려 노력했지만 내용에 오류가 있을 수 있습니다.*


# REST 란?
- **REST** : Representational State Transfer 의 약자로 '네트워크에서 통신을 구성할 때 이런 구조로 설계하라는 지침' 
<br>
> 즉,<br> 
    1. HTTP URI(Uniform Resource Identifier)를 통해 자원(Resource)을 명시
<br>
    2. HTTP Method(POST, GET, PUT, DELETE, PATCH 등)를 통해
<br>
    3. 해당 자원(URI)에 대한 CRUD Operation을 적용하는 것을 의미

 **REST가 필요한 이유**
  1. 애플레케이션 분리 및 통합
  2. 다양한 클라이언트의 등장
  3. 최근의 서버 프로그램은 다양한 브라우저와 안드로이드폰, 아이폰과 같은 모바일 디바이스에서도 통신을 할 수 있어야 한다.
  4. 이러한 멀티 플랫폼에 대한 지원을 위해 서비스 자원에 대한 아키텍처를 세우고 이용하는 방법을 모색한 결과, REST에 관심을 가지게 되었다. 


- **REST 구성 요소**
  1. 자원 (Resource) : HTTP URI
  2. 자원에 대한 행위 (Verb) : HTTP Method
  3. 자원에 대한 행위의 내용 (Repressentations) : HTTP Message Pay Load 

- **REST 특징**
  1. Server-Client (서버-클라이언트 구조)
  2. Stateless (무상태)
  3. Cacheable (캐시 처리 가능)
  4. Layered System (계층화)
  5. Uniform Interface (인터페이스 일관성)

# REST API 란?
- 두 개의 컴퓨터가 인터넷을 통해 정보를 안전하게 교환하기 위해 사용하기 인터페이스
- REST 기반으로 서비스 API를 구현한 것
- 최근 OpenAPI(누구나 사용할 수 있도록 공개된 API (ex) 구글맵, 공공 데이터 등)), <br> 마이크로 서비스(하나의 큰 애플리케이션을 여러 개의 작은 애플리케이션으로 쪼개어 변경과 조합이 가능하도록 만든 아키텍처)등을 제공하는 업체 대부분은 REST API를 제공한다.

# REST API 특징
- 사내 시스템들도 REST기반으로 시스템을 분산해 확장성과 재사용성을 높여 유지보수 및 운용을 편리하게 할 수 있다.
- REST는 HTTP표준을 기반으로 구현하므로, HTTP를 지원하는 프로그램 언어로 클라이언트, 서버를 구현할 수 있다.
- 즉, REST API를 제작하면 델파이 클라이언트 뿐 아니라, 자바, C#, 웹 등을 이용해 클라이언트를 제작할 수있다.
# REST API 장단점
**장점**
  1. **쉬운사용 (Easy to use)**<br>
    - REST API는 HTTP 프로토콜을 기반으로 하기 때문에, 개발자들이 이미 익숙한 웹 표준을 사용하여 간단하게 통신할 수 있다. 이는 API를 더 쉽게 이해하고 구현할 수 있게 한다.
  2. **서버와 클라이언트간의 완전한 분리 (Complete Seperation between Client and Server)**<br>
    - REST API는 서버와 클라이언트 간의 역할을 명확하게 분리한다. 이로 인해 서버와 클라이언트의 각 부분을 독립적으로 개발하고 유지보수할 수 있다. 
  3. **특정 데이터 유형에 대한 상세한 표현 (Detail expression for specific data type)**<br>
    - REST API는 다양한 데이터 유형을 표현할 수 있는 자유도를 제공한다. 이는 클라이언트가 필요에 따라 JSON, XML 등 다양한 형식으로 데이터를 주고 받을 수 있음을 의미한다.
  <br>

**단점**
  1. **HTTP 메서드의 제약 (Restriction of HTTP Method)**<br>
    - REST API는 기본적으로 HTTP 메서드를 사용하여 작업을 수행하는데, 때로는 이러한 제한된 메서드 세트가 필요한 작업을 수행하기에 부적합할 수 있다.
  2. **표준의 부재 (Absence of Standard)**<br>
    - REST는 아키텍처 스타일이지만, 정확한 표준은 없다. 이는 종종 서로 다른 구현 사이의 호환성 문제를 야기할 수 있으며, 표준이 부족하다는 느낌을 줄 수 있다.

# REST API의 역할
1. 데이터와 기능 제공
2. 통신 중계
3. 표준화된 인터페이스
4. 상태 관리
5. 명확한 의사소통

# REST API를 사용하는 이유
1. **간편한 통신** : REST API를 사용하면 클라이언트와 서버 간에 통신을 간편하게 할 수 있다.
<br>**why?** REST API는 HTTP 프로토콜을 기반으로 통신 하며, GET, POST, PUT, DELETE와 같은 HTTP 메서드를 사용하여 리소스에 대한 요청과 응답을 주고 받기 때문.

2. **유연성** : 클라이언트와 서버 간의 통신을 단순화 하고 유연하게 만들어줌
<br>**why?** 리소스 지향 아키텍처를 따르기 때문에 URI를 사용하여 각 리소스를 식별할 수 있기 때문에 클라이언트와 서버 간의 통신이 간편하고 유연해진다.

3. **확장성** : REST API는 HTTP 표준을 사용하기 때문에 다양한 플랫폼과 언어에서 지원됩니다. 이는 시스템을 확장하고 통합할 때 유용합니다.

4. **자체 설명력** : REST API는 자체 설명력을 갖추고 있다. 그래서 URI와 HTTP 메서드를 통해 요청의 의도를 명확하게 표현할 수 있으며, 표준 HTTP 상태 코드를 사용하여 요청의 결과를 명시적으로 알려준다.

5. **상태없음(Statelessness)**: REST API는 상태없는(stateless) 특성을 갖는다. 이는 클라이언트의 상태를 서버에 저장하지 않고 각각의 요청이 독립적으로 처리되어야 함을 의미하는데, 이는 서버의 부하를 줄이고 확장성을 높이는 데 도움이 됩니다.

# Reference
* https://stdio-han.tistory.com/88
* https://velog.io/@taeha7b/api-restapi-restfulapi
* https://aws.amazon.com/ko/what-is/restful-api/
* https://khj93.tistory.com/entry/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-REST-API%EB%9E%80-REST-RESTful%EC%9D%B4%EB%9E%80
* https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html
* https://velog.io/@gimminjae/REST-API%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80-%EC%99%9C-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94%EA%B0%80
* https://wallees.wordpress.com/2018/04/19/rest-api-%EC%9E%A5%EB%8B%A8%EC%A0%90/