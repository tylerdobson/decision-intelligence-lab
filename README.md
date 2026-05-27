# Decision Intelligence Lab

## Overview
A Python analytics project that turns sample business data into KPI views, forecast ranges, and recommendation-style outputs. The public copy focuses on reproducible analysis rather than production claims.

## Problem
Business stakeholders need a clear way to inspect KPI changes, scenario inputs, and recommendation logic without reading raw data tables.

## Features
- Sample business dataset
- Streamlit analytics app
- SQLite/SQL support files
- KPI and forecast calculations
- Tests for core logic

## Tech Stack
- Python
- Pandas
- SQLite
- Streamlit
- pytest

## Architecture
Python modules and scripts handle data preparation, metrics, and app presentation. Tests live under `tests/`, SQL/database helpers live under `sql/` and `database/`, and docs explain methodology.

## Data Source

The repository includes sample business data for reproducible portfolio demonstration. It does not claim to represent a real company or market.

## Data Limitations

The analysis demonstrates workflow and logic; it should not be used for operational decisions.

## Reproducibility

Run setup, then tests, then the Streamlit app from the repo root.

## Setup
```powershell
py -3.12 -m venv .venv
.\.venv\Scripts\python.exe -m pip install -r requirements.txt
```

## Environment Variables
No required secrets. The included sample data is for demo/reproducibility use.

## How To Run
```powershell
.\.venv\Scripts\python.exe -m streamlit run app.py
```

## Tests
```powershell
.\.venv\Scripts\python.exe -m pytest
```

## Demo / Screenshots
Demo assets are generated from the included modeled dataset:

- `assets/demo/hero.png`
- `assets/demo/dashboard-overview.png`
- `assets/demo/kpi-explorer.png`
- `assets/demo/forecasting-lab.png`
- `assets/demo/scenario-analysis.png`
- `assets/demo/executive-recommendations.png`
- `assets/demo/data-explorer.png`
- `assets/demo/demo.webm`
- `assets/demo/demo.gif`
- `assets/demo/narrated-demo.mp4`

The narrated MP4 is generated from the public-safe WebM capture plus local text-to-speech narration. It uses modeled data only and does not claim production forecasting accuracy.

Regenerate them with:

```powershell
.\.venv\Scripts\python.exe -m playwright install chromium
.\.venv\Scripts\python.exe scripts\capture_decision_lab_media.py
```

## Security / Privacy Notes
The public copy excludes old history and non-public working notes. Included data is sample/demo material only.

## Limitations
- Not a production forecasting system.
- Outputs are analytical examples, not business advice.
- Demo media uses modeled sample data, not real company records.

## Roadmap
- Add a concise walkthrough writeup.
- Tighten methodology notes after reviewer feedback.
- Add deployment notes only if a real public deployment exists.

## License
MIT License. See `LICENSE`.
