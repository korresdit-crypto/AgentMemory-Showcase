# 🚦 Operational Readiness

Перед запуском workflow AgentMemory проверяет, что необходимые компоненты действительно готовы к работе.

## Что может входить в readiness

- Git repository;
- project memory;
- runtime storage;
- executor adapters;
- локальная модель;
- внешние AI providers;
- required configuration;
- policy state.

## Упрощённая схема

```text
Configuration
      ↓
Passive Checks
      ↓
Health / Readiness
      ↓
READY / BLOCKED
```

## Почему это важно

Наличие бинарного файла или записи в конфигурации не доказывает, что компонент действительно работоспособен.

Например:

- CLI может быть не авторизован;
- provider может быть недоступен;
- локальный runtime может быть остановлен;
- repository state может быть некорректным.

## Принцип

AgentMemory старается обнаружить такие проблемы до начала дорогостоящего или изменяющего проект выполнения.
