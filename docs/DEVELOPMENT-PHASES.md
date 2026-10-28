# Development phases

[← README](../README.md)

The implementation is organized into five reviewable delivery phases. They describe the repository's packaging and review structure; they do not claim to reproduce the original chronological development history.

Each phase has a feature branch and a PR targeting `main`. Phases are merged in order, keeping their branches and merge commits for reference.

| Phase | Feature branch | Scope | Pull request |
| --- | --- | --- | --- |
| 01 · Foundation | `feature/phase-01-foundation` | Cartridge identity, job step types, template hook registration, custom objects, Order attributes, preferences and jobs | [PR #1](https://github.com/Vedesh-reddy/sfcc-storefront-analytics/pull/1) |
| 02 · Engine and jobs | `feature/phase-02-engine-jobs` | Collection, aggregation, reconciliation and reporting helpers, job steps, template hook, desk labels, order and report tests | [PR #2](https://github.com/Vedesh-reddy/sfcc-storefront-analytics/pull/2) |
| 03 · Storefront and desk | `feature/phase-03-storefront-desk` | Controller extensions, Analytics-Collect, storefront script, Business Manager reports, remaining tests | [PR #3](https://github.com/Vedesh-reddy/sfcc-storefront-analytics/pull/3) |
| 04 · Tooling and quality | `feature/phase-04-tooling-quality` | npm dependencies, build, lint checks, metadata ZIP, GitHub Actions, PR template | [PR #4](https://github.com/Vedesh-reddy/sfcc-storefront-analytics/pull/4) |
| 05 · Documentation | `feature/phase-05-documentation` | Feature guide with highlighted sandbox screenshots, guides, contributing guide, attribution | [PR #5](https://github.com/Vedesh-reddy/sfcc-storefront-analytics/pull/5) |

The same cartridges are integrated in [SFCC-RefArch](https://github.com/Vedesh-reddy/SFCC-RefArch) through PRs #60–#63 and #64.

The final `main` branch contains all five phases. Build output is generated locally or downloaded from a successful GitHub Actions run; it is not committed.
