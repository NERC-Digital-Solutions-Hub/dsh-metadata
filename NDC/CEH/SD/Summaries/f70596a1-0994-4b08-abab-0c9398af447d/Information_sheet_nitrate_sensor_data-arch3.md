# Supporting information Hydrochemical and nitrate sensor data between May 2016 and Oct 2017 for three sites in a karst catchment in SW China: Chenqi, Laoheitan, Maoshuikeng in the Houzhai Catchment

## Study area and sensors
- Three sites in the Houzhai Catchment, Puding Karst Critical Zone Observatory, SW China: Chenqi (CHQ), Laoheitan (LHT), Maoshuikeng (MSK).
- Hydrological and chemical measurements using:
  - In-situ Aqua TROLL® 600 sensors for temperature, specific conductivity, pH, and dissolved oxygen (DO) saturation.
  - Nitrate-N sensors based on Hach nitrate ion-selective electrodes (NISE) with SC200 controller.
- Monitoring period: 19 May 2016 – 31 Oct 2017 (CHQ, LHT, MSK).

## Sensor calibration and measurement details
- Hydrochemical sensors:
  - Calibration/quality control aligned with the Troll 600 manual.
  - Specific conductivity automatically temperature-compensated.
  - pH sensor calibrated monthly by trained operators.
  - Data sampling interval set at 15 minutes.
- Nitrate sensors:
  - Weekly or biweekly discrete water samples collected for validation; additional samples during precipitation using autosamplers (1–4 hour intervals).
  - Samples filtered in the field and analyzed (NO3--N) within ~2 hours of collection using SKALAR Sans Plus automatic analyzer; detection limit ~10 μg/L.
  - Sensor NO3--N values calibrated against laboratory measurements using linear regression.

## Nitrate sensor calibration and uncertainty
- Calibration approach:
  - Statistical relationships established between sensor-estimated NO3--N and lab-measured NO3--N.
  - Shorter-interval calibration (time-window-based) found to reduce uncertainty compared with a single calibration for the entire period.
  - Uncertainty in the shorter-interval calibration generally lower; the final reported NO3--N values use the time-interval calibration results.
- Uncertainty:
  - Reported as Uncertainty (mg/L) for nitrate-N calibration at each site (per-site calibration details summarized in the attached table).

## Data gaps and quality
- Missing data checked and documented (blank cells indicate gaps).
- Possible causes: power failures, instrument malfunctions, fieldworker errors.
- Reported percentages of missed data by site and parameter:
  - Chenqi: T 0.41%, EC 0.42%, pH 0.57%, DO 7.5%, NO3--N 5.3%.
  - Laoheitan: T 7.6%, EC 7.6%, pH 7.6%, DO 7.6%, NO3--N 8.7%.
  - Maoshuikeng: T 13%, EC 43%, pH 16%, DO 13%, NO3--N 1.5%.

## Format and contents of the dataset
- Data format: CSV file containing hydrochemical and nitrate sensor data for the three sites (May 2016 – Oct 2017).
- File name reference: “Hydrochemical and nitrate sensor data … Houzhai Catchment” (with supporting information in an accompanying RTf file).
- Dataset structure:
  - 19 columns total, including:
    - Date_time (timestamp in yyyy-mm-dd hh:mm).
    - CHQ: Temperature (°C), Specific Conductivity (μS/cm), pH, Dissolved Oxygen Saturation (%), Calibrated nitrate-N sensor data (mg/L), Calibrated Uncertainty (mg/L).
    - LHT: Temperature (°C), Specific Conductivity (μS/cm), pH, Dissolved Oxygen Saturation (%), Calibrated nitrate-N sensor data (mg/L), Calibrated Uncertainty (mg/L).
    - MSK: Temperature (°C), Specific Conductivity (μS/cm), pH, Dissolved Oxygen Saturation (%), Calibrated nitrate-N sensor data (mg/L), Calibrated Uncertainty (mg/L).
  - Each site includes corresponding per-site measurements and nitrate sensor data with associated uncertainty.
- Data provenance:
  - The dataset supports the study published in Yue et al. 2019 (Sci Total Environ 696, 134062), which examines land-use interactions with catchment hydrology and nitrate pollution in karst waters, including strong seasonality in nitrate export.
  - The publication notes five sites in total; for complete site coverage, contact the authors.

## Publication context
- Yue, F.-J.; Waldron, S.; Li, S.-L.; Wang, Z.-J.; Zeng, J.; Xu, S.; Zhang, Z.-C.; Oliver, D.M. 2019. Land use interacts with changes in catchment hydrology to generate chronic nitrate pollution in karst waters and strong seasonality in excess nitrate export. Science of The Total Environment, 696, 134062. DOI: https://doi.org/10.1016/j.scitotenv.2019.134062.
- The supplementary information provides dataset details, calibration procedures, data quality assessments, and the data structure used in the publication.