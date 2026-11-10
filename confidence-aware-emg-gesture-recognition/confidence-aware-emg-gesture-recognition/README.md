# Confidence-Aware EMG Gesture Recognition

Reproducible Python notebook for **hybrid EMG-4 hand-gesture classification with confidence-aware prediction filtering**. It evaluates conventional classifiers, a stacked Extra Trees + Logistic Regression model, probability fusion with Gradient Boosting, and selective prediction.

## Highlights

- **96.35%** test accuracy and **96.38%** macro-F1 for the proposed hybrid.
- **99.37%** accuracy on accepted predictions at **81.54%** coverage.
- **61 of 71** incorrect classifications withheld by the confidence gate.

## Quick start

1. Install **Python 3.10+** and dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Download the [EMG-4 dataset](https://www.kaggle.com/datasets/kyr7plus/emg-4) and place its four CSV files (`0.csv`, `1.csv`, `2.csv`, `3.csv`) in `data/`.
3. From the repository root, open the notebook and run its cells in order:
   ```bash
   jupyter notebook notebooks/EMG4_Confidence_Aware_Recognition.ipynb
   ```

The notebook exports CSV tables and PNG figures to `results/`. Selected outputs from the recorded run are provided there for reference. If launching Jupyter from `notebooks/`, the data path is also resolved automatically.

## Repository contents

- `notebooks/` — executed research notebook (with saved cell outputs)
- `results/figures/` — five selected figures
- `results/tables/` — evaluation and ablation summaries
- `data/` — put the original CSVs here (not redistributed)

**Evaluation scope:** EMG-4 comprises four gestures recorded from one wearer. Recording boundaries are approximated using contiguous blocks; 
