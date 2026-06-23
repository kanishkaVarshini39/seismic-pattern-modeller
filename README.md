# seismic-pattern-modeller


### Law 1: Gutenberg-Richter Results

| Parameter / Metric | Model Symbol | Attained Value  | Rubric Benchmark | Certification Status |
| :--- | :---: | :---: | :---: | :---: |
| **Magnitude Ratio Slope** | $b$ | `1.08`  | 🟢 **OPTIMAL** |
| **Coefficient of Determination** | $R^2$ | `0.997`  | $R^2 \ge 0.95$ | ✅ **PASSED** |


### Law 2: Omori Aftershock Decay Results (Top 5 Sequences)

| Sequence Event | Mainshock ($M$) | Aftershocks ($n$) | Decay Exponent ($p$) | Time Offset ($c$) | Statistical $p$-value | Benchmark Status |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Ridgecrest Earthquake Sequence** | 7.1 | 2,332 | 1.54 | 0.001 | `6.18e-09` | ✅ **PASSED** |
| **The 1999 Hector Mine** | 7.1 | 1,412 | 1.29 | 0.649 | `3.07e-20` | ✅ **PASSED** |
| **Ocotillo (8km ESE)** | 5.7 | 226 | 1.39 | 0.001 | `1.03e-06` | ✅ **PASSED** |
| **2004 Parkfield** | 6.0 | 104 | 1.51 | 0.001 | `5.30e-03` | ✅ **PASSED** |
| **Lone Pine (18km SSE)** | 5.8 | 66 | 2.50 | 1.023 | `3.33e-02` | ✅ **PASSED** |

### XGBoost Aftershock Rate Forecasting Results

| Model Architecture | Target Framing | Key Engineered Features | Test RMSE (quakes/day) | Variance Explained ($R^2$) | ETAS Baseline Benchmark |
| :--- | :--- | :--- | :---: | :---: | :---: |
| **v1.0 Naive Baseline** | Raw Integer ($Y$) | Static metadata only | `95.615` | `0.232` | FAILED |
| **v2.0 Log-Target** | $\ln(1 + Y)$ | Ghost Sequence Filter | `23.685` | `0.614` | FAILED |
| **v3.0 Operational Hybrid** | $\ln(1 + Y)$ | **Day 1 Anchor + Omori Math** | **`10.004`** | **`0.86`** | 🏆 **OUTPERFORMED** |

## Repository Structure
```text
seismic-pattern-modeler/
│
├── Data/
│   ├── southern_california_cleaned.csv
│   └── southern_california_raw.csv
├── Docs/
│   ├── Seismic_Activity_Pattern_Model...
│   └── Seismic_Activity_Pattern_Model...
├── Visualisation/
│   ├── Folium_Map.png
│   ├── gutenberg_richter_fit.png
│   ├── omori_law_fits.png
│   └── xgboost_residual_analysis.png
├── src/
│   ├── Data Pipeline.ipynb    # Data Loading and Processing
│   ├── Gutenberg-Richter Law.ipynb
│   ├── Interactive-Folium-Map.ipynb
│   ├── Omori-Law.ipynb
│   └── XGBoost-Regressor.ipynb
├── .gitignore
├── requirements.txt
└── README.md
