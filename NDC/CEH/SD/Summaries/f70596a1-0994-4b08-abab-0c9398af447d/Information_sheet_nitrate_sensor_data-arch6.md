# Supporting information Hydrochemical and nitrate sensor data between May 2016 and Oct 2017 for three sites in a karst catchment in SW China: Chenqi, Laoheitan, Maoshuikeng in the Houzhai Catchment

## Overview
- Dataset covers hydrochemical and nitrate sensor observations from May 2016 to Oct 2017 at three sites: Chenqi (CHQ), Laoheitan (LHT), and Maoshuikeng (MSK) in the Houzhai Catchment, SW China.
- Instruments include in-situ Aqua TROLL 600 sensors (temperature, specific conductivity, pH, dissolved oxygen saturation) and nitrate-N sensors (Hach NISE) with SC200 controller.
- Nitrate data are calibrated against laboratory measurements to produce calibrated nitrate-N values and associated uncertainties.

## Sites and sensors
- Chenqi (CHQ): coordinates 26°15′37.2816″ N, 105°46′17.742″ E; monitoring 19 May 2016 – 31 Oct 2017.
- Laoheitan (LHT): coordinates 26°13′11.427″ N, 105°44′31.149″ E; monitoring 18 May 2016 – 31 Oct 2017.
- Maoshuikeng (MSK): coordinates 26°16′4.6806″ N, 105°41′36.9816″ E; monitoring 26 May 2016 – 31 Oct 2017.
- Each site collected: temperature (°C), specific conductivity (μS/cm), pH, dissolved oxygen saturation (%), calibrated nitrate-N (mg/L), and nitrate-N calibration uncertainty (mg/L).

## Data collection and calibration
- Sensors operated at 15-minute intervals.
- Hydrochemical measurements: temperature automatically temperature-compensated for EC; pH Sondes calibrated monthly by trained operators following SOPs.
- Nitrate calibration: discrete water samples collected weekly or biweekly; autosamplers used during precipitation events (sampling every 1–4 hours). Lab analyses performed with SKALAR Sans Plus; detection limit for NO3-N = 10 μg/L.
- Calibration approach: linear regression between sensor-estimated NO3-N and laboratory NO3-N. Compared two calibration strategies:
  - Short time-interval calibration
  - One calibration for the entire monitoring period
  - Short-interval calibrations showed lower uncertainty and were used to generate final NO3-N values (per site).

## Data format and structure
- Format: CSV file containing hydrochemical and nitrate sensor data for the three sites.
- Supporting information: accompanying .rtf file with methodological details.
- Columns (19 total) include:
  - Date_time (yyyy-mm-dd hh:mm)
  - Chenqi_Temperature_degC
  - Chenqi_Specific_Conductivity_microS_per_cm
  - Chenqi_pH
  - Chenqi_Dissolved_Oxygen_(Saturation)_% 
  - Chenqi_Calibrated_nitrate-N_sensor_data_mg/L
  - Chenqi_Calibrated_Uncertainty_mg/L
  - Laoheitan_Temperature_degC
  - Laoheitan_Specific_Conductivity_microS_per_cm
  - Laoheitan_pH
  - Laoheitan_Dissolved_Oxygen_(Saturation)_% 
  - Laoheitan_Calibrated_nitrate-N_sensor_data_mg/L
  - Laoheitan_Calibrated_Uncertainty_mg/L
  - Maoshuikeng_Temperature_degC
  - Maoshuikeng_Specific_Conductivity_microS_per_cm
  - Maoshuikeng_pH
  - Maoshuikeng_Dissolved_Oxygen_(Saturation)_% 
  - Maoshuikeng_Calibrated_nitrate-N_sensor_data_mg/L
  - Maoshuikeng_Calibrated_Uncertainty_mg/L

## Missing data
- Data completeness varies by variable and site (percent missing during monitoring period):
  - Chenqi: Temperature 0.41%, Specific Conductivity 0.42%, pH 0.57%, Dissolved Oxygen 7.5%, NO3-N 5.3%
  - Laoheitan: Temperature 7.6%, Specific Conductivity 7.6%, pH 7.6%, Dissolved Oxygen 7.6%, NO3-N 8.7%
  - Maoshuikeng: Temperature 13%, Specific Conductivity 43%, pH 16%, Dissolved Oxygen 13%, NO3-N 1.5%
- Noted higher missing data for Maoshuikeng EC (specific conductivity) compared to other variables/sites.

## Data access and publication
- Data format: CSV file for hydrochemical and nitrate sensor data; accompanying supporting information in an .rtf file.
- Publication reference: Yue, F.-J.; Waldron, S.; Li, S.-L.; Wang, Z.-J.; Zeng, J.; Xu, S.; Zhang, Z.-C.; Oliver, D.M., 2019. Land use interacts with changes in catchment hydrology to generate chronic nitrate pollution in karst waters and strong seasonality in excess nitrate export. Science of The Total Environment, 696, 134062. DOI: 10.1016/j.scitotenv.2019.134062.
- Note: The publication covers five sites; for other sites of interest, contact the authors.

## Data use and context
- The dataset supports analyses of how hydrochemical variables and nitrate concentrations respond to catchment processes in karst systems.
- Calibration approach and data quality considerations (e.g., time-interval calibration and missing data) are documented to aid data cleaning and interpretation for broader reuse.