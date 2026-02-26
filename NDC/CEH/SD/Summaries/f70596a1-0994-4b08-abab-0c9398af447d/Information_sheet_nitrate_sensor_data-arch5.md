# Hydrochemical and nitrate sensor data between May 2016 and Oct 2017 for three sites in a karst catchment in SW China: Chenqi, Laoheitan, Maoshuikeng in the Houzhai Catchment

## Summary
- Dataset of hydrochemical and nitrate sensor measurements from three sites (Chenqi CHQ, Laoheitan LHT, Maoshuikeng MSK) in the Houzhai Karst Catchment, SW China, May 2016–Oct 2017.
- Sensor suite: Aqua TROLL 600 for hydrochemistry (temperature, specific conductivity, pH, dissolved oxygen) and Hach nitrate-N sensors with SC200 controller.
- Data interval: 15 minutes; pH calibrated monthly; conductivity automatically temperature compensated.
- Nitrate calibration: weekly/biweekly field samples plus autosampler samples during precipitation; lab analysis with SKALAR Sans Plus; calibration using site-specific linear regression between sensor estimates and lab measurements; time-interval calibrations preferred over a single full-period calibration.
- Data quality: documented uncertainty for nitrate sensor calibrations; missing data accounted for and reported by parameter/site.
- Data format: CSV dataset (19 columns) plus supporting information (RTF); includes time, site-specific hydrochemistry, and calibrated nitrate-N data with uncertainty.
- Related publication: Yue et al. 2019, Sci Total Environ; five sites in study; contact authors for data beyond the three sites.

## Study Area and Sensors
- Location: Houzhai Catchment, Karst Critical Zone Observatory, SW China.
- Sites: Chenqi (CHQ), Laoheitan (LHT), Maoshuikeng (MSK).
- Monitoring period: 19 May 2016 – 31 Oct 2017 (Chenqi and Laoheitan); 26 May 2016 – 31 Oct 2017 (Maoshuikeng).
- Instruments:
  - Hydrochemical: Aqua TROLL 600 (temperature, specific conductivity, pH, DO).
  - Nitrate: Hach nitrate-N sensors with SC200 controller.
- Data interval: 15-minute sampling for all measurements.

## Calibration, Quality Assurance, and Uncertainty
- Hydrochemical calibration:
  - Specific conductivity automatically temperature compensated.
  - pH calibrated monthly by trained operators following SOPs.
- Nitrate sensor calibration:
  - Field validation with discrete water samples weekly/biweekly; additional samples during precipitation (autosamplers every 1–4 hours).
  - Lab analysis of NO3-N using SKALAR Sans Plus; detection limit ~10 μg/L NO3-N.
  - Calibration via linear regression between sensor-estimated NO3-N and lab-measured NO3-N.
  - Assessment compared shorter-term calibration vs. one full-period calibration; shorter-term calibrations yielded lower uncertainty.
  - Final data use time-interval calibrated nitrate-N values with associated uncertainty.
- Uncertainty reporting:
  - Each site’s nitrate-N data include Calibrated_Uncertainty_mg/L.
- Data gaps:
  - Missing data attributed to power/instrument/fieldworker issues; percentages vary by site/parameter (e.g., Maoshuikeng EC shows notably higher missingness).

## Data Format and Structure
- Format: CSV data file plus supporting information (RTF).
- Columns: 19 total, including:
  - Time column (Date_time, in yyyy-mm-dd hh:mm, 24h clock).
  - For each site: Temperature (°C), Specific Conductivity (μS/cm), pH, Dissolved Oxygen Saturation (%), Calibrated_nitrate-N_sensor_data_mg/L, Calibrated_Uncertainty_mg/L.
- Coverage: May 2016–Oct 2017 across three karst sites.

## Data Access and Publication
- Publication: Yue et al., 2019, Sci Total Environ, "Land use interacts with changes in catchment hydrology to generate chronic nitrate pollution in karst waters and strong seasonality in excess nitrate export."
- Availability: Dataset corresponds to three of five sites reported; for all sites, contact authors.
- Reuse notes: Data suitable for analyses of nitrate pollution dynamics, land-use impacts, and catchment hydrology; calibration strategy and uncertainties documented to support reproducibility.

## Governance, Stewardship Considerations
- Metadata and provenance:
  - Calibration procedures, QA procedures, and data processing steps are documented (including time-interval calibration rationale).
  - Sensor specifications and measurement intervals clearly stated.
- Data quality and updates:
  - Missing data quantified by site/parameter; user should account for gaps in analyses.
  - Time-interval calibration preferred; future updates should maintain calibration history and versioning.
- Accessibility and sharing:
  - Raw and calibrated data are provided with uncertainty estimates; related RTf file provides additional context.
  - If broader site coverage is needed, contact authors (publication notes indicate five-site scope).
- Compliance and governance:
  - Follow standard data management practices for environmental sensor data: maintain calibration logs, version datasets, document changes, and provide clear lineage for data-derived values (e.g., calibrated NO3-N).