# MVC2의 정의
###### 작성일 : 2022년 6월 07일

## 개요
모델-뷰-컨트롤러(Model-View-Controller, MVC)는 소프트웨어 개발에 사용되어지는 디자인 패턴이다.

## 구성요소
![mvc relation diagram](https://upload.wikimedia.org/wikipedia/commons/thumb/a/a0/MVC-Process.svg/200px-MVC-Process.svg.png)
![mvc composition in web application](https://upload.wikimedia.org/wikipedia/commons/thumb/5/53/Router-MVC-DB.svg/300px-Router-MVC-DB.svg.png)
1. 모델 
   - 어떠한 동작을 수행하는 코드를 말한다.
   - 표시형식에 의존하지 않는다. (사용자에게 어떻게 보일지에 대해선 신경쓰지 않아도 된다.)
   - 모델은 상태의 변화가 있을 때 컨트롤러와 뷰에 이를 통보한다.
2. 뷰 
   - 흔히 사용자가 보는 화면을 의미한다.
   - 모델은 여러개의 뷰를 가질 수 있다.
   -  뷰는 컨트롤러부터 모델을 가져와 최신상태를 보여준다.
3. 컨트롤러
   - 사용자의 입력이나 어플리케이션에 이미 지정된 명령 등에 따라 모델에 명령을 내려 모델의 상태를 변경한다.
   - 뷰는 여러개의 컨트롤러를 가지고 있다.
   - 사용자는 컨트롤러를 사용하여 모델의 상태를 바꾼다.
   - 컨트롤러는 모델의 변화에 따른 명령을 추가,수정 및 제거할 수 있다.

> 참조
> https://ko.wikipedia.org/wiki/%EB%AA%A8%EB%8D%B8-%EB%B7%B0-%EC%BB%A8%ED%8A%B8%EB%A1%A4%EB%9F%AC