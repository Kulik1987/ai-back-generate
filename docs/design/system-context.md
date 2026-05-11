# System Context

## Purpose

тот документ описывает верхнеуровневый контекст системы: какие части будут в проекте, кто ими пользуется, какие внешние интеграции возможны и где проходят границы ответственности.

## Current Status

Status: Draft

а текущем этапе система еще не реализована. тот документ задает стартовую рамку для будущей архитектуры.

## Main Actors

| Actor | Description |
|---|---|
| Customer | аказчик или конечный пользователь продукта |
| Product Owner | еловек, утверждающий требования и приоритеты |
| Developer | еловек или AI-агент, реализующий задачи |
| QA | еловек или AI-агент, проверяющий качество |
| Release Manager | еловек или AI-агент, готовящий релиз |

## Planned Subsystems

| Subsystem | Description |
|---|---|
| Transcript Processing | бработка транскриптов и создание project brief |
| Product Documentation | Требования, backlog, architecture docs |
| Backend | API и бизнес-логика |
| Frontend | ользовательский интерфейс |
| API Contract | OpenAPI спецификация |
| QA | Test strategy, test cases, QA reports |
| Release | Release notes, rollback plan, release checklist |
| Infrastructure | Docker, CI/CD, deployment |

## External Integrations

отенциальные интеграции:

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

а текущем этапе source of truth:

- код и документация — GitHub repository;
- задачи — пока markdown backlog, позже GitHub Issues;
- API contract — openapi/;
- архитектурные решения — docs/adr/;
- статус процесса — project-status.json.

## Open Questions

- акой backend стек будет основным: Python или Java?
- ужен ли frontend сразу?
- акая база данных будет использоваться?
- удет ли production deployment на первом этапе?
- ужна ли интеграция с Figma на первом этапе?
