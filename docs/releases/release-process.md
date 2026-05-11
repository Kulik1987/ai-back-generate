# Release Process

## Purpose

Этот документ описывает базовый процесс подготовки и выпуска релизов.

## Current Status

Status: Draft

Production deployment пока не настроен. До появления production окружения этот документ используется как шаблон.

## Branching Model

Планируемые ветки:

```text
main        стабильная ветка
develop     интеграционная ветка
feature/*   новая функциональность
fix/*       исправления
docs/*      документация
infra/*     инфраструктура
release/*   подготовка релиза
```

## Release Flow

1. Все задачи для версии завершены.
2. Все PR смержены в `develop`.
3. Пройдены проверки.
4. Создан release branch.
5. QA проверяет release candidate.
6. Создаются release notes.
7. Создается rollback plan.
8. Пользователь вручную подтверждает release.
9. Выполняется production deployment.
10. Выполняется smoke test.
11. Релиз закрывается.

## Manual Approval

Production release нельзя выполнять автоматически без ручного подтверждения.

Manual approval обязателен для:

- production deployment;
- database migrations;
- rollback;
- изменения secrets;
- изменения production infrastructure.

## Release Checklist

Перед релизом проверить:

- [ ] Все задачи закрыты.
- [ ] Все критичные баги исправлены.
- [ ] Тесты пройдены.
- [ ] QA report готов.
- [ ] Release notes готовы.
- [ ] Rollback plan готов.
- [ ] Production approval получен.

## Rollback

Rollback plan должен содержать:

- предыдущую стабильную версию;
- команды rollback;
- проверку после rollback;
- владельца решения;
- условия, при которых rollback запускается.

## Open Questions

- Будет ли использоваться Semantic Versioning?
- Где будет production environment?
- Как будет выполняться deployment?
- Нужны ли GitHub Releases?
