# data-policy-syncer

Update training/eval datasets to reflect policy changes by identifying and re-processing affected data segments with LLM-as-a-judge.

## Layout

- **`src/`** – Application code
  - **`policy/`** – Policy definitions, loading, change detection (`loader.py`, `diff.py`)
  - **`judge/`** – LLM-as-a-judge: prompts, client, scoring (`prompts.py`, `llm_client.py`)
  - **`data/`** – Dataset I/O, segment identification, re-processing pipeline (`datasets.py`, `segments.py`, `pipeline.py`)
  - **`cli.py`** – CLI entry point
- **`config/`** – Policy files and app config (e.g. `config/policies/`)
- **`data/`** – `input/` (source datasets), `output/` (updated datasets)
- **`scripts/`** – Helper or one-off scripts
- **`tests/`** – Unit and integration tests
