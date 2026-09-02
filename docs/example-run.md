# ▶️ Example Run

Ниже показан упрощённый пример одного AgentMemory workflow.

## Задача

Исправить ошибку в программном проекте и безопасно подготовить изменение к merge.

## Ход выполнения

```text
1. Task received
      ↓
2. Repository validated
      ↓
3. Project memory loaded
      ↓
4. Relevant context selected
      ↓
5. Model Router selects IMPLEMENTER
      ↓
6. Codex works in isolated worktree
      ↓
7. Focused tests run
      ↓
8. Independent review runs
      ↓
9. Change Gate validates result
      ↓
10. Human approves
      ↓
11. Merge
```

## Что сохраняется

В ходе выполнения система может сохранить:

- run identity;
- выбранного executor;
- stage transitions;
- test results;
- gate result;
- ссылки на artifacts;
- final status.

## Что этот пример показывает

AgentMemory превращает AI-assisted изменение кода из одного непрозрачного вызова в последовательность проверяемых этапов.
