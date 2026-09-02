# ✅ Testing Evidence

AgentMemory развивается с большим автоматизированным тестовым набором.

## Масштаб

На текущих этапах разработки проект превышает **1100 автоматизированных тестов**.

Точное количество меняется по мере развития системы.

## Что проверяется

- model routing;
- executor selection;
- context planning;
- context handoff;
- secret filtering;
- recovery;
- Git worktrees;
- Git Change Gate;
- security workflows;
- CLI;
- error handling;
- fail-closed сценарии;
- regression cases.

## Инженерный цикл

```text
Reproduce
   ↓
Understand root cause
   ↓
Add regression test
   ↓
Implement fix
   ↓
Run focused tests
   ↓
Run broader test suite
```

## Дополнительные проверки

- `git diff --check`;
- проверки Git-состояния;
- boundary-тесты;
- integration-тесты;
- security-focused tests;
- независимый AI-review для отдельных критичных изменений.

Этот Showcase не публикует полный внутренний тестовый набор и production fixtures.
