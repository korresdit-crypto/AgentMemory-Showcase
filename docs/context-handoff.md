# 📦 Context Handoff

Context Handoff — механизм подготовки и безопасной передачи контекста между AgentMemory и AI-исполнителями.

## Зачем он нужен

AI не должен автоматически получать всю память проекта.

AgentMemory формирует только тот контекст, который нужен для конкретной задачи.

## Упрощённый процесс

```text
Project Memory
      ↓
Context Planning
      ↓
Relevant Data Selection
      ↓
Security Filtering
      ↓
Size Limits
      ↓
AI Executor
