# Learning Plan

[English](learning-plan.md) | [한국어](learning-plan.ko.md)

## How to study

Follow the stages in order, without treating the video's “seven weeks” as a deadline. For each stage: watch the relevant material, explain the key idea, apply it to the same agent, and check the result. Prior ML/DL experience makes ML a refresher; Python is a focused refresher before implementation. Use [the checklist](../progress/plan.md) for completion. Write detailed notes only when they help solve or explain a problem.

## Video map

The seven-step screen recording showed Python → ML → LLMs → LangChain → RAG → LangGraph → Agentic AI. Its thumbnails and durations match these videos. Karpathy and Lauren Tan are placed where they best support the project.

| When | Video | Focus |
|---|---|---|
| Orientation and later review | [Lauren Tan — SpaceX AI Engineer Lauren Tan: Part 1](https://www.youtube.com/watch?v=PaPpyQocMww) | Define, delegate, verify, and improve coding-agent work |
| Python refresher | [Dave Ebbelaar — Python for AI: Full Beginner Course](https://www.youtube.com/watch?v=ygXn5nV5qFc) | Select the parts needed for a typed, tested CLI |
| ML refresher | [freeCodeCamp/Kylie Ying — Machine Learning for Everybody](https://www.youtube.com/watch?v=i_LwzRVP7bg) | Evaluation, generalization, and data quality |
| LLM foundations | [Andrej Karpathy — Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI) | Tokens, training, inference, and why outputs need verification |
| Optional model-training depth | [Stanford CME295 — Reinforcement Learning with LLMs](https://www.youtube.com/watch?v=3Vaj0Oka_t4) | Advanced model training; not a prerequisite for building the agent |
| Framework comparison | [NeuralNine — LangChain Full Crash Course](https://www.youtube.com/watch?v=J7j5tCB_y4w) | Compare framework components with a small manual implementation |
| Retrieval | [Jack Roberts — RAG Masterclass](https://www.youtube.com/watch?v=dxeCH2duhMo) | Source-grounded retrieval; thumbnail reads “Ultimate RAG Course” |
| Stateful workflows | [freeCodeCamp — LangGraph Complete Course](https://www.youtube.com/watch?v=jGg_1h0qzaM) | State, branches, interruptions, and resume |
| Synthesis | [codebasics — Agentic AI Crash Course using LangChain](https://www.youtube.com/watch?v=D74el9mvNak) | Review the complete agent pattern |

## Stages and deliverables

| Stage | Study and build | Exit criterion |
|---|---|---|
| **0. Baseline** | Inspect `waiting-queue`, its tests, and one safe change/defect fixture. Record existing failures. | A repeatable baseline run and a known input diff exist. |
| **1. Python and AI-assisted development** | Refresh Python, watch Lauren Tan, create a tested CLI that reads Git refs and lists changed code/tests. | The CLI produces valid JSON for a real fixture and handles invalid inputs. |
| **2. LLM and tools** | Watch Karpathy; learn structured output, tool contracts, validation, budgets, and stop conditions. | An impact analysis cites real files and test IDs; tool errors stop cleanly. |
| **3. First complete cycle** | Compare manual code with LangChain. Connect impact analysis, mandatory/relevant test selection, execution, missing-scenario proposal, Java/JUnit candidate validation, and reporting. | One fixture runs from diff to reviewed QA report. Mark a first working version. |
| **4. Retrieval and evaluation** | Watch RAG and Agentic AI videos. Compare exact search with semantic retrieval; expand seeded-defect cases and evaluate misses. | An evaluation report shows detected and missed defects, test quality, time, and cost. |
| **5. Stateful operation** | Watch LangGraph and revisit Lauren Tan. Add resume, approval, traceability, failure handling; add MCP/API/CI where useful. | Interrupted, failed, and rejected runs can be reproduced and explained. |
| **6. Portfolio and extension** | Polish reproducibility, architecture decisions, results, and limits. Compare a selected Rust component with Python if useful. | Another developer can reproduce the demo and understand the evidence. |

The first complete cycle is deliberately small. It is followed by deeper cycles on the same product. The [stage checklist](../progress/plan.md) breaks each stage into actions we can check together.
