# PostAir Weather API — End-to-End Automated Testing Ecosystem

[![Postman](https://img.shields.io/badge/Postman-v11+-FF6C37?logo=postman&logoColor=white)](https://www.postman.com/)
[![Newman](https://img.shields.io/badge/CLI-Newman-FF6C37?logo=npm&logoColor=white)](https://github.com/postmanlabs/newman)
[![CI/CD](https://img.shields.io/badge/CI%2FCD-GitHub_Actions-2088FF?logo=githubactions&logoColor=white)](https://github.com/features/actions)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

A centralized Quality Assurance & Test Engineering ecosystem for the **PostAir Weather API**. This repository unifies functional smoke validations, deep contract schema assertions, negative/RFC-7807 error-handling, and performance/load benchmarking into a single structured portfolio.

---

## 📦 Test Suite Architecture

| Module | Scope & Objectives | Direct Repository |
| :--- | :--- | :--- |
| **01. Baseline Tests** | Core smoke validations, basic status codes, and happy-path checks | [`postair-api-baseline-test-suite`](https://github.com/xfxradeon/postair-api-baseline-test-suite) |
| **02. Error Handling** | RFC 7807 Problem Details compliance, negative paths, and 4xx/5xx boundaries | [`PostAir-Weather-API-postair-api-error-handling-suite`](https://github.com/xfxradeon/PostAir-Weather-API-postair-api-error-handling-suite) |
| **03. Data Validation** | Strict regex patterns, enum checks, and `skipTest` pipeline resilience | [`PostAir-Weather-API-Data-Validation`](https://github.com/xfxradeon/PostAir-Weather-API-Data-Validation) |
| **04. Performance Tests** | Multi-user load profiles, latency thresholds, and virtual user benchmarks | [`PostAir-Weather-Api-Performance-Test`](https://github.com/xfxradeon/PostAir-Weather-Api-Performance-Test) |

---

## 🛠️ Key Testing Practices Demonstrated

- **Contract & Schema Auditing:** Deep schema validations enforcing types, required field arrays, and ISO 8601 temporal formatting beyond surface-level `200 OK` statuses.
- **Pipeline Resilience (`skipTest` Pattern):** Gracefully routes missing test records (`404`) as warnings using `console.warn()` to protect CI pipelines from non-deterministic false negatives.
- **RFC 7807 Problem Details Standards:** Verifies structured machine-readable error payloads (`type`, `title`, `status`, `detail`, `instance`).
- **Automated CI/CD Reporting:** Integrates Newman CLI with GitHub Actions workflows to auto-generate self-contained HTML test execution reports via `newman-reporter-htmlextra`.

---

## 🚀 Getting Started

### Clone All Repositories

Because this parent repository links individual test modules via Git submodules, clone it with the `--recurse-submodules` flag:

```bash
git clone --recurse-submodules [https://github.com/xfxradeon/PostAir-Weather-API-Comprehensive-Testing-Suite.git](https://github.com/xfxradeon/PostAir-Weather-API-Comprehensive-Testing-Suite.git)