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
- `candidate-ceilings.json` — DAGER/FILM truth-assisted independent best-of-K candidate ceilings for eight cells × 10 runs
- `v2-assembly-examples.json` — five deterministic assembly-anatomy examples selected from 740 V2 reference assemblies

The autonomous results table preserves R1/R2/RL F1 and also shows the soft-set RL precision/recall/F1 breakdown so the cardinality penalty is visible. It labels support-type F1 as **bag F1**: the harmonic mean of precision and recall comparing each method's inferred unique token support with the unique tokens in the private references' visible prefixes. It is unordered and makes no multiplicity, order, endpoint, or sequence-recovery claim.

The public data projection excludes raw private schedules, source-row mappings, internal paths, credentials, and retained private evidence. Both added views are strictly diagnostic:

- The DAGER/FILM candidate ceiling independently selects the best emitted candidate for every private reference. A candidate may be reused for multiple references and extra outputs are not penalized. It reports best-of-K RL mean and 95% CI, coverage at RL ≥ 0.25, and mean K; it is not autonomous/set performance and is not directly comparable to the headline table or V2 assembly.
- The V2 diagnostic uses private references to assign fragments on ≥2-token verbatim overlap, truth-order them, and concatenate them without overlap merging. The aggregate table reports token-ID ROUGE macro F1 over one assisted assembly per reference, while the anatomy file exposes five examples and every assigned fragment in order. Neither is autonomous attack performance nor a fourth method.

At DAGER's exact full-row-rank wall, its subspace is the whole feature space and cannot discriminate candidates. One run was marked unsupported and retained as zero instead of applying an unlabeled heuristic truncation.

## Local preview

```bash
python3 -m http.server 8000
```

Then open `http://127.0.0.1:8000/`.
