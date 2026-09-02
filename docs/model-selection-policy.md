# 🧠 Model Selection Policy

AgentMemory выбирает AI-исполнителя по роли, capability и readiness, а не только по имени модели.

## Основные факторы

- тип задачи;
- требуемая роль;
- доступность executor;
- локальное или облачное выполнение;
- стоимость;
- privacy requirements;
- необходимость независимой проверки.

## Пример

```text
Need code implementation?
        ↓
IMPLEMENTER
        ↓
Codex

Need architecture review?
        ↓
ARCHITECT
        ↓
Claude

Need local low-cost analysis?
        ↓
LOCAL_WORKER
        ↓
Qwen
```

## Приоритет выбора

```text
Explicit override
      ↓
Role policy
      ↓
Default / fallback
```

## Принцип

Выбранная модель должна быть не просто подходящей по роли, но и реально доступной для выполнения.
