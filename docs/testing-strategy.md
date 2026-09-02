# 🧪 Testing Strategy

AgentMemory развивается по принципу: найденная проблема должна по возможности превращаться в воспроизводимый тест.

## Уровни проверки

### Unit Tests

Проверяют отдельные функции и контракты.

### Integration Tests

Проверяют взаимодействие нескольких компонентов.

### Regression Tests

Фиксируют ранее найденные реальные ошибки.

### Boundary Tests

Проверяют ограничения размеров, количества элементов, timeout и другие граничные значения.

### Security Tests

Проверяют secret filtering, Git safety, context isolation и fail-closed сценарии.

### End-to-End Scenarios

Используются для проверки реальных цепочек выполнения, а не только отдельных mocked-компонентов.

## Предпочтительный цикл

```text
Reproduce
   ↓
Write failing test
   ↓
Root cause
   ↓
Fix
   ↓
Focused tests
   ↓
Full suite
   ↓
Independent review
```

## Масштаб

На текущих этапах AgentMemory имеет более **1100 автоматизированных тестов**.

Количество меняется по мере развития системы.
