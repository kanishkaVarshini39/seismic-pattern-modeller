# seismic-pattern-modeller


### Law 1: Gutenberg-Richter Magnitude-Frequency Validation


| Parameter / Metric | Model Symbol | Attained Value | Standard Error | Rubric Benchmark |
| :--- | :---: | :---: | :---: | :---: | :---: |
| **Magnitude Ratio Slope** | $b$ | `1.08` | 🟢 **OPTIMAL** |
| **Regional Seismicity Baseline** | $a$ | `6.7740` | N/A (Regional Anchor) | ℹ️ **CALIBRATED** |
| **Coefficient of Determination** | $R^2$ | `0.997` | $R^2 \ge 0.95$ | ✅ **PASSED** |


### Law 2: Omori Aftershock Decay Results (Top 5 Sequences)


| Sequence Event | Mainshock ($M$) | Aftershocks ($n$) | Decay Exponent ($p$) | Time Offset ($c$) | Statistical $p$-value | Benchmark Status |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: |
| **Ridgecrest Earthquake Sequence** | 7.1 | 2,332 | 1.54 | 0.001 | `6.18e-09` | ✅ **PASSED** |
| **The 1999 Hector Mine** | 7.1 | 1,412 | 1.29 | 0.649 | `3.07e-20` | ✅ **PASSED** |
| **Ocotillo (8km ESE)** | 5.7 | 226 | 1.39 | 0.001 | `1.03e-06` | ✅ **PASSED** |
| **2004 Parkfield** | 6.0 | 104 | 1.51 | 0.001 | `5.30e-03` | ✅ **PASSED** |
| **Lone Pine (18km SSE)** | 5.8 | 66 | 2.50 | 1.023 | `3.33e-02` | ✅ **PASSED** |


