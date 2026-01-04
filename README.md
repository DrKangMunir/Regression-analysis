# Regression Analysis – GDT500 (Group 4)

![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)
![R ≥ 4.0](https://img.shields.io/badge/R-≥%204.0-blue.svg)
![Quarto ≥ 1.4](https://img.shields.io/badge/Quarto-≥%201.4-orange.svg)

Reproducible multiple **logistic** and multiple **linear** regression analyses using simulated public health data for the GDT500 Multivariable Analysis course (DrPH, Universiti Sains Malaysia).

---

## 📑 Table of Contents


- [Overview](#overview)
- [Contributors](#contributors)
- [Folder Structure](#folder-structure)
- [Published Reports](#published-reports)
- [Installation](#installation)
- [Usage](#usage)
- [Data](#data)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

---

## 📘 Overview

- Examines how work-related and lifestyle factors relate to **quality of life (continuous)** and **depression (binary)** outcomes using multiple linear and multiple logistic regression on simulated data.  
- Uses **R**, **Quarto**, and **tidyverse-based workflows** to demonstrate data simulation, EDA, model building, interaction terms, diagnostics, and interpretation.  
- Status: Stable teaching example for the GDT500 Regression Analysis group assignment (Group 4).

---

## 👥 Contributors
- DR. NAZIRUL MUNIR BIN ABU HASSAN (23202537)
- DR. NURFARIHAH ZULKIFLI (23202679)
- DR. KHAIRUNNISA BINTI ARIFFIN (23202532)
- DR. SANGGARY MARIMUTHU (23202894)

---

## 📂 Folder Structure

Layout within this repository:

- `Multiple-Linear-Regression/` – multiple linear regression (MLR) component  
  - `Group4_MLR.qmd`  – MLR analysis document  
  - `Group4_MLR.html` – rendered HTML report for MLR  
  - `data/` – simulated QoL dataset and generation script  
    - `simulated_qol_data.csv`  
    - `data_generation_qol.R`  

- `Multiple-Logistic-Regression/` – multiple logistic regression (MLogR) component  
  - `Group4_MLogR.qmd`  – MLogR analysis document  
  - `Group4_MLogR.html` – rendered HTML report for MLogR  
  - `data/` – simulated depression dataset and generation script  
    - `simulated_depression_data.csv`  
    - `data_generation_depression.R`  

- `README.md` – this overview file  

---

## 📄 Published Analysis in Posit-Connect
- [Linear Regression Analysis](https://posit-connect.kk.usm.my/content/2987b23e-f1f1-47ef-a116-90260349bf05)  
- [Logistic Regression Analysis](https://posit-connect.kk.usm.my/content/6f3c7710-f751-495d-baf4-80ec79ab0cc1](https://posit-connect.kk.usm.my/content/b9144dca-f26c-4d55-91ca-6085d73494db))  

---

## ⚙️ Installation

### Prerequisites

- R (≥ 4.0.0) and RStudio (recommended)  
- Quarto or R Markdown  
- Required R packages:  
  `tidyverse`, `dplyr`, `tibble`, `modelr`,  
  `ggplot2`, `GGally`, `patchwork`, `corrplot`,  
  `broom`, `broom.helpers`, `performance`, `car`, `lmtest`, `mfp`,  
  `gtsummary`, `gt`, `knitr`,  
  `summarytools`, `labelled`, `DT`,  
  `caret`, `ResourceSelection`, `pROC`  

### Setup

```bash
git clone https://github.com/DrKangMunir/regression-analysis-assignment.git
cd regression-analysis-assignment
```

Then in R:

```r
install.packages(c(
  "tidyverse", "dplyr", "tibble", "modelr",
  "ggplot2", "GGally", "patchwork", "corrplot",
  "broom", "broom.helpers", "performance", "car", "lmtest", "mfp",
  "gtsummary", "gt", "knitr",
  "summarytools", "labelled", "DT",
  "caret", "ResourceSelection", "pROC"
))
```

---

## ▶️ Usage

### 1. Multiple Logistic Regression (Part 1)

From the repository root:

```bash
cd Multiple-Logistic-Regression

# Quarto
quarto render Group4_MLogR.qmd

```

This generates `Group4_MLogR.html` with the simulated depression dataset, EDA, multiple logistic regression models, diagnostics, and interpretation.

### 2. Multiple Linear Regression (Part 2)

```bash
cd Multiple-Linear-Regression

# Quarto
quarto render Group4_MLR.qmd

```

This generates `Group4_MLR.html` with the simulated QoL dataset, EDA, multiple linear regression models, diagnostics, and interpretation.

---

## 📊 Data

All datasets are **fully simulated** for educational purposes and contain no real participant data.

### Multiple Logistic Regression

- Source: `Multiple-Logistic-Regression/data/simulated_depression_data.csv`  
- Variables (example):  
  - `depression` – binary outcome  
  - `years_working` – continuous predictor  
  - `phys_activity` – categorical physical activity level  
  - `obesity` – binary obesity status  
- Generated with fixed random seeds (`set.seed()`) in `data_generation_depression.R` or in Part A of the analysis document.

### Multiple Linear Regression

- Source: `Multiple-Linear-Regression/data/simulated_qol_data.csv`  
- Variables (example):  
  - `qol` – continuous quality of life score  
  - `years_working`, `phys_activity`, `obesity`, plus interaction terms where specified  
- Generated with fixed seeds in `data_generation_qol.R` or in Part A of the MLR analysis document.

A more detailed data dictionary can be included in each HTML report or a separate markdown file if required.

---

## 📈 Results

- **Logistic regression:** Odds ratios, ROC curves, diagnostics, and interpretation in `Group4_MLogR.html`.  
- **Linear regression:** Coefficient estimates, assumption checks, diagnostics, and interpretation in `Group4_MLR.html`.  

Key learning outcomes:

- Demonstrates reproducible regression workflows in R.  
- Shows how to specify, fit, and interpret multiple regression models using simulated public health data.

---

## 🤝 Contributing

This repository is part of a course assignment; external contributions are not accepted.  

For corrections or suggestions, please contact the group members or instructor with the relevant file name and section.

---

## 📄 License

This project is licensed under the **MIT License**.  
See the top-level `LICENSE` file for full details.
