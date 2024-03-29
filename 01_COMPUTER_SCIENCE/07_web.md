# Web 개념

## 목차
1. [브라우저에서 URL치면 발생하는 일](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80%EC%97%90-url%EC%9D%84-%EC%B9%98%EB%A9%B4-%EB%B0%9C%EC%83%9D%ED%95%98%EB%8A%94-%EC%9D%BC)
1. [쿠키와 세션](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#쿠키와-세션)
    1. [쿠키](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#1-%EC%BF%A0%ED%82%A4)
    1. [세션](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#2-세션)
    1. [쿠키와 세션의 차이](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#3-쿠키와-세션의-차이)
1. [캐시](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#캐시)
1. [URI, URL, URN](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#uri-url-urn)
1. [REST, REST API, RESTful](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#rest-rest-api-restful)
    1. [REST API의 장점과 단점](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#rest-api의-장점과-단점)
1. [HTTP 1,2,3의 차이](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#http-1-2-3의-차이)
1. [HTTP 응답코드](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#http-응답코드)
    1. [301, 302 차이] ()
    1. [401, 403 차이] ()
1. [HTTPS](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#https)
    1. [SSL 동작방식] ()
    1. [HSTS] ()
    1. [SSL Stripping] ()
1. [GET, POST 차이](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#get-post-차이)
1. [검색엔진] ()
    1. [웹 크롤러] ()
1. [HTTP 멱등성](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#http-멱등성)
1. [토큰 기반 인증] ()
    1. [JWT] ()
    1. [OAuth] ()
1. [CORS] ()
    1. [CORS 해결방법] ()
1. [JSON, XML의 차이](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#json-xml의-차이)
1. [MIME](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#mime)
1. [AWS](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/07_web.md#aws)

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />


## 브라우저에 url을 치면 발생하는 일
1. 가장 먼저 브라우저에서 DNS서버로 접근하여 입력한 도메인명으로 IP 주소를 가져온다.
2. 브라우저는 HTTP Request Message를 작성한다.
3. 브라우저는 작성한 Message를 OS의 Protocol Stack에 전송을 의뢰한다.
4. 프로토콜 스택이 제어정보를 붙인 패킷을 LAN 어댑터에 넘긴다.
5. LAN 어댑터는 전달받은 패킷을 전기신호로 변환하여 케이블로 송출한다.
6. 메시지는 허브->스위치->라우터->프로바이더->수많은 엑세스 회선->POP->인터넷핵심부 로 이동한다.
7. 메시지는 목적의 서버에 도달한다.
8. 서버의 방화벽은 들어온 패킷에 이상이 없는지 확인하고 캐시서버에 전달한다.
9. 캐시서버는 동일한 요청이 있었는지 확인하고, 만약 있다면 캐시서버에서 즉답하고 없었다면 웹서버로 패킷을 보낸다.
10. 웹서버에 메시지가 도착하면 프로토콜 스택은 메시지에서 패킷을 추출하여 WAS에 전달한다.
11. WAS는 HTTP Response Message를 작성하여 클라이언트에서 Request를 보내는 방법과 같은 방법으로 클라이언트에 송신한다.

> 첫번째는 브라우저가 DNS 서버에서 도메인명으로 IP를 가져오게 됩니다. 그리고 HTTP request 메시지 작성을 하구요. 그리고 OS의 프로토콜 스택에 메시지 전송을 의뢰하게 됩니다. 그럼 프로토콜 스택이 LAN에 제어정보를 붙인 패킷을 LAN 어댑터에 넘기게 되고 LAN어댑터는 이것을 전기 신호로 바꾸어서 LAN 케이블로 송출하게 됩니다. 그러면 송신한 패킷은 허브, 스위치, 라우터를 거쳐 이제 프로바이더에 전달이 되구요. 그러면 패킷은 수많은 엑세스 회선을 통해서 POP를 거쳐 인터넷 핵심부에 들어가게 되고 그 다음에 많은 고속 라우터들 사이로 패킷이 상대방 서버까지 도달하게 됩니다. 서버측의 LAN에 도달하게 되면 방화벽이 패킷을 검사하게 되구요. 이상이 없을 때에는 캐시서버가 먼저 응답 데이터가 있는지 확인하게 됩니다. 그래서 해당 데이터가 없을 경우 웹서버로 전송을 하고 패킷이 웹서버에 도착했을 경우에는 이제 프로토콜 스택은 패킷을 추출해서 WAS에 전달하게 됩니다. 그러면 WAS는 응답 메시지를 많들어서 다시 클라이언트에게 보내게 되는데 이때는 이미 말씀드린 방법대로 다시 클라이언트에게 전달하게 됩니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />


## 쿠키와 세션
HTTP는 상태와 연결에 대한 정보를 저장하지 않기 때문에 이를 개선하기 위하여 쿠키와 세션을 사용한다.

### 1. 쿠키
- 쿠키는 사용자의 정보가 저장된 텍스트 파일이다.
- 쿠키는 브라우저에 저장된다.
- 쿠키는 통신할때 HTTP의 헤더에 담아서 전송된다.
- 쿠키는 HTTP 통신 중 노출될 가능성이 있기 때문에 비교적 보안에 취약하다.

### 2. 세션
- 세션은 서버에 사용자 정보를 저장한다.
- 세션은 브라우저가 종료될 때까지 정보가 유지된다.
- 통신간에 데이터가 전달되지 않기 때문에 비교적 보안이 강하다.

### 3. 쿠키와 세션의 차이
쿠키와 세션은 여러 차이가 있는데, 첫번째로 쿠키는 브라우저에 저장되지만 세션은 서버에 저장된다. 두번째로 쿠키는 텍스트파일이라 삭제하기 전까지 유지되지만 세션은 브라우저가 종료되면 정보를 잃어버리게 된다. 마지막으로 쿠키는 통신중 HTTP 헤더에 담겨 통신에 사용되지만 세션은 통신간 세션데이터가 전송되지 않아 보안에 유리하다.

> HTTP의 경우에는 상태와 연결에 대한 정보를 저장하지 않아서 이것을 저장하는 것이 쿠키와 세션입니다. 우선, 쿠키는 사용자의 정보가 기록된 텍스트 파일인데. 브라우저에 저장되면서, 통신할때 HTTP 헤더에 포함되어 전송되게 됩니다. 그리고 HTTP 통신중에 쿠키 정보가 노출될 수 있기 때문에 보안에 취약하다는 특징을 가지고 있습니다. 두번째는 세션인데요, 세션은 사용자의 정보를 서버에 저장하는데요. 이때 브라우저가 종료될 때까지 유지되게 됩니다. 그리고 서버에 저장되기 때문에 비교적 보안이 강하다는 특징을 가지고 있습니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 캐시
사용자(client)가 웹 사이트(server)에 접속할 때, 정적 컨텐츠(이미지, JS, CSS 등)를 특정 위치(client, network 등)에 저장하여, 웹 사이트 서버에 해당 컨텐츠를 매번 요청하여 받는것이 아니라, 특정 위치에서 불러옴으로써 사이트 응답시간을 줄이고, 서버 트래픽 감소 효과를 볼 수 있다.
웹 캐쉬의 종류
 
### 웹 캐시의 종류 
1. Browser Caches
- 브라우저 또는 HTTP요청을 하는 Client Application에 의해 내부 디스크에 캐쉬
- Cache된 Resource를 공유하지 않는 한 개인에 한정된 Cache
- 브라우저의 Back버튼 또는 이미 방문한 페이지를 재 방문하는 경우 극대화
 
2. Proxy Caches
- Browser Cache와 동일한 원리로 동작하며 Client나 Server가아닌 네트워크 상에서 동작.
- 큰회사나 IPS의 방화벽에 설치 되며 대기시간 & 트래픽 감소, 접근정책 & 제한 우회, 사용률 기록등 수행
- 한정된 수의 클라이언트을 위하여 무한대의 웹서버의 컨텐츠를 캐쉬
  
3. Gateway Caches (REVERSE OR SURROGATE PROXY)
- 서버 앞 단에 설치되어 요청에 대한 캐쉬 및 효율적인 분배를 통해 가용성, 신뢰성, 성능등을 향상
- Encryption / SSL acceleration, Load balancing, Serve/cache static content, Compression등을 수행
- 무한대의 클라이언트들에게 한정된 수(또는 하나)의 웹서버 컨텐츠를 제공

> 캐시는 사용자가 웹 사이트에 접속할 때, 사용자의 빈번한 요청을 특정 위치에 저장하여 불러옴으로써 응답시간 감소와 트래픽 감소를 위하여 사용하는 방법입니다. 웹 캐시의 종류로는 캐시가 저장되는 주체에 따라 브라우저캐시, 프록시캐시, 게이트웨이 캐시 등으로 구분됩니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## URI, URL, URN
- **URI**  
인터넷 자원을 나타내는 고유 식별자이다. URI는 유일하여야 한다는 특징을 지닌다. 전체 주소에서 URL과 URN을 합친 모든 경로를 포함한다.
- **URL**  
URI 중 프로토콜 포함한다. 해당 자원의 위치, Path를 의미하며 일반적으로 사이트 도메인을 의미한다.
웹 상 뿐만 아니라 컴퓨터 네트워크상의 자원은 모두 나타낼 수 있다.
- **URN**  
URI에서 프로토콜 포함하지 않고 실제 주소부터 시작한다. 해당 자원의 이름을 의미하며 독립적인 자원 지시자이다. URL과 다르게 Page 이후 부분까지 포함한다.

> URI는 인터넷 자원을 나타내는 고유 식별자입니다. URI는 유일하여야 한다는 특징을 지니며, 전체 주소에서 URL과 URN을 모두 포함하는 경로를 가집니다. URL은 프로토콜을 포함하여 path까지를 의미하며 자원의 위치, path를 의미합니다. URN은 URI에서 프로토콜을 포함하지 않는 실제 주소부터 시작하여 page 이후 부분까지 포함합니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## REST API, RESTful
REpresentational State Transfer. REST를 기반으로 서비스 API를 구현한 것이다. REST란 자원의 표현(이름)을 통해서 정보를 주고받는 것이다. 자원을 URI로 표현하고 자원에 대한 행위는 HTTP Method로 표현한 것이다. RESTful은 이러한 REST의 원리를 잘 따르고 있는 시스템을 RESTful한 시스템이라고 한다. 즉 자원을 uri로 행위에 맞는 적절한 HTTP Method를 사용한 것이 RESTful한 메소드이다.

**HTTP Method**  
- 삽입: POST
- 수정: PUT
- 조회: GET
- 삭제: DELETE

### REST API의 장점과 단점
- 장점
1. 메시지 자체로 의도가 드러나 이해하기 쉽다.
2. HTTP 프로토콜을 기반으로 클라이언트와 서버의 구분이 명확해진다.
3. 상세한 표현으로 인한 가독성 향상

- 단점
1. 메소드 형태가 제한적이다.
2. 공식화된 표준이 존재하지 않는다.

> RESTAPI는 REST를 기반으로 서비스 API를 구현한 것인데요.  REST란 자원의 표현, 즉 이름을 통해서 자원의 정보를 주고받는 것을 의미합니다. 자원을 URI로 표현하고 자원에 대한 행위는 HTTP Method로 표현한 것이 REST API입니다. RESTful은 이러한 REST의 원리를 잘 따르고 있는 시스템인데요. 자원을 uri로, 행위에 맞는 적절한 HTTP Method를 사용한 것이 RESTful한 메소드입니다. RESTful하지 않은 경우를 예로 들면, CRUD 기능을 모두 POST로 처리한 것을 예로 들 수 있습니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## HTTP 1,2,3의 차이
1. HTTP 1.x
- 텍스트 프로토콜
- 헤더등장
- 서버 상태를 상태코드로 확인 가능
- HTML 외 컨텐츠 파일 전송 가능
- 표준 모델
- Keep Alive 기능 추가
- 지속 커넥션 기능으로 TCP Connection 재활용
- 파이프라이닝 기능 추가
- OPTIONS, GET, HEAD, POST, PUT, DELETE, TRACE 메서드 추가

2. HTTP 2.x
- 구글이 개발한 SPDY를 기반
- HTTP 헤더 압축
- 서버 푸시 기능 추가
- 바이너리 프로토콜로 변환
- 다중 처리 기능 추가

3. HTTP 3.x
- 구글이 개발한 QUIC(Quick UDP Internet Connections) 이용
- UDP로 변경
- QUIC 3 way handshaking 구현
- 보안 강화

>

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## HTTP 응답코드
- 1xx: 조건부 응답. 요청이 정상적으로 수신되었고 처리중임을 의미한다.
- 2xx: 처리성공. 요청이 성공적으로 처리되었음을 의미한다.
- 3xx: Redirection. 클라이언트를 지정된 곳으로 이동시킨다.
- 4xx: 클라이언트 오류. HTTP Request가 잘못되었거나 권한이 없을때 발생한다.
- 5xx: 서버 오류. 서버가 요청을 제대로 수행하지 못할때 발생한다.

> 100번대는 조건부 응답이구요. 요청이 정상적으로 수신되었고 처리하고 있음을 의미합니다. 200번대는 Successful Response로 Request가 성공적으로 처리되었음을 의미합니다. 300번대는 Redirection으로 클라이언트를 지정된 곳으로 이동시킵니다. 400번대는 클라이언트 오류입니다. HTTP Request가 잘못되었거나 권한이 없을때 발생하게 됩니다. 500번대는 서버 오류로, 서버가 요청을 제대로 수행하지 못할때 발생합니다.

### 1. 301, 302 차이
> 301은 영구적인 리다이렉션입니다. 301의 경우 완전히 다른 페이지로 이동하며 이전 페이지의 정보를 가지고 있지 않은 채로 리다이렉션합니다. 그에 비하여 302는 임시 리다이렉션이며, 필요에 따라 이전 페이지의 정보를 가지고 있을 수 있습니다.

### 2. 401, 403 차이
> 둘 다 결론적으로는 권한이 부족할 때 나타나는 메시지이지만, 인증 수준에 따라 다릅니다. 401의 경우에는 사용자가 인증되지 않았기 때문에 요청을 처리하지 못하는 경우 생기며, 403은 사용자가 인증되었지만, 해당 요청에 대한 권한이 없어 거부되었음을 나타내는 상태코드입니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## HTTPS
HTTPS는 암호화 프로토콜(SSL, TLS)을 사용하여 HTTP 통신을 안전하게 하는 프로토콜이다. HTTPS를 사용하는 이유는 HTTP에 다음과 같은 3가지의 문제가 있어서인데, 첫 번째로 http는 평문통신을 하여 중간에 도청이 가능하고, 두 번째로 http는 통신상대를 확인하지 않아 위장이 가능하고, 마지막으로는 완전성을 증명할 수 없기 때문에 변조가 가능하다. 이를 개선하기 위하여 HTTPS를 사용하며 구체적으로는 HTTP 통신 소켓을 암호화 프로토콜을 사용하여 TCP 통신한다.

### 1. SSL 동작방식
### 2. HSTS
### 3. SSL Stripping

>HTTPS는 HTTP에 3가지 문제점이 있어 사용하게 되었습니다. 첫번째는, 평문통을 해서 도청이 가능하고, 두번째는 통신상대를 확인하지 않아 위장이 가능합니다. 마지막으로는 완전성을 증명할 수 없기 때문에 변조가 가능합니다. 이러한 3가지를 보완하기 위하여 HTTPS를 사용하며 구체적으로는 HTTP 통신 소켓을 암호화 프로토콜을 사용하여 TCP와 통신합니다. 그래서 암호화 프로토콜을 사용함으로써 HTTPS는 암호화, 증명서, 변조를 방지할 수 있습니다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## GET, POST 차이
1. 사용목적
GET은 서버의 리소스에서 데이터를 요청할 때, POST는 서버의 리소스를 새로 생성할 때 사용한다. DB로 따지면 GET은 SELECT 에 가깝고, POST는 Create 에 가깝다고 보면 된다.
2. 요청에 body 유무
GET 은 URL 파라미터에 요청하는 데이터를 담아 보내기 때문에 HTTP 메시지에 body가 없다. POST 는 body 에 데이터를 담아 보내기 때문에 당연히 HTTP 메시지에 body가 존재한다.
3. 멱등성 (idempotent)
GET 요청은 단순 조회이기 때문에 몇번을 요청하더라도 결과가 달라지지 않지만, POST는 메소드 자체가 추가의 동작을 하므로 요청으로 인한 결과가 달라질 수 있기 때문에 멱등이 아니다.

> GET과 POST는 세가지의 차이점이 있습니다. 첫번째로 사용목적에 있는데요 GET은 서버에 데이터를 요청할때 사용하고 POST는 서버의 리소스를 새로 생성하기 위하여 사용합니다. 두번째로는 요청 형식입니다. get은 url 파라미터에 요청 데이터를 담아 보내기 때문에 http 메시지에 body가 없지만 post는 body에 데이터를 담아 보내기 때문에 body가 존재합니다. 마지막으로 멱등성입니다. get은 단순 조회를 위한 것이기 때문에 몇번을 요청하더라도 결과가 달라지지 않지만, post는 메소드 자체가 추가 동작을 하므로 요청으로 인한 결과가 달라질 수 있기 때문에 멱등이 아닙니다.
 
 
[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 검색엔진
### 웹 크롤러

>

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## HTTP 멱등성
멱등성(Idempotent)은 수학이나 전산학에서 연산을 여러 번 적용하더라도 결과가 달라지지 않는 성질을 의미한다. 이 멱등성을 HTTP Method에 적용하면 동일한 요청을 한번 보내는 것과 여러번 연속으로 보내는 것이 같은 효과를 가지고, 서버의 상태도 동일하게 남을 때 해당 HTTP Method가 멱등성을 가진다고 한다.

>

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## 토큰 기반 인증
### 1. JWT
### 2. OAuth

>

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## CORS
Cross Origin Resource Sharing. 서로 다른 출처끼리 자원을 공유한다는 뜻으로써 보통 클라이언트와 서버의 도메인이 다를 경우 발생한다.
### CORS 해결방법

>

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## JSON, XML의 차이
||JSON|XML|
|-|-|-|
|태그사용|X|O|
|속도|빠름|느림|
|배열|사용가능|사용불가|
|파싱|js의 eval()함수|XMl 파서 사용|
|안정성|낮음|높음|
|인코딩|UTF-8|다양한 형식 지원|

>

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## MIME
Multipurpose Internet Mail Extensions의 약자로 간단히 말하면 파일 변환을 의미한다. 현재는 웹을 통해 여러 형태의 파일을 인코딩하여 전달하는데 사용한다. MIME으로 인코딩한 파일은 Content-type정보를 앞부분에 담게되며 Content-type은 오디오, 파일 등 여러가지 타입이 있다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />

## AWS
AWS는 아마존닷컴에서 개발한 클라우드 서비스로, 네트워킹을 기반으로 가상 컴퓨터와 스토리지, 네트워크 인프라 등 다양한 서비스를 제공하고 있다. 비즈니스와 개발자가 웹 서비스를 사용하여 확장 가능하고 정교한 애플리케이션 구축하도록 지원하여 준다.

[처음으로 돌아가기](https://github.com/HK-An/today_i_learned/)
<hr />
