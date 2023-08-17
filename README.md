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
<details>
<summary> OSI 7 Layer 또는 TCP/IP Layer에서 계층화하는 이유가 무엇인가요?</summary>
<div markdown="1">
- 계층구조를 가짐으로써 각 구간별로 데이터의 움직임을 알 수 있다.
- 설계가 간단해진다.
</div>
</details>  

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

<details>
<summary> 로드 밸런싱이란 무엇인가요?</summary>
<div markdown="1">
- Load Balancer를 클라이언트와 서버 사이에 두고, 부하가 일어나지 않도록 여러 서버에 분산시켜주는 방식이다.
- scale-out: 기존의 서버 성능과 동일하거나 낮은 성능의 서버를 증설
이렇게 여러대의 서버로 분산해주는 것을 로드 밸런싱이라고 한다.  
  
- 로드 밸런스 알고리즘
1. 라운드 로빈
  - 서버에 들어온 요청을 순서대로 돌아가며 배정하는 방식
  - 여러 대의 서버가 동일한 스펙을 갖고 있고, 서버와의 연결(세션)이 오래 지속되지 않는 경우 활용하기 적합하다.
2. 가중 라운드로빈
  - 각각의 서버마다 가중치를 매기고 가중치가 높은 서버의 요청을 우선적으로 배분하는 방식
  - 서버의 트래픽 처리 능력이 상이한 경우 활용하기 적합하다.
3. IP 해시
  - 클라이언트의 IP 주소를 특정 서버로 매핑하여 요청을 처리하는 방식
  - 사용자의 IP를 해싱(임의의 길이를 지닌 데이터를 고정된 길의 데이터로 매핑하는 것)해 로드를 분배하므로
  - 사용자가 항상 동일한 서버로 연결되는 것을 보장한다.
4. 최소 연결
  - 요청이 들어온 시점에 가장 적은 연결 상태를 보이는 서버에 우선적으로 트래픽을 배분하는 방식
  - 자주 세션이 길어지거나, 서버에 분배된 트래픽들이 일정하지 않은 경우 적합한 방식
5. 최소 요청 시간
  - 서버의 현재 연결 상태와 응답 시간을 모두 고려하여 트래픽을 배분하는 방식
  - 가장 적은 연결 상태와 가장 짧은 응답시간을 보이는 서버에 우선적으로 로드를 배분한다.  

- OSI 7계층에서 사용되는 로드밸런서 종류와 특징
  - L4 : 중간의 스위치를 통해 각각의 서버에 접속을 분산시켜 보내주는 역할을 한다. 전송 계층(Transport Layer)에서 작동하며 IP, Port, Session을 기반으로 한 로드밸런싱을 담당한다. TCP/UDP 프로토콜을 이용하여 프로토콜의 헤더를 보고 로드 밸런싱을 수행하며 주로 Round Robin 방식을 이용해 부하를 분산한다.
  - L7 : Application 계층을 사용, URL 또는 HTTP 헤더에서 부하 분산이 가능
</div>
</details> 

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
- 3-Handshaking과 4-Handshaking의 과정을 설명해주세요.

<details>가
<summary> TCP 연결 설정 과정과 연결 종료 과정의 단계가 다른 이유는 무엇인가? </summary>
<div markdown="1">

연결 과정에서는 연결 과정 수립을 위한 최소한의 설정을 진행한다.  
종료 과정시에는 Client가 데이터 전송을 마쳤다고 하더라도 Server는 아직 보낼 데이터가 남아있을 수 있기 때문에   
일단 FIN에 대한 ACK만 보내고, 데이터를 모두 전송한 후에 자신도 FIN 메시지를 보내는 방식으로 진행되어야 하기 때문이다.

</div>
</details>  

- LAN과 WAN의 차이
- Cookie와 Session의 차이

<details>
<summary> DNS서버 란? </summary>
<div markdown="1">
- 컴퓨터에 접속하려면 IP주소를 입력해야 하는데 [www.naver.com](http://www.naver.com) 을 입력해도 들어가짐
간단히 말하면 DNS는 URL을 IP주소로 변환하는 서비스다.

- IP주소가 아닌 naver.com과 같은 주소를 사용하여 접속하도록 돕는 것을 DNS의 이름해석이라고 한다.
- naver.com과 같이 컴퓨터나 네트워크를 식별하기 위해 붙여진 이름을 도메인 이름이라고 한다.
- www는 호스트 이름(서버 이름)이라고 한다.

</div>
</details> 

## 🍀운영체제
