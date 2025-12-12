# Modeling the Socio-Economic Impact of AI & Automation — Code Implementation

This repository contains the computational implementation of the research project **“Modeling the Impact of AI and Automation on Companies and Workforce using Fractional‑Order Dynamics.”** It provides the full set of numerical and machine‑learning tools used to analyze how automation influences companies, employees, layoffs, and entrepreneurship through time‑dependent, memory‑driven dynamics.

At the heart of this work is a fractional‑order mathematical model that captures the realistic inertia of socio‑economic systems—where past workforce patterns, innovation shocks, and organizational behaviors continue to influence future outcomes. To bring these ideas to life, this repository includes four core components.

---

## Repository Components

### 1. MATLAB — Fractional RK‑2 Scheme

A complete MATLAB implementation of the generalized fractional Runge–Kutta (RK‑2) method used to numerically solve the Caputo–Fabrizio fractional‑order system. It simulates the evolution of automation–company–employee–entrepreneurship dynamics under memory effects.

**Files:** `MATLAB CODE RK-2 (With Memory)/`, `MATLAB CODE RK-2 (Without Memory)/`

---

### 2. Python — PINNs for Parameter Estimation

A Physics‑Informed Neural Network (PINN) that learns model parameters directly from real or synthetic data while enforcing the underlying fractional differential equations. The PINN captures hidden socio‑economic behavior with physically consistent constraints and produces interpretable results.

**Files:** `Python Code for PINNs & Layoff Forecasting/train_pinn.py`, `Python Code for PINNs & Layoff Forecasting/utils.py`

---

### 3. Python — Layoff Forecasting Pipeline

A forecasting module built on top of PINN outputs. It uses a neural time‑series model to predict layoff trends (short‑term and long‑term) and reflect technological disruption patterns such as recession shocks and automation waves.

**Files:** `Python Code for PINNs & Layoff Forecasting/forecast.py`, `Python Code for PINNs & Layoff Forecasting/models/`

---

### 4. Python — Convergence Analysis

Code that tests the stability and convergence of the fractional‑order model as the system approaches equilibrium (TCEE or TCE). This reproduces the stability behaviors derived in the theoretical analysis.

**Files:** `Python Code for Convergence (TCE)/`, `Python Code for Convergence (TCEE)/`

---

### 5. Python — Heatmap Generation

Scripts to generate heatmaps for sensitivity insights, parameter interactions, and dynamic transitions in the system. These visualizations highlight how automation, reskilling, company activity, and entrepreneurship influence each other over time.

**Files:** `Heatmap Generation Scripts/`, `images/` (recommended storage for plots)

---

## 🧰 Purpose of the Repository

This repository is intended for:

* Researchers exploring fractional‑order modeling
* Students studying automation‑driven socio‑economic dynamics
* Engineers working with PINNs or hybrid physics–ML systems
* Anyone analyzing technology‑induced labor transitions

It provides ready‑to‑use numerical code, allowing users to experiment with fractional dynamics, PINNs, forecasting models, and parameter effects without needing the full research manuscript.

---

## 🖼️ Visuals & Examples


```
![Model Architecture](Graphs/Convergence/Convergence_1.png)
![Fractional vs Classical Dynamics](images/dynamics_compare.png)
![PINN Loss Convergence](images/pinn_loss.png)
![Layoff Forecast Output](images/forecast_layoffs.png)
![Parameter Sensitivity Heatmaps](images/heatmap_sensitivity.png)
```

---

## 📁 Repository Structure (Suggested)

```plaintext
/
├─ MATLAB CODE RK-2 (With Memory)/
├─ MATLAB CODE RK-2 (Without Memory)/
├─ Python Code for PINNs & Layoff Forecasting/
│  ├─ train_pinn.py
│  ├─ forecast.py
│  └─ models/
├─ Python Code for Convergence (TCE)/
├─ Python Code for Convergence (TCEE)/
├─ Heatmap Generation Scripts/
├─ images/
└─ README.md
```

---

## ⚙️ Installation

Clone the repo and set up the Python environment:

```bash
git clone https://github.com/HarshitPranjal/Modeling-the-Impact-of-AI-and-Automation-on-Companies-and-Workforce-using-Fractional-Order-Dynamics.git
cd Modeling-the-Impact-of-AI-and-Automation-on-Companies-and-Workforce-using-Fractional-Order-Dynamics
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

**MATLAB:** MATLAB R2022a or later (Symbolic Math Toolbox recommended).

---

## 🚀 Quick Start

### Run fractional dynamics (MATLAB)

```matlab
run('MATLAB CODE RK-2 (With Memory)/FractionalDynamics_WithMemory.m')
```

### Train PINN

```bash
cd "Python Code for PINNs & Layoff Forecasting"
python train_pinn.py --data data/input.csv --config configs/pinn_config.yaml
```

### Forecast layoffs

```bash
python forecast.py --model saved_model.pt --horizon 90
```

### Generate heatmaps

```bash
python heatmap_generator.py --results results/ --out images/heatmaps/
```

---

## 📊 Interpretation & Best Practices

* Validate PINN estimates against baseline statistical models (ARIMA, VAR) before claiming improvements.
* Document data provenance and pre‑processing steps — PINNs can learn garbage if data is noisy or biased.
* Run sensitivity analyses on fractional orders and reskilling parameters to show robustness.

---

## 🔧 Suggested Improvements

* Add example Jupyter notebooks with end‑to‑end demos.
* Provide small, synthetic datasets to help users reproduce results quickly.
* Add unit tests for numerical solvers and PINN loss terms.
* Include CI workflows to automate tests and formatting.

---

## 📜 License

MIT License

---

