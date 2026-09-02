# 🔁 Change Lifecycle

AgentMemory разделяет создание изменения и его принятие в основную ветку.

## Жизненный цикл изменения

```text
Task
  ↓
Prepare isolated worktree
  ↓
Implementation
  ↓
Commit candidate
  ↓
Automated checks
  ↓
Independent review
  ↓
Change Gate
  ↓
Human approval
  ↓
Push / Merge
```

## Почему этапы разделены

AI может создать технически корректный diff, но это ещё не означает, что изменение:

- соответствует задаче;
- прошло все тесты;
- безопасно;
- не содержит неожиданных файлов;
- готово к merge.

## Revalidation

Перед критическим действием состояние может проверяться повторно.

Например, commit, который был reviewed, должен оставаться тем же commit перед финальным действием.

## Принцип

```text
Reviewed State
      =
Acted-On State
```

Если состояние изменилось между проверкой и действием, операция должна быть остановлена и проверена заново.
