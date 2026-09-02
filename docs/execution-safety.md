# 🧯 Execution Safety

AgentMemory ограничивает AI-выполнение не только на уровне prompt, но и на уровне runtime.

## Основные меры

- контролируемые executor adapters;
- ограниченное child-process environment;
- timeout;
- проверка readiness;
- ограничение размера input/output;
- Git isolation;
- проверка контекста;
- безопасная обработка ошибок.

## Общая схема

```text
Task
  ↓
Validated Context
  ↓
Executor Adapter
  ↓
Controlled Environment
  ↓
AI / CLI Process
  ↓
Validated Result
```

## Почему это важно

Даже хороший prompt не гарантирует безопасное выполнение.

Ошибки могут происходить из-за:

- неправильного runtime;
- неожиданного provider response;
- зависшего процесса;
- некорректной среды;
- изменившегося репозитория.

## Принцип

Безопасность execution path должна проверяться отдельно от качества текстовой инструкции.
