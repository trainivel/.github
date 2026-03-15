# Trainify

> Integrating Fitness applications with Bookkeeping software — powered by pull/push syncing.

---

## What is Trainify?

**Trainify** is a Laravel-based integration platform that bridges **Fitness applications** (such as TrainMore, MindBody, or other gym/studio platforms) with **Bookkeeping software** (such as Exact Online, Moneybird, or other accounting systems).

It uses a **pull/push syncing method**:

- **Pull** — Trainify fetches data (memberships, transactions, revenue) from connected fitness platforms.
- **Push** — Trainify forwards the processed data to the connected bookkeeping system, ensuring accurate and up-to-date financial records.

---

## Repository Purpose

This is the **`.github`** repository for the [trainivel](https://github.com/trainivel) organization (Trainify). It contains:

| Path | Purpose |
|------|---------|
| `.github/workflows/` | Reusable GitHub Actions workflows (Pint, PHPUnit, PHPStan, Composer updates, Yarn updates) |
| `.github/actions/` | Composite actions (e.g. PHP + Composer setup) |
| `.github/ISSUE_TEMPLATE/` | Standardized issue templates (Bug Report, Feature Request) |
| `.github/PULL_REQUEST_TEMPLATE/` | PR checklist template |
| `.github/scripts/` | Helper scripts for CI reporting |
| `.github/copilot-instructions.md` | Coding conventions for GitHub Copilot |
| `.coderabbit.yaml` | CodeRabbit AI review configuration |

---

## Workflows

| Workflow | Trigger | Purpose |
|----------|---------|---------|
| `pint.yml` | Manual / PR | Enforce Laravel Pint code style |
| `phpunit.yml` | Manual | Run PHPUnit test suite |
| `phpstan.yml` | Manual | Static analysis with PHPStan |
| `composer-update.yml` | Manual / Schedule | Update Composer dependencies & open PR |
| `yarn-update.yml` | Manual / Schedule | Update Yarn (npm) dependencies & open PR |

---

## Stack

- **Backend:** Laravel 12 (PHP 8.4)
- **Frontend:** Vite + TailwindCSS
- **Testing:** PHPUnit
- **Code Style:** Laravel Pint
- **Static Analysis:** PHPStan

---

*ND Software — made in Holland*
