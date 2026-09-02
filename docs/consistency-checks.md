# 🧩 Consistency Checks

AgentMemory использует проверки согласованности между различными источниками состояния.

## Что может сравниваться

- project memory;
- runtime state;
- Git repository;
- workflow events;
- expected commit;
- selected executor;
- gate results.

## Общая схема

```text
Source A
   │
   ├── Compare
   │
Source B
   ↓
CONSISTENT / CONFLICT
```

## Пример

Если долговременная память утверждает, что задача завершена, а Git-состояние или runtime events показывают другое состояние, система не должна автоматически доверять одному источнику.

## Принцип

При конфликте важнее зафиксировать несогласованность, чем тихо выбрать удобную версию состояния.

## Цель

Consistency checks помогают обнаруживать:

- устаревшую память;
- повреждённое runtime state;
- ошибочный recovery;
- работу не с тем commit;
- несогласованные решения между workflow и проектом.
