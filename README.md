# brandon-fox/.github

> **Status:** active — shared GitHub Actions, reusable CI workflows, and community health defaults for personal repositories under [brandon-fox](https://github.com/brandon-fox).

## Composite Actions

- `.github/actions/setup-uv-cached` — installs `uv` with caching enabled and optionally runs `uv sync`.
- `.github/actions/setup-rust-cached` — sets up Python (optional, for PyO3), Rust toolchain (`clippy`, `rustfmt`), and `Swatinem/rust-cache`.
- `.github/actions/setup-node-cached` — sets up Node.js with `npm` caching.
- `.github/actions/cache-ml-weights` — caches `~/.cache/huggingface/hub` and `~/.cache/torch/hub` keyed on `pyproject.toml` and `uv.lock`.
- `.github/actions/run-autofixers` — runs safe, deterministic auto-fixers (`uv lock`, `ruff check --fix`, `ruff format`, `cargo fmt`).

## Reusable Workflows

- `.github/workflows/python-ci.yml` — parameterized Python CI (`uv lock --check`, `ruff`, `mypy`, `pytest` with coverage).
- `.github/workflows/links-check.yml` — markdown/HTML link validation via `lycheeverse/lychee-action`.
- `.github/workflows/ade-axioms.yml` — First-ADE axiom validation wrapper pinned to a verified upstream commit SHA.
- `.github/workflows/pr-size-guard.yml` — warns above 400 non-lockfile lines and fails above 1000 lines.
- `.github/workflows/pr-queue-rebase.yml` — auto-merges eligible PRs and serializes rebasing 1 behind PR per `main` push.
- `.github/workflows/ci-autofix.yml` — self-healing CI workflow that applies safe fixes via a verified `autofix/pr-<n>` sub-PR (or direct push) with loop protection.

## Independence

All work here is personal and independent of any employer, built on my own time and equipment. Licensed under the MIT License; principles at [First-ADE/PRINCIPLES.md](https://github.com/First-ADE/.github/blob/main/PRINCIPLES.md).
