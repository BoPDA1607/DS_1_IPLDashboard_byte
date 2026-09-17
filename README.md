# IPL 2026 Statistics Dashboard

Interactive dashboard summarizing key team and player statistics from the IPL 2026 season.

## Data Source
- **Source:** https://www.kaggle.com/datasets/sujalninawe/ipl-2026-ball-by-ball-dataset-daily-updated
- **Extraction date:** 9/16/2026 2:33 PM
- **Coverage:** 75 matches, 28-Mar-2026 to 31-May-2026 (full IPL 2026 season)
- **Granularity:** Ball-by-ball delivery data

### Known limitations
- Dataset covers a single season (2026) only — season filter is therefore not meaningful; team filters are provided instead.
- No dismissal-type column exists, so wicket counts credit every fallen wicket to the bowler on strike, including run-outs. This may slightly overcount a small number of bowlers.
- 1 incomplete row was dropped during cleaning (out of 17,527 total rows).

## Repo Structure
```
ipl-dashboard/
├── data/raw/              # original dataset
├── data/processed/        # cleaned CSVs
├── notebooks/ipl_dashboard.ipynb
├── exports/ipl_dashboard.html
├── exports/charts/        # PNG snapshots of each chart
├── README.md
```

## How to Run
1. `pip install -r requirements.txt` (pandas, numpy, plotly, kaleido)
2. Open `notebooks/ipl_dashboard.ipynb`
3. Restart & Run All
4. Interactive dashboard is generated at `exports/ipl_dashboard.html`; static chart PNGs are saved to `exports/charts/`

## Dashboard Contents
- Runs per match (time series), filterable by team
- Top 10 run-scorers, filterable by team
- Top 10 wicket-takers, filterable by team
- Team win percentages
```