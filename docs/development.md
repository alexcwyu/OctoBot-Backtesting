# Development

<!-- current-documentation-provenance -->
Documentation reviewed: 2026-10-13 · Git source base: `00614352fbe4789f0791762aba9ead0883ae52ad` · [Current architecture and feature guide](ayu-develop.md).
Historical execution commands/results below retain their original dates and scope; this metadata update is not a new application test run.
<!-- /current-documentation-provenance -->


## uv maintenance workflow (2026-10-12)

Selected complete environment: Python 3.15.0; build backend `hatchling.build`. The workspace uses uv 0.13.0. Python 3.15 was attempted before any fallback; the actual failure and selected runtime are recorded in [validation](validation.md).

```sh
export UV_PYTHON_PREFERENCE=only-managed
uv python install 3.15.0
uv lock --upgrade
uv sync --all-extras --python 3.15.0
uv build --python 3.15.0
uv run --frozen --all-extras python -m compileall -q src/octobot_backtesting
uv run --frozen --all-extras python -m pytest tests
```

Keep source resources inside their package and preserve the repository's existing src layout. Rebuild after source/native/asset changes. Use the locked environment for final verification. Commands above are the standard workflow, not a promise that every existing suite currently passes; consult validation for exact outcomes and unresolved compatibility issues.
