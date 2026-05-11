# Test Strategy

## Purpose

Этот документ описывает базовую стратегию тестирования проекта.

## Current Status

Status: Draft

Проект пока находится на этапе настройки. Конкретные тесты появятся после выбора стека и реализации первых компонентов.

## Quality Goals

Минимальные цели качества:

- изменения должны быть маленькими и проверяемыми;
- новая бизнес-логика должна иметь тесты;
- backend API должен проверяться unit/integration тестами;
- frontend должен проверяться component/e2e тестами, если frontend появится;
- перед release должен быть QA report.

## Test Levels

| Level | Purpose | Required Now |
|---|---|---|
| Unit tests | Проверка отдельных функций и классов | Да, когда появится код |
| Integration tests | Проверка взаимодействия компонентов | Да, для backend API |
| Contract tests | Проверка соответствия OpenAPI | Позже |
| E2E tests | Проверка пользовательских сценариев | Позже |
| Smoke tests | Быстрая проверка после deploy | Позже |
| Regression tests | Повторная проверка после фиксов | Позже |

## Python Checks

bash
python -m pytest
python -m compileall .
Java Checks

Maven:

mvn test
mvn package

Gradle:

gradle test
gradle build
JavaScript Checks
npm test
npm run build
Minimal Quality Gate

Перед завершением задачи Codex должен сообщить:

какие файлы изменены;
какие проверки запущены;
какие проверки не запускались и почему;
какие риски остались.
Bug Report Requirements

Каждый bug report должен содержать:

краткое описание;
шаги воспроизведения;
ожидаемый результат;
фактический результат;
окружение;
логи или скриншоты, если есть;
severity;
linked requirement, если есть.

Open Questions
Какой test framework будет использоваться для Python?
Будет ли Java использовать Maven или Gradle?
Будет ли frontend на React/Vue/Angular?
Нужны ли e2e тесты на первом MVP?