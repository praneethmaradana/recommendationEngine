# Music Recommendation System

Simple popularity and item-similarity recommender built on the Million Song Dataset samples.

## Project structure
- Recommenders.py — recommender classes (popularity / item-similarity)
- Million Songs Data - Recommendation Engine.ipynb — example notebook
- evaluation.py — (suggested) evaluation helpers
- data/ (not tracked) — expected location for dataset files

## Data (not included)
Do NOT commit large dataset files to GitHub. Place the following in `data/`:
- triplets_file.csv — user song play interactions
- song_data.csv — song metadata

Download links:
- song data example: https://www.kaggle.com/datasets/geomack/songdata
(Place downloaded files as `data/triplets_file.csv` and `data/song_data.csv`.)

## Setup
1. Create virtual env and activate (Windows PowerShell):
```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
pip install -r requirements.txt
```

2. If `requirements.txt` not present, install:
```powershell
pip install pandas numpy scikit-learn tqdm
```

## Usage
1. Open the notebook in VS Code or Jupyter and run cells in order.
2. In Python scripts:
```python
from Recommenders import popularity_recommender_py, item_similarity_recommender_py
# load data into `song_df` (must contain 'user_id' and 'song' columns)
```

## Evaluation
Add an `evaluation.py` with precision/recall/MAP helpers and run train/test split per user before evaluating. See notebook for examples.

## Git / GitHub
- Keep large files out of repo. Use `.gitignore`:
```
*.csv
*.rar
__pycache__/
.venv/
```
- If large files were previously committed, remove them from tracking:
```powershell
git rm --cached *.csv *.rar
git commit -m "Remove large files from tracking"
```

## License
Add a license file if needed.
