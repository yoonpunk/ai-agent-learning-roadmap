# Stage Checklist

[English](plan.md) | [한국어](plan.ko.md)

This is our study schedule. Stages are ordered, but have no deadline. At the start of a session, open [current status](status.md) and choose the next unchecked item. At the end, we check completed items together and set the next action. A check means the result was demonstrated, not merely watched or discussed. Detailed study notes are optional.

## Stage 0 — Baseline

- [ ] Confirm the `waiting-queue` baseline ref and test inventory.
    - Read: [`waiting-queue` README](https://github.com/yoonpunk/waiting-queue) and [Gradle testing guide](https://docs.gradle.org/current/userguide/java_testing.html).
- [ ] Separate environment failures from application/test expectation failures.
- [ ] Create one normal-change fixture and one seeded-defect fixture outside the target `main` branch.
    - Read: [Git worktree documentation](https://git-scm.com/docs/git-worktree).
- [ ] Record the baseline command and expected result in the repository.

## Stage 1 — Python refresher and AI-assisted development

- [ ] Watch Lauren Tan; define a small coding task and its verification steps.
    - Watch: [Lauren Tan — SpaceX AI Engineer Lauren Tan: Part 1](https://www.youtube.com/watch?v=PaPpyQocMww).
- [ ] Refresh Python parts needed for CLI, JSON, types, subprocesses, and pytest.
    - Watch/read: [Python for AI](https://www.youtube.com/watch?v=ygXn5nV5qFc), [Python tutorial](https://docs.python.org/3/tutorial/), and [pytest documentation](https://docs.pytest.org/en/stable/).
- [ ] Review ML evaluation concepts only where needed.
    - Watch: [Machine Learning for Everybody](https://www.youtube.com/watch?v=i_LwzRVP7bg); use only the sections you need to refresh.
- [ ] Build a CLI that reads Git base/head refs and emits changed files/tests as JSON.
    - Read: [Git diff documentation](https://git-scm.com/docs/git-diff) and [Python `subprocess`](https://docs.python.org/3/library/subprocess.html).
- [ ] Verify the CLI on a real fixture and one invalid input.

## Stage 2 — LLM foundations and tools

- [ ] Watch Karpathy and explain tokens, inference, and why outputs need checks.
    - Watch: [Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI). Optional depth: [Stanford CME295 RL with LLMs](https://www.youtube.com/watch?v=3Vaj0Oka_t4).
- [ ] Define validated schemas for impact findings and test scenarios.
    - Read: [Pydantic validation](https://docs.pydantic.dev/latest/) and [LangChain structured output](https://docs.langchain.com/oss/python/langchain/structured-output).
- [ ] Implement read-only `get_diff` and `get_test_catalog` tools.
    - Read: [LangChain tools](https://docs.langchain.com/oss/python/langchain/tools) for the tool contract; implement the first version without requiring LangChain.
- [ ] Reject invented source paths/test IDs and handle tool errors.
- [ ] Set a tool-call budget and a clear stop condition.

## Stage 3 — First complete working version

- [ ] Build a simple manual agent loop; compare it with the LangChain video and implementation.
    - Watch/read: [LangChain crash course](https://www.youtube.com/watch?v=J7j5tCB_y4w) and [LangChain overview](https://docs.langchain.com/oss/python/langchain/overview).
- [ ] Select mandatory and relevant existing tests with evidence.
- [ ] Run allowed tests and classify pre-existing versus new failures.
    - Read: [Gradle testing guide](https://docs.gradle.org/current/userguide/java_testing.html).
- [ ] Propose one missing Java/JUnit test with a meaningful assertion.
    - Read: [JUnit 5 user guide](https://docs.junit.org/5.14.4/overview.html).
- [ ] Compile/run the candidate in isolation without editing the target `main` branch.
    - Read: [Git worktrees](https://git-scm.com/docs/git-worktree); consult [Docker Engine security](https://docs.docker.com/engine/security/) when adding a container.
- [ ] Generate a reviewable JSON and Markdown QA report.
- [ ] Demonstrate a full diff-to-report run and tag the first working version.

## Stage 4 — Retrieval and evaluation

- [ ] Watch the RAG and Agentic AI videos.
    - Watch: [RAG masterclass](https://www.youtube.com/watch?v=dxeCH2duhMo) and [Agentic AI crash course](https://www.youtube.com/watch?v=D74el9mvNak).
- [ ] Measure exact path/symbol search before adding semantic retrieval.
- [ ] Add retrieval only where it improves documented misses.
    - Read: [LangChain RAG guide](https://docs.langchain.com/oss/python/langchain/rag) as a pattern reference after measuring exact search.
- [ ] Expand normal-change and seeded-defect fixtures.
- [ ] Compare selected versus full-suite detection, candidate-test value, time, and cost.
- [ ] Publish an evaluation report including misses and limits.

## Stage 5 — Stateful operation

- [ ] Watch LangGraph and revisit Lauren Tan.
    - Watch: [LangGraph course](https://www.youtube.com/watch?v=jGg_1h0qzaM) and [Lauren Tan](https://www.youtube.com/watch?v=PaPpyQocMww).
- [ ] Persist run state and resume after an interruption.
    - Read: [LangGraph persistence](https://docs.langchain.com/oss/python/langgraph/persistence).
- [ ] Pause before proposing a code change; exercise approval and rejection.
    - Read: [LangGraph interrupts](https://docs.langchain.com/oss/python/langgraph/interrupts).
- [ ] Trace decisions, tool calls, failures, latency, and cost.
    - Read: [OpenTelemetry documentation](https://opentelemetry.io/docs/).
- [ ] Add MCP, an API, or CI only after defining the need and comparison criteria.
    - Read as needed: [MCP introduction](https://modelcontextprotocol.io/docs/getting-started/intro), [FastAPI documentation](https://fastapi.tiangolo.com/), [GitHub Actions documentation](https://docs.github.com/en/actions).
- [ ] Reproduce timeout, bad tool output, and failed-run behavior.

## Stage 6 — Portfolio and extension

- [ ] Make the public demo reproducible from documented Git refs.
- [ ] Explain architecture choices, evaluation results, and remaining limits.
- [ ] Complete the [portfolio goals](../docs/portfolio.md).
- [ ] If useful, implement one component in Rust and compare it on the same fixtures.
    - Read if chosen: [official Rust MCP SDK](https://github.com/modelcontextprotocol/rust-sdk).

## Session routine

1. Read [status](status.md); choose one or two unchecked items.
2. Study and implement them together.
3. Demonstrate the result; check the corresponding items in both language versions.
4. Update the current stage and next action in both status pages.
5. Commit meaningful progress with an English branch name and commit message. Write longer notes only when needed.
