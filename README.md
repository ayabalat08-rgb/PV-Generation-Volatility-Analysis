# Solar PV Generation Volatility Analysis (Plant 2)

End-to-end data processing and volatility analysis pipeline for 15-minute SCADA telemetry from a utility-scale solar photovoltaic plant (22 inverters). 

This repository serves as a baseline exploratory data analysis (EDA) framework for investigating severe weather ramps, data integrity filtering, and power fluctuations in arid-region solar energy systems.

## 📊 Key Pipeline Steps
1. **Automated Ingestion & Resampling:** Automatically detects and loads plant generation data, parsing timestamps and enforcing a regular 15-minute time grid.
2. **Data Integrity Filtering:** Aggregates total plant AC power while strictly filtering out incomplete timestamps where not all 22 inverters reported (preventing artificial drop artifacts).
3. **Ramp Rate Quantification:** Computes absolute power changes ($kW/min$) and percentage ramps relative to rated plant capacity ($P_{99.9%}$).
4. **Daytime Volatility Metrics:** Isolates operational daytime generation, calculates peak surges and drops, and quantifies extreme ramping frequencies (e.g., drops $> 20\%$ of rated capacity within 15 minutes).
5. **Visualization:** Generates high-resolution dual-axis time-series plots tracking total AC power and corresponding ramp rates.

## 🛠️ Tech Stack
* **Python** (NumPy, Pandas, Matplotlib)
* **Data Source:** SCADA generation datasets (e.g., Plant 2 solar records)

## 🚀 Future Roadmap & Ph.D. Integration
* [x] **Phase 1:** Data cleaning, inverter-level aggregation, and ramp-rate volatility statistics.
* [ ] **Phase 2:** Integration of Split Conformal Prediction and Adaptive Conformal Inference (ACI) to track coverage gaps during extreme ramps.
* [ ] **Phase 3:** Extreme Value Theory (EVT) tail calibration for robust prediction intervals under sudden dust and cloud transients.
* [ ] **Phase 4:** Physics-informed bounds (clear-sky models and inverter capacity limits) and open-source Python package release.
