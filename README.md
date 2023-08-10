# cs-study
## 스터디 시간 !
화요일 9시  
8월 1,8,22,29(4번), 9월 5,12,19,26(4번) -> 8번 9월 26일 종료  

## 스터디 규칙 !	
3회 불참시 추방  

## 스터디 방식 !
금요일까지 질문 3~5개 각자 올리기 (구글 문서에)  
화요일에 만나면   
주 별 답변 못한 문제를 재응답 (30분)  
(10~20 분 사이 정해두고 3:1 한명에게 질문하기 궁금한것 계속 물어보면서 , 리뷰(5분) ) * 4   (80분)  
리드미 정리  (30분)  


## 각 주차별 계획
1주차 : 네트워크   
2주차 : 네트워크   
3 주차 : 운영체제   
4 주차 : 운영체제   
5 주차 : 자바/스프링/JPA  
6 주차 : 자바/스프링/JPA  
7 주차 : 데이터 베이스  
8 주차 : 알고리즘 / 자료구조  

## 참고 사이트
https://github.com/gyoogle/tech-interview-for-developer  
https://github.com/JaeYeopHan/Interview_Question_for_Beginner  

## 프로젝트 정리법  
가장 도전적이 었던것  
실수, 실패담  
즐거웠던것 
리더십 
팀원과의 갈등 
남들과 다르게 행동했던 것  


## 🍀네트워크 
<details>
<summary>Http는 Stateful 한가요?</summary>
<div markdown="1">

안녕

</div>
</details> 

- TCP와 UDP의 차이점에 대해서 설명하기 
- 웹 브라우저가 웹 사이트를 렌더링 하는 과정에 대해서 설명하기 
- Synchronous & Asynchronous와 Blocking & Nonblocking의 차이 
- 대칭키, 비대칭키 암호화 방식에 대해 설명 
- GET과 POST 차이를 설명 
- TCP/IP 프로토콜 4계층 종류와 설명 
- IP란 무엇인가? IP의 풀네임 및 정의
- 게이트 웨이란?
- HTTPS 프로토콜이란?
- ARP와 RARP 차이
- OSI7계층 각각의 의미와 순서
- 브라우저에 "www.google.com" 입력하면 어떤일이 일어날까요?
- RESTful API란 무엇인가요?
- CORS는 무엇인가요?
- CSRF는 무엇인가요?
- OSI 7 Layer 또는 TCP/IP Layer에서 계층화하는 이유가 무엇인가요?
<details>
<summary> 현대 웹 에서는 비연결성을 해결방법을 설명해주세요.</summary>
<div markdown="1">

- 비 연결성 :  HTTP 요청에 대한 응답을 제공한 후에 연결을 끊는다. 
- 비 상태성 : HTTP 요청과 응답하는 동안 상태를 저장하지 않는다.  

### HTTP 비지속 연결
![connectionless.png](images/img2_connectionless.png)
서버에서 응답이후에 TCP에게 연결을 끊으라고 요청하고 HTTP클라이언트가 응답메시지를 받으면 TCP 연결이 중단된다.   
(연결이 유지 되지 않는다, 즉 하나의 요청메세지와 하나의 응답메시지에 하나의 연결이다)


### HTTP 지속 연결(Persistent Connections)
![persist_connection.png](images/img1_persist_connection.png)
HTTP/1.1 부터 Keep-Alive 기능이 추가되어 하나의 TCP연결로 여러개의 요청과 응답을 처리할 수 있다.
일정시간 동안 연결을 유지해서 요청과 응답이 모두 끝날때까지 연결해준다.
keep-alive : 서버의 HTTP요청시, 요청 message 헤더 추가   

</div>
</details> 

- 로드 밸런싱이란 무엇인가요
- 프록시에 대해서 설명해주세요
- 서브넷 마스크에 대해서 설명해주세요
- 매체 접근 제어 (Media Access Control)에 대해서 설명해주세요

<details>
<summary> patch put post의 차이 </summary>
<div markdown="1">

### POST(create)
리소스의 생성을 담당한다.  
요청시마다 새로운 리소스를 할당한다. 

### PUT(update)
멱등성을 보장한다 (여러번 보내도 같은 리소스를 반환한다)  
리소스의 생성과 수정을 담당한다.  
수정시 전체를 덮어쓴다.  

### PATCH(update)
수정만 담당하며 리소스의 일부분만 수정할때 사용한다. (일부만 업데이트)  
PATCH는 멱등하지 않다. 하지만 멱등으로 설계할 수도 있다.  


</div>
</details> 

- TCP/IP 혼잡 제어 기법이 왜 사용되는가?
- TCP 연결 설정 과정과 연결 종료 과정의 단계가 다른 이유?
- 3-Handshaking과 4-Handshaking의 과정을 설명해주세요.
- LAN과 WAN의 차이
- Cookie와 Session의 차이
- DNS서버 란?

## 🍀운영체제
