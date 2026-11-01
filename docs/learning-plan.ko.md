# 학습 계획

[English](learning-plan.md) | [한국어](learning-plan.ko.md)

## 학습 방법

단계 순서대로 진행하되 영상의 “7주”를 마감 기한으로 삼지 않습니다. 각 단계에서 관련 자료 시청 → 핵심 개념 설명 → 같은 Agent에 적용 → 결과 확인 순서로 공부합니다. 이전 ML/DL 경험을 고려해 ML은 복습으로, Python은 구현에 필요한 부분을 집중 복습합니다. 완료 여부는 [체크리스트](../progress/plan.ko.md)로 관리하고 자세한 기록은 문제 해결이나 설명에 도움이 될 때만 작성합니다.

## 영상 지도

화면 녹화의 순서는 Python → ML → LLMs → LangChain → RAG → LangGraph → Agentic AI입니다. 썸네일과 재생 시간을 대조한 영상이며, 카파시와 로렌 탄 영상은 프로젝트에 가장 도움이 되는 시점에 배치했습니다.

| 시점 | 영상 | 학습 초점 |
|---|---|---|
| 시작과 나중의 재검토 | [Lauren Tan — SpaceX AI Engineer Lauren Tan: Part 1](https://www.youtube.com/watch?v=PaPpyQocMww) | 코딩 Agent 작업 정의·위임·검증·개선 |
| Python 복습 | [Dave Ebbelaar — Python for AI: Full Beginner Course](https://www.youtube.com/watch?v=ygXn5nV5qFc) | 타입과 테스트를 갖춘 CLI에 필요한 부분 선택 학습 |
| ML 복습 | [freeCodeCamp/Kylie Ying — Machine Learning for Everybody](https://www.youtube.com/watch?v=i_LwzRVP7bg) | 평가, 일반화, 데이터 품질 |
| LLM 기초 | [Andrej Karpathy — Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI) | 토큰, 학습, 추론, 결과 검증의 필요성 |
| 선택 심화 | [Stanford CME295 — Reinforcement Learning with LLMs](https://www.youtube.com/watch?v=3Vaj0Oka_t4) | 모델 학습 심화. Agent 구현의 선행 조건은 아님 |
| 프레임워크 비교 | [NeuralNine — LangChain Full Crash Course](https://www.youtube.com/watch?v=J7j5tCB_y4w) | 수동 구현과 프레임워크 구성요소 비교 |
| 검색 | [Jack Roberts — RAG Masterclass](https://www.youtube.com/watch?v=dxeCH2duhMo) | 출처 기반 검색. 썸네일에는 “Ultimate RAG Course”라고 표기됨 |
| 상태 기반 실행 | [freeCodeCamp — LangGraph Complete Course](https://www.youtube.com/watch?v=jGg_1h0qzaM) | 상태, 분기, 중단과 재개 |
| 종합 | [codebasics — Agentic AI Crash Course using LangChain](https://www.youtube.com/watch?v=D74el9mvNak) | 전체 Agent 구성 복습 |

## 단계와 산출물

| 단계 | 학습과 구현 | 완료 기준 |
|---|---|---|
| **0. 기준 상태** | `waiting-queue`, 테스트, 안전한 변경·결함 사례를 확인하고 기존 실패를 기록합니다. | 반복 가능한 기준 테스트와 입력 diff가 있습니다. |
| **1. Python과 AI 활용 개발** | Python을 복습하고 로렌 탄 영상을 봅니다. Git ref를 읽고 변경 코드·테스트를 나열하는 CLI를 만듭니다. | 실제 사례에서 유효한 JSON을 만들고 잘못된 입력을 처리합니다. |
| **2. LLM과 도구** | 카파시 영상을 보고 구조화 출력, 도구 계약, 검증, 예산·종료 조건을 공부합니다. | 영향 분석이 실제 파일·테스트 ID를 인용하고 도구 오류 시 안전하게 종료합니다. |
| **3. 첫 완성 사이클** | 수동 코드와 LangChain을 비교합니다. 영향 분석, 필수·관련 테스트 선정, 실행, 누락 시나리오, Java/JUnit 후보 검증, 보고를 연결합니다. | 하나의 사례가 diff부터 검토 가능한 QA 보고서까지 실행됩니다. 첫 동작 버전을 남깁니다. |
| **4. 검색과 평가** | RAG·Agentic AI 영상을 봅니다. 정확 검색과 의미 검색을 비교하고 결함 사례를 늘려 누락을 평가합니다. | 검출·누락, 테스트 품질, 시간·비용을 보여주는 평가 보고서가 있습니다. |
| **5. 상태 기반 운영** | LangGraph 영상을 보고 로렌 탄 영상을 다시 봅니다. 재개, 승인, 추적, 실패 처리와 필요한 MCP/API/CI를 추가합니다. | 중단·실패·승인 거절 사례를 재현하고 설명할 수 있습니다. |
| **6. 포트폴리오와 확장** | 재현 방법, 설계 결정, 결과와 한계를 정리합니다. 필요하면 Rust 구성요소를 Python과 비교합니다. | 다른 개발자가 데모를 재현하고 근거를 이해할 수 있습니다. |

첫 완성 사이클은 작게 만듭니다. 이후 같은 제품을 심화합니다. 각 단계의 세부 작업은 [단계별 체크리스트](../progress/plan.ko.md)에 있습니다.
