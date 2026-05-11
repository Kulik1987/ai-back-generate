# System Context

## Purpose

Этот документ описывает верхнеуровневый контекст системы: какие части будут в проекте, кто ими пользуется, какие внешние интеграции возможны и где проходят границы ответственности.

## Current Status

Status: Draft

На текущем этапе система еще не реализована. Этот документ задает стартовую рамку для будущей архитектуры.

## Main Actors

| Actor | Description |
|---|---|
| Customer | Заказчик или конечный пользователь продукта |
| Product Owner | Человек, утверждающий требования и приоритеты |
| Developer | Человек или AI-агент, реализующий задачи |
| QA | Человек или AI-агент, проверяющий качество |
| Release Manager | Человек или AI-агент, готовящий релиз |

## Planned Subsystems

| Subsystem | Description |
|---|---|
| Transcript Processing | Обработка транскриптов и создание project brief |
| Product Documentation | Требования, backlog, architecture docs |
| Backend | API и бизнес-логика |
| Frontend | Пользовательский интерфейс |
| API Contract | OpenAPI спецификация |
| QA | Test strategy, test cases, QA reports |
| Release | Release notes, rollback plan, release checklist |
| Infrastructure | Docker, CI/CD, deployment |

## External Integrations

Потенциальные интеграции:

- GitHub;
- Codex CLI;
- Figma;
- Jira или GitHub Issues;
- Slack/Telegram;
- Docker;
- Kubernetes;
- PostgreSQL/MySQL;
- Sentry;
- Grafana/Prometheus.

## System Boundaries

На текущем этапе source of truth:

- код и документация — GitHub repository;
- задачи — пока markdown backlog, позже GitHub Issues;
- API contract — `openapi/`;
- архитектурные решения — `docs/adr/`;
- статус процесса — `project-status.json`.

## Open Questions

- Какой backend стек будет основным: Python или Java?
- Нужен ли frontend сразу?
- Какая база данных будет использоваться?
- Будет ли production deployment на первом этапе?
- Нужна ли интеграция с Figma на первом этапе?
