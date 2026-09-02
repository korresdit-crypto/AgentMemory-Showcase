# 🗂 Project Structure

Публичный Showcase AgentMemory организован так, чтобы отделять обзор системы от детальной документации.

## Структура

```text
AgentMemory-Showcase/
├── README.md
└── docs/
    ├── architecture.md
    ├── system-overview.md
    ├── model-routing.md
    ├── memory.md
    ├── security.md
    ├── testing.md
    ├── workflows.md
    └── ...
```

## Корневой README

Главная страница проекта кратко объясняет:

- что такое AgentMemory;
- зачем он создан;
- какие AI участвуют;
- какие основные механизмы реализованы;
- где находится подробная документация.

## Папка docs

В `docs` вынесены отдельные темы:

- архитектура;
- память;
- routing;
- verification;
- security;
- recovery;
- Git workflow;
- runtime state;
- testing;
- audit.

## Принцип

Главная страница должна оставаться понятной за несколько минут, а технические детали — находиться в отдельных документах.
