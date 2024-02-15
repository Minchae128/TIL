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
- HTTP통신은 <b>클라이언트(Front-End)</b>와 <b>서버(Back-End)</b>로 나위어진 구조로 되어 있다.
- 클라이언트가 요청하면 서버(Request)가 응답(Response) 하는 것이다.

> 예를 들어,
<br>
클라이언트가 HTTP메세지를 만들어 보내고, 서버에서 요청에 대한 응답이 올 때까지 기다린다.
<br>
그리고 서버는 요청에 대한 결과를 만들어서 응답한다.

### HTTP통신을 하는데 있어, 왜 클라이언트와 서버를 분리해야 할까?
- 각자의 역할에 집중할 수 있기 때문!!
- 클라이언트에서는 복잡한 비즈니스로직이나 데이터를 다룰 필요 없고, UI를 그리는데 집중할 수 있다.
- 서버에서는 복잡한 비즈니스 로직이나, 데이터를 다루는데만 집중하면 된다.<br>
    만약 트래픽이 폭주해 고도화가 필요한 경우 클라이언트는 신경쓰지 않고 서버만 개선하면 된다.

> 즉, 클라이언트와 서버를 독립적으로 구분한다는 것은 각자의 책임을 나눠 해당 책임에만 집중하여,<br> 클라이언트와 서버 양쪽이 각각 독립적으로 고도화 할 수 있다는 것이다. 

# HTTP 상태 코드
- 상태코드는 클라이언트가 보낸 요청의 처리 상태를 응답에서 알려주는 기능으로서, 3자리 숫자로 이루어져 있다. <br>(100 ~ 500번대 숫자로 이루어져 있다.)

<details>
<summary>1. <b>1XX(정보)</b> : 임시 응답으로 현재 클라이언트의 요청까지는 처리되었으니 계속 진행하라는 의미입니다.
<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(HTTP 1.1 버전부터 추가되었습니다.)<br></summary>

|상태 코드|상태 텍스트|한국어 뜻|서버 측면에서의 의미|
|---|---|---|---|
|1xx|Information|정보 제공|<b>클라이언트의 요청을 받았으며, 작업을 계속 진행하고 있다.</b>|
|100|Continue|계속|<b>계속 진행하라.</b>|
|101|Switching Protocols|프로토콜 전환|<b>프로토콜을 전환하라.</b>|
|102|Processing|처리중|<b>(WebDAV) 처리 중이다.</b>|
|103 ~ 199|Unassigned||현재 할당되지 않은 상태 코드입니다.|

</details>

<br>

<details>
<summary>2. <b>2xx(성공)</b> : 클라이언트의 요청이 서버에서 성공적으로 처리되었다는 의미입니다.</summary>

|상태 코드|상태 텍스트|한국어 뜻|서버 측면에서의 의미|
|---|---|---|---|
|2xx|Success|성공|<b>클라이언트가 요청한 동작을 수신하여 이해하였고 승낙하였으며, 성공적으로 처리하였다.</b>|
|**200**|OK|성공|<b>서버가 요청을 성공적으로 처리하였다.</b>|
|**201**|Created|생성됨|<b>요청이 처리되어서 새로운 리소스가 생성되었다.</b>|
|**202**|Accepted|허용됨|<b>요청은 접수하였지만, 처리가 완료되지 않았다.</b>|
|203|Non-Authoritative Information|신뢰할 수 없는 정보|<b>응답 헤더가 오리지널 서버로부터 제공된 것이 아니다.</b>|
|204|No Content|콘텐츠 없음|<b>처리를 성공하였지만, 클라이언트에게 돌려줄 콘텐츠가 없다.</b>|
|205|Reset Content|콘텐츠 재설정|<b>처리를 성공하였고 브라우저의 화면을 리셋하라.</b>|
|206|Partial Content|일부 콘텐츠|<b>콘텐츠의 일부만을 보낸다.</b>|
|207|Multi-Status|다중 상태|<b>(WebDAV) 처리 결과의 스테이터스가 여러 개이다.</b>|
|208 ~ 299|Unassigned||현재 할당되지 않은 상태 코드입니다.|

</details>

<br>

<details>
<summary>3. <b>3xx(리다이렉션)</b> : 완전한 처리를 위해서 추가 동작이 필요한 경우입니다. 주로 서버의 주소 또는 요청한 URI의 웹 문서가 이동되었으니 그 주소로 다시 시도하라는 의미입니다.</summary>

