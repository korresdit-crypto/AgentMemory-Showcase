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
```

## Multi-model workflow

Для сложных задач могут использоваться несколько моделей.

Пример:

```text
Research / Analysis
        ↓
     Qwen / Grok
        ↓
Architecture Review
        ↓
      Claude
        ↓
Implementation
        ↓
       Codex
        ↓
Independent Verification
```

Роли и порядок могут меняться в зависимости от задачи.

## Security Remediation

Для security-задач применяется отдельный процесс:

```text
Finding
   ↓
Evidence Collection
   ↓
Root Cause Analysis
   ↓
Remediation
   ↓
Focused Tests
   ↓
Security Verification
   ↓
Independent Review
```

Критические выводы должны подтверждаться проверяемыми evidence, а не только текстовым утверждением AI.

## Prompt Gate

Для задач, где AI формирует инструкции другому AI, используется отдельный контроль prompt.

Проверяются:

- структура;
- ограничения;
- противоречия;
- безопасность;
- соответствие задаче;
- полнота необходимых требований.

## Recovery

AgentMemory хранит состояние выполнения workflow.

Если процесс прерывается, система может определить:

- на каком этапе произошла остановка;
- что уже было выполнено;
- какие результаты сохранены;
- можно ли безопасно продолжить;
- требуется ли вмешательство человека.

## Цель

Workflow отделяет сложную задачу от одного непрерывного AI-вызова и превращает её в контролируемую последовательность этапов с проверками и сохранением состояния.
