# 🛡 Safe Context Policy

AgentMemory передаёт AI только ограниченный и проверенный контекст.

## Перед передачей

Контекст проходит несколько уровней проверки:

```text
Candidate Context
      ↓
Relevance
      ↓
Reference Safety
      ↓
Secret Detection
      ↓
Sensitivity Rules
      ↓
Size Budget
      ↓
Executor Handoff
```

## Что блокируется

- явные credentials;
- приватные ключи;
- секретные configuration files;
- небезопасные ссылки на файлы;
- контекст, нарушающий ограничения конкретного workflow.

## Почему этого недостаточно само по себе

Secret detection не считается абсолютной гарантией.

Поэтому AgentMemory использует защиту в несколько слоёв:

- минимизация контекста;
- фильтрация;
- bounded data;
- controlled adapters;
- audit;
- human control для критичных операций.

## Принцип

Лучший секрет для внешнего AI — тот, который вообще не был включён в контекст.
