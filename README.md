# FLattacks final results

Static GitHub Pages presentation of the frozen `flattacks-final-v1-n10` evaluation.

- 80 shared victim-gradient aggregates across eight Pythia-160m/Pythia-410m cells
- 10 independent aggregate runs per cell
- DAGER-Pythia-adapted, FILM-inspired Pythia adaptation with autonomous reordering, and autonomous FLattacks V2
- 240 autonomous attack evaluations scored with candidate-flooding-aware set metrics

## Public files

- `index.html` — compact interactive results page
- `results.json` — public aggregate statistics and bootstrap intervals, including bag/support-type F1
- `examples.json` — five deterministic rank-quantile matched examples per method
- `oracle.json` — eight-cell, 10-run V2 truth-assisted evaluator diagnostic

The results table labels support-type F1 as **bag F1**: the harmonic mean of precision and recall comparing each method's inferred unique token support with the unique tokens in the private references' visible prefixes. It is unordered and makes no multiplicity, order, endpoint, or sequence-recovery claim. The public data projection excludes raw private schedules, source-row mappings, internal paths, credentials, and retained private evidence. The V2 truth-assisted diagnostic uses private references for evaluator-only fragment assignment and ordering; it reports token-ID ROUGE macro F1 over one assembled reconstruction per reference and is neither autonomous attack performance nor a fourth method.

## Local preview

```bash
python3 -m http.server 8000
```

Then open `http://127.0.0.1:8000/`.
