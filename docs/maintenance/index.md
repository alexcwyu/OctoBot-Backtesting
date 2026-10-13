# OctoBot-Backtesting: portable verification records

<!-- current-documentation-provenance -->
Documentation reviewed: 2026-10-13 · Git source base: `00614352fbe4789f0791762aba9ead0883ae52ad` · [Current architecture and feature guide](../ayu-develop.md).
Historical execution commands/results below retain their original dates and scope; this metadata update is not a new application test run.
<!-- /current-documentation-provenance -->


Full raw logs are retained in the workspace maintenance evidence, not distributed here. Hashes identify those original logs. A successful build or selected test subset does not imply a full test-suite pass. Commands containing <workspace> describe the original execution environment.

[Machine-readable records](verification.json) · [Repository validation summary](../validation.md)

## Executed commands

| Check | Exit | Duration | Command | Outcomes |
| --- | ---: | ---: | --- | --- |
| build | 0 | 1.0s | `uv build --python 3.15` | Successfully built dist/octobot_backtesting-1.10.0.tar.gz<br>Successfully built dist/octobot_backtesting-1.10.0-py3-none-any.whl |
| compile | 0 | 0.13s | `<workspace>/OctoBot-Backtesting/.venv/bin/python -m compileall -q src` | See exit status; no test-count assertion. |
| final-build | 0 | 1.49s | `uv build --python 3.15.0` | Successfully built dist/octobot_backtesting-1.10.0.tar.gz<br>Successfully built dist/octobot_backtesting-1.10.0-py3-none-any.whl |
| final-build-2 | 0 | 0.97s | `uv build --python 3.15.0` | Successfully built dist/octobot_backtesting-1.10.0.tar.gz<br>Successfully built dist/octobot_backtesting-1.10.0-py3-none-any.whl |
| final-compile | 0 | 0.09s | `.venv/bin/python -m compileall -q src` | See exit status; no test-count assertion. |
| final-compile-2 | 0 | 0.08s | `.venv/bin/python -m compileall -q src` | See exit status; no test-count assertion. |
| final-lock | 0 | 0.25s | `uv lock --upgrade` | See exit status; no test-count assertion. |
| final-lock-2 | 0 | 0.46s | `uv lock --upgrade` | See exit status; no test-count assertion. |
| final-sync | 0 | 0.05s | `uv sync --all-extras --frozen --python 3.15.0` | See exit status; no test-count assertion. |
| final-sync-2 | 0 | 0.05s | `uv sync --all-extras --frozen --python 3.15.0` | See exit status; no test-count assertion. |
| lock-3.15 | 0 | 1.42s | `uv lock --upgrade --python 3.15` | See exit status; no test-count assertion. |
| public-manager-sync | 0 | 0.56s | `uv sync --all-extras --python 3.15` | See exit status; no test-count assertion. |
| sync-3.15 | 0 | 2.28s | `uv sync --all-extras --python 3.15` | See exit status; no test-count assertion. |
| tests | 2 | 1.97s | `<workspace>/OctoBot-Backtesting/.venv/bin/python -m pytest tests` | See exit status; no test-count assertion. |
| tests-2 | 0 | 6.59s | `.venv/bin/python -m pytest tests` | 19 passed in 4.88s |
| tests-3 | 0 | 2.51s | `.venv/bin/python -m pytest tests` | 19 passed in 1.25s |
