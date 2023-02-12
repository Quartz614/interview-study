# interview-study 
기술면접을 뿌수기 위해 결의를 다진 백엔드 개발자 모임 <br> 
<table>
  <tbody> 
    <tr>
      <td align="center"><a href="https://github.com/LimJaeminZ"><img src="https://user-images.githubusercontent.com/96826217/207522331-6c49b2ed-c7a9-45df-9e9d-c2442f5307de.jpg" width="400px;" alt=""/><br /><sub><b>임재민</b></sub></a><br /><a href="https://github.com/breaking-interviews/interview-study/tree/main/%EC%9E%AC%EB%AF%BC" title="Documentation">📖</a>         
      <td align="center"><a href="https://github.com/Quartz614"><img src="https://user-images.githubusercontent.com/96826217/207523159-7ac7ebf8-1e77-4f11-b1f4-b25f8a53125f.jpeg" width="400px;" alt=""/><br /><sub><b>주석영</b></sub></a><br /><a href="https://github.com/breaking-interviews/interview-study/tree/main/%EC%84%9D%EC%98%81">📖</a>
      <td align="center"><a href="https://github.com/Mozzi327"><img src="https://user-images.githubusercontent.com/96826217/207523663-38ca521d-cb3e-4510-a010-6eb411d5d557.png" width="400px;" alt=""/><br /><sub><b>조경민</b></sub></a><br /><a href="https://github.com/breaking-interviews/interview-study/tree/main/%EA%B2%BD%EB%AF%BC">📖</a> 
      <td align="center"><a href="https://github.com/LeeGoh"><img src="https://user-images.githubusercontent.com/96826217/207792292-34598bae-eaa1-49b9-93c6-6d45aaf94c60.jpg" width="400px;" alt=""/><br /><sub><b>
이규리</b></sub></a><br /><a href="https://github.com/breaking-interviews/interview-study/tree/main/%EA%B7%9C%EB%A6%AC" title="Documentation">📖</a> 
    </tr>  
  </tbody>
</table>

<br><br>

## 💡 Java
- Java 장단점
- OOP(객체 지향 프로그래밍) 특징
- SOLID 원칙
- 객체 지향 프로그래밍 vs 절차 지향 프로그래밍
- JVM
  - JVM의 구성 요소
  - JVM 실행과정
  - JVM 메모리(Runtime Data Area) 구조
- 가비지 컬렉터
- 접근 제한자
- String vs Char
- ==과 equals
- 데이터 타입
- Call By Value와 Call By Reference
- hashcode
- Wrapper class
- 박싱, 언박싱
- non-static vs static
- main이 static인 이유
- final vs finally vs finalize
- try with resources
- 제네릭
- 직렬화와 역직렬화
- 오버로딩, 오버라이딩
- 추상 클래스와 인터페이스 차이
- Error, Exception
- Checked Exception, Unchecked Exception
- Java Collections
- String, StringBuilder, StringBuffer
- Blocking vs Non-Blocking
- Sync vs Async
- 리플렉션
- Stream
- Fork Join Pool
- 람다식
- Optional
- 자바8 추가된 내용
- Java 8 -> Java 11
- 함수형 프로그래밍
- 멀티스레드 프로그래밍
- Java 동기화 방식
- Synchronized와 Lock & Condition 동기화
- Atomic 동기화

<br><br>

## 💡 Spring & JPA
- 프레임워크란
- Spring 정의 및 장점
- DI (Dependency Injection)
  - 주입 방식
- IoC
- 스프링 컨테이너
- Bean 정의
  - 생명주기
  - 스코프
- 싱글톤 vs 스프링 싱글톤
- Annotation
- Spring Annotation
- 웹 서버와 웹 애플리케이션 서버
- 서블릿
- 서블릿 컨테이너
- MVC 패턴
- AOP(Aspect Oriented Programming)
- POJO
- DAO, DTO
- Filter vs Interceptor
- AOP vs Interceptor
- 레이어드 아키텍처
- OSIV
- 커넥션 풀
- DataSource
- 트랜잭션을 추상화하는 이유
- 트랜잭션 동기화 매니저
- 선언적 트랜잭션 vs 프로그래밍 방식 트랜잭션
- @Transactional
- Propagation 전파단계
- ORM
- 영속성 컨텍스트
- N+1 문제
- fetch join 한계
- OneToMany fetch join 페이징 쿼리 성능 이슈
- MultipleBagFetchException
- OneToOne 양방향 관계 Lazy 로딩 주의
- 상속관계 매핑
- QueryDsl을 사용하는 이유
- Spring batch
- MSA vs Monolithic(모놀리식)
- DDD 구조

<br><br>

## 💡 Database
- DBMS
- DB를 사용하는 이유
- 스키마
- 뷰
- 키
  - 기본키
  - 후보키
  - 슈퍼키
  - 외래키
  - 무결성 제약조건
- 트랜잭션
  - 트랜잭션 ACID
  - 트랜잭션 상태
  - 트랜잭션 격리수준
  - Commit
  - Rollback
  - 동시성 제어
  - 갱신 분실 문제
  - Locking
  - MVCC(격리 수준 제어) 대신 락을 사용하는 이유
  - 낙관적 락보다 DB 트랜잭션 레벨을 Repeatable Read로 하면 되지 않을까?
- 조인
- 트리거
- 힌트
- 인덱스
- Cluster 인덱스
- Non-Cluster 인덱스
- 멀티 인덱스
- B 트리
- 정규화, 반정규화
- 커넥션 풀
- 관계형 DB vs NoSQL
- Redis, MongoDB, Memcached
- Elastic search
- 클러스터링
- 레플리케이션
- 수직 파티셔닝
- 샤딩(수평 파티셔닝)
- SQL Injection
- 행의 개수가 많은 테이블 설계
- Statement, PreparedStatement
- RabbitMQ와 Kafka

<br><br>

## 💡 Network
- OSI 7계층
- DNS
- www.google.com에 접속할 때 일어나는 일
- 4 way-hand shaking
- 포트와 소켓
- CIDR(사이더)
- 서브넷
- 캐스트
- TCP, UDP
- MTU
- HTTP, HTTPS
- HTTP 1.0 vs HTTP 1.1 vs HTTP 2.0
- CORS
- REST API
- 쿠키, 세션
- JWT
- OAuth
- URI, URL, URN
- 중간자 공격
- WebSocket과 Socket.io
- gRPC

<br><br>

## 💡 Operating System
- 운영체제
- 커널
- 메모리구조
- 스택과 힙의 차이점
  - 힙영역을 크게 잡으면 안되는 이유
- 프로세스와 스레드
  - 프로세스 생성 과정
- 멀티 스레드 vs 멀티 프로세스
  - 크롬 탭은 프로세스인지 쓰레드인지
  - 스레드마다 스택을 독립적으로 할당하는 이유
  - 스레드마다 PC 레지스터를 독립적으로 할당하는 이유
- 컨텍스트 스위칭
- IPC(Inter Process Communication)
- 프로세스 종류
- Deadlock
- Critical Section(임계영역)
- 경쟁 상태(Race Condition)
- 수준 스레드
- 사용자 모드와 커널 모드
- 프로세스 스케줄러 종류
- CPU Scheduling
- 인터럽트
- 시스템 콜
- 메모리 관리
- 가상 메모리
- Trashing
- 캐시의 지역성
