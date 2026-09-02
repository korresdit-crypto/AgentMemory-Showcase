# 🛡 Threat Model

AgentMemory рассматривает безопасность как часть orchestration-архитектуры.

Этот документ описывает threat model высокого уровня без раскрытия production-конфигурации.

## Что система старается защищать

- API credentials;
- приватную память проектов;
- исходный код целевых репозиториев;
- Git history;
- локальную среду пользователя;
- контекст, передаваемый AI;
- integrity результатов workflow.

## Основные классы рисков

### Secret leakage

Чувствительные данные могут случайно попасть в prompt, лог или внешний provider.

### Unsafe AI output

AI может предложить ошибочное или небезопасное изменение.

### Repository corruption

Некорректное действие может затронуть primary checkout или неверный commit.

### Incomplete verification

Частично проверенный результат может ошибочно выглядеть как успешный.

### Context confusion

Данные одного проекта могут быть ошибочно использованы для другого.

### External provider failure

Облачный provider может быть недоступен, вернуть неполный ответ или нарушить ожидаемый контракт.

## Mitigations высокого уровня

- context filtering;
- secret detection;
- repository binding;
- isolated worktrees;
- bounded inputs and outputs;
- independent review;
- automated tests;
- fail-closed gates;
- human approval;
- recovery validation.

## Ограничение

Публичный Showcase намеренно не содержит детальные production security policies, credentials, реальные memory datasets и приватную runtime-конфигурацию.
