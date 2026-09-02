# 🧪 Security Evidence

Для security-задач AgentMemory стремится опираться на проверяемые evidence, а не только на текстовый вывод AI.

## Evidence может включать

- changed hunks;
- file excerpts;
- commit references;
- результаты тестов;
- regression tests;
- diff validation;
- независимые findings.

## Общая схема

```text
Finding
  ↓
Evidence Collection
  ↓
Validation
  ↓
Remediation
  ↓
Verification
```

## Ограничения

Evidence ограничивается по:

- размеру;
- количеству элементов;
- допустимым путям;
- типу содержимого;
- соответствию конкретному commit.

## Fail-Closed

Если evidence неполное, усечённое или не связано с ожидаемым состоянием репозитория, критическая проверка не должна автоматически считаться успешной.

## Цель

Security evidence делает исправление:

- проверяемым;
- воспроизводимым;
- связанным с конкретным кодом;
- пригодным для независимого review.
