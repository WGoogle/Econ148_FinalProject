# Econ148_FinalProject

Econ 148 Final Project, GDP Nowcasting from Mixed-Frequency Indicators.

## Run in the browser (no setup)

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/WGoogle/Econ148_FinalProject/main)

Click the badge to launch the whole project in Binder. Everything runs end-to-end without any API keys — notebook `1_Data_Collection.ipynb` transparently falls back to the raw CSVs checked into `data/raw/` when no `FRED_API_KEY` is set. Notebooks 2–4 only read from those CSVs, so they are fully reproducible.

Recommended run order:
1. `1_Data_Collection.ipynb`
2. `2_Baseline_Bridge.ipynb`
3. `3_MLStuff.ipynb`
4. `4_Comparisons.ipynb`

## Run locally

```
pip install -r requirements.txt
jupyter notebook
```

To refresh the cached CSVs against live FRED data, create a `secret_key.env` file in the repo root with:

```
FRED_API_KEY=your_key_here
```

Without this file, notebook 1 simply re-uses the committed CSVs.

## Reproducibility notes

- Raw FRED series are committed under `data/raw/` so the pipeline runs offline.
- Binder uses the config in `binder/` (Python 3.11, CPU-only PyTorch) so the image stays small and builds quickly.
- Processed outputs land in `data/processed/` and are overwritten each run.
