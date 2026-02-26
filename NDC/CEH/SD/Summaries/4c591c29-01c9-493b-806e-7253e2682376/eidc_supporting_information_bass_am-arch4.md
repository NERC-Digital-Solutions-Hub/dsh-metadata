# Data Overview:

## Dataset context and scope
- High-resolution water quality, dissolved and particulate carbon data from the Drumtree peatland catchment in SW Scotland.
- Timeframe: 23/05/2012 to 16/12/2014, covering two complete hydrological years.
- Catchment details: 5.81 km² area, altitude 195–260 m a.s.l., contains eight wind turbines (Whitelee Wind Farm).

## Variables and data frequency
- Collected variables include: water temperature (°C), air temperature (°C), discharge (m³/s), pH, specific conductivity (µS cm⁻¹), dissolved organic carbon [DOC] (mg/L), estimated max [DOC] (mg/L), estimated min [DOC] (mg/L), and particulate organic carbon [POC] (mg/L).
- Data frequency: most variables recorded at 30-minute intervals; POC is not recorded at 30-minute frequency.
- Data set name: Drumtree_Water_Quality-DOC_Time_Series (single CSV with ten data columns).

## Provenance and data curation
- Initial data collection as part of Dr. Coleman’s Ph.D. research; subsequent re-calibration by A. Bass and co-authors for publication.
- Calibration and processing steps described (sensor calibration against standards, manual sample validation, TOC analysis with precision ±3%).

## Instrumentation and methods
- Water quality: MP Troll 9000 hydrochemistry Sonde; calibrated against pH standards (4, 7, 10) and conductivity standard (147 µS cm⁻¹).
- Discharge: Teledyne ISCO 2150 flow logger with depth measurement via a pressure transducer.
- DOC: field UV-Vis Spectrometer (S::can Spectro::lyser); data calibrated against manually collected samples, filtered, acidified, and analyzed with Thermalox TOC analyzer.

## Data quality and gaps
- Periods of sensor failure introduced data gaps in water quality and DOC data.
- Discharge data is complete; some gaps remain in water quality and DOC measurements.

## Data structure and access
- File: Drumtree_Water_Quality-DOC_Time_Series.csv
- Columns (approximate): Date / Time, Water temp (deg C), Air temp (deg C), pH, discharge (m3/s), [DOC] (mg/L), [DOC] (max), [DOC] (min), [POC] (mg/L).
- Emphasizes provenance and calibration history to support data usability and reuse.

## Relevance for data strategy and governance
- Demonstrates the management of a high-frequency environmental data asset, including metadata, calibration lineage, and data quality considerations.
- Highlights the importance of documenting data gaps, sensor failures, and data provenance to facilitate discovery, validation, and cross-site reuse.
- Illustrates potential data sharing and collaboration needs across research teams and broader data communities to improve standards and reduce duplicated efforts.