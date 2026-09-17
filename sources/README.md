# 출처와 작성 범위

작성 기준일: **2026-09-17**

## 작성 방법

CS 스터디의 접근 가능한 네트워크 학습 노트를 바탕으로 공통 논점을 추출하고 중복을 통합했습니다. 계층과 라우팅, 전송, 웹, 종합 진단으로 재구성했으며 면접 질문·연습문제는 새로 작성했습니다.

공식 RFC와 MDN을 통해 특히 TCP 번호·종료·윈도, DNS TCP/EDNS, HTTP 연결·멱등성, TLS 버전, 쿠키 속성을 확인했습니다. 보완한 논점은 [정확성 보완 기록](corrections.md)에 있습니다.

## 범위와 한계

- 네트워크 1~3회차를 토대로 학습자료를 만들고 4회차 종합 연습을 구성했습니다.
- 운영체제·DB·Spring은 커리큘럼 로드맵 단계이며 상세 원본 종합을 완료한 교재가 아닙니다.
- 원본의 일부 미지원 블록과 접근 불가 링크, 이미지 속 텍스트, 첨부 PDF, 데이터베이스 전체 행은 수집 범위에 포함하지 않았습니다.
- 공개본은 원본 전체의 백업이나 완전한 내보내기가 아닙니다.

## 원본 추적과 공개 범위

비공개 원본 링크·페이지 ID·수정일 목록은 공개 저장소에 넣지 않았습니다. 원본 추적 기록은 별도 로컬 파일 `notion-source-map.local.md`로 보관합니다. 공개 저장소에는 재작성한 설명과 아래 공개 참고문서만 제공합니다.

새 환경에서 원본을 갱신할 때는 연결된 Notion에서 사용자가 지정한 CS 스터디 페이지를 다시 확인합니다. 원본을 수정하거나 공개하지 않았으며 자동 동기화도 설정되어 있지 않습니다.

## 공식 확인 자료

| 자료 | 확인 논점 |
|---|---|
| [RFC 826](https://www.rfc-editor.org/rfc/rfc826.html) | ARP와 다음 홉 주소 해석 |
| [RFC 9293](https://www.rfc-editor.org/rfc/rfc9293.html) | TCP 기본 서비스·순서 번호·상태·종료 |
| [RFC 5681](https://www.rfc-editor.org/rfc/rfc5681.html) | 전통적 TCP 혼잡 제어 모델 |
| [RFC 7766](https://www.rfc-editor.org/rfc/rfc7766.html) | DNS over TCP |
| [RFC 6891](https://www.rfc-editor.org/rfc/rfc6891.html) | EDNS |
| [RFC 9110](https://www.rfc-editor.org/rfc/rfc9110.html) | HTTP 의미·메서드·멱등성 |
| [RFC 9112](https://www.rfc-editor.org/rfc/rfc9112.html) | HTTP/1.1 지속 연결 |
| [RFC 9114](https://www.rfc-editor.org/rfc/rfc9114.html) | HTTP/3 |
| [RFC 9000](https://www.rfc-editor.org/rfc/rfc9000.html) | QUIC 스트림과 전송 |
| [RFC 8446](https://www.rfc-editor.org/rfc/rfc8446.html) | TLS 1.3 |
| [MDN 쿠키](https://developer.mozilla.org/en-US/docs/Web/HTTP/Guides/Cookies) | 쿠키 범위·보안 속성 |

## 갱신 기록

- 2026-09-17: 네트워크 초판 작성 및 공개용 출처 정리.
