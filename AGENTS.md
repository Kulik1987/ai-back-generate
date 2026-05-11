# AGENTS.md

## Назначение файла

Этот файл содержит правила для Codex и других AI-агентов, которые работают в этом репозитории.

Codex должен использовать этот файл как основной источник инструкций перед любыми изменениями в проекте.

## Главная цель проекта

Этот репозиторий предназначен для построения AI-assisted product development workflow.

Основная цепочка:

1. Транскрипт разговора с заказчиком.
2. Project brief.
3. Product research.
4. Техническое задание.
5. Backlog.
6. UX/UI specification.
7. Architecture.
8. Backend implementation.
9. Frontend implementation.
10. QA.
11. Release preparation.

## Основные правила

1. Не изменять файлы без необходимости.
2. Не делать изменения вне поставленной задачи.
3. Не удалять файлы без явного разрешения пользователя.
4. Не добавлять секреты, токены, пароли, ключи или credentials в репозиторий.
5. Не изменять production-настройки без явного разрешения пользователя.
6. Не выполнять опасные команды без объяснения.
7. Перед большими изменениями сначала объяснить план.
8. После изменений показать список измененных файлов.
9. Если задача неясна — задать уточняющий вопрос.
10. Если есть риск сломать проект — предупредить пользователя.

## Git workflow

Codex должен соблюдать следующие правила Git:

1. Не работать напрямую в ветке main для больших задач.
2. Для новой задачи предлагать отдельную ветку.
3. Названия веток:
   - docs/<short-task-name>
   - feature/<short-task-name>
   - fix/<short-task-name>
   - infra/<short-task-name>
   - qa/<short-task-name>
4. Перед изменениями проверять статус:
   bash
   git status
После изменений показывать:

git diff
Commit делать только по просьбе пользователя.
Push делать только по просьбе пользователя.
Не выполнять force push.
Не менять историю Git без явного разрешения.
Не трогать чужие изменения, если они уже есть в working tree.
Структура репозитория

Репозиторий должен использовать следующую структуру:

transcripts/
docs/
docs/adr/
docs/design/
docs/qa/
docs/releases/
openapi/
apps/backend/
apps/frontend/
infra/
.github/
project-status.json
AGENTS.md

Назначение папок:

transcripts/ — исходные транскрипты разговоров с заказчиками.
docs/ — основная документация проекта.
docs/adr/ — Architecture Decision Records.
docs/design/ — UX/UI спецификации, sitemap, user flows, wireframes.
docs/qa/ — test plans, test cases, QA reports.
docs/releases/ — release notes, release checklist, rollback plan.
openapi/ — OpenAPI specifications.
apps/backend/ — backend-приложения.
apps/frontend/ — frontend-приложения.
infra/ — Docker, Kubernetes, CI/CD, deployment.
.github/ — GitHub templates, workflows, automation.
project-status.json — текущее состояние процесса.
AGENTS.md — правила для Codex.
Документация

Codex должен создавать и обновлять документацию в Markdown.

Основные документы:

docs/brief.md
docs/product-research.md
docs/requirements.md
docs/backlog.md
docs/architecture.md
docs/adr/0001-initial-architecture.md
docs/design/sitemap.md
docs/design/user-flows.md
docs/design/wireframes.md
docs/design/figma-spec.md
docs/qa/test-plan.md
docs/qa/qa-report.md
docs/releases/release-checklist.md
docs/releases/rollback-plan.md

Правила документации:

Использовать понятные заголовки.
Не смешивать факты и предположения.
Помечать предположения как Assumption.
Помечать открытые вопросы как Open Question.
Для требований использовать ID:
REQ-001
REQ-002
REQ-003
Для user stories использовать ID:
US-001
US-002
US-003
Для ADR использовать формат:
docs/adr/0001-title.md
docs/adr/0002-title.md
Работа с транскриптами

Если задача связана с транскриптом, Codex должен:

Читать файл из transcripts/.
Не изменять исходный транскрипт.
Создать или обновить docs/brief.md.
Выделить:
цели заказчика;
требования;
ограничения;
риски;
открытые вопросы;
предположения.
Не выдумывать требования, которых нет в транскрипте.
Если данных недостаточно — явно написать это.
Работа с требованиями

При создании ТЗ Codex должен использовать структуру:

Executive Summary.
Goals.
Out of Scope.
User Roles.
Functional Requirements.
Non-Functional Requirements.
User Stories.
Acceptance Criteria.
Data Requirements.
API Requirements.
Integrations.
Risks.
Open Questions.

Acceptance Criteria должны быть в формате:

Given ...
When ...
Then ...
Работа с backlog

