# brandon-fox/.github

Shared GitHub Actions, reusable CI workflows, and community health defaults for personal repositories under `brandon-fox`.

## Composite Actions

- `.github/actions/setup-uv-cached` — installs `uv` with caching enabled and optionally runs `uv sync`.
- `.github/actions/setup-rust-cached` — sets up Python (optional, for PyO3), Rust toolchain (`clippy`, `rustfmt`), and `Swatinem/rust-cache`.
- `.github/actions/setup-node-cached` — sets up Node.js with `npm` caching.
- `.github/actions/cache-ml-weights` — caches `~/.cache/huggingface/hub` and `~/.cache/torch/hub` keyed on `pyproject.toml` and `uv.lock`.

## Reusable Workflows

- `.github/workflows/python-ci.yml` — parameterized Python CI (`uv lock --check`, `ruff`, `mypy`, `pytest` with coverage).
- `.github/workflows/links-check.yml` — markdown/HTML link validation via `lycheeverse/lychee-action`.
- `.github/workflows/ade-axioms.yml` — First-ADE axiom validation wrapper pinned to a verified upstream commit SHA.

## Independence

All work here is personal and independent of any employer. Licensed under the MIT License.
