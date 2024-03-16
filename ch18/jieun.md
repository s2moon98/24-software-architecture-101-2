# 최적의 아키텍처 스타일 선정

## 유행

- 새로운 아키텍처 설계는 과거 아키텍처 스타일에서 발견된 결함이 반영된 경우가 많다.
- 끊임없는 생태계의 변화 : 쿠버네티스
- 새로운 기능 : 도커처럼 게임 체인저가 될 만한 변경 사항이 있을 수 있다.
- 가속
- 도메인 변경
- 기술 변화
- 외부 팩터

## 결정 기준

- 도메인
- 구조에 영향을 미치는 아키텍처 특성
- 데이터 아키텍처
- 조직 문제
- 프로세스, 팀, 운영 문제에 대한 지식
- 도메인/아키텍처 동형성
- 모놀리스냐 분산이냐
- 데이터를 어디에 둘 것인가?
- 서비스 간 통신은 동기,비동기 중 어떤 스타일로 할 것인가?

## 모놀리식 사례 연구 : 실리콘 샌드위치

- 도메인 분할된 컴포넌트, 기술 분할된 컴포넌트으로 나눠서 설계
- 모듈러 모놀리스
    - 단일 퀀텀으로 배포된 단일 데이터베이스 기반의 도메인 중심 시스템
    - 비용을 줄일 수 있다.
- 마이크로커널
    - 커플링될 일이 없다.

## 분산 아키텍처 사례 연구 : GGG

- 이벤트 기반 아키텍처 스타일로 설계
    - 오케스트레이션 방식이냐 코페오그래피 방식이냐로 구분
- 동기 통신 스타일과 비동기 통신 스타일을 주의 깊게 식별
    - 비동기 통신을 선택 : 서비스마다 상이한 운영 아키텍처 특성을 감안
    - 서비스 간에 동기 통신을 하면 타임아웃과 여러가지 안정성 문제 발생 → 메시지 큐를 사용