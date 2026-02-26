# Data Overview: Drumtree Water Quality-DOC Time Series

- Dataset scope
  - High-resolution (30-minute frequency) water quality and carbon data from a peatland catchment.
  - Variables include water temperature, air temperature, pH, specific conductivity, discharge, dissolved organic carbon ([DOC]), estimated max/min [DOC], and particulate organic carbon ([POC]).
  - POC concentration is the only variable not recorded at 30-minute intervals.

- Temporal and geographic context
  - Location: Drumtree peatland catchment, SW Scotland (55°41'16''N, 4°23'37''W).
  - Catchment size and features: 5.81 km² catchment, altitude 195–260 m a.s.l.; contains eight wind turbines (Whitelee Wind Farm).
  - Time span: 23 May 2012 to 16 Dec 2014, covering two complete hydrological years.

- Data collection and measurement methods
  - Water quality and temperature: MP Troll 9000 hydrochemistry sonde (calibrated with pH standards and conductivity standards).
  - Discharge: Teledyne ISCO 2150 flow logger with depth (pressure transducer) data for discharge calculations.
  - DOC: Field-deployable UV-Vis spectrometer (S::can Spectro::lyser) calibrated against manually collected samples, filtered, acidified, and analyzed with a Thermalox TOC analyzer (precision ±3%).
  - Data provenance: Collected during Dr. Coleman’s Ph.D. research; subsequent recalibration by A. Bass and co-authors for publication.
  - Data gaps: Sensor failures caused periods of data gaps; discharge data is complete, while some gaps exist in water quality and DOC data.

- Data structure and access
  - File: Drumtree_Water_Quality-DOC_Time_Series.csv
  - Columns (ten total; listed here): Date/Time, Water temp (°C), Air temp (°C), pH, discharge (m³/s), [DOC] (mg/L), [DOC] (max), [DOC] (min), [POC] (mg/L), plus one additional column not explicitly detailed in the summary.
  - POC is recorded but not at the same 30-minute frequency as the other variables.

- Data quality and suitability for GIS use
  - High temporal resolution supports coupling with hydrological and GIS-based time-series analyses.
  - Data quality relies on in-field calibration and cross-checks against manual samples; known data gaps due to sensor failures should be accounted for in analyses.
  - Useful for spatially-explicit water quality visualization within the Drumtree catchment and for linking with other GIS layers (topography, land use, wind-farm infrastructure).

- Provenance and example applications
  - Data provenance linked to Dr. Coleman’s Ph.D. research; publicly referenced via the associated thesis.
  - Potential GIS applications: create time-enabled map layers of water quality indicators, trend mapping across the catchment, correlation of discharge with DOC/POC concentrations, and integration with catchment-scale environmental datasets.