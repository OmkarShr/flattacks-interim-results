# FLattacks verified non-LAMP development results

Public site: https://omkarshr.github.io/flattacks-interim-results/

This repository publishes an independently reviewed, deterministic development snapshot for:

- FLattacks V2;
- DAGER adapted to Pythia/GPT-NeoX;
- the current support-constrained/no-reorder FILM adaptation;
- Pythia-160m and Pythia-410m across eight prescribed `N/B/M/S` cells.

## Files

- `index.html` — interactive, responsive results page;
- `results.json` — machine-readable public projection;
- `verification-report.pdf` — nine-page artifact-backed report;
- `verification-report.html` — editable/browser report.

## Scope

These are eight seed-0 development aggregates, not repeated held-out benchmark estimates. V2 truth-assisted values are oracle diagnostics. FILM lacks the planned candidate-gradient-norm reorder and does not persist its in-memory support hash in the current development receipt. LAMP is intentionally excluded.

Verified evidence bundle SHA-256:

```text
0f152be5047225a8c6c442d685613d4ababcff723811950ecb3c87c582f9ba97
```
