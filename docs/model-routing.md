# 🧭 Model Routing

AgentMemory использует собственный слой маршрутизации задач между AI-моделями.

Цель Model Router — не отправлять все задачи одной модели, а выбирать исполнителя в зависимости от роли, типа задачи и доступности конкретного AI.

## Основные роли

```text
IMPLEMENTER  → Codex
ARCHITECT    → Claude
CRITIC       → Claude
LOCAL_WORKER → Qwen
RESEARCHER   → Research route
