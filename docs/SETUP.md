# Setup Guide

Decision Intelligence Lab runs locally with Python, Streamlit, pandas, Plotly, SQLite, and pytest. It does not require external APIs, paid services, or credentials.

## Mac/Linux

```bash
git clone https://github.com/tylerdobson/decision-intelligence-lab.git
cd decision-intelligence-lab
python -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt
python scripts/setup_database.py
streamlit run app.py
```

Open `http://localhost:8501`.

## Windows PowerShell

```powershell
git clone https://github.com/tylerdobson/decision-intelligence-lab.git
cd decision-intelligence-lab
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
python scripts\setup_database.py
streamlit run app.py
```

Open `http://localhost:8501`.

## Tests

```bash
python -m pytest
python -m compileall -q app.py src scripts tests
```

## Screenshot Capture

Install the Playwright browser runtime once:

```bash
python -m playwright install chromium
```

Capture project screenshots:

```bash
python scripts/capture_decision_lab_media.py
```

The checked-in proof assets are static screenshots and a poster image only.

## Troubleshooting

- If Streamlit cannot find data, run `python scripts/setup_database.py`.
- If Playwright reports missing Chromium, run `python -m playwright install chromium`.
- If PowerShell blocks activation, run `Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass` for that terminal session only.
