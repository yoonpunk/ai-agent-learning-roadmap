# AI Agent Engineering Roadmap

[English](README.md) | [한국어](README.ko.md)

This repository is the source of truth for a hands-on AI agent engineering study plan. The project is a **PR change-impact and regression-testing agent** for the public [waiting-queue](https://github.com/yoonpunk/waiting-queue) toy application. There is no fixed end date: build one complete working cycle, then improve the same agent in deeper cycles.

## Start here

1. Follow the [learning plan](docs/learning-plan.md) and its video sequence.
2. Check the [stage checklist](progress/plan.md) before each study session.
3. Use the [status page](progress/status.md) to see the current stage and next action. We update both pages together after a session; detailed notes are optional.
4. Use the [architecture](docs/architecture.md) and [portfolio goals](docs/portfolio.md) to connect study work to a reproducible project.

## First working version

Input: a Git diff between two refs of `waiting-queue`. Output: an evidence-based QA report that explains the affected behavior, runs mandatory and relevant existing tests, proposes a missing Java/JUnit test, and validates that candidate in an isolated runner. A person reviews any proposed code change.

The agent starts as a Python CLI. Later stages add retrieval, LangGraph, MCP, an optional API, observability, and CI. Rust is a later comparison exercise.

**Status:** planning. The agent has not been implemented and no performance result is claimed.

The repository uses English for default documentation, branch names, and commit messages. Every main document has a Korean translation linked below its title. This public project uses the public toy app and synthetic evaluation cases.

## GitHub workflow

The learning plan, checklist, status, code, target deliverables, and evaluation results live in this repository. We work on English-named branches, use English commit messages, and review changes through draft pull requests before merging. Each study session updates the checklist and status only when there is meaningful progress.
