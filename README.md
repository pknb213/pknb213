# CYJ

**Backend & Data Systems Engineer**

데이터 수집부터 API, 비동기 작업, 검색 인덱스까지 연결하는 시스템을 만듭니다.<br>
Python · Kotlin · TypeScript를 중심으로, **데이터의 정확성과 실패 이후의 복구까지 설명할 수 있는 설계**를 지향합니다.

[포트폴리오](https://pknb213.github.io/) · [업무 경험](https://pknb213.github.io/#experience) · [이메일](mailto:pknb213@naver.com)

---

## What I build

- **Backend systems** — API와 worker의 책임을 나누고, 비동기 작업의 상태·재시도·중복 처리를 설계합니다.
- **Data platforms** — 수집, 배치·스트림 처리, 저장, 운영 관측으로 이어지는 데이터 흐름을 구축합니다.
- **Retrieval systems** — 원본 데이터와 검색 인덱스를 분리하고, 인덱스 재구축·증분 동기화·검색 품질을 검증합니다.

## Selected engineering work

업무 시스템은 공개 가능한 설계와 검증 근거를 포트폴리오에 정리했습니다.

### [cms-rag · 재생성 가능한 검색 인덱스](https://pknb213.github.io/#cms-rag)

원본 DB를 기준 데이터로 유지하고, 벡터 저장소를 다시 만들 수 있는 검색용 인덱스로 분리했습니다. 별도 인덱스를 구축·검증한 뒤 교체하고, 변경 이벤트는 증분 반영합니다.

**23,601개 문항의 원본·인덱스 건수 일치** · **2개 벡터 저장소 어댑터** · **58개 테스트 함수**

`Python` `FastAPI` `BGE-M3` `pgvector` `Qdrant`

### [cms-api · 비동기 작업과 데이터 일관성](https://pknb213.github.io/#cms-api)

API는 작업을 기록하고 ID를 반환하며, worker는 실행과 상태 전이를 맡습니다. 사용자 작업 상태와 내부 검색 인덱스 갱신 이벤트를 분리해 실패·재시도 경계를 명확하게 했습니다.

**14개 API 경로** · **9개 DB 마이그레이션** · **19개 테스트 함수**

`Python` `FastAPI` `SQS` `SQLAlchemy` `Alembic`

> 수치는 2026년 7월 코드 스냅샷과 개발 환경 검증 기준입니다. 테스트 함수 수는 실행 통과율이나 커버리지를 뜻하지 않으며, 문항 수는 운영 트래픽 지표가 아닙니다. [측정 근거와 범위](https://pknb213.github.io/#evidence)

## Public code

직접 구현하며 학습·실험한 공개 저장소입니다. 업무 프로젝트와 구분하고, 언어별 대표 저장소만 모았습니다.

- **[Python-Projects](https://github.com/pknb213/Python-Projects)** — REST API, 배치 스케줄링, 캐시, 크롤러
  - Flask · APScheduler · Redis · SQLAlchemy
- **[Kotlin-SpringBoot-Servers](https://github.com/pknb213/Kotlin-SpringBoot-Servers)** — 비동기 API, 인증, 반응형 데이터 접근
  - Spring WebFlux · Coroutines · R2DBC · Kafka
- **[TypeScript-Servers](https://github.com/pknb213/TypeScript-Servers)** — REST·GraphQL·WebSocket 서버, 인증, 메시징
  - NestJS · TypeORM · Redis · Kafka

**AI 학습 기록** — [LangChain-Challenge](https://github.com/pknb213/LangChain-Challenge): Nomad Coder 강의 기반으로 문서 검색, 메모리, 도구 호출과 Streamlit 앱을 실습했습니다.

[전체 공개 프로젝트와 구현 범위 보기](https://pknb213.github.io/#open-source)

## Engineering approach

- 원본 데이터와 파생 데이터를 구분하고, 다시 만들 수 있는 경로를 남깁니다.
- 정상 응답뿐 아니라 실패, 재시도, 상태 전이까지 시스템의 일부로 다룹니다.
- 기술 목록보다 구현 범위, 측정 조건, 확인 가능한 근거로 설명합니다.

---

Backend · Data Platform · Retrieval 관련 기회와 기술 대화를 환영합니다.<br>
[pknb213@naver.com](mailto:pknb213@naver.com) · [Engineering portfolio](https://pknb213.github.io/)