|상태 코드|상태 텍스트|한국어 뜻|서버 측면에서의 의미|
|---|---|---|---|
|3xx|Redirection|리다이렉션|<b>클라이언트는 요청을 마치기 위해 추가 동작을 취해야 한다.</b>|
|300|Multiple Choices|여러 선택항목|<b>선택 항목이 여러 개 있다.</b>|
|**301**|Moved Permanently|영구 이동|<b>지정한 리소스가 새로운 URI로 이동하였다.</b>|
|302|Found|다른 위치 찾음|<b>요청한 리소스를 다른 URI에서 찾았다.</b>|
|**303**|See Other|다른 위치 보기|<b>다른 위치로 요청하라.</b>|
|304|Not Modified|수정되지 않음|<b>마지막 요청 이후 요청한 페이지는 수정되지 않았다.</b>|
|305|Use Proxy|프록시 사용|<b>지정한 리소스에 액세스하려면 프록시를 통해야 한다.</b>|
|306|(Unused)||예전 버전에서 사용하다가 현재는 사용하지 않는 상태 코드입니다.|
|**307**|Temporary Redirect|임시 리다이렉션|<b>임시로 리다이렉션 요청이 필요하다.</b>|
|308 ~ 399|Unassigned||현재 할당되지 않은 상태 코드입니다.|

</details>

<br>

<details>
<summary>4. <b>4xx(클라이언트 오류)</b> : 없는 페이지를 요청하는 등 클라이언트의 요청 메시지 내용이 잘못된 경우를 의미합니다.</summary>

|상태 코드|상태 텍스트|한국어 뜻|서버 측면에서의 의미|
|---|---|---|---|
|4xx|Client Error|클라이언트 오류|<b>클라이언트의 요청에 오류가 있다.</b>|
|**400**|Bad Request|잘못된 요청|<b>요청의 구문이 잘못되었다.</b>|
|**401**|Unauthorized|권한 없음|<b>지정한 리소스에 대한 액세스 권한이 없다.</b>|
|402|Payment Required|결제 필요|<b>지정한 리소스를 액세스하기 위해서는 결제가 필요하다.</b>|
|**403**|Forbidden|금지됨|<b>지정한 리소스에 대한 액세스가 금지되었다.</b>|
|**404**|Not Found|찾을 수 없음|<b>지정한 리소스를 찾을 수 없다.</b>|
|405|Method Not Allowed|허용되지 않은 메소드|<b>요청한 URI가 지정한 메소드를 지원하지 않는다.</b>|
|406|Not Acceptable|수용할 수 없음|<b>클라이언트가 Accept-* 헤더에 지정한 항목에 관해 처리할 수 없다.</b>|
|407|Proxy Authentication Required|프록시 인증 필요|<b>클라이언트는 프록시 서버에 인증이 필요하다.</b>|
|408|Request Timeout|요청 시간초과|<b>요청을 기다리다 서버에서 타임아웃하였다.</b>|
|409|Conflict|충돌|<b>서버가 요청을 수행하는 중에 충돌이 발생하였다.</b>|
|410|Gone|사라짐|<b>지정한 리소스가 이전에는 존재하였지만, 현재는 존재하지 않는다.</b>|
|411|Length Required|길이 필요|<b>요청 헤더에 Content-Length를 지정해야 한다.</b>|
|412|Precondition Failed|사전 조건 실패|<b>If-Match와 같은 조건부 요청에서 지정한 사전 조건이 서버와 맞지 않는다.</b>|
|413|Request Entity Too Large|요청 객체가 너무 큼|<b>요청 메시지가 너무 크다.</b>|
|414|Request-URI Too Large|요청 URI가 너무 긺|<b>요청 URI가 너무 길다.</b>|
|415|Unsupported Media Type|지원되지 않는 미디어 유형|<b>클라이언트가 지정한 미디어 타입을 서버가 지원하지 않는다.</b>|
|416|Range Not Satisfiable|처리할 수 없는 요청 범위|<b>클라이언트가 지정한 리소스의 범위가 서버의 리소스 사이즈와 맞지 않는다.</b>|
|417|Expectation Failed|예상 실패|<b>클라이언트가 지정한 Expect 헤더를 서버가 이해할 수 없다.</b>|
|418 ~ 421|Unassigned||현재 할당되지 않은 상태 코드입니다.|
|422|Unprocessable Entity|처리할 수 없는 엔티티|<b>(WebDAV) 클라이언트가 송신한 XML이 구문은 맞지만, 의미상 오류가 있다.</b>|
|423|Locked|잠김|(WebDAV) 지정한 리소스는 잠겨있다.|
|424|Failed Dependency|의존 관계로 실패|<b>(WebDAV) 다른 작업의 실패로 인해 본 요청도 실패하였다.</b>|
|426|Upgraded Required|업그레이드 필요함|<b>클라이언트의 프로토콜의 업그레이드가 필요하다.</b>|
|428|Precondition Required|사전 조건 필요함|<b>If-Match와 같은 사전조건을 지정하는 헤더가 필요하다.</b>|
|429|Too Many Requests|너무 많은 요청|<b>클라이언트가 주어진 시간 동안 너무 많은 요청을 보냈다.</b>|
|431|Request Header Fields Too Large|너무 큰 헤더|<b>헤더의 길이가 너무 크다.</b>|
|444|Connection Closed Without Response|응답없이 연결 닫음|(NGINX) 응답을 보내지 않고 연결을 종료하였다. <br> 보통 악의적인 요청에 대해서 사용하며 클라이언트에서는 응답을 볼 수 없고 Nginx로그에는 나타납니다.|
|451|Unavailable For Legal Reasons|법적 사유로 불가|법적으로 문제가 있는 리소스를 요청하였다.| 
|452 ~ 499|Unassigned||현재 할당되지 않은 상태 코드입니다.|

