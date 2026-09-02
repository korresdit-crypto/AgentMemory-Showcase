# 🔬 How AgentMemory Differs

AgentMemory не является просто интерфейсом для вызова нескольких AI-моделей.

## Обычный подход

```text
User
  ↓
One AI
  ↓
Answer / Code
```

## AgentMemory

```text
User / Workflow
      ↓
Long-Term Memory
      ↓
Context Planning
      ↓
Model Routing
      ↓
Specialized Executor
      ↓
Verification
      ↓
Security / Quality Gates
      ↓
Human Control
```

## Основные отличия

### Общая память

Контекст проекта сохраняется отдельно от конкретной модели.

### Разделение ролей

Разные AI могут выполнять разные функции.

### Проверка результата

Исполнитель не является единственным источником оценки собственной работы.

### Git-aware workflow

Система учитывает состояние репозитория, commit и worktree.

### Recovery

Workflow может восстанавливаться после сбоя на основе сохранённого состояния.

### Security boundaries

Контекст, runtime и критические действия проходят отдельные проверки.
