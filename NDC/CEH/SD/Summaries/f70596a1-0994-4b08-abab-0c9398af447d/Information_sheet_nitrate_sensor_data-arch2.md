# Supporting information Hydrochemical and nitrate sensor data between May 2016 and Oct 2017 for three sites in a karst catchment in SW China: Chenqi, Laoheitan, Maoshuikeng in the Houzhai Catchment.

## Overview
- This Supporting Information accompanies Yue et al. 2019 and describes hydrochemical and nitrate sensor datasets from three karst catchment sites in SW China (May 2016–Oct 2017): Chenqi (CHQ), Laoheitan (LHT), Maoshuikeng (MSK) in the Houzhai Catchment, Puding Karst Critical Zone Observatory.
- Documents instrumentation, calibration, data quality, and data structure used in the study of nitrate pollution and catchment hydrology.

## Study sites and sensors
- Sites: Chenqi (CHQ), Laoheitan (LHT), Maoshuikeng (MSK).
- Monitoring dates: CHQ 19 May 2016–31 Oct 2017; LHT 18 May 2016–31 Oct 2017; MSK 26 May 2016–31 Oct 2017.
- Instruments:
  - Hydrochemical: IN-situ Aqua TROLL 600 with Temperature, Specific Conductivity, pH, Dissolved Oxygen (saturation) sensors.
  - Nitrate: Hach nitrate-N sensor (NISE) with SC200 controller.
- Location and study area: Houzhai Catchment, Southwestern China (Puding Karst CZO).

## Sensor and nitrate calibration
- Hydrochemical calibration:
  - Procedures follow Troll 600 manual.
  - Specific conductivity automatically temperature compensated.
  - pH sensor calibrated monthly by trained operators.
  - Data collection interval: 15 minutes.
- Nitrate calibration:
  - Discrete water samples collected weekly or biweekly for validation; autosamplers during precipitation events (sampling intervals 1–4 hours).
  - Samples filtered on return, refrigerated, analyzed within ~12 hours.
  - Lab NO3--N measured with SKALAR Sans Plus; detection limit 10 μg/L.
  - Calibration: linear regression between sensor NO3--N and lab NO3--N.
  - Compared two approaches for calibration uncertainty: shorter monitoring-period calibration vs one calibration for the whole period; shorter-period calibration yielded lower uncertainty.
  - Final NO3--N values used are time-interval calibrated data.

## Data quality and missing data
- Data checked for missing values; gaps due to power/instrument failure or fieldworker error.
- Missing data percentages (approximate):
  - Chenqi: Temperature 0.41%, EC 0.42%, pH 0.57%, DO 7.5%, NO3--N 5.3%.
  - Laoheitan: Temperature 7.6%, EC 7.6%, pH 7.6%, DO 7.6%, NO3--N 8.7%.
  - Maoshuikeng: Temperature 13%, EC 43%, pH 16%, DO 13%, NO3--N 1.5%.

## Dataset format and structure
- Data formats:
  - Hydrochemical and nitrate sensor data (May 2016–Oct 2017) for the three sites are provided as CSV files.
  - Supporting information also available in an RTF document.
- Data content:
  - 19 columns per dataset, including a time column and site-specific hydrochemical and nitrate sensor data (calibrated values and calibration uncertainty).

## Data structure details
- The CSV files contain columns for:
  - Date_time (yyyy-mm-dd hh:mm)
  - Chenqi: Temperature, Specific Conductivity, pH, Dissolved Oxygen (Saturation), Calibrated nitrate-N, Calibrated Uncertainty
  - Laoheitan: Temperature, Specific Conductivity, pH, Dissolved Oxygen (Saturation), Calibrated nitrate-N, Calibrated Uncertainty
  - Maoshuikeng: Temperature, Specific Conductivity, pH, Dissolved Oxygen (Saturation), Calibrated nitrate-N, Calibrated Uncertainty

## Publication context and related work
- Publication: Yue, F.-J., Waldron, S., Li, S.-L., et al., 2019. Land use interacts with changes in catchment hydrology to generate chronic nitrate pollution in karst waters and strong seasonality in excess nitrate export. Science of the Total Environment, 696, 134062.
- Note: Five sites are discussed in the publication; for information on all sites, contact the authors.
- Relevance: The dataset supports analysis of nitrate pollution linked to land use and hydrology in karst systems, with attention to seasonality and long-term trends.