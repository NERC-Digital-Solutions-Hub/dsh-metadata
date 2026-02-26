# Drumtree_Water_Quality-DOC_Time_Series

## Data Overview
- High-resolution (30-minute frequency) water quality, dissolved and particulate carbon data from a peatland catchment.
- Measured: water temperature (°C), air temperature (°C), specific conductivity (µS cm⁻¹), discharge (m³ s⁻¹), dissolved organic carbon concentration ([DOC] mg L⁻¹), estimated max [DOC], estimated min [DOC], particulate organic carbon concentration ([POC] mg L⁻¹).
- POC is the only dataset not recorded at 30-minute frequency.
- Collected 23/05/2012 to 16/12/2014, covering two complete hydrological years.
- Context: data collected in Drumtree peatland catchment with eight wind turbines (Whitelee Wind Farm) in SW Scotland.

## Location and Catchment
- Drumtree peatland catchment, area 5.81 km².
- Elevation range 195–260 m above sea level.
- Coordinates: 55°41'16''N, 4°23'37''W.

## Measurements and Methods
- Water quality: MP Troll 9000 hydrochemistry Sonde (In-Situ); calibrated with pH standards (4, 7, 10) and conductivity standard (147 µS cm⁻¹).
- Discharge: Teledyne ISCO 2150 flow logger with depth via pressure transducer.
- DOC: field UV-Vis spectrometer (S::can Spectro::lyser) calibrated against manual samples; samples filtered, acidified, and run on a Thermalox TOC analyser (precision ±3%).
- Some data gaps due to sensor failure; discharge data is complete; gaps exist for some water quality and DOC measurements.

## Data Structure
- Single CSV file: Drumtree_Water_Quality-DOC_Time_Series.
- Columns: Date / Time, Water temp (°C), Air temp (°C), pH, discharge (m³/s), [DOC] (mg/L), [DOC] (max), [DOC] (min), [POC] (mg/L).

## Provenance and Processing
- Initial data collection as part of Dr. Coleman’s Ph.D. research; re-calibrated by A. Bass and co-authors for publication.
- Data period spans 2012–2014; calibration and processing documented in associated work.

## Data Quality and Gaps
- 30-minute frequency for most variables; POC measured at a different (non-30-min) frequency.
- Sensor failures cause data gaps in water quality and DOC; discharge remains complete.
- DOC precision: ±3% from TOC analysis.

## Relevance for Monitoring and Analysis
- Provides standardized, time-resolved carbon and hydrology data for peatland monitoring.
- Enables assessment of environmental health, carbon dynamics, and watershed policy performance over time.
- Useful baseline for linking environmental data with management context (Wind Farm site).

## Accessibility and Usage Notes
- Data contained in a single CSV with clear provenance (Ph.D. origin and subsequent calibration).
- Ready for integration with other datasets to enhance monitoring value and data accessibility to stakeholders.