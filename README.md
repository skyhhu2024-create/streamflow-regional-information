# Streamflow regional information

Code and reproducible cases for **Global data availability does not make nearby streamflow gauges dispensable**.

## Download

[Download the complete source package](streamflow-regional-information.zip). Extract it before running the commands below. The ZIP preserves the directory tree and contains 236 files, including 214 Python modules and package initializers. The checksum is in [SHA256SUMS.txt](SHA256SUMS.txt).

## Functional organization

The calculation workflows are organized by purpose in `workflows/`:

- `archive_diagnosis`: missing records and reference support
- `benchmarks`: matched information and reconstruction comparisons
- `regional_dependence`: global reference pools, withdrawal and seasonal controls
- `rainfall`: precipitation inputs and complementarity
- `monitoring`: added observations and location experiments
- `validation`: identities, genuine gaps and retrieved observations
- `water_resources`: low-flow timing, deficits and interval water volume
- `shared`: common data, model and evaluation utilities

The reusable numerical core is in `src/streamflow_info/`; runnable cases are in `examples/`, checks in `tests/`, and English reproduction instructions in `docs/`. The package includes an English and Chinese README.

## Quick start

From the extracted `streamflow-regional-information` directory:

```sh
python -m pip install -e .
python -m unittest discover -s tests -v
python examples/run_synthetic_case.py --output-dir outputs/synthetic_case
```

Python 3.10 or later is required. The synthetic case needs no provider observations. The registered Paraná / Posadas case accepts an explicit JSON input configuration; see `examples/README.md`. Full study inputs and entry points are documented in `docs/REPRODUCTION.md` and `docs/EXPERIMENT_MAP.csv`.

## Checks

All 37 portable tests passed. The registered observational case reproduced 15 input arrays and 25 output arrays exactly, including 2,880 predictions. A separate core comparison found 1,860 exactly matching array/scalar outputs across 12 synthetic conditions. Source imports, functional paths and documentation links were checked. Detailed scope is recorded in `docs/VERIFICATION.md` inside the package.

Provider observations are not included. Data access remains governed by GSIM, GRDC, ERA5 and Caravan terms. No open-source licence or software DOI has yet been assigned.

[中文说明](README_zh.md)
