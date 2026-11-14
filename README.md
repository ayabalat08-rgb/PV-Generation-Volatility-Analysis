## Roadmap

- [x] Clean and aggregate multi-inverter SCADA data (Plant 2), masking timestamps where inverters stop reporting
- [x] Compute 15-minute power ramp rates (kW/min) and daytime statistics
- [ ] Add weather covariates (irradiance, temperature) to link ramps to atmospheric conditions
- [ ] Define extreme ramp events formally (e.g. top 5% of irradiance ramps) and study their duration and frequency
- [ ] Repeat the analysis on a second plant and compare ramp distributions
- [ ] Add `requirements.txt` and a short data-quality report