При создании backlog Codex должен группировать задачи:

Product tasks.
UX/UI tasks.
Architecture tasks.
Backend tasks.
Frontend tasks.
DevOps tasks.
QA tasks.
Release tasks.

Каждая задача должна иметь:

ID;
title;
area;
priority;
description;
acceptance criteria;
dependencies.
Работа с архитектурой

При создании architecture docs Codex должен описывать:

Architecture overview.
Backend architecture.
Frontend architecture.
Data architecture.
API architecture.
Infrastructure architecture.
Security.
Observability.
Scalability.
Risks.
ADR decisions.
Python правила

Если задача относится к Python, Codex должен:

Работать внутри apps/backend/ или отдельной явно указанной папки.
Предлагать виртуальное окружение .venv, но не добавлять его в Git.
Использовать requirements.txt или pyproject.toml.
Добавлять тесты, если меняет бизнес-логику.
Предпочитать pytest для тестов.
Перед завершением предлагать команды проверки.

Типовые команды:

python -m venv .venv
python -m pip install -r requirements.txt
python -m pytest
python -m compileall .
Java правила

Если задача относится к Java, Codex должен:

Определить сборщик проекта: Maven или Gradle.
Не смешивать Maven и Gradle без необходимости.
Класть код в стандартную структуру:
src/main/java
src/test/java
Добавлять unit tests.
Перед завершением предлагать команды проверки.

Maven:

mvn test
mvn package

Gradle:

gradle test
gradle build
JavaScript / TypeScript правила

Если задача относится к JavaScript или TypeScript, Codex должен:

Проверить package.json.
Не менять package manager без необходимости.
Не удалять lock-файл.
Добавлять тесты для измененной логики.
Перед завершением предлагать команды проверки.

Типовые команды:

npm install
npm run lint
npm test
npm run build

Если используется pnpm:

pnpm install
pnpm lint
pnpm test
pnpm build
Frontend правила

Frontend-код должен находиться в:

apps/frontend/

Codex должен:

Следовать design docs из docs/design/.
Не хардкодить данные, если есть API contract.
Реализовывать loading, empty и error states.
Не добавлять тяжелые UI-библиотеки без разрешения.
Добавлять тесты для компонентов, если это возможно.
Backend правила

Backend-код должен находиться в:

apps/backend/

Codex должен:

Читать docs/requirements.md и docs/architecture.md.
Следовать openapi/openapi.yaml, если файл существует.
Не менять API contract без объяснения.
Добавлять тесты.
Не хранить secrets в коде.
Не делать destructive database migrations без разрешения.
Infra правила

Infra-код должен находиться в:

infra/

Codex может создавать:

Dockerfile;
docker-compose.yml;
Kubernetes manifests;
Helm charts;
GitHub Actions workflows.

Codex не должен:

Добавлять production secrets.
Удалять production resources.
Создавать cluster-admin permissions.
Автоматически деплоить production.
Менять production без ручного подтверждения.
Безопасность

Запрещено добавлять в Git:

.env
.env.*
*.key
*.pem
*.p12
*.pfx
*.jks
kubeconfig
credentials/
secrets/
database dumps
production config

Если Codex видит такие файлы, он должен предупредить пользователя и не коммитить их.

Команды проверки

Перед завершением coding-задачи Codex должен предложить подходящие проверки.

Для документации:

git diff

Для Python:

python -m pytest

Для Java:

mvn test

или:

gradle test

Для JavaScript:

npm test
npm run build

Для всего проекта, если появится Makefile:

make test
make build
Формат ответа Codex после выполнения задачи

После работы Codex должен дать краткий отчет:

Что сделано:
- ...

Измененные файлы:
- ...

Проверки:
- ...

Риски:
- ...

Следующий шаг:
- ...
Ограничения

Codex не должен выполнять следующие действия без явного разрешения пользователя:

Commit.
Push.
Force push.
Удаление файлов.
Установка новых крупных зависимостей.
Изменение CI/CD.
Изменение Docker/Kubernetes production config.
Запуск миграций базы данных.
Деплой.
Изменение секретов.
Приоритет инструкций

Если пользовательская команда противоречит правилам безопасности из этого файла, Codex должен остановиться и объяснить риск.

Если задача требует изменения этих правил, Codex должен сначала предложить изменение AGENTS.md и дождаться подтверждения пользователя.
"@ | Out-File -FilePath "AGENTS.md" -Encoding utf8


---

# 4. Проверь, что файл записался

powershell
Get-Content .\AGENTS.md

Или коротко:

Get-Content .\AGENTS.md -TotalCount 40   