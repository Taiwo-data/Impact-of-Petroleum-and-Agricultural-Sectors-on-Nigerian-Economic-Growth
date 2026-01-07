# Impact-of-Petroleum-and-Agricultural-Sectors-on-Nigerian-Economic-Growth
This project examines how Nigeria’s petroleum and agricultural sectors influenced GDP from 1980–2015. Using regression analysis, it shows oil drives growth while agriculture remains vital for food, jobs, and raw materials, highlighting the need for balanced sectoral development.

[![Python](https://img.shields.io/badge/Python-3.10-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

---

## Overview
This project investigates the relationship between **Nigeria's petroleum sector, agricultural sector, and GDP** from 1980 to 2014. Using **time-series data** and **multiple linear regression (OLS)**, the study quantifies each sectors impact on economic growth and provides insights for **policy makers, economists, and researchers** on economic diversification and sustainable development.

---

## Project Objectives
- Determine the relationship between petroleum sector, agriculture, and GDP.
- Assess the relative contribution of petroleum and agriculture to Nigeria economic growth.
- Identify causes of sectoral booms or declines and their implications for the economy.

---

## Dataset
- **Source:** Central Bank of Nigeria Statistical Bulletin (2013, 2014)
- **Variables:**
  - `RGDP`: Gross Domestic Product (dependent variable)
  - `AGRIC`: Agricultural sector output (independent variable)
  - `PETROL`: Petroleum sector output (independent variable)
- **Period:** 1980-2014 (35 annual observations)
- **Format:** CSV file (`data/nigeria_sector_data.csv`)

---

##  Methodology
1. **Data Collection:** Secondary data from CBN Statistical Bulletin.
2. **Analysis:** Multiple linear regression using **Ordinary Least Squares (OLS)**.
3. **Model Specification:**
   ```
   GDP = Î±â‚ + Î±â‚(AGRIC) + Î±â‚‚(PETROL) + Î¼
   ```
   - Î±â‚ = Intercept
   - Î±â‚Î±â‚ = Regression coefficients
   - Î¼ = Error term

4. **Assumptions Checked:**
   - Errors have zero mean and are independent
   - Constant variance (homoscedasticity)
   - Normality of errors
   - No autocorrelation (Durbinâ€“Watson test)

---

## Key Findings
- **Both agricultural output and petroleum revenue significantly contribute to GDP.**
- Agricultural output has a **stronger positive impact** on GDP than petroleum revenue.
- Over-reliance on petroleum has caused **neglect of agriculture**, food import dependency, and structural economic imbalance.
- Model has high explanatory power (**R² = 0.994**) with reliable estimates.

---

### Table 1: Descriptive Statistics
| Variable | Mean | Std. Deviation | N |
|---|---|---|---|
| RGDP (â‚¦ Million) â” Dependent (Y) | 10,301,041.75 | 14,454,142.308 | 35 |
| AGRICULTURAL OUTPUT (â‚¦ Million) â” Independent (X‚) | 3,406,834.63 | 4,971,271.758 | 35 |
| OIL REVENUE (â‚¦ Million) â” Independent (Xâ‚‚) | 2,171,391.78 | 2,751,293.692 | 35 |

**Interpretation:** This table summarizes the central tendency and dispersion of GDP, agricultural output, and oil revenue. AGRIC and PETROL show high variability, indicating significant fluctuations over the study period.

---

### Table 2: Model Summary
| Model | R | R Square | Adjusted R Square | Std. Error of the Estimate | F Change | Sig. F Change | Durbin Watson |
|---|---|---|---|---|---|---|---|
| 1 | .997 | .994 | .994 | 1,162,356.697 | 2,613.235 | .000 | 1.637 |

**Interpretation:** The model explains **99.4% of the variation in GDP**, indicating a very strong fit. The Durbin-Watson value (1.637) suggests slight positive autocorrelation but is acceptable for time-series data.

---

### Table 3: Collinearity Diagnostics
| Model | Dimension | Eigenvalue | Condition Index | Variance Proportions (Constant) | AGRICULTURAL OUTPUT X1 | OIL REVENUE X2 |
|---|---|---|---|---|---|---|
| 1 | 1 | 2.440 | 1.000 | .06 | .02 | .02 |
|   | 2 | .506 | 2.196 | .89 | .04 | .02 |
|   | 3 | .054 | 6.724 | .05 | .95 | .97 |

**Interpretation:** Variance inflation factors (VIFs) and condition indices suggest moderate multicollinearity. AGRICULTURAL OUTPUT and OIL REVENUE are slightly correlated but acceptable for regression analysis.

---

### Table 4: Regression Coefficients
| Variable | B | Std. Error | Beta | t | Sig. | VIF |
|---|---|---|---|---|---|---|
| Constant | 96,992.30 | 252,347.97 | - | 0.384 | 0.703 | - |
| AGRICULTURAL OUTPUT (Xâ‚) | 2.500 | 0.100 | 0.860 | 25.109 | 0.000 | 6.165 |
| OIL REVENUE (Xâ‚‚) | 0.777 | 0.180 | 0.148 | 4.322 | 0.000 | 6.165 |

**Interpretation:**
- AGRICULTURAL OUTPUT has a highly significant positive impact on GDP. A unit increase in AGRIC corresponds to an increase of 2.5 units in GDP.
- OIL REVENUE is also significant but has a smaller effect (0.777 units increase per unit change).
- Both variables are statistically significant (**p < 0.001**) with acceptable multicollinearity levels.

---

## Recommendations
1. **Economic Diversification:** Strengthen agriculture and agro-industrial sectors.
2. **Strategic Reinvestment:** Use petroleum revenues for agriculture and infrastructure.
3. **Credit Access & Mechanization:** Expand NACB and ACGS support for farmers.
4. **Research & Extension Services:** Enhance agricultural productivity and sustainability.
5. **Policy Consistency:** Maintain long-term agricultural development policies.

---


---

##  Tools & Technologies
- Python 3.10 (pandas, statsmodels, matplotlib, seaborn)
- Microsoft Word (full project report)
- GitHub (version control & collaboration)

---

## License
This project is **open-source** and licensed under the [MIT License](LICENSE).

---

## References
1. Central Bank of Nigeria Statistical Bulletin (2013, 2014)
2. Reynolds, D. (1975). *Agricultural Development and Economic Growth*
3. Omawalea & Rodrigues (1979). *Agriculture and National Development*
4. Oji-Okoro, I. (2011). *FDI and Agricultural Development in Nigeria*
5. Ekpo & Umoh (2012). *Agriculture and GDP Growth in Nigeria*

