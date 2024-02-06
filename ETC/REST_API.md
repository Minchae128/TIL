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
  1. 쉬운사용 (Easy to use)
  2. Complete Seperation between Client and Server
  3. Detail expression for specific data type
  <br>

**단점**
  1. Restriction of HTTP Method
  2. 표준의 부재 (Absence of Standard) 


# REST API의 역할
1. API는 서버와 데이터베이스에 대한 출입구 역할을 한다.
    - 데이터베이스에는 수 많은 정보들이 저장된다. 그래서 불특정 다수의 사람들이 데이터베이스에    
      접근할 수 있으면 안되는데, API는 이를 방지하기 위해 서버와 데이터베이스에 대한 출입구 역할을 하며, 허용된 사람들에게만 접근성을 부여해준다.

2. API는 애플리케이션과 기기가 원활하게 통신할 수 있도록 한다.
    - 위 설명에서 애플리케이션은 어플 or 프로그램을 말합니다.
      API는 애플리케이션과 기기가 데이터를 원활히 주고받을 수 있도록 돕는 역할을 합니다.

3. API는 모든 접속을 표준화한다.
    - API는 모든 접속을 표준화 합니다.
      그래서 장비 / 운영체제 등과 상관없이 누구나 동일한 액세스를 얻을 수 있다.
      API는 범용 플러그처럼 작동한다고 볼 수 있습니다.

# REST API를 사용하는 이유
* private API를 이용할 경우
    - 개발자들이 애플리케이션 코드를 작성하는 방법을 표준화함으로써, <br> 
      간소화되고 빠른 프로세스 처리를 가능하게 하고, 소프트웨어를 통합하고자 할 때는 <br>
      개발자들 간의 협업을 용이하게 만들어 줄 수 있다.


# Reference
* https://stdio-han.tistory.com/88
* https://velog.io/@taeha7b/api-restapi-restfulapi
* https://aws.amazon.com/ko/what-is/restful-api/
* https://khj93.tistory.com/entry/%EB%84%A4%ED%8A%B8%EC%9B%8C%ED%81%AC-REST-API%EB%9E%80-REST-RESTful%EC%9D%B4%EB%9E%80
* https://gmlwjd9405.github.io/2018/09/21/rest-and-restful.html
* https://velog.io/@gimminjae/REST-API%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%B8%EA%B0%80-%EC%99%9C-%EC%82%AC%EC%9A%A9%ED%95%98%EB%8A%94%EA%B0%80
* https://wallees.wordpress.com/2018/04/19/rest-api-%EC%9E%A5%EB%8B%A8%EC%A0%90/