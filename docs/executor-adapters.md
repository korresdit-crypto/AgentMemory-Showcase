# 🔌 Executor Adapters

AgentMemory подключает AI-модели через отдельные executor adapters.

## Зачем нужны adapters

Разные AI-инструменты имеют разные:

- CLI;
- API;
- форматы ответа;
- правила авторизации;
- ограничения;
- health checks;
- timeout behavior.

Adapter скрывает эти различия от orchestration-слоя.

## Упрощённая схема

```text
Orchestrator
    ↓
Executor Contract
    ↓
Adapter
    ↓
AI Provider / Local Model
```

## Примеры исполнителей

- Codex CLI;
- Claude Code CLI;
- Local Qwen;
- research / external provider adapters.

## Что контролирует adapter

Adapter может отвечать за:

- проверку доступности;
- подготовку запроса;
- запуск процесса или вызов provider;
- timeout;
- нормализацию результата;
- обработку ошибок;
- ограничение environment;
- безопасную передачу metadata.

## Принцип

Orchestrator работает с общим контрактом и не должен зависеть от внутренних особенностей конкретного AI-провайдера.
