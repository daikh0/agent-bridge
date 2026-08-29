# Agent Bridge

Minimal communication channel between ChatGPT (control) and Gemini Spark (execution).

## Protocol

ChatGPT writes a task to `inbox/task.md`.
Spark executes it and writes the result to `outbox/result.md`.
ChatGPT reads the result, validates evidence, and sends the next task.

**Never put secrets, API keys, passwords, cookies, private customer data, or credentials in this repository.**

## Task
```text
TASK_ID:
GOAL:
INPUT:
DONE_WHEN:
CONSTRAINTS:
```

## Result
```text
TASK_ID:
STATUS: PASS|FAIL|BLOCKED|PARTIAL
RESULT:
EVIDENCE:
BLOCKERS:
NEXT_ACTION:
```
