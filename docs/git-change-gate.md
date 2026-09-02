# 🌳 Git Change Gate

Git Change Gate — механизм контроля изменений перед попаданием кода в основную ветку.

## Зачем он нужен

AI-исполнитель не должен самостоятельно:

- изменить код;
- проверить собственную работу;
- решить, что всё корректно;
- сразу отправить изменения в main.

AgentMemory разделяет эти этапы.

## Упрощённый процесс

```text
Task
  ↓
Isolated Worktree
  ↓
Implementation
  ↓
Automated Tests
  ↓
Independent Review
  ↓
Change Gate
  ↓
Human Approval
  ↓
Push / Merge
