# AI Agent Engineering 학습 로드맵

[English](README.md) | [한국어](README.ko.md)

이 저장소는 직접 구현하며 공부하는 AI Agent Engineering 학습 계획의 기준 문서입니다. 프로젝트는 공개 [waiting-queue](https://github.com/yoonpunk/waiting-queue) 토이 앱을 대상으로 한 **PR 변경 영향·회귀 테스트 Agent**입니다. 학습 종료일을 고정하지 않습니다. 먼저 끝까지 동작하는 버전을 만들고, 같은 Agent를 심화 단계에서 계속 개선합니다.

## 시작하기

1. [학습 계획](docs/learning-plan.ko.md)과 영상 순서를 따라갑니다.
2. 공부하기 전에 [단계별 체크리스트](progress/plan.ko.md)를 확인합니다.
3. [진행 현황](progress/status.ko.md)에서 현재 단계와 다음 작업을 확인합니다. 학습 후 두 문서를 함께 갱신하며, 자세한 학습 기록은 필요할 때만 작성합니다.
4. [아키텍처](docs/architecture.ko.md)와 [포트폴리오 목표](docs/portfolio.ko.md)를 사용해 학습을 재현 가능한 프로젝트로 연결합니다.

## 첫 동작 버전

입력은 `waiting-queue`의 두 Git ref 간 diff입니다. 출력은 영향받은 동작의 설명, 필수·관련 기존 테스트 실행, 빠진 Java/JUnit 테스트 제안과 격리 검증 결과가 담긴 근거 중심 QA 보고서입니다. 코드 변경 제안은 사람이 검토합니다.

Agent는 Python CLI로 시작합니다. 이후 검색, LangGraph, MCP, 선택적 API, 관측성, CI를 추가합니다. Rust는 추후 비교 실습으로 다룹니다.

**현재 상태:** 계획 단계. Agent 구현이나 성능 향상을 주장하지 않습니다.

기본 문서, 브랜치명, 커밋 메시지는 영어를 사용합니다. 주요 문서는 제목 바로 아래에 한국어 번역본 링크를 둡니다. 공개 토이 앱과 합성 평가 사례를 사용합니다.

## GitHub 작업 방식

학습 계획, 체크리스트, 진행 현황, 코드, 목표 산출물, 평가 결과를 이 저장소에서 관리합니다. 영어 브랜치명·커밋 메시지를 사용하고, 머지 전에 Draft PR로 변경 사항을 검토합니다. 학습 후 의미 있는 진행이 있을 때 체크리스트와 진행 현황을 갱신합니다.
