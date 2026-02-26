# Data Overview

- High-resolution (30-minute) water quality, dissolved carbon, and particulate carbon data from the Drumtree peatland catchment in SW Scotland (55°41'16''N, 4°23'37''W; area 5.81 km2; altitude 195–260 m a.s.l.; contains eight wind turbines of the Whitelee Wind Farm).
- Variables recorded: water temperature (°C), air temperature (°C), specific conductivity (µS cm−1), discharge (m3 s−1), dissolved organic carbon concentration [DOC] (mg L−1), estimated max [DOC] (mg L−1), estimated min [DOC] (mg L−1), and particulate organic carbon [POC] (mg L−1). POC data are not at 30-minute frequency.
- Data collection window: 23 May 2012 to 16 Dec 2014 (two complete hydrological years); data period accompanies fieldwork for Dr. Coleman’s PhD, with subsequent re-calibration and publication work by A. Bass and co-authors.
- Data collection methods and calibration:
  - Water quality and pH/SpEC measured with MP Troll 9000 hydrochemistry Sonde; pH standards (4, 7, 10) and conductivity standards used for calibration.
  - Discharge calculated with Teledyne ISCO 2150 flow logger linked to pressure depth sensor.
  - DOC measured with a field UV-Vis spectrometer (S::can Spectro::lyser) calibrated against manually collected samples; samples filtered, acidified, and analyzed with a Thermalox TOC analyzer (precision ±3%).
- Data structure: a single CSV file titled Drumtree_Water_Quality-DOC_Time_Series containing ten data columns (Date/Time, Water temp (°C), Air temp (°C), pH, discharge (m3/s), [DOC] (mg/L), [DOC] (max), [DOC] (min), [POC] (mg/L); note spacing/terminology in the original description may vary slightly, but all key variables are included.

- Data quality and gaps:
  - Periods of sensor failure introduce gaps in water quality and DOC data; discharge data are complete.
  - Some metadata limitations and data gaps pose challenges for rapid reuse without additional sourcing or metadata augmentation.

- Provenance and usage notes:
  - Primary data collection and initial processing occurred during Dr. Coleman’s PhD work; re-calibration and publication contributed by M. Coleman and co-authors.
  - Location specificity (Drumtree peatland catchment) and detailed instrumentation provide a traceable basis for monitoring and modeling of peatland hydrology and carbon dynamics.

- Relevance for monitoring and policy:
  - Supports evaluation of carbon dynamics and hydrological responses in peatland systems.
  - Useful for developing and validating monitoring frameworks, particularly around high-frequency environmental measurements, data quality assurances, metadata completeness, and governance for data sharing.
  - Highlights practical challenges relevant to monitoring programs: data gaps, data standardization, metadata completeness, and the need for transparent data governance.