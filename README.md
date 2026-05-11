# AI Back Generate

## Назначение проекта

Этот репозиторий предназначен для настройки AI-assisted workflow разработки продукта с помощью локального Codex CLI.

Основная идея:

1. Загружается транскрипт разговора с заказчиком.
2. На основе транскрипта создается project brief.
3. Затем формируется техническое задание.
4. После этого создается backlog.
5. Далее проектируется архитектура.
6. Затем реализуются backend/frontend задачи.
7. QA проверяет результат.
8. Release process готовит выпуск.

## Текущий статус

Статус: initial setup.

Проект пока находится на этапе настройки структуры репозитория и правил работы Codex.

## Планируемый стек

Проект может использовать несколько стеков:

- Python для backend, automation scripts или AI workflow;
- Java для backend-сервисов, если потребуется enterprise-стек;
- JavaScript/TypeScript для frontend и tooling.

Финальный стек должен быть зафиксирован в ADR.

## Структура репозитория

```text
transcripts/          исходные транскрипты и интервью
docs/                 документация проекта
docs/adr/             архитектурные решения
docs/design/          UX/UI и системный контекст
docs/qa/              стратегия тестирования и QA отчеты
docs/releases/        процесс релизов и rollback
openapi/              API contracts
apps/backend/         backend application
apps/frontend/        frontend application
infra/                инфраструктура, Docker, Kubernetes, CI/CD
.github/              GitHub templates and workflows
AGENTS.md             правила для Codex
project-status.json   состояние проекта
Правила работы

Перед любыми изменениями Codex должен читать AGENTS.md.

Основные правила:

не коммитить секреты;
не пушить без разрешения;
не делать destructive changes без разрешения;
работать маленькими шагами;
показывать diff перед commit;
держать документацию в актуальном состоянии.