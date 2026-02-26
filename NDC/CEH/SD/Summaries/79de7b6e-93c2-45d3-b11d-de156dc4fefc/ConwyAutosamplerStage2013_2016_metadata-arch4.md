# Experimental design/Sampling regime

- Scope and purpose
  - 15-minute river stage height measurements for 6 monitoring stations in the Conwy catchment, North Wales, covering 2013–2016.
  - One site (Cwm Llanerch) also records water temperature.
  - Data were collected by CEH staff for the NERC project on multi-scale responses of water quality, biodiversity, and carbon sequestration (NE/J011991/1).
  - Note: gaps exist in the dataset due to equipment, battery, or system failures.

- Sites and parameters
  - Cwm Llanerch: Water level (mm) and Water temperature (°C); coordinates: 53.106627, -3.7916149.
  - Glasgwm: Water level (mm); coordinates: 53.027723, -3.8462502.
  - Nant y Brwyn: Water level (mm); coordinates: 52.990162, -3.8018288.
  - Nant y Coed: Water level (mm); coordinates: 53.049063, -3.7183329.
  - Hiraethlyn: Water level (mm); coordinates: 53.204355, -3.7827381.
  - Dyffryn Mymbyr: Water level (mm); coordinates: 53.089587, -3.9718091.

- Collection methods and instrumentation
  - Water level: measured at all sites using a pressure transducer every 10 seconds; 15-minute mean recorded on a Campbell data logger.
  - Cwm Llanerch: Temperature data recorded in the same way.
  - Field instrumentation varied by site due to availability:
    - General sites (except Cwm Llanerch): Druck PDCR 1830 pressure transducers with Campbell CR10 data loggers.
    - Cwm Llanerch: Campbell CS451 pressure transducer with Campbell CR1000 data logger.
  - The variation in instruments occurred because older CR10x and PDCR products were discontinued.

- Calibration and data integrity
  - Pre-deployment calibration: Druck PDCR 1830 calibrated with Druck DPI 510 (2013) at CEH Wallingford.
  - Cwm Llanerch CS451 transducer was brand new and factory calibrated prior to deployment.
  - Regular site visits and data downloads used for quality checks; issues mainly due to power failures resolved by battery replacement.

- Data structure and storage
  - Data organized as CSV files, one per site.
  - File naming includes site name and coverage period (e.g., 2013–2016).
  - Common columns (for Glasgwm, Nant y Brwyn, Nant y Coed, Hiraethlyn, Dyffryn Mymbyr):
    - ID: sample identifier
    - Date: date of measurement (dd/mm/yyyy)
    - Time: time of measurement (hh:mm:ss)
    - Stage_ht_mm: water level above transducer (mm)
    - Battery_volt: battery voltage powering logger/transducer (V)
  - Cwm Llanerch adds:
    - Temp_degC: water temperature (°C)
  - Data compiled from field laptop downloads and stored in an Access database.

- Metadata and supporting information
  - Site coordinates provided for all locations.
  - Temperature data available only for Cwm Llanerch.
  - Data availability window per site outlined in miscellaneous documents (start/end dates; some entries show truncated year digits, indicating 2013–2016 coverage overall).

- Quality control and data gaps
  - Quality checks involved plotting data after downloads to identify obvious issues.
  - Primary data gaps caused by power failures requiring site visits and battery changes.
  - Data gaps also noted due to equipment/battery/system issues across sites.

- Implications for data reuse and governance
  - Dataset enables multi-site hydrological comparisons with consistent 15-minute temporal resolution and occasional temperature data.
  - Instrument heterogeneity across sites necessitates careful metadata governance and potential harmonization for cross-site analyses.
  - Clear documentation of calibration, data collection cadence, and data quality checks supports reliability and traceability.
  - Data is tied to a broader NERC project, suggesting potential for integration with related datasets and ongoing data updates within the project scope.