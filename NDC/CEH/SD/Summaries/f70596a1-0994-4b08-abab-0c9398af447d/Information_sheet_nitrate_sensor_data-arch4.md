# Hydrochemical and nitrate sensor data between May 2016 and Oct 2017 for three sites in a karst catchment in SW China: Chenqi, Laoheitan, Maoshuikeng in the Houzhai Catchment

- Purpose and scope
  - Provides hydrochemical and nitrate sensor data for three sites in the Houzhai Karst Catchment (Puding Karst Critical Zone Observatory), SW China.
  - Linked to a publication investigating how land use and catchment hydrology drive chronic nitrate pollution and seasonal nitrate export.

- Study sites and monitoring period
  - Chenqi (CHQ), Laoheitan (LHT), Maoshuikeng (MSK)
  - Coordinates:
    - CHQ: 26°15′37.28″ N, 105°46′17.74″ E
    - LHT: 26°13′11.43″ N, 105°44′31.15″ E
    - MSK: 26°16′04.68″ N, 105°41′36.98″ E
  - Monitoring dates: 19 May 2016 – 31 Oct 2017 (CHQ and LHT); 26 May 2016 – 31 Oct 2017 (MSK)

- Sensor platforms and measured variables
  - Hydrochemical sensors: In-situ Aqua TROLL 600 measuring Temperature, Specific Conductivity, pH, Dissolved Oxygen (saturation)
  - Nitrate sensors: Hach nitrate-N ion-selective electrodes (NISE) with SC200 controller
  - Data cadence: 15-minute intervals

- Sensor calibration and data processing
  - Hydrochemical sensors
    - pH calibrated monthly by trained operators
    - Conductivity automatically temperature-compensated
  - Nitrate sensors
    - Discrete water samples collected weekly/biweekly for validation; during precipitation events, autosamplers at 1–4 hour intervals
    - Lab nitrate-N analysis by SKALAR Sans Plus (detection limit ~10 μg/L NO3--N)
    - Sensor calibration: linear regression between sensor-estimated NO3--N and lab-measured NO3--N
    - Calibration approaches compared: short time-interval calibration vs one single calibration for the entire period
    - Final NO3--N values used: time-interval calibration data, due to lower uncertainty than the single calibration
  - Uncertainty: uncertainty of sensor calibration (μL) reported for each calibration interval

- Data quality and completeness
  - Missed data due to power/instrument/fieldwork issues
  - Missing data percentages by site and variable (illustrative):
    - Chenqi: T 0.41%, EC 0.42%, pH 0.57%, DO 7.5%, NO3--N 5.3%
    - Laoheitan: T 7.6%, EC 7.6%, pH 7.6%, DO 7.6%, NO3--N 8.7%
    - Maoshuikeng: T 13%, EC 43%, pH 16%, DO 13%, NO3--N 1.5%

- Dataset format and structure
  - Format: CSV file with supporting information in .rtf
  - Columns: 19 total, including
    - Time column (Date_time: yyyy-mm-dd hh:mm)
    - For each site (Chenqi, Laoheitan, Maoshuikeng): Temperature (°C), Specific Conductivity (μS/cm), pH, Dissolved Oxygen Saturation (%), Calibrated nitrate-N (mg/L), Calibrated Uncertainty (mg/L)
  - The dataset is labeled and structured to reflect per-site hydrochemical and nitrate sensor readings

- Publication and usage notes
  - Related publication: Yue, F.-J. et al. 2019. Land use interacts with changes in catchment hydrology to generate chronic nitrate pollution in karst waters and strong seasonality in excess nitrate export. Science Total Environment, 696, 134062
  - This supporting information complements the paper; five sites are discussed in the publication
  - For access to all sites or additional data, contact the authors

- Relevance for data leadership and data management
  - Demonstrates end-to-end data lifecycle: instrument setup, calibration methodology, data validation against lab measurements, and handling of missing data
  - Highlights the importance of multiple calibration approaches and uncertainty assessment for sensor-derived measurements
  - Emphasizes data availability, metadata clarity, and format standardization to support reuse and cross-site analyses across networks and partners