# dq-delivery-tests

My work repository for **DQ Kolo — Course 1: Data Quality Foundations**.

| Resource | Link |
|----------|------|
| Course platform | DQ Kolo (lessons & homework) |
| Practice company (read-only) | [dq-delivery](https://github.com/smoliarliliia-sudo/dq-delivery) |
| This repo template | [dq-delivery-tests-template](https://github.com/smoliarliliia-sudo/dq-delivery-tests-template) |

## First-time setup

1. Start the company platform locally (in the `dq-delivery` folder):

   ```bash
   cp .env.example .env
   docker compose up --build
   ```

2. Configure this repo:

   ```bash
   cp .env.example .env
   ```

3. Connect to PostgreSQL on port **5433** (see `.env.example`).

## Folder structure

| Folder | Purpose |
|--------|---------|
| `sql/` | SQL validation queries by DQ dimension |
| `tests/` | pytest suite |
| `docs/` | DQ Strategy Document (Phase 1) and phase notes |
| `reports/` | Profiling results and test run reports |
| `config/` | Database and rules configuration (later modules) |
| `utils/` | Shared Python helpers |
| `data/` | Local test fixtures (if needed) |

## Git workflow

One branch per module → Pull Request → merge to `main`.

Commit messages: lowercase, imperative — e.g. `add email validity check for customers`.
