# 단계별 체크리스트

[English](plan.md) | [한국어](plan.ko.md)

이 문서가 함께 관리하는 학습 일정입니다. 단계에는 순서가 있지만 마감 기한은 없습니다. 학습을 시작할 때 [진행 현황](status.ko.md)을 열고 다음 미완료 항목을 고릅니다. 마칠 때 결과를 함께 확인하고 체크한 뒤 다음 작업을 정합니다. 시청하거나 대화만 한 것은 완료로 표시하지 않습니다. 자세한 학습 기록은 선택 사항입니다.

## 0단계 — 기준 상태

- [ ] `waiting-queue` 기준 ref와 테스트 목록을 확정합니다.
    - 읽기: [`waiting-queue` README](https://github.com/yoonpunk/waiting-queue), [Gradle 테스트 가이드](https://docs.gradle.org/current/userguide/java_testing.html).
- [ ] 환경 오류와 앱/테스트 기대값 오류를 분리합니다.
- [ ] 대상 `main` 밖에 정상 변경 사례와 주입 결함 사례를 하나씩 만듭니다.
    - 읽기: [Git worktree 문서](https://git-scm.com/docs/git-worktree).
- [ ] 기준 실행 명령과 예상 결과를 저장소에 기록합니다.

## 1단계 — Python 복습과 AI 활용 개발

- [ ] 로렌 탄 영상을 보고 작은 코딩 작업과 검증 절차를 정합니다.
    - 영상: [Lauren Tan — SpaceX AI Engineer Lauren Tan: Part 1](https://www.youtube.com/watch?v=PaPpyQocMww).
- [ ] CLI, JSON, 타입, subprocess, pytest에 필요한 Python을 복습합니다.
    - 영상·문서: [Python for AI](https://www.youtube.com/watch?v=ygXn5nV5qFc), [Python 튜토리얼](https://docs.python.org/3/tutorial/), [pytest 문서](https://docs.pytest.org/en/stable/).
- [ ] 필요한 ML 평가 개념만 복습합니다.
    - 영상: [Machine Learning for Everybody](https://www.youtube.com/watch?v=i_LwzRVP7bg). 필요한 부분만 선택해 복습합니다.
- [ ] Git base/head ref를 읽어 변경 파일·테스트를 JSON으로 출력하는 CLI를 만듭니다.
    - 읽기: [Git diff 문서](https://git-scm.com/docs/git-diff), [Python `subprocess`](https://docs.python.org/3/library/subprocess.html).
- [ ] 실제 사례와 잘못된 입력 하나로 CLI를 검증합니다.

## 2단계 — LLM 기초와 도구

- [ ] 카파시 영상을 보고 토큰, 추론, 출력 검증의 필요성을 설명합니다.
    - 영상: [Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI). 선택 심화: [Stanford CME295 RL with LLMs](https://www.youtube.com/watch?v=3Vaj0Oka_t4).
- [ ] 영향 분석과 테스트 시나리오의 검증 가능한 스키마를 정의합니다.
    - 읽기: [Pydantic 검증](https://docs.pydantic.dev/latest/), [LangChain 구조화 출력](https://docs.langchain.com/oss/python/langchain/structured-output).
- [ ] 읽기 전용 `get_diff`, `get_test_catalog` 도구를 구현합니다.
    - 읽기: 도구 계약을 참고할 [LangChain 도구 문서](https://docs.langchain.com/oss/python/langchain/tools). 첫 버전은 LangChain 의존 없이 구현합니다.
- [ ] 존재하지 않는 출처·테스트 ID를 거부하고 도구 오류를 처리합니다.
- [ ] 도구 호출 예산과 종료 조건을 정합니다.

## 3단계 — 첫 완성 버전

- [ ] 간단한 수동 Agent 반복 실행을 만들고 LangChain 영상·구현과 비교합니다.
    - 영상·문서: [LangChain crash course](https://www.youtube.com/watch?v=J7j5tCB_y4w), [LangChain 개요](https://docs.langchain.com/oss/python/langchain/overview).
- [ ] 근거와 함께 필수·관련 기존 테스트를 선정합니다.
- [ ] 허용된 테스트를 실행하고 기존 실패와 새 실패를 분류합니다.
    - 읽기: [Gradle 테스트 가이드](https://docs.gradle.org/current/userguide/java_testing.html).
- [ ] 의미 있는 검증 조건을 가진 Java/JUnit 테스트 후보 하나를 제안합니다.
    - 읽기: [JUnit 5 사용자 가이드](https://docs.junit.org/5.14.4/overview.html).
- [ ] 대상 `main`을 수정하지 않고 후보를 격리 컴파일·실행합니다.
    - 읽기: [Git worktree](https://git-scm.com/docs/git-worktree). 컨테이너를 추가할 때는 [Docker Engine 보안 문서](https://docs.docker.com/engine/security/)를 참고합니다.
- [ ] 검토 가능한 JSON 및 Markdown QA 보고서를 생성합니다.
- [ ] diff부터 보고서까지 시연하고 첫 동작 버전에 태그를 붙입니다.

## 4단계 — 검색과 평가

- [ ] RAG와 Agentic AI 영상을 봅니다.
    - 영상: [RAG masterclass](https://www.youtube.com/watch?v=dxeCH2duhMo), [Agentic AI crash course](https://www.youtube.com/watch?v=D74el9mvNak).
- [ ] 의미 검색 전에 정확한 경로·심볼 검색을 평가합니다.
- [ ] 기록된 검색 누락을 개선할 때만 검색 기능을 추가합니다.
    - 읽기: 정확 검색을 먼저 평가한 뒤 [LangChain RAG 가이드](https://docs.langchain.com/oss/python/langchain/rag)를 구현 참고 자료로 봅니다.
- [ ] 정상 변경·주입 결함 사례를 늘립니다.
- [ ] 선정/전체 스위트의 검출, 생성 테스트의 가치, 시간·비용을 비교합니다.
- [ ] 누락과 한계를 포함한 평가 보고서를 게시합니다.

## 5단계 — 상태 기반 운영

- [ ] LangGraph 영상을 보고 로렌 탄 영상을 다시 봅니다.
    - 영상: [LangGraph course](https://www.youtube.com/watch?v=jGg_1h0qzaM), [Lauren Tan](https://www.youtube.com/watch?v=PaPpyQocMww).
- [ ] 실행 상태를 저장하고 중단 뒤 재개합니다.
    - 읽기: [LangGraph 상태 저장](https://docs.langchain.com/oss/python/langgraph/persistence).
- [ ] 코드 변경 제안 전에 중단하며 승인·거절을 시험합니다.
    - 읽기: [LangGraph 인터럽트](https://docs.langchain.com/oss/python/langgraph/interrupts).
- [ ] 판단, 도구 호출, 실패, 지연, 비용을 추적합니다.
    - 읽기: [OpenTelemetry 문서](https://opentelemetry.io/docs/).
- [ ] 필요와 비교 기준을 정한 뒤 MCP, API, CI를 추가합니다.
    - 필요할 때 읽기: [MCP 소개](https://modelcontextprotocol.io/docs/getting-started/intro), [FastAPI 문서](https://fastapi.tiangolo.com/), [GitHub Actions 문서](https://docs.github.com/en/actions).
- [ ] 시간 초과, 잘못된 도구 출력, 실행 실패를 재현합니다.

## 6단계 — 포트폴리오와 확장

- [ ] 문서의 Git ref만으로 공개 데모를 재현할 수 있게 합니다.
- [ ] 아키텍처 선택, 평가 결과, 남은 한계를 설명합니다.
- [ ] [포트폴리오 목표](../docs/portfolio.ko.md)를 완료합니다.
- [ ] 유용하다면 Rust 구성요소 하나를 같은 사례로 비교합니다.
    - 선택 시 읽기: [공식 Rust MCP SDK](https://github.com/modelcontextprotocol/rust-sdk).

## 함께 공부할 때의 순서

1. [진행 현황](status.ko.md)을 읽고 미완료 항목 한두 개를 고릅니다.
2. 함께 공부하고 구현합니다.
3. 결과를 확인한 뒤 두 언어 체크리스트를 함께 갱신합니다.
4. 두 언어 진행 현황의 현재 단계와 다음 작업을 갱신합니다.
5. 의미 있는 진행을 영어 브랜치명·커밋 메시지로 기록합니다. 자세한 기록은 필요할 때만 씁니다.
