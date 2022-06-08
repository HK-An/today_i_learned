# 정의
###### 작성일 : 2022년 06월 08일

## 개요
Spring Secuirty는 스프링 기반의 애플리케이션의 보안(인증과 권한, 인가 등)을 담당하는 스프링의 하위 프레임워크이다.
스프링 시큐리티를 이용하면 단순 인증 및 권한처리뿐 아니라, 각종 보안이슈도 처리할 수 있다.

## 기본용어
- 접근 주체(Principal)
  - 보호된 리소스에 접근하는 대상
  - ex) 사용자(User), 손님(Guest) 등
- 인증(Authentication)
  - 현재 접근을 시도한 대상의 Identification을 확인하는 절차
  - SecurityContext에 보관되고 사용됨.
  - ex) 로그인 등의 상황에서 ID와 PASSWORD를 보내는 등의 방법으로 올바른 유저인지 확인한다.
- 인가(Authorize)
  - 해당 리소스에 대하여 접근한 대상이 해당 권한을 가지고 있는지 확인하는 과정
  - 인증(Authentication)이 선행되어야 한다.
  - ex) 회원전용게시판 글작성, 관리자페이지 접근 등
- 권한(Authority)
  - 요청한 유저의 권한을 검사함
  - 인가(Authorize)의 요소로 사용됨

## 주요 기능
- 간소화된 인증 및 권한 부여
- [스프링 MVC](https://github.com/HK-An/today_i_learned/blob/main/CONCEPT/mvc/definition.md)와 서블릿 API와의 통합
- 공통적인 보안 공격 방지(CSRF, XSS 등))
- SAML 및 LDAP과의 통합

## 특징
- 보안과 관련하여 체계적으로 많은 옵션을 제공하여 편리하게 사용할 수 있음
- Filter 기반으로 동작하여 MVC와 분리하여 관리 및 동작
- Annotation을 통한 간단한 설정
- Spring Security는 기본적으로 세션 및 쿠키 방식으로 인증
![tempimg](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FRdJGx%2FbtqD9Ouzlub%2F5At2yq9zCxACpguIwWKHE1%2Fimg.png)
- 인증관리자(Authentication Manger)와 접근 결정 관리자(Access Decision Manger)를 통하여 사용자의 리소스 접근을 관리한다.
- 인증 관리자는 UsenamePasswordAuthenticationFilter, 접근 결정 관리자는 FilterSecurityInterceptor가 수행

## 구조
###  인증관련 Architecture
![spring security structure](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=http%3A%2F%2Fcfile23.uf.tistory.com%2Fimage%2F99A7223C5B6B29F003F5F0)

### 인증 순서
Spring security는 전통적인 cookie-session 인증 방식을 사용한다. 인증은 아래와 같은 순서로 이루어진다.
1. 유저가 로그인을 시도 (AuthenticationFilter접근)
2. Authentication 인터페이스의 구현체인 UsernamePasswordAuthenticationToken 생성
3. AuthenticationManager에게 해당 토큰이 올바른 유저인지 확인
4. DB에 존재하는 유저의 경우 UserDetails로 꺼내서 유저의 Session 생성
5. Spring secuirty의 인메모리 세션저장소인 SecurityContextHolder에 저장
6. 유저에게 Session ID와 함께 응답을 내려줌
7. 이후 요청에서는 요청쿠키에서 JSESSIONID를 확인하여 검증 후 유효하면 Authentication을 부여한다.

> 참조  
> https://sjh836.tistory.com/165  
> https://devuna.tistory.com/55
