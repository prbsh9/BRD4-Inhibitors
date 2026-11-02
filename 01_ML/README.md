# 01_ML

`brd4_inhibitors.ipynb` — the notebook used for the final run.

## Inputs

| File | Placed at |
|---|---|
| ChEMBL activity export, target `CHEMBL1163125` | `data/brd4/ml/CHEMBL1163125_raw.csv` |
| COCONUT 09-2026 snapshot | `data/coconut/coconut_csv-09-2026.csv` |

Paths are set by `TargetConfig` in cell 1 and default to `../data` relative to the
notebook.

## Run

Run cells 0–46 in order. Cell 2 sets `COMPUTE_PROFILE` (`mac` for a quick run,
`college` for the full run); cell 3 sets `SMOKE`.

| Setting | Value used in the paper |
|---|---|
| Activity cut | pChEMBL ≥ 7.0 — 939 actives / 3,931 compounds |
| Seed | 42 |
| Test fraction | 0.20 |
| Splits | random, scaffold, Butina |
| Fingerprints | ECFP4+MACCS, Avalon |
| Selection metric | BEDROC, α = 20 |
| Deployment models | RandomForest (ECFP4+MACCS), HistGradientBoosting (Avalon) |

Results are written to `data/brd4/out/results/`. Stage 6 (screening) needs the COCONUT
file; stages 1–5 need only the ChEMBL export.

