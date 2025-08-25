# Practical Statistics for Data Practitioners

*A hands-on guide to descriptive and inferential statistics with Python.*

**Author:** Amir Kiani  
**Status:** Work in progress — contributions welcome!

![Python](https://img.shields.io/badge/Python-3.9%2B-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![Made with Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange.svg)

---

## 📚 Table of Contents

- [🧠 Overview](#overview)  
- [👥 Who This Book Is For](#who-this-book-is-for)  
- [✅ Features](#features)  
- [🗂️ Book Outline](#book-outline)  
- [📦 Requirements](#-requirements)  
- [🚀 Getting Started](#-getting-started)  
- [📁 Repository Structure](#-repository-structure)  
- [🔍 Examples](#-examples)  
- [🧪 Reproducibility](#-reproducibility)  
- [🤝 Contributing](#-contributing)  
- [📄 License](#-license)  
- [📌 Cite This Work](#-cite-this-work)  
- [✨ Acknowledgements](#-acknowledgements)

---

## 🧠 Overview

**Practical Statistics for Data Practitioners** is a concise, code-first introduction to the statistics you actually use in analytics and ML pipelines. Each concept is paired with a minimal proof sketch (where helpful), an intuition, and a Python example you can run in a notebook.

---

## 👥 Who This Book Is For

- Data analysts, scientists, and engineers who want reliable statistics without the fluff  
- Students and professionals working on A/B testing, experiment design, or model evaluation  
- Anyone who prefers *read → run → apply* learning

---

## ✅ Features

- Clean derivations with just-enough math  
- End-to-end Python examples with `pandas`, `NumPy`, `SciPy`, and `statsmodels`  
- Practical guidance on assumptions, diagnostics, and interpretation  
- Jupyter-ready notebooks for immediate exploration

---

## 🗂️ Book Outline

### Part I — Descriptive Statistics
1. Measures of Central Tendency  
2. Measures of Dispersion  
3. Measures of Shape  
4. Measures of Dependence  
5. Descriptive Stats in Python

### Part II — Inferential Statistics
2. Hypothesis Testing: Continuous Data (t-tests, ANOVA)  
3. Hypothesis Testing: Categorical Data (χ² tests)  
4. A/B Testing

### Part III — Linear Models
5. Linear Regression  
6. Logistic Regression

---

Required libraries:

- pandas
- numpy
- scipy
- statsmodels
- matplotlib (optional, for visualizations)

## 🚀 Getting Started
Clone the repository
```bash
git clone https://github.com/<your-username>/practical-statistics.git
cd practical-statistics
```

## 🔍 Examples
### Descriptive Stats in Pandas
```python
df.describe()
df['column'].mean()
df['column'].std()
df['column'].quantile([0.25, 0.75])
```
### Two-sample t-test with SciPy
```python
from scipy import stats
import numpy as np

group1 = np.array([...])
group2 = np.array([...])

t_stat, p_val = stats.ttest_ind(group1, group2)
print(t_stat, p_val)
```
### Linear Regression with statsmodels
```python
import statsmodels.api as sm
import pandas as pd

df = pd.DataFrame({"age": [2, 6, 7], "weight": [5, 20, 30]})
X = sm.add_constant(df[["age"]])
y = df["weight"]

model = sm.OLS(y, X).fit()
print(model.summary())
```
## 🧪 Reproducibility

- Version-controlled dependencies
- Random seed settings in notebooks
- Sample data included in `/data/`

## 🤝 Contributing

Want to improve the book?

1. Fork the repo
2. Create a feature branch: `git checkout -b my-feature`
3. Commit changes and push: `git push origin my-feature`
4. Open a pull request!
5. Feel free to fix typos, add clarifications, examples, or new sections.

## 6. 📄 License

This project is licensed under the MIT License.
You are free to use, modify, and distribute it with attribution.

## 📌 Cite This Work
```bibtex
@misc{kiani_practical_stats,
  author    = {Kiani, Amir},
  title     = {Practical Statistics for Data Practitioners},
  year      = {2025},
  url       = {https://github.com/<your-username>/practical-statistics}
}
```
## ✨ Acknowledgements

Thanks to the open-source community behind pandas, numpy, scipy, statsmodels, and jupyter. This book stands on your shoulders.

