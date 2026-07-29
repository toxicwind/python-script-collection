# 🐍 Python Script Collection

[![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-blue.svg)](https://www.python.org/)
[![Python 3.11](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/)
[![Python 3.12](https://img.shields.io/badge/python-3.12-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![CI](https://github.com/toxicwind/python-script-collection/actions/workflows/ci.yml/badge.svg)](https://github.com/toxicwind/python-script-collection/actions)

> **Curated collection of reusable Python scripts for security research, automation, and API exploration.**
>
> Sanitized public twin of the private `scripts` repository. No proprietary internals, no credentials, no Kimi-specific hooks.

## Scripts

| Script | Purpose | Python | Async |
|--------|---------|--------|-------|
| `audit_engine.py` | Deep-audit any Python package: API maps, comment harvest, obfuscation scan | 3.8+ | ✅ |
| `aggregate.py` | Multi-source data aggregation with rate-limited parallel fetching | 3.8+ | ✅ |
| `fetch_pkgs.py` | Batch package fetch from PyPI with retry and mirror fallback | 3.8+ | ✅ |
| `api_probe.py` | REST/GraphQL endpoint shape discovery with schema inference | 3.8+ | ✅ |
| `compat_scan.py` | AST-based Python 3.12→3.8 compatibility checker | 3.8+ | ❌ |

## Install

```bash
git clone https://github.com/toxicwind/python-script-collection.git
pip install -r requirements.txt
```

## Usage

```bash
# Audit a package
python audit_engine.py --package requests --output json

# Aggregate multiple APIs
python aggregate.py --sources sources.yaml --workers 30

# Probe an API shape
python api_probe.py --url https://api.example.com --discover
```

## Requirements

- Python 3.8+ (3.11 recommended, 3.12 for latest features)
- `aiohttp`, `httpx`, `pyyaml`, `rich`

## Contributing

PRs welcome. All contributions must pass `black`, `ruff`, and `pytest`.

## License

MIT — see [LICENSE](./LICENSE).
