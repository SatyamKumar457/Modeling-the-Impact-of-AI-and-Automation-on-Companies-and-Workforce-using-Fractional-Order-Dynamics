Modeling the Socio-Economic Impact of AI & Automation — Code Implementation
This repository contains the computational implementation of the research project “Modeling the Impact of AI and Automation on Companies and Workforce using Fractional-Order Dynamics.”It provides the full set of numerical and machine-learning tools used to analyze how automation influences companies, employees, layoffs, and entrepreneurship through time-dependent, memory-driven dynamics.
At the heart of this work is a fractional-order mathematical model that captures the realistic inertia of socio-economic systems—where past workforce patterns, innovation shocks, and organizational behaviors continue to influence future outcomes. To bring these ideas to life, this repository includes four core components:

Repository Components
MATLAB – Fractional RK-2 Scheme
A complete MATLAB implementation of the generalized fractional Runge–Kutta (RK-2) method used to numerically solve the Caputo–Fabrizio fractional-order system.
It simulates the evolution of the automation-company-employee-entrepreneurship dynamics under memory effects.
Python – PINNs for Parameter Estimation
A Physics-Informed Neural Network (PINN) that learns model parameters directly from real or synthetic data while enforcing the underlying fractional differential equations.
The PINN captures hidden socio-economic behavior with physically consistent constraints and produces interpretable results.
Python – Layoff Forecasting Pipeline
A forecasting module built on top of the PINN outputs.
It uses a neural time-series model to predict layoff trends (short-term and long-term) and reflect technological disruption patterns such as recession shocks and automation waves.
Python – Convergence Analysis
Code that tests the stability and convergence of the fractional-order model as the system approaches equilibrium (TCEE or TCE).
This reproduces the stability behaviors derived in the theoretical analysis.
Python – Heatmap Generation
Scripts to generate heatmaps for sensitivity insights, parameter interactions, and dynamic transitions in the system.
These visualizations highlight how automation, reskilling, company activity, and entrepreneurship influence each other over time.
Purpose of the Repository
This repository is intended for:
Researchers exploring fractional-order modeling
Students studying automation-driven socio-economic dynamics
Engineers working with PINNs or hybrid physics–ML systems
Anyone analyzing technology-induced labor transitions
It provides ready-to-use numerical code, allowing users to experiment with fractional dynamics, PINNs, forecasting models, and parameter effects without needing the full research manuscript
