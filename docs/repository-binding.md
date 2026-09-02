# 🔗 Repository Binding

AgentMemory связывает проектную память и workflow с конкретным Git-репозиторием.

## Зачем это нужно

При работе с несколькими проектами система должна исключать ситуацию, когда память одного проекта используется для другого репозитория.

## Общая схема

```text
Project Key
    ↓
Expected Repository
    ↓
Canonical Repository Root
    ↓
Validation
    ↓
Context / Workflow
```

## Что проверяется

- соответствие project identity;
- ожидаемый repository root;
- Git-состояние;
- commit provenance;
- worktree identity.

## Fail-Closed

Если проект и репозиторий не совпадают, workflow не должен продолжаться с чужой памятью или неправильным кодом.

## Цель

Предотвратить cross-project context confusion и ошибочное выполнение задач не в том репозитории.
