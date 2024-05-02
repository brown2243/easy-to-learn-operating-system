# 운영체제의 개요

24/05/02 사당에서 스터디 진행

## 1. 운영체제 소개

- 운영체제: 컴퓨터 전체를 관리하는 소프트웨어(인터페이스, 커널)
  - 모든 하드웨어와 소프트웨어를 관리
  - 사용자와 응용프로그램에게 컴퓨터자원에 직접 접근하는 것을 막음
  - 대신 자원을 사용할 수 있는 인터페이스를 제공(system call)

운영체제의 역활

- 자원 관리 -> 효율
- 자원 보호 -> 안정
- 하드웨어 인터페이스 제공 -> 확장
- 사용자 인터페이스 제공 -> 편리

## 2. 운영체제의 발전

- 하드 와이어링: 전선으로 프로그램
- 일괄 작업 시스템: 모든 작업을 한꺼번에 처리
  - 천공카드로 하나의 작업을 읽어 실행 후 결과를 출력 후, 다음 작업 실행
  - 필요한 프로그램과 데이터를 동시에 입력해야함
  - 작업의 최종결과만 확인가능
- 대화형 시스템: 키보드와 모니터가 개발되어, 프로그램 진행중 진행과정 확인가능, 사용자 입력 가능
- 시분할 시스템: 멀티프로그래밍(하나의 cpu로 여러 프로그램 동시 실행 가능)가능
  - 동시성: 동시에 실행되는 것처럼 보이는 것
  - 시분할 시스템: 여러작업을 조금씩 처리해, 동시에 이루어 지는 것 처럼 보이게 하는 것
  - 작업 처리시간 예상하기 어려움
  - 실시간 시스템: 일정 시간내에 작업이 처리되는 것을 보장하는 시스템
  - 다중 사용자 시스템: 하나의 컴퓨터에서 여러사람이 작업할 수 있는 시스템
- 분산 시스템: 네트워크 상에 분산 된 여러 컴퓨터로 작업을 처리하고 결과를 교환하는 시스템
- 클라이언트/서버 시스템: 요청(클라이언트), 응답(서버)
  - 웹 시스템
- p2p: 서버는 중재, 사용자끼리 데이터 교환(peer to peer)
  - 메신저(중앙형), 블록체인(탈증앙)
- 클라우드 컴퓨팅: 인터넷을 통해 하드웨어와 소프트웨어를 클라우드라는 중앙시스템을 이용해 사용
  - 그리드 컴퓨팅: 여러 컴퓨터를 묶어 하나의 컴퓨터처럼 사용

## 3. 운영체제의 구성

- 응용 프로그램 / 유틸리디
- 사용자 인터페이스(CLI,GUI)
- 커널(시스템 콜, 드라이버...)
  - 프로세스 관리: cpu를 배분, 프로세스에 필요한 환경 제공
  - 메모리 관리
  - 파일 시스템
  - 입출력 관리
  - 프로세스 간 통신(IPC) 지원
- 하드웨어

- 단일형 커널: 모든기능을 메인에 때려박음
- 계층형 커널: 비슷한 기능을 모아 모듈화 - 현시점 대부분 운영체제
- 마이크로 커널: 가장 기본적인 기능만 제공 - 각 모듈이 독립적으로 동작