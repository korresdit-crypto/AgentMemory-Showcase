# ♻️ Recovery Scenarios

AgentMemory должен уметь безопасно реагировать на прерванные или частично выполненные workflow.

## Сценарий: timeout AI

```text
AI Call
  ↓
Timeout
  ↓
Record failure state
  ↓
Retry / fallback / block
```

## Сценарий: изменился Git commit

Если состояние репозитория изменилось после review:

```text
Reviewed Commit
      ↓
Repository Changed
      ↓
Mismatch Detected
      ↓
Block
      ↓
Re-run verification
```

## Сценарий: неполный контекст

Если обязательный контекст не удалось безопасно сформировать, workflow не должен продолжать выполнение как будто всё в порядке.

## Сценарий: неизвестное состояние

```text
UNKNOWN
   ↓
Validation
   ↓
Cannot prove safety
   ↓
Human review
```

## Основной принцип

Recovery не должен угадывать.

Если безопасная точка продолжения не подтверждена, система блокирует workflow и требует дополнительной проверки.
