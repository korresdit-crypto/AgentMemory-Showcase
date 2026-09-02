# ✅ Verification Pipeline

AgentMemory отделяет создание результата от доказательства его корректности.

## Упрощённый pipeline

```text
Implementation
      ↓
Focused Tests
      ↓
Static / Repository Checks
      ↓
Independent Review
      ↓
Evidence Validation
      ↓
Gate Decision
```

## Возможные проверки

- regression tests;
- integration tests;
- security tests;
- `git diff --check`;
- проверка ожидаемого commit;
- независимый AI-review;
- проверка completeness evidence;
- отсутствие блокирующих findings.

## Главный принцип

```text
Result ≠ Verified Result
```

Успешное выполнение AI-задачи само по себе не означает, что изменение готово к merge.
