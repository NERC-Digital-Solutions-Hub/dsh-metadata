# Supporting information Hydrochemical and nitrate sensor data between May 2016 and Oct 2017 for three sites in a karst catchment in SW China: Chenqi, Laoheitan, Maoshuikeng in the Houzhai Catchment

- Study area and sensors
  - Location: Houzhai Karst Catchment, SW China; three sites: Chenqi (CHQ), Laoheitan (LHT), Maoshuikeng (MSK).
  - Sensors: IN-situ Aqua TROLL600 measuring Temperature, Specific Conductivity, pH, and Dissolved Oxygen; Hach nitrate-N sensors (NISE) with SC200 controller for nitrate-N.
  - Monitoring period: May 2016 to Oct 2017 (dates summarized per site); precise coordinates provided for each site.
  - Data collection interval: 15 minutes.

- Sensor calibration and validation
  - Nitrate calibration: weekly/biweekly manual water samples analyzed in-lab (SKALAR Sans Plus) for NO3-N; linear regression used to relate sensor estimates to lab measurements.
  - Calibration approach: compared short-interval (time-period) calibration vs one single calibration for the full period.
  - Final data product: time-interval (short-term) calibration data used as final NO3-N values for each site; shorter calibrations yielded lower uncertainty.
  - Uncertainty: table of calibration uncertainties shows substantially lower values with short-interval calibration compared to a single calibration.

- Data quality and missing data
  - Missing data check: blank cells indicate missing values due to power/instrument/fieldwork issues.
  - Missing data percentages by site and parameter:
    - Chenqi: Temperature 0.41%, EC 0.42%, pH 0.57%, DO 7.5%, NO3-N 5.3%.
    - Laoheitan: Temperature 7.6%, EC 7.6%, pH 7.6%, DO 7.6%, NO3-N 8.7%.
    - Maoshuikeng: Temperature 13%, EC 43%, pH 16%, DO 13%, NO3-N 1.5%.
  - Note: Maoshuikeng shows notably higher missing data for EC and pH.

- Dataset format and structure
  - Format: CSV file containing hydrochemical and nitrate sensor data for the three sites (May 2016–Oct 2017); accompanying Supporting Information in RTF.
  - Structure: 19 columns total
    - Time column: Date_time (yyyy-mm-dd hh:mm)
    - For each site (Chenqi, Laoheitan, Maoshuikeng): four hydrochemical columns (Temperature, Specific Conductivity, pH, Dissolved Oxygen Saturation) and two nitrate sensor columns (Calibrated nitrate-N sensor data mg/L; Calibrated Uncertainty mg/L)
    - Total: 1 time column + 18 site-specific data columns = 19 columns

- Related publication and data access notes
  - Publication: Yue, F.-J.; Waldron, S.; Li, S.-L.; Wang, Z.-J.; Zeng, J.; Xu, S.; Zhang, Z.-C.; Oliver, D.M. (2019). Land use interacts with changes in catchment hydrology to generate chronic nitrate pollution in karst waters and strong seasonality in excess nitrate export. Sci Total Environ 696, 134062.
  - Additional sites: Five sites are reported in the publication; for access to all sites, consider contacting the authors.
  - Data usability: calibrated nitrate-N data and associated metadata are suitable for examining nitrate dynamics, catchment hydrology, and karst water quality; analysis aligns with aims to identify correlations and inform understanding of nitrate pollution patterns.