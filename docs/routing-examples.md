# 🧭 Routing Examples

Ниже показаны упрощённые примеры маршрутизации в AgentMemory.

## Реализация функции

```text
Role: IMPLEMENTER
      ↓
Codex
```

## Архитектурный анализ

```text
Role: ARCHITECT
      ↓
Claude
```

## Независимая критика

```text
Role: CRITIC
      ↓
Claude
```

## Локальная проверка

```text
Role: LOCAL_WORKER
      ↓
Qwen
```

## Research

```text
Role: RESEARCHER
      ↓
Research route
```

## Приоритет выбора

```text
Explicit executor
      ↓
Role policy
      ↓
Default / fallback
```

## Важно

Routing учитывает не только роль, но и:

- доступность adapter;
- health;
- ограничения workflow;
- локальное или облачное выполнение;
- правила безопасности.
