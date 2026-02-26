# Data Overview:

- High-resolution water quality and carbon data from the Drumtree peatland catchment (30-minute frequency for water quality and dissolved carbon; particulate organic carbon [POC] at a lower frequency).
- Variables included: water temperature (°C), air temperature (°C), specific conductivity (SpEC, µS cm-1), discharge (m3 s-1), dissolved organic carbon [DOC] (mg L-1), estimated max [DOC] (mg L-1), estimated min [DOC] (mg L-1), and particulate organic carbon [POC] (mg L-1). Note: POC is not recorded at 30-minute frequency; SpEC is mentioned as a measured parameter.

## Context and Location

- Dataset collected in the Drumtree peatland catchment, SW Scotland (5.81 km2; 195–260 m a.s.l.).
- Catchment contains eight wind turbines (part of Whitelee Wind Farm).
- Data collection period: 23 May 2012 – 16 Dec 2014, covering two complete hydrological years.
- Originates from Dr. Coleman’s PhD research; subsequent re-calibration by A. Bass and co-authors for publication.

## Data Collection and Methods

- Water quality: MP Troll 9000 hydrochemistry Sonde; calibrated against pH standards (4, 7, 10) and conductivity standards (147 µS cm-1).
- Discharge: Teledyne ISCO 2150 flow logger with depth sensing.
- DOC: field UV-Vis Spectrometer (S::can Spectro::lyser); calibrated against manually collected samples, acidified, and run on Thermalox TOC analyser (precision ±3%).
- Data gaps: sensor failures caused periods of missing data; discharge data is complete, while some gaps exist in water quality and DOC.

## Data Structure

- Single CSV file: Drumtree_Water_Quality-DOC_Time_Series.
- Columns (ten total, including time): Date / Time, Water temp (deg C), Air temp (deg C), pH, discharge (m3/s), [DOC] (mg/L), [DOC] (max), [DOC] (min), [POC] (mg/L), plus additional parameter(s) (likely SpEC and/or another ancillary variable as noted in the narrative).
- Dataset captures high-frequency water quality and DOC measurements with a slower-frequency POC series.

## Data Quality and Provenance

- Provenance: data collected during PhD research; re-calibrated for publication; raw and processed data linked to the Drumtree site.
- Quality considerations: calibration steps documented; known data gaps due to sensor issues; complete discharge time series enables reliable hydrological analyses; other variables may require gap handling.

## Relevance for Data Support and Use

- Suitable for building dashboards, self-serve analyses, and reports around hydrology and carbon dynamics in peatland systems.
- Can be integrated with other datasets (e.g., wind-farm context, meteorological data) to support policy, planning, or local governance insights.
- Important to document data gaps, units, and column mappings; POC at lower frequency and any frequency mismatches should be accounted for in analyses.