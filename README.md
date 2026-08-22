# FLattacks final results

Static GitHub Pages presentation of the frozen `flattacks-final-v1-n10` evaluation.

- 80 shared victim-gradient aggregates across eight Pythia-160m/Pythia-410m cells
- 10 independent aggregate runs per cell
- DAGER-Pythia-adapted, FILM-inspired Pythia adaptation with autonomous reordering, and autonomous FLattacks V2
- 240 autonomous attack evaluations scored with candidate-flooding-aware set metrics

## Public files

- `index.html` — compact interactive results page
- `results.json` — public aggregate statistics and bootstrap intervals
- `examples.json` — selected highest/lowest matched qualitative examples

The public data projection excludes raw private schedules, source-row mappings, internal paths, credentials, and retained private evidence. Truth-assisted diagnostics are not presented as autonomous attack performance.

## Local preview

```bash
python3 -m http.server 8000
```

Then open `http://127.0.0.1:8000/`.