</details>

<br>

<details>
<summary>5. <b>5xx(서버 오류)</b> : 서버 사정으로 메시지 처리에 문제가 발생한 경우입니다. 서버의 부하, DB 처리 과정 오류, 서버에서 익셉션이 발생하는 경우를 의미합니다.</summary>

|상태 코드|상태 텍스트|한국어 뜻|서버 측면에서의 의미|
|---|---|---|---|
|5xx|Server Error|서버 오류|<b>클라이언트의 요청은 유효한데 서버가 처리에 실패했다.</b>|
|**500**|Internal Server Error|내부 서버 오류|<b>서버에 에러가 발생하였다.</b>|
|**501**|Not Implemented|구현되지 않음|<b>요청한 URI의 메소드에 대해 서버가 구현하고 있지 않다.</b>|
|**502**|Bad Gateway|불량 게이트웨이|<b>게이트웨이 또는 프록시 역할을 하는 서버가 그 뒷단의 서버로부터 잘못된 응답을 받았다.</b>|
|503|Service Unavailable|서비스 제공불가|<b>현재 서버에서 서비스를 제공할 수 없다.</b>|
|504|Gateway Timeout|게이트웨이 시간초과|<b>게이트웨이 또는 프록시 역할을 하는 서버가 그 뒷단의 서버로부터 응답을 기다리다 타임아웃이 발생하였다.</b>|
|505|HTTP Version Not Supported|HTTP버전 미지원|<b>클라이언트가 요청에 사용한 HTTP버전을 서버가 지원하지 않는다.</b>|
|506|Unassigned||<b>현재 할당되지 않은 상태 코드입니다.</b>|
|507|Insufficient Storage|용량 부족|<b>(WebDAV) 서버에 저장 공간 부족으로 처리에 실패하였다.</b>|
|512 ~ 599|Unassigned||현재 할당되지 않은 상태 코드입니다.|

</details>

<br>

# Reference
* https://www.cloudflare.com/ko-kr/learning/ddos/glossary/hypertext-transfer-protocol-http/
* https://ittrue.tistory.com/192
* https://developer.mozilla.org/ko/docs/Web/HTTP/Overview
* https://inpa.tistory.com/entry/HTTP-%F0%9F%8C%90-%EB%B0%B1%EC%97%94%EB%93%9C-%EB%A1%9C%EB%93%9C%EB%A7%B5-HTTP%EB%8A%94-%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C%EC%9A%94
* https://hongong.hanbit.co.kr/http-%EC%83%81%ED%83%9C-%EC%BD%94%EB%93%9C-%ED%91%9C-1xx-5xx-%EC%A0%84%EC%B2%B4-%EC%9A%94%EC%95%BD-%EC%A0%95%EB%A6%AC/