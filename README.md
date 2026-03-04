# Healthcare Data Preprocessing & Analysis
**Tools:** Python · Pandas · NumPy · PyTorch · Matplotlib · Seaborn

## Overview
End-to-end preprocessing and exploratory analysis of a 55,500-record
Kaggle healthcare dataset. The project prepares raw patient data for
machine learning through structured cleaning, feature engineering,
dimensionality reduction, and visualization.

## Dataset
- Source: Kaggle Healthcare Dataset (CC0 License)
- Records: 55,500 (54,966 after deduplication)
- Features: 15 original + 2 engineered
- Covers: patient demographics, medical conditions, billing,
  admission type, insurance provider, hospital stay details

## Project Workflow

### 1. Data Cleaning
- Standardized inconsistent text casing across 10 categorical columns
- Parsed date columns to datetime format
- Removed 534 duplicate records
- Replaced negative billing values with column mean

### 2. Feature Engineering
- Hospital Stay Duration: derived from admission and discharge dates
- Age Group: binned into 3 segments (0–18, 19–50, 51+)

### 3. Outlier Detection
- Applied IQR method across 5 numeric features
- No significant outliers detected — confirmed data consistency

### 4. Data Discretization
- Billing Amount binned into Low / Medium / High cost tiers
- Applied both equal-width and equal-frequency binning for comparison

### 5. Dimensionality Reduction (PCA)
- Standardized features using PyTorch tensors
- Computed SVD to derive PCA component loadings
- Identified Room Number as lowest-importance feature → dropped
- Reduced feature set to: Age, Billing Amount,
  Hospital Stay Duration, Age Group

### 6. EDA & Visualization
- Age distribution and billing amount spread
- Average billing by medication type
- Age group patient count distribution
- Correlation heatmap across numeric features

## Key Stats

| Metric | Value |
|--------|-------|
| Original records | 55,500 |
| After deduplication | 54,966 |
| Billing range | $9 – $52,764 |
| Avg billing amount | ~$25,595 |
| Avg hospital stay | ~15.5 days |
| Features after PCA | 4 |

## Files
| File | Description |
|------|-------------|
| `healthcare_preprocessing.ipynb` | Full analysis notebook |
| `healthcare_dataset.csv` | Raw dataset (via Kaggle) |

## Skills Demonstrated
`Python` `Pandas` `NumPy` `PyTorch` `PCA` `Feature Engineering`
`Outlier Detection` `Data Discretization` `EDA` `Seaborn`
