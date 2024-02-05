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
- 

# REST API 특징

# REST API 장단점


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