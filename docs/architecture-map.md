# 🗺 Architecture Map

Карта основных подсистем AgentMemory.

```text
                         Human
                           │
                           ▼
                    ┌─────────────┐
                    │ Orchestrator│
                    └──────┬──────┘
                           │
          ┌────────────────┼────────────────┐
          │                │                │
          ▼                ▼                ▼
   Long-Term Memory   Context Planner   Model Router
          │                │                │
          └────────────────┼────────────────┘
                           ▼
                    Context Handoff
                           │
                           ▼
                    Executor Adapters
                           │
             ┌─────────────┼─────────────┐
             ▼             ▼             ▼
           Codex         Claude         Qwen
             │             │             │
             └─────────────┼─────────────┘
                           ▼
                      Verification
                           │
                           ▼
                   Security / Quality Gates
                           │
                           ▼
                  Git Change Lifecycle
                           │
                           ▼
                     Human Approval
```

## Связанные подсистемы

Дополнительно работают:

- runtime state;
- event model;
- recovery;
- audit provenance;
- artifact handling;
- repository isolation;
- health checks.

Эта схема показывает архитектуру высокого уровня и намеренно не раскрывает приватную production-конфигурацию.
