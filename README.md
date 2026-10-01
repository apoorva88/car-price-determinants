# Car price determinants

Analysis of ~426K Craigslist used-vehicle listings to identify what drives listing price and to support inventory and pricing decisions for a used car dealership.

## Notebook

Open and run from the `code_files` directory:

**[code_files/prompt_II.ipynb](code_files/prompt_II.ipynb)**

```bash
cd code_files
jupyter lab prompt_II.ipynb
```

## Summary of findings

- **Mileage and age matter most:** Newer model years and lower odometer readings are consistently associated with higher prices.
- **Configuration and brand:** Fuel type, drivetrain, body type, title status, and manufacturer shift median prices after accounting for age and mileage in regression models.
- **Data quality:** Many listings have missing condition/size fields or invalid prices ($0 or extreme outliers); models use cleaned rows (e.g., price between $5K and $200K, year ≥ 1990).
- **Modeling:** Linear, Ridge, and Random Forest regressors were compared with cross-validation and hyperparameter tuning; Ridge coefficients and test-set **R²**, **RMSE**, and **MAE** support interpretable pricing guidance.
- **Recommendations for dealers:** Prioritize newer, lower-mileage units; avoid or discount salvage-title inventory; use model predictions as a pricing assistant alongside inspections and local market knowledge.

## Repository layout

```
car-price-determinants/
├── README.md
└── code_files/
    ├── prompt_II.ipynb    # Main analysis (CRISP-DM)
    ├── data/
    │   └── vehicles.csv
    └── images/            # Figures referenced in the notebook
```

## Requirements

Python 3 with `pandas`, `numpy`, `matplotlib`, `seaborn`, and `scikit-learn`.
