# Wafer Defect Classifier

Automatically classifies semiconductor wafer maps into 9 distinct failure type labels using a CNN

## Why?
Wafers have to be labeled one by one by engineers, and there are far too many to keep up. In WM-811K, 78.7% of wafers were never labeled.
Each failure pattern points to a cause, e.g. Scratch means something physically scraped the wafer, likely during handling.
Classifying wafers automatically helps engineers find and fix the faulty step sooner.

## Dataset
WM-811K: 811,457 semiconductor wafer maps from real fabs, 172,950 (21.3%) of them labeled into 9 classes.
Download `LSWMD.pkl` from Kaggle and place it in `data/`.

## Setup
```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```
Note: pandas is pinned to 2.3.2 because 'LSWMD.pkl' was saved with an old pandas version, and pandas 3 can't load it.

## Roadmap
- [x] Explore the data
- [ ] scikit-learn baseline
- [ ] CNN in PyTorch, handling class imbalance
- [ ] Evaluation: confusion matrix, per-class precision/recall
- [ ] FastAPI endpoint
- [ ] Docker
- [ ] GitHub Actions running tests
