# 정확성 보완 기록

확인일: 2026-09-17. 원본에서 설명이 단순화되거나 서로 달라질 수 있는 지점을 교재 작성 과정에서 보완했습니다. 아래 문구는 특정 작성자의 직접 인용이 아니라 교정할 일반화의 요약입니다.

| 주의할 일반화 | 교재에 반영한 설명 | 확인 근거 |
|---|---|---|
| 스위치는 목적지 주소로 학습한다 | 출발지 MAC과 입력 포트를 학습하고 목적지로 전달 | Notion Switch/Router 및 주소 Q&A 대조 |
| 외부 서버의 MAC을 ARP로 구한다 | 경로로 다음 홉을 정한 후 그 링크 주소를 확인 | [RFC 826](https://www.rfc-editor.org/rfc/rfc826.html) |
| 라우터를 지나도 IP 패킷이 그대로다 | NAT가 없어도 TTL과 IPv4 체크섬 등은 달라짐 | Notion 계층·주소·라우팅 설명 대조 |
| TCP 순서 번호는 패킷 번호다 | 바이트 단위이며 SYN·FIN도 번호를 소비 | [RFC 9293](https://www.rfc-editor.org/rfc/rfc9293.html) |
| ACK를 받으면 서버 업무가 완료됐다 | TCP 수신과 앱의 처리 완료는 다름 | [RFC 9293](https://www.rfc-editor.org/rfc/rfc9293.html) 서비스 범위 |
| TCP 종료는 반드시 네 패킷이다 | 양방향 종료는 독립적이며 FIN·ACK 병합 가능 | [RFC 9293](https://www.rfc-editor.org/rfc/rfc9293.html) 종료 |
| min(rwnd,cwnd)만큼 즉시 새로 보낸다 | 이미 보낸 미확인 데이터가 차지하는 양을 고려 | [RFC 5681](https://www.rfc-editor.org/rfc/rfc5681.html) 윈도 정의 |
| Slow start 이후의 동작은 모든 TCP가 같다 | 입문 Reno 모델과 실제 알고리즘 구분 | [RFC 5681](https://www.rfc-editor.org/rfc/rfc5681.html), Notion 혼잡 제어 |
| DNS는 512바이트를 넘으면 반드시 TCP다 | EDNS 수신 크기와 TC 비트, TCP 지원을 함께 설명 | [RFC 6891](https://www.rfc-editor.org/rfc/rfc6891.html), [RFC 7766](https://www.rfc-editor.org/rfc/rfc7766.html) |
| HTTP 무상태라서 매 요청 연결을 끊는다 | 상태 관리와 연결 재사용은 별개 | [RFC 9112](https://www.rfc-editor.org/rfc/rfc9112.html) 지속 연결 |
| HTTPS는 항상 TCP 뒤에 TLS를 얹는다 | HTTP/3는 QUIC과 통합된 TLS 사용 | [RFC 9114](https://www.rfc-editor.org/rfc/rfc9114.html), [RFC 9000](https://www.rfc-editor.org/rfc/rfc9000.html) |
| TLS는 RSA로 세션 키를 전송한다 | 구버전 방식과 TLS 1.3 구분, RSA 서명과 키 교환 구분 | [RFC 8446](https://www.rfc-editor.org/rfc/rfc8446.html) |
| HTTPS는 모든 요청·응답에 공개키 전자서명을 붙인다 | 핸드셰이크 인증과 대칭키 AEAD 레코드 보호를 구분 | [RFC 8446](https://www.rfc-editor.org/rfc/rfc8446.html) |
| 세션은 쿠키보다 무조건 안전하다 | 서버 상태 저장과 세션 ID 전달·탈취 위험을 함께 설명 | Notion 웹 정리, [MDN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Cookies) |
| 멱등 요청은 응답까지 항상 같다 | 반복한 의도된 효과를 기준으로 판단 | [RFC 9110](https://www.rfc-editor.org/rfc/rfc9110.html) |

공식 문서 링크는 해당 논점을 확인하기 위한 근거입니다. 특정 제품의 모든 버전과 환경에서 동일하게 동작한다고 확대 해석하지 않습니다.
