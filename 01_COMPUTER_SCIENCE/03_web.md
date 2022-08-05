# Web 개념

## 목차
1. [브라우저에 url을 치면 일어나는 일](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/02_web.md#브라우저에-url을-치면-일어나는-일)
2. [쿠키와 세션](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/02_web.md#쿠키와-세션)
    1. [쿠키](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/02_web.md#쿠키)
    2. [세션](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/02_web.md#세션)
3. [REST API, RESTful이란](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/02_web.md#REST-API-RESTful이란)
4. [HTTP 응답코드](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/02_web.md#HTTP-응답코드)
5. [HTTPS](https://github.com/HK-An/today_i_learned/blob/main/01_COMPUTER_SCIENCE/02_web.md#HTTPS)

## 브라우저에 url을 치면 일어나는 일
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

## 쿠키와 세션
> HTTP는 상태와 연결에 대한 정보를 저장하지 않기 때문에 이를 개선하기 위하여 쿠키와 세션을 사용한다.

### 1. 쿠키
- 쿠키는 사용자의 정보가 저장된 텍스트 파일이다.
- 쿠키는 브라우저에 저장된다.
- 쿠키는 통신할때 HTTP의 헤더에 담아서 전송된다.
- 쿠키는 HTTP 통신 중 노출될 가능성이 있기 때문에 비교적 보안에 취약하다.

### 2. 세션
- 세션은 서버에 사용자 정보를 저장한다.
- 세션은 브라우저가 종료될 때까지 정보가 유지된다.
- 통신간에 데이터가 전달되지 않기 때문에 비교적 보안이 강하다.

## REST API, RESTful이란
> REST;REpresentational State Transfer

REST를 기반으로 서비스 API를 구현한 것이다. REST란 자원의 표현(이름)을 통해서 정보를 주고받는 것이다. 자원을 URI로 표현하고 자원에 대한 행위는 HTTP Method로 표현한 것이다. RESTful은 이러한 REST의 원리를 잘 따르고 있는 시스템을 RESTful한 시스템이라고 한다. 즉 자원을 uri로 행위에 맞는 적절한 HTTP Method를 사용한 것이 RESTful한 메소드이다.

**HTTP Method**  
- 삽입: POST
- 수정: UPDATE ===
- 조회: GET
- 삭제: DELETE ===

## HTTP 응답코드
- 1xx: 조건부 응답. 요청이 정상적으로 수신되었고 처리중임을 의미한다.
- 2xx: 처리성공. 요청이 성공적으로 처리되었음을 의미한다.
- 3xx: Redirection. 클라이언트를 지정된 곳으로 이동시킨다.
- 4xx: 클라이언트 오류. HTTP Request가 잘못되었거나 권한이 없을때 발생한다.
- 5xx: 서버 오류. 서버가 요청을 제대로 수행하지 못할때 발생한다.

## HTTPS
HTTPS는 암호화 프로토콜(SSL, TLS)을 사용하여 HTTP 통신을 안전하게 하는 프로토콜이다. HTTPS를 사용하는 이유는 HTTP에 다음과 같은 3가지의 문제가 있어서인데, 첫 번째로 http는 평문통신을 하여 중간에 도청이 가능하고, 두 번째로 http는 통신상대를 확인하지 않아 위장이 가능하고, 마지막으로는 완전성을 증명할 수 없기 때문에 변조가 가능하다. 이를 개선하기 위하여 HTTPS를 사용하며 구체적으로는 HTTP 통신 소켓을 암호화 프로토콜을 사용하여 TCP 통신한다.
