# promptmill

Feed a thousand prompts, get a thousand answers

## Examples

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Getting started

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## Features

- Idempotent: skips ids already present in the output
- JSONL in, JSONL out: stream-safe for huge inputs
- Concurrent workers with a rate ceiling
- Retries failed items with backoff, logs them aside

## Project structure

```text
├── .github/
│   ├── dependabot.yml
│   └── pull_request_template.md
├── docs/
│   ├── configuration.md
│   ├── faq.md
│   ├── roadmap.md
│   └── usage.md
├── examples/
│   └── quickstart.md
├── tests/
│   └── test_smoke.py
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── batch.py
├── prompts.sample.jsonl
└── requirements.txt
```

## Development

```bash
python -m venv .venv && source .venv/bin/activate
pip install -r requirements.txt
python -m pytest -q
```
