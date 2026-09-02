# 🛠 Security Remediation Flow

AgentMemory поддерживает отдельный подход к исправлению security findings.

## Общий workflow

```text
Finding
  ↓
Reproduce
  ↓
Collect Evidence
  ↓
Root Cause
  ↓
Implement Fix
  ↓
Regression Test
  ↓
Focused Security Tests
  ↓
Independent Verification
  ↓
Change Gate
```

## Почему сначала reproduction

Без воспроизводимого сценария легко исправить симптом, а не причину.

## Почему нужен regression test

Regression test фиксирует найденную проблему и снижает риск её повторного появления.

## Почему нужен independent verification

Исполнитель исправления не должен быть единственным источником уверенности в результате.

## Fail-Closed

Если evidence неполное или проверка не может подтвердить исправление, security workflow не должен автоматически завершаться как успешный.

## Цель

Security remediation должна быть:

- доказуемой;
- воспроизводимой;
- связанной с конкретным кодом;
- покрытой тестами;
- независимо проверенной.
