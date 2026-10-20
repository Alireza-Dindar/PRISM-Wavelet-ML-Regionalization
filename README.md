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

All scripts utilize portable relative paths pointing to the ./Sample Date/ directory.

Target Stations
To run the notebooks for a specific climate region, simply initialize or modify the station parameter in the code to your desired code:

sf — San Francisco, California (Temperate / C)

ph — Phoenix, Arizona (Arid / B)

ch — Chicago, Illinois (Continental/Cold / D)

mi — Miami, Florida (Tropical / A)

Execution Flow
Clone or download this repository and launch Jupyter Notebook from the root folder.

Run the scripts in the following logical sequence:

Step 1: Run Predictor-screening.ipynb to select optimal CMIP6 realizations using Mutual Information.

Step 2: Run wavelet_denoising.ipynb to decompose and smooth inputs using DWT hard thresholding.

Step 3: Run Deep Model.ipynb to train and validate shallow ML models (FFNN, SVR, ANFIS), the BPNN Ensemble, and the LSTM benchmark.

Step 4: Run SSP Projections.ipynb to execute the 2015–2024 revalidation and generate far-future projections through 2100.

🛠️ Requirements & Dependencies
The workflows require standard Python libraries:

numpy, pandas, scikit-learn, scipy, PyWavelets, tensorflow / keras, matplotlib, seaborn

📄 License & Citation
Open-source under the MIT License. If you utilize this code, please cite the accompanying manuscript.
