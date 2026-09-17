# 24회차 학습 로드맵

CS 스터디의 24회차 커리큘럼을 기준으로 구성했습니다. 목표는 개념 간 연결과 면접 답변 능력이며, 아래 완료 기준은 학습을 돕기 위해 재구성했습니다.

현재 네트워크 1~3회차 정리를 종합했고 4회차용 종합·모의면접을 구성했습니다. 5~24회차는 학습 계획이며, 원본 상세 정리를 수집해 완성한 교재가 아닙니다.

| 회차 | 주제 | 말로 설명할 수 있어야 하는 것 | 자료 상태 |
|---|---|---|---|
| 01 | OSI/TCP-IP, IP/MAC/ARP, Switch/Router | 외부 서버로 가는 첫 프레임과 라우터 이후 프레임 비교 | [학습자료](study/network/01-layers-and-routing.md) |
| 02 | TCP/UDP, Port/Socket, Handshake, 전송량 제어 | SEQ/ACK 계산, 연결 식별, 수신자와 경로의 병목 구분 | [학습자료](study/network/02-transport.md) |
| 03 | DNS, HTTP/HTTPS, Cookie/Session | 이름 조회부터 인증 상태까지 단계와 예외 설명 | [학습자료](study/network/03-web.md) |
| 04 | 네트워크 총정리 | 전체 요청 흐름과 장애 가설을 2분 안에 설명 | [종합](study/network/04-end-to-end.md) · [모의면접](interview/mock-interview.md) |
| 05 | Process/Thread, PCB, Context Switching | 자원 공유와 격리 차이, 전환 비용의 원인 비교 | 상세 자료 대기 |
| 06 | CPU Scheduling, Interrupt, System Call, 실행 모드 | 시스템 콜의 흐름과 응답성·처리량의 관계 설명 | 상세 자료 대기 |
| 07 | Race Condition, Critical Section, Mutex/Semaphore/Monitor | 공유 변수 경쟁 사례와 적절한 동기화 방식 제시 | 상세 자료 대기 |
| 08 | Deadlock | 발생 조건, 예방·회피·탐지·회복과 기아 비교 | 상세 자료 대기 |
| 09 | Virtual Memory, Paging, Page Fault, 교체, Thrashing | 주소 변환과 페이지 부재 처리, 성능 저하 원인 설명 | 상세 자료 대기 |
| 10 | 운영체제 총정리 | 요청을 처리하는 스레드의 CPU·메모리·동기화 연결 | 상세 자료 대기 |
| 11 | RDB, SQL, PK/FK, JOIN | 관계 모델의 제약과 JOIN 결과를 예제로 설명 | 상세 자료 대기 |
| 12 | ERD, 정규화, 이상 현상, 반정규화 | 중복 때문에 생기는 문제와 설계 선택 근거 제시 | 상세 자료 대기 |
| 13 | Index, B-Tree/B+Tree, 복합 인덱스 | 검색·쓰기 비용과 컬럼 순서의 영향을 설명 | 상세 자료 대기 |
| 14 | Transaction, ACID, Commit/Rollback | 한 업무의 원자성이 필요한 사례와 실패 처리 | 상세 자료 대기 |
| 15 | Lock, Isolation, MVCC, 읽기 이상 | 두 트랜잭션의 실행 순서로 이상 현상을 재현 | 상세 자료 대기 |
| 16 | 데이터베이스 총정리 | 실행 계획·인덱스·격리 수준으로 성능과 정합성 판단 | 상세 자료 대기 |
| 17 | IoC/DI, Bean, 생명주기/Scope, AOP/Proxy | 객체 생성 책임과 프록시가 동작하는 경계 설명 | 상세 자료 대기 |
| 18 | Servlet, Container, Tomcat, Spring MVC | DispatcherServlet부터 응답까지 호출 흐름 설명 | 상세 자료 대기 |
| 19 | REST, Method/Status, 멱등성, 인증/인가, Session/JWT, CORS/CSRF | API 재시도와 인증 정보를 전달하는 방식 비교 | 상세 자료 대기 |
| 20 | ORM/JPA, Entity, 영속성 컨텍스트, Flush | 객체 변경과 SQL 실행·커밋 시점을 구분 | 상세 자료 대기 |
| 21 | 연관관계, Lazy/Eager, N+1, Fetch Join/EntityGraph | 조회 수 증가를 관측하고 해결책의 한계 설명 | 상세 자료 대기 |
| 22 | @Transactional, 전파/격리, 낙관/비관 Lock, Pool | 트랜잭션 경계와 동시 갱신 문제를 연결 | 상세 자료 대기 |
| 23 | Cache, Scale-up/out, LB, 비동기/MQ, 장애·병목 | 정합성·지연·장애 대응의 선택 근거 제시 | 상세 자료 대기 |
| 24 | 전 범위 총정리 | HTTP부터 DB 반영까지 프로젝트 사례로 설명 | 상세 자료 대기 |

## 자료구조 연결 과제

- 네트워크: 수신 버퍼와 큐, 캐시 조회와 해시 테이블
- 운영체제: 스케줄링 큐, 페이지 교체 정책의 자료구조
- 데이터베이스: B+Tree 탐색과 범위 조회
- 백엔드: LRU 캐시, 메시지 큐와 적체

## 회차별 60분 운영 예시

| 시간 | 활동 |
|---|---|
| 0~10분 | 지난 회차 오답 3개와 사전 질문 공유 |
| 10~30분 | 개념 발표: 정의·필요성·동작·예시 |
| 30~50분 | 꼬리질문과 상황형 문제, 번갈아 답변 |
| 50~60분 | 오해 수정, 답변 점수와 다음 복습 날짜 기록 |

처음 읽었다고 완료 처리하지 않습니다. 하루 뒤 자료 없이 원리와 예외를 설명하고, 일주일 뒤 상황형 문제를 다시 해결하면 복습 완료로 기록합니다.
