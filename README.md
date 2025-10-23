# Data Pipeline Project

This repository contains a Python script (`execute.py`) and data file (`data.csv`) for analytics processing. It is CI/CD-enabled with GitHub Actions, utilizing Ruff for linting and automatically publishing the computation results to GitHub Pages.

## Features

- Converts provided Excel data into CSV format for reproducibility.
- Processes data via `execute.py` using Pandas 2.3+ and Python 3.11+.
- Lints code with [Ruff](https://beta.ruff.rs/docs/).
- Publishes calculation results as `result.json` to GitHub Pages on each push.

## Usage

### Requirements

- Python 3.11+  
- pandas 2.3+

### Running locally

bash
python execute.py > result.json


### Development

- Edit `execute.py` or `data.csv` as needed.
- Push to GitHub.  
- CI will run Ruff, generate `result.json`, and deploy it via GitHub Pages.

### Files

- `execute.py`: Main analytics script
- `data.csv`: Data extracted from Excel
- `.github/workflows/ci.yml`: GitHub Actions workflow
- `result.json`: Generated _only in CI_; **DO NOT COMMIT MANUALLY**

### Outputs

View the latest published result at  
`https://<your-username>.github.io/<your-repository>/result.json`