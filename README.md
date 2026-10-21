# AI for Sustainable Plant Extraction
### A beginner-friendly Random Forest teaching demonstration
**Dr. Abdul Bari Shah · KBTU**

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/abshah-ai/ai-green-extraction-demo/blob/main/extraction_demo.ipynb)

Companion to **AI for Sustainable Chemistry and Chemical Engineering: From Green Extraction to Process Optimization**.

> All data are simulated for teaching. No experiments on a real plant species were performed for this example. Predictions are not laboratory recommendations.

## Run in your browser
1. Click **Open in Colab** above (a Google sign-in may be required).
2. Choose **Runtime → Run all**, or run individual cells using their play buttons.
3. Read the explanation above each cell. Change the four conditions in section 7 and rerun that cell.

The notebook includes the exact CSV data internally, so no separate data upload is required. The button assumes the notebook is uploaded to the repository root on branch `main`; change the link if you use another branch.

## What you learn
- Input features, regression and a held-out test set.
- Training a Random Forest and comparing it with a mean baseline.
- MAE, RMSE, R² and a predicted-versus-observed plot.
- Prediction for 70% ethanol, 65°C, 50 minutes and 20 mL/g.
- Searching candidate conditions and interpreting trade-offs.

## Files
| File | Purpose |
|---|---|
| extraction_demo.ipynb | Explained, executed notebook with figures |
| simulated_extraction_data.csv | 300 synthetic rows for inspection or reuse |
| requirements.txt | Packages for optional local installation |
| TEACHING_GUIDE.md | Short speaking guide and student exercise |

## Data and limitations
The material is a hypothetical dried plant, not a particular species. Inputs are ethanol concentration (% v/v in the initial solvent), temperature (°C), time (min), and solvent volume per dry plant mass (mL/g). Recovery is target-compound mass recovered divided by target-compound mass initially present, times 100.

The notebook contains the full invented generating equation and fixed random seed (42). The training/test split is 240/60 independent synthetic rows. Hyperparameters are fixed in advance. Performance describes this artificial distribution only. Real batch/replicate data require group-aware validation and independent laboratory confirmation.

The heating-effort index is arbitrary, not energy or carbon. It cannot support emissions claims. Candidate rankings are limited to the selected grid and fitted model; they are not proven global optima.

## Optional local use
With Python 3.10 or newer, in this folder:
```bash
python -m pip install -r requirements.txt
python -m jupyterlab
```
Open `extraction_demo.ipynb` and run it from the top. Package ranges allow updates; versions are printed in the notebook. Exact results may vary slightly across versions.

## Sources
- [scikit-learn Random Forest documentation](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestRegressor.html)
- [scikit-learn common pitfalls](https://scikit-learn.org/stable/common_pitfalls.html)
- [Google Colab FAQ](https://research.google.com/colaboratory/faq.html)

See the repository LICENSE for reuse terms.
