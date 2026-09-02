# 🚀 Release Readiness

AgentMemory отделяет факт завершения реализации от готовности результата к публикации, merge или использованию.

## Что может входить в readiness

- обязательные тесты прошли;
- нет блокирующих findings;
- Git diff валиден;
- repository state согласован;
- ожидаемый commit подтверждён;
- security checks завершены;
- независимый review завершён;
- human approval получен, если требуется.

## Общая схема

```text
Implementation Complete
      ↓
Verification Complete
      ↓
Security / Quality Gates
      ↓
Repository Consistency
      ↓
Human Approval
      ↓
READY
```

## Fail-Closed

Если один из обязательных этапов не подтверждён, результат не должен автоматически считаться готовым.

## Принцип

```text
DONE ≠ READY
```

Реализация может быть закончена технически, но ещё не готова к финальному принятию.
