# Data Overview:

- High-resolution water quality and carbon data from a peatland catchment (Drumtree, SW Scotland) over two hydrological years (2012-2014), with 30-minute frequency for most variables.
- Variables included: water temperature (°C), air temperature (°C), specific conductivity (µS cm-1), discharge (m3 s-1), dissolved organic carbon concentration [DOC] (mg L-1), estimated max [DOC] (mg L-1), estimated min [DOC] (mg L-1), and particulate organic carbon [POC] (mg L-1). POC is not recorded at 30-minute frequency.

- Study location details:
  - Catchment area: 5.81 km2; altitude 195–260 m a.s.l.
  - Eight wind turbines within the Whitelee Wind Farm.
  - Data collection period: 23/05/2012 to 16/12/2014 (two complete hydrological years).

- Data collection and calibration:
  - Water quality: MP Troll 9000 hydrochemistry Sonde; calibrated with pH standards (4, 7, 10) and conductivity standard (147 µS cm-1).
  - Discharge: Teledyne ISCO 2150 flow logger with depth from a pressure transducer.
  - DOC: field-deployable UV-Vis Spectrometer (S::can Spectro::lyser); calibration against manually collected samples, filtered, acidified, and analysed with a Thermalox TOC analyser (precision ±3%).

- Data quality and gaps:
  - Periods of sensor failure caused data gaps in water quality and DOC.
  - Discharge dataset is complete; some gaps exist in other measurements.

- Data structure:
  - Single CSV file: Drumtree_Water_Quality-DOC_Time_Series.
  - Ten data columns (as described): Date / Time, Water temp (deg C), Air temp (deg C), pH, discharge (m3/s), [DOC] (mg/L), [DOC] (max), [DOC] (min), [POC] (mg/L) (note: exact column naming may reflect these items).

- Provenance and access:
  - Initial data collection part of Dr. Coleman’s Ph.D. work; subsequent recalibration by A. Bass and co-authors for publication.
  - Data linked to the Ph.D. thesis (http://theses.gla.ac.uk/8539/).

- Potential analytic use for analysts:
  - Investigate correlations and temporal dynamics between hydrological variables and DOC/POC.
  - Develop predictive relationships (e.g., DOC response to discharge or temperature).
  - Leverage the 30-minute resolution to study rapid hydrological and carbon processes, while accounting for data gaps and calibration details.