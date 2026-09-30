<div align="right">

![Python 3.8+](https://img.shields.io/badge/python-3.8%2B-3776ab.svg?style=for-the-badge&logo=python&logoColor=white)
![Scripts 5](https://img.shields.io/badge/scripts-5-blueviolet.svg?style=for-the-badge)
![Sanitized](https://img.shields.io/badge/sanitized-public_twin-2EAD33.svg?style=for-the-badge)
[![License: MIT](https://img.shields.io/badge/license-MIT-yellow.svg?style=for-the-badge)](LICENSE)

</div>

# 🐍 Python Script Collection

**Curated, reusable Python scripts for security research, automation, and API exploration.**

> Why should I care? Everyone rebuilds the same one-off tooling: audit a package's API surface, fan out across APIs with rate limits, bulk-fetch from PyPI, discover an endpoint's shape, check version compatibility. This is the public, sanitized home for that toolkit — no proprietary internals, no credentials, no Kimi-specific hooks. Grab a script, run it, move on.

**License:** [MIT](LICENSE) · **Security:** sanitized public twin — secret hygiene is enforced by `.gitignore` (`*.pat`, `*.token`, `secrets/`, `.env` are never committed).

## Script catalog

| Script | Purpose | Python | Async |
|--------|---------|--------|-------|
| `audit_engine.py` | Deep-audit any Python package: API maps, comment harvest, obfuscation scan | 3.8+ | ✅ |
| `aggregate.py` | Multi-source data aggregation with rate-limited parallel fetching | 3.8+ | ✅ |
| `fetch_pkgs.py` | Batch package fetch from PyPI with retry and mirror fallback | 3.8+ | ✅ |
| `api_probe.py` | REST/GraphQL endpoint shape discovery with schema inference | 3.8+ | ✅ |
| `compat_scan.py` | AST-based Python 3.12→3.8 compatibility checker | 3.8+ | ❌ |

## 🚀 Quick start

```bash
git clone https://github.com/toxicwind/python-script-collection.git
cd python-script-collection
python audit_engine.py --package requests --output json   # audit a package
```

More recipes:

```bash
# Aggregate multiple APIs
python aggregate.py --sources sources.yaml --workers 30

# Probe an API shape
python api_probe.py --url https://api.example.com --discover
```

## ⚙️ Requirements

- Python 3.8+ (3.11 recommended, 3.12 for latest features)
- `aiohttp`, `httpx`, `pyyaml`, `rich`

## 🛠️ Status

This repo is the sanitized public twin of a private scripts repository and is being populated — the catalog above is the target index. Scripts land here as they are sanitized for public release.

## Contributing

PRs welcome. All contributions must pass `black`, `ruff`, and `pytest`.

## 📄 License

MIT — see [LICENSE](LICENSE).
