# 🌐 Provider Strategy

AgentMemory не привязывает orchestration-логику к одному AI-провайдеру.

## Разделение

```text
Workflow
   ↓
Role
   ↓
Executor Contract
   ↓
Provider Adapter
   ↓
AI Provider
```

## Почему это важно

AI-провайдеры отличаются по:

- качеству;
- доступности;
- стоимости;
- latency;
- интерфейсу;
- ограничениям;
- privacy properties.

AgentMemory отделяет provider-specific детали от общей workflow-логики.

## Текущие направления

- Codex для реализации;
- Claude для архитектурного анализа и review;
- локальный Qwen для дешёвых локальных задач;
- внешний research-маршрут для актуальной информации.

## Принцип

Workflow должен зависеть от требуемой роли и capability, а не от жёстко зашитого имени одной модели.
