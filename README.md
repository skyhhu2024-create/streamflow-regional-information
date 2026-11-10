# Streamflow regional information — code release 0.2.0

Code and reproducible cases for **Global data availability does not make nearby streamflow gauges dispensable**.

## Download the complete source tree

[Download streamflow-regional-information v0.2.0](streamflow-regional-information_v0.2.0.zip).

The checked source tree is distributed as a ZIP to preserve its nested directory structure. Extract it before following the commands below. The archive contains **182 files**, including **142 archived calculation sources**, the portable numerical core, synthetic and registered observational-case examples, tests, and English/Chinese reproduction guides. It is aligned to the audited manuscript and supplement dated 8 November 2026.

## Quick start

1. Download and extract the ZIP.
2. Open a terminal in the extracted `streamflow-regional-information` directory.
3. Run:

```bash
python -m pip install -e .
python -m unittest discover -s tests -v
python examples/run_synthetic_case.py --output-dir outputs/synthetic_case
```

Python 3.10 or later is required. The synthetic case needs no provider data or credentials. For the exact study contracts, read the extracted `README.md`, `docs/REPRODUCTION.md`, `docs/MANUSCRIPT_ALIGNMENT.md`, and `docs/EXPERIMENT_MAP.csv`.

## What is included

- Archive gaps and reference-support diagnosis.
- Controlled information and reconstruction-system comparisons.
- Global reference selection, regional-source withdrawal, and reference history/gap agreement.
- Rainfall complementarity and observation-location experiments.
- Low-flow timing, cumulative deficits, total interval water volume, and paired uncertainty summaries.
- Supplementary genuine-gap evaluation and a registered river-case exporter.

The release includes code and case configurations, not GSIM, GRDC, ERA5 or other provider observation arrays. Full global reproduction additionally needs the original frozen study inputs, identity decisions and registrations described in the archive. A current data download alone does not recreate that snapshot.

## Verification

On 10 November 2026, all **33 tests** passed. The registered Paraná / Posadas case reproduced **16 arrays exactly, including 2,880 predictions**. All 142 archived source checksums and syntax checks passed. The full global empirical experiments were not rerun during packaging.

The ZIP SHA-256 is listed in [SHA256SUMS.txt](SHA256SUMS.txt). Data-free verification receipts and source hashes are included inside the archive.

## Licence and citation

No open-source licence has yet been assigned. Dataset access and use remain governed by their providers. A final paper citation and software DOI can be added when available.

[中文说明](README_zh.md)
