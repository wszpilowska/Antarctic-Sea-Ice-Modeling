# Antarctic Sea Ice Extent Modeling (1978-2009)
Spatio-temporal modeling of Antarctic sea ice extent using Fourier Series and Random Forest

![Antarctic Ice Edge Dynamics](ice_edge_dynamics.gif)

## Project Overview
This project presents a spatio-temporal analysis of the daily sea ice edge around Antarctica. Using a historical dataset spanning over 30 years, I developed models to approximate the ice extent function and visualize its annual pulsation.

## Methodology
The analysis utilizes two distinct modeling approaches:
1. **Harmonic Analysis (Fourier Series):** A smooth mathematical approximation using 5 harmonics to capture the core seasonal cycle for 360 individual longitudes.
2. **Machine Learning (Random Forest):** A non-linear regression model (`RandomForestRegressor`) trained to predict ice latitude based on time and geographical position.

## Key Results & Performance
The models demonstrate high precision in capturing the complex dynamics of the Southern Ocean:

* **Random Forest Model:**
    * **$R^2$ Score:** `0.9962` (Explains over 99.6% of data variance).
    * **Mean Absolute Error (MAE):** `0.12°` (~13 km), showing exceptional predictive accuracy.
* **Fourier Series Model:**
    * **MAE:** `0.95°` (~105 km), providing a robust, noise-resistant seasonal trend.
* **Phase Shift Correction:**
    * Identified and corrected a temporal anomaly in historical satellite sampling. The final model shows a negligible phase shift of only **-1.17 days**, confirming perfect synchronization with the natural seasonal cycle.

## Visualization Note
The header animation shows a **3-year representative sample** (1095 days) of the modeled vs. observed ice edge. This subset was selected to ensure high performance and accessibility of the repository while perfectly demonstrating the model's seasonal accuracy.

## Tech Stack
* **Python** (Pandas, NumPy, Scikit-Learn)
* **SciPy** (Optimization & Signal Processing)
* **Matplotlib** (Dynamic visualization via `FuncAnimation`)

## Repository Contents
* `Antarctic_Ice_Analysis.ipynb` - Main analysis and model training.
* `daily_ice_edge.zip` - Compressed historical dataset (CSV).
* `ice_edge_dynamics.gif` - 3-year visualization of ice movement.
