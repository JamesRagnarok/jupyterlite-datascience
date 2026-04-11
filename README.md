# qPCR Normalized Expression Analysis (JupyterLite Demo)

[![lite-badge](https://jupyterlite.rtfd.io/en/latest/_static/badge.svg)](https://jamesragnarok.github.io/jupyterlite-datascience/)

This repository demonstrates a complete workflow for analyzing qPCR data using Python—from raw Cq values to normalized gene expression, followed by statistical analysis using appropriate experimental designs.

The project is built with **JupyterLite** and deployed via **GitHub Pages**, allowing users to run the analysis entirely in a web browser without local installation.

👉 **Live Demo:**  
https://jamesragnarok.github.io/jupyterlite-datascience/

---

## 📌 Project Overview

Quantitative PCR (qPCR) generates Cq (quantification cycle) values that require normalization and statistical analysis to yield biologically meaningful conclusions.

This project demonstrates:

1. Conversion of **Cq values → ΔCq → ΔΔCq**
2. Calculation of **normalized expression (relative expression)**
3. Statistical analysis under two common experimental designs:
   - **CRD (Completely Randomized Design)** → One-way ANOVA  
   - **RCBD (Randomized Complete Block Design, batch as block)** → Two-way ANOVA (*without interaction term*)

---

## 🔬 Methodological Background

### qPCR Normalization

- ΔCq = Cq(target) − Cq(reference)
- ΔΔCq = ΔCq(sample) − ΔCq(control)
- Normalized expression = 2^(-ΔΔCq)

---

## 📊 Statistical Framework

### 1. CRD — One-Way ANOVA

Model:
Expression ~ Treatment

---

### 2. RCBD — Two-Way ANOVA (No Interaction)

Model:
Expression ~ Treatment + Batch

---

### 3. Multiple Comparisons

Post hoc tests are applied after ANOVA to identify significant differences between groups.

---

## 🚀 Features

- Fully browser-based (JupyterLite)
- End-to-end qPCR workflow
- Supports CRD and RCBD
- Interactive notebooks
- No installation required

---

## 🧭 How to Use

1. Open the demo
2. Run the notebook
3. Modify inputs as needed

---

## ⚙️ Technical Details

- Python (v3.11)
- pandas (v1.5.3), numpy, scipy, statsmodels, bioinfokit, scikit_posthocs
- JupyterLite

---

## 📜 References

[How to Perform ANOVA in Python](https://www.reneshbedre.com/blog/anova.html)
[CFX Maestro Software User Guide v2.3](https://www.bio-rad.com/sites/default/files/webroot/web/pdf/lsr/literature/10000126764.pdf)
