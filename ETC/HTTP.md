> *개인적인 학습을 위해 작성한 내용입니다. 옳은 내용만 작성하려 노력했지만 내용에 오류가 있을 수 있습니다.*

# HTTP 란?
- **Hyper Text Transfer Protocol**
    - HTTP는 서버와 클라이언트가 서로 데이터를 주고받기 위해 사용되는 통신규약.
    - 웹 문서간에 링크를 통해 연결 할 수 있는 프로토콜이며, 문서뿐 아니라 다음과 같은 여러 종류의 데이터들을 폭 넓게 전송할 수 있다.
        1. HTML, TEXT
        2. 이미지, 음성, 영상, 파일
        3. JSON, XML(API)
        4. 거의 모든 형태의 데이커가 전송 가능
    - 서버간에 데이터를 주고 받을 떄 대부분 HTTP라는 프로토콜을 사용해서 통신한다고 보면 된다.

    > 예를 들어 
        인터넷 주소를 지정할때, <b>http://www.naver.com</b>와 같이 시작하는 것은,<br> <b>www.naver.com</b>이라는 인터넷 주소가 가진 데이터 정보 등의 교환을 HTTP통신 규약대로 처리하라는 것을 의미 한다.
        <br><br>
        또한 인터넷 기반 서비스에는 HTTP외에도 Email, FTP, DNS, NEWS등이 있다.

# HTTP의 통신 구조
- HTTP통신은 **클라이언트(Front-End)**와 **서버(Back-End)**로 나위어진 구조로 되어 있다.
- 클라이언트가 요청하면 서버(Request)가 응답(Response) 하는 것이다.

> 예를 들어,
<br>
클라이언트가 HTTP메세지를 만들어 보내고, 서버에서 요청에 대한 응답이 올 때까지 기다린다.
<br>
그리고 서버는 요청에 대한 결과를 만들어서 응답한다.

## HTTP통신을 하는데 있어, 왜 클라이언트와 서버를 분리해야한 할까?
- 각자의 역할에 집중할 수 있기 때문!!
- 클라이언트에서는 복잡한 비즈니스로직이나 데이터를 다룰 필요 없고, UI를 그리는데 집중할 수 있다.
- 서버에서는 복잡한 비즈니스 로직이나, 데이터를 다루는데만 집중하면 된다.<br>
    만약 트래픽이 폭주해 고도화가 필요한 경우 클라이언트는 신경쓰지 않고 서버만 개선하면 된다.

> 즉, 클라이언트와 서버를 독립적으로 구분한다는 것은 각자의 책임을 나눠 해당 책임에만 집중하여,<br> 클라이언트와 서버 양쪽이 각각 독립적으로 고도화 할 수 있다는 것이다. 

# HTTP 상태 코드


# Reference
* https://www.cloudflare.com/ko-kr/learning/ddos/glossary/hypertext-transfer-protocol-http/
* https://ittrue.tistory.com/192
* https://developer.mozilla.org/ko/docs/Web/HTTP/Overview
* https://inpa.tistory.com/entry/HTTP-%F0%9F%8C%90-%EB%B0%B1%EC%97%94%EB%93%9C-%EB%A1%9C%EB%93%9C%EB%A7%B5-HTTP%EB%8A%94-%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C%EC%9A%94