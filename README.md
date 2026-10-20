# Precipitation Regionalization and Projections Across U.S. Climate Regimes Using a Wavelet-Machine Learning Framework

This repository contains the official Python implementation for the manuscript:
> **Nourani, V., Dindar, A., Bejani, M., & Gebremichael, M.** (2026). *"Precipitation Regionalization and Projections Across U.S. Climate Regimes Using a Wavelet-Machine Learning Framework"*.

---

## 📂 Repository Structure

```text
├── Sample Date/
│   ├── historical Inputs/   # Historical GCM realization inputs (CMIP6)
│   ├── observation/         # Observational reference data & PRISM targets
│   └── ssp inputs/          # Future scenario inputs (SSP2-4.5 and SSP5-8.5)
├── Deep Model.ipynb         # Model training, validation, and ensemble architecture
├── Predictor-screening.ipynb# Mutual Information (MI) predictor screening
├── SSP Projections.ipynb    # Near-term revalidation & far-future projections (2025–2100)
└── wavelet_denoising.ipynb  # Discrete Wavelet Transform (DWT) signal preprocessing
