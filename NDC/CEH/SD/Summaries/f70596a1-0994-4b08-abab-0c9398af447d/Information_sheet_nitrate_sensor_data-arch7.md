# Hydrochemical and nitrate sensor data between May 2016 and Oct 2017 for three sites in a karst catchment in SW China: Chenqi, Laoheitan, Maoshuikeng in the Houzhai Catchment

## Overview
- Provides hydrochemical and nitrate-N sensor data from three sites (Chenqi CHQ, Laoheitan LHT, Maoshuikeng MSK) in the Houzhai Karst Catchment, SW China.
- Data were collected May 2016 to Oct 2017 using in-situ hydrochemical sensors and nitrate sensors to support understanding of catchment hydrology and nitrate dynamics in karst systems.
- Source relates to a publication examining land-use interactions with catchment hydrology and chronic nitrate pollution with strong seasonality in nitrate export.

## Study Area and Sensors
- Study sites and coordinates:
  - Chenqi (CHQ): lat 26°15′37.28″, lon 105°46′17.74″
  - Laoheitan (LHT): lat 26°13′11.43″, lon 105°44′31.15″
  - Maoshuikeng (MSK): lat 26°16′04.68″, lon 105°41′36.98″
- Monitoring dates:
  - CHQ: 19 May 2016 – 31 Oct 2017
  - LHT: 18 May 2016 – 31 Oct 2017
  - MSK: 26 May 2016 – 31 Oct 2017
- Sensor types:
  - Hydrochemical: IN-situ Aqua TROLL 600 (temperature, specific conductivity, pH, dissolved oxygen)
  - Nitrate: Hach nitrate-N ion-selective electrodes (NISE) with SC200 controller
- Data interval: sensor readings at 15-minute intervals

## Sensor Calibration
- Hydrochemical sensors calibrated and operated per Troll 600 manual.
- Specific conductivity automatically temperature compensated.
- pH sensor calibrated monthly by trained operators following standard procedures.
- Calibration framework for nitrate-N based on lab measurements (NO3-N) and sensor estimates using linear regression.

## Nitrate Sensor Calibration Details
- Validation samples: weekly or biweekly discrete stream samples; autosamplers used during precipitation events (intervals 1–4 hours).
- Lab analysis: NO3-N measured with SKALAR Sans Plus; detection limit 10 μg/L.
- Calibration approach: relate sensor-estimated NO3-N to lab NO3-N via linear regression.
- Uncertainty assessment: compared short-interval calibration uncertainty with a single calibration over the whole period; shorter interval calibrations showed lower uncertainty.
- Final nitrate-N values used: time-interval calibrated data (as opposed to a single, period-wide calibration).

## Data Gaps and Quality
- Data completeness varies by site and parameter.
- Reported missing data percentages (Table 3):
  - Chenqi: T 0.41%, EC 0.42%, pH 0.57%, DO 7.5%, NO3-N 5.3%
  - Laoheitan: T 7.6%, EC 7.6%, pH 7.6%, DO 7.6%, NO3-N 8.7%
  - Maoshuikeng: T 13%, EC 43%, pH 16%, DO 13%, NO3-N 1.5%

## Format and Structure of the Dataset
- Data files: CSV format (Hydrochemical and nitrate sensor data for May 2016–Oct 2017 for CHQ, LHT, MSK).
- Supporting information: an accompanying RTf document provides methodological details.
- Dataset structure: 19 columns total, including one time column and three sites’ data:
  - Time column: Date_time (format: yyyy-mm-dd hh:mm)
  - Chenqi (CHQ) columns: Temperature (°C), Specific Conductivity (μS/cm), pH, Dissolved Oxygen (Saturation) (%), Calibrated nitrate-N sensor data (mg/L), Calibrated Uncertainty (mg/L)
  - Laoheitan (LHT) columns: Temperature (°C), Specific Conductivity (μS/cm), pH, Dissolved Oxygen (Saturation) (%), Calibrated nitrate-N sensor data (mg/L), Calibrated Uncertainty (mg/L)
  - Maoshuikeng (MSK) columns: Temperature (°C), Specific Conductivity (μS/cm), pH, Dissolved Oxygen (Saturation) (%), Calibrated nitrate-N sensor data (mg/L), Calibrated Uncertainty (mg/L)

## Dataset Contents and Availability
- Primary dataset: CSV file containing hydrochemical and nitrate sensor data for CHQ, LHT, and MSK from May 2016 to Oct 2017.
- Supporting information: accompanying RTf with calibration and data handling details.
- Publication reference: Yue, F.-J.; Waldron, S.; Li, S.-L.; Wang, Z.-J.; Zeng, J.; Xu, S.; Zhang, Z.-C.; Oliver, D.M. (2019). Land use interacts with changes in catchment hydrology to generate chronic nitrate pollution in karst waters and strong seasonality in excess nitrate export. Sci Total Environ 696, 134062. DOI: 10.1016/j.scitotenv.2019.134062.
- Note: The cited publication includes five sites; for full site coverage, contact the authors.