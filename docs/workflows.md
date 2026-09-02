# 🔄 Workflows

AgentMemory использует отдельные workflow для разных типов задач.

## Основной принцип

Каждый workflow определяет:

- цель задачи;
- набор AI-исполнителей;
- порядок этапов;
- правила передачи контекста;
- проверки;
- условия остановки;
- правила финального подтверждения.

## Пример общего процесса

```text
Task
  ↓
Context Planning
  ↓
Model Routing
  ↓
AI Execution
  ↓
Verification
  ↓
Security Checks
  ↓
Git Change Gate
  ↓
Human Decision
