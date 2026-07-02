# dbt Analytics Engineering — Olist Jinja, Macros & Packages

## Introduction

This project is **Milestone 2** of the Olist E-Commerce Analytics Engineering portfolio, building directly on the foundational dbt pipeline established in [Milestone 1](https://github.com/soichi-berson/dbt_olist_milestone1).

While Milestone 1 focused on core analytics engineering fundamentals — staging models, mart models, data quality testing, and documentation — this milestone demonstrates intermediate dbt development skills: **Jinja templating, custom macros, and third-party dbt packages**.

All macros are applied to the existing Olist dataset rather than built as isolated exercises, keeping the portfolio cohesive and demonstrating how a real analytics engineering project evolves incrementally.

## Milestone 1 Reference

> **Milestone 1 repository:** [github.com/soichi-berson/dbt_olist_milestone1](https://github.com/soichi-berson/dbt_olist_milestone1)

Milestone 1 includes:
- 6 staging models cleaning and standardising raw source tables
- 4 mart models (1 fact table, 3 dimension tables) with business logic applied
- 23 automated data quality tests (unique, not_null)
- Full model and column documentation via schema.yml
- Global table materialisation configured in dbt_project.yml

## What This Milestone Adds

### Packages
Two community packages installed via `packages.yml`:
- `dbt-labs/dbt_utils` — utility macros including surrogate key generation
- `calogica/dbt_expectations` — extended data quality test suite

### Custom Macros

| Macro | Purpose | Jinja Feature Demonstrated |
|---|---|---|
| `cents_to_dollars` | Converts a cents column to a rounded dollar value | Arguments with default values |
| `clean_string` | Lowercases and trims whitespace from text fields | Reusable single-argument macro |
| `coalesce_columns` | Generates a dynamic COALESCE across a list of columns | `for` loop with `loop.last` conditional |


## Tech Stack

- dbt Cloud (Fusion)
- Google BigQuery (EU region)
- SQL + Jinja2
- YAML
- GitHub

## Data Source

Dataset: [Brazilian E-Commerce Public Dataset by Olist (Kaggle)](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)

License: [Creative Commons CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/)
Used for non-commercial portfolio purposes only.

## Author

Soichiro Tanabe  
Feel free to explore the project and reach out if you have any questions.
