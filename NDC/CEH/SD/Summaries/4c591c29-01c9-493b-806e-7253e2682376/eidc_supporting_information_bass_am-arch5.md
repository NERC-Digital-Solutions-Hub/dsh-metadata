# Data Overview

## Scope and contents
- High-resolution water quality, dissolved and particulate carbon data from a peatland catchment (Drumtree, SW Scotland).
- Variables include: water temperature (°C), air temperature (°C), pH, specific conductivity (µS cm-1), discharge (m3 s-1), dissolved organic carbon [DOC] (mg L-1), estimated max [DOC] (mg L-1), estimated min [DOC] (mg L-1), and particulate organic carbon [POC] (mg L-1).
- Frequency: 30-minute for all variables except POC (POC not 30-minute).
- Temporal coverage: 23/05/2012 – 16/12/2014, spanning two complete hydrological years.
- Provenance: data originally collected as part of Dr. Coleman’s PhD; subsequent re-calibration by A. Bass and co-authors for publication.

## Site and context
- Location: Drumtree peatland catchment, SW Scotland (55°41'16''N, 4°23'37''W).
- Catchment characteristics: area 5.81 km2; altitude 195–260 m a.s.l.
- Nearby infrastructure: eight wind turbines as part of the Whitelee Wind Farm.
- PhD link for provenance: http://theses.gla.ac.uk/8539/

## Measurement methods and calibration
- Water quality: MP Troll 9000 hydrochemistry Sonde; calibrated against pH standards (4, 7, 10) and conductivity standard (147 µS cm-1).
- Discharge: Teledyne ISCO 2150 flow logger with depth from a pressure transducer.
- DOC: field deployable UV-Vis Spectrometer (S::can Spectro::lyser); calibration against manually collected samples; samples filtered, acidified, and measured on a Thermalox TOC analyser (precision ±3%).
- Data gaps: periods of sensor failure causing data gaps; discharge dataset complete; some gaps in water quality and DOC.

## Data structure
- Single CSV file: Drumtree_Water_Quality-DOC_Time_Series.
- Columns (ten total as stated): 'Date / Time', 'Water temp (deg C)', 'Air temp (deg C)', 'pH', 'discharge (m3/s)', '[DOC] (mg/L)', '[DOC] (max)', '[DOC] (min)', and '[POC] (mg/L)' (note: the description lists ten columns but only nine are enumerated here).

## Provenance and lineage
- Original collection and interpretation by Dr. Coleman (PhD work).
- Later re-calibration and processing by A. Bass and co-authors for publication.

## Data quality and governance notes
- Calibration and QA steps documented; TOC analyser precision ±3%.
- Data gaps due to sensor failures; discharge data fully available.
- Historic dataset (2012–2014); potential needs for reprocessing or harmonisation if integrated with other datasets.

## Sharing, access and stewardship considerations
- The dataset should be uploaded to appropriate data portals/catalogues and accompanied by:
  - Detailed metadata on instruments, calibration standards, units, time period, and data gaps.
  - Provenance information (Dr. Coleman PhD origin; re-calibration by Bass et al.).
  - Link to the source PhD thesis for provenance and context (http://theses.gla.ac.uk/8539/).
- Clear documentation on data quality, QA steps, and handling of gaps to support discoverability and reuse.