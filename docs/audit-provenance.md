# 🧾 Audit & Provenance

AgentMemory стремится сохранять проверяемую связь между задачей, контекстом, исполнителем и результатом.

## Что может связываться

- run;
- stage;
- task;
- выбранный executor;
- context bundle;
- repository commit;
- worktree;
- gate result;
- test evidence;
- human approval.

## Упрощённая цепочка

```text
Task
  ↓
Context
  ↓
Executor
  ↓
Result
  ↓
Verification
  ↓
Gate
  ↓
Final Action
```

## Зачем нужна provenance

После выполнения важно иметь возможность понять:

- какой AI получил задачу;
- какой контекст использовался;
- к какому commit относился результат;
- какие проверки были выполнены;
- почему операция была разрешена или заблокирована.

## Privacy

Audit-данные должны быть ограниченными.

В долговременное состояние не должны без необходимости попадать:

- полные prompts;
- API-ключи;
- credentials;
- приватные environment values;
- необработанные внешние ответы.
