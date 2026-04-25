# Common Design Guidelines

Документы, общие для backend и frontend (не дублируются в `go/` и `vue/`).

- `check_list.md` — общий чек-лист (дальше — профильные в `go/` и `vue/`).
- `project_architecture.md` — зоны, границы ответственности, структура репо.
- `design_principles.md` — DDD/SOLID/DRY/KISS/Clean Architecture.
- `libraries_reusable_code_requirements.md` — общие правила выноса кода в `libs/*`.
- `external_dependencies_catalog.md` — единый каталог внешних библиотек и инструментов.

Дополнительно для `kodex`:
- процессы выполняются по webhook-событиям, а не через GitHub Actions workflows;
- Kubernetes и repository-провайдеры подключаются только через интерфейсы и адаптеры;
- модель данных и синхронизация multi-pod держатся на PostgreSQL (`JSONB` + `pgvector`).
- env/secrets/CI variable names для платформы используют префикс `KODEX_`
  (кроме значений, требуемых внешними runtime-контрактами).
- проектное планирование и документационная каноника задаются корневым `AGENTS.md` и актуальной проектной документацией, а не этим техническим гайдом.
