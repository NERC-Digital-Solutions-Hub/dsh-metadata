# Experimental design/Sampling regime

- Study scope and period
  - 15-minute river stage height data for 6 monitoring stations in the Conwy catchment, North Wales
  - Period: 2013–2016
  - At one site (Cwm Llanerch) water temperature was also sampled
  - Data collected by CEH for the NERC project NE/J011991/1
  - Gaps exist due to equipment/battery/system failures

- Sites and spatial context
  - Cwm Llanerch (53.106627, -3.7916149)
  - Glasgwm (53.027723, -3.8462502)
  - Nant y Brwyn (52.990162, -3.8018288)
  - Nant y Coed (53.049063, -3.7183329)
  - Hiraethlyn (53.204355, -3.7827381)
  - Dyffryn Mymbyr (53.089587, -3.9718091)
  - Parameters sampled: water level (mm) at all sites; water temperature (°C) at Cwm Llanerch

- Data collection methods
  - Water level measured with pressure transducers every 10 seconds; mean value recorded every 15 minutes
  - Temperature data at Cwm Llanerch recorded similarly
  - Data downloaded to field laptop and uploaded to an Access database
  - Instrumentation differences due to equipment availability and discontinuation:
    - Most sites: Druck PDCR 1830 transducers + Campbell CR10x loggers
    - Cwm Llanerch: Campbell CS451 transducer + Campbell CR1000 logger

- Calibration and instrumentation notes
  - Druck PDCR 1830s calibrated with Druck DPI 510 (2013)
  - Cwm Llanerch CS451 transducer factory calibrated prior to deployment
  - Calibration rationale and equipment changes documented

- Data structure and metadata
  - Data stored as CSV files, one per site; filenames indicate site and time span (e.g., 2013–2016)
  - Site data columns (five sites): ID, Date (dd/mm/yyyy), Time (hh:mm:ss), Stage_ht_mm, Battery_volt
  - Cwm Llanerch includes an additional column: Temp_degC
  - Start/end dates per site provided in supporting documents (approx. 2013 to 2016)

- Data quality and processing
  - Routine site visits and data downloads; data checked for obvious issues
  - Common issue: data gaps due to power failures, resolved by site visits and battery replacement

- Miscellaneous notes relevant for GIS use
  - Data are time-series suitable for mapping temporal patterns of water level
  - Temperatures available only at Cwm Llanerch
  - Data are recorded as water level height above the transducer (Stage_ht_mm) and battery voltage (Battery_volt); interpreted relative to installation height
  - Underlying dataset originally stored in an Access database, now organized as per-site CSVs for GIS ingestion

- Project and provenance
  - Related to the NERC project NE/J011991/1
  - Supporting information table provides coordinates and sampled parameters for each site