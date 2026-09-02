# 📦 Artifact Handling

AgentMemory отделяет результаты AI-выполнения от обычного текстового ответа модели.

## Что может считаться artifact

- patch;
- diff;
- generated file;
- structured report;
- test evidence;
- review result;
- промежуточный workflow output.

## Общая схема

```text
AI / Tool Result
      ↓
Validation
      ↓
Artifact Store
      ↓
Event Reference
      ↓
Workflow State
```

## Почему это важно

Большие или бинарные результаты не всегда удобно хранить прямо внутри workflow state.

Отдельные artifacts позволяют:

- хранить результат независимо;
- ссылаться на него из событий;
- повторно использовать его при recovery;
- проверять целостность;
- не раздувать основное состояние.

## Принцип

Workflow должен ссылаться на подтверждённый artifact, а не полагаться на случайный временный файл.

## Privacy

Showcase не публикует реальные production artifacts, private patches и содержимое рабочих проектов.
