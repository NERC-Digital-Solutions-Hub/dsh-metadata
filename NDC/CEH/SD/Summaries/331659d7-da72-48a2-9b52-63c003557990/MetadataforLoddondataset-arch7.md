# Supporting information for 'High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017- Sept 2018)'

## Overview
- A comprehensive, multi-resolution dataset from Bow Brook, a headwater tributary to the River Loddon in Hampshire, collected Sept 2017–Sept 2018.
- Data types include hourly high-frequency water quality and flow data, daily and stormwater samples with laboratory analyses, and spectroscopic scans (UV-Vis) at field and lab stages.
- Aimed at enabling GIS-based visualization and spatial-temporal analysis of catchment water quality and hydrology.

## Data access and citation
- Data access: https://doi.org/10.5285/331659d7-da72-48a2-9b52-63c003557990
- Citation: Hawkins et al. (2019). High resolution water quality and flow monitoring data coupled with daily and storm samples from the Loddon catchment (Sept 2017-Sept 2018). NERC Environmental Information Data Centre. Dataset.

## Experimental design and sampling regime
- Study site: Bow Brook near the confluence with the Loddon near Sherfield-on-Loddon, predominantly agricultural catchment.
- Monitoring period: 08/09/2017 to 09/09/2018.
- Sampling regimes:
  - High-resolution water quality and flow data collected hourly (start 00:00 GMT 08/09/2017).
  - Daily water quality samples collected at 09:00 GMT (08/09/2017 to 08/09/2018).
  - Storm water quality samples collected intermittently, hourly during storm events (11:00 GMT 11/09/2017 to 08:00 GMT 22/01/2018).
- Missing data: equipment breakdowns (temperature-related freezes, measurement errors) caused gaps; turbidity measurements began later (10/10/2017) due to equipment delay.

## Collection, laboratory and analytical methods and instrumentation
- Field sampling:
  - Peristaltic pump system with two flow-through cells.
  - TriOS OPUS UV/VIS Spectral Analyser (200–800 nm; 2.2 nm per pixel) and YSI 6600 V2-2 multi-parameter Sonde (turbidity, ammonium, pH, conductivity, temperature, DO).
  - Sontek IQ flow gauge for flow and height at sampling point.
  - Autosamplers: two ISCO 6712 units for daily and storm samples (300 mL in 350 mL glass bottles; storm samples triggered hourly during storms).
- Laboratory analyses:
  - pH (Mettler Toledo), conductivity (Mettler Toledo), turbidity (Hanna HI-93703), full UV-Vis spectral scans (Jenway 7315, before/after filtering), suspended sediment (TSS via filtration), DOC/NPOC (Shimadzu TOC-L after filtration and acidification for NPOC method), and pesticide analysis (Affinity Water Ltd.; LC-MS/MS for 12 pesticides).
  - Filtration and sample handling: 0.7 μm filtration for UV-Vis and NPOC prep; storage at 4°C; analysis within 48 hours.
- Data integrity notes:
  - UV sensor requires weekly cleaning due to fouling.
  - Pesticide samples preserved with sodium thiosulphate; detection limits around 0.01 μg/L.

## Nature and units of recorded values, and data structure
- Six CSV data files:
  - DailyWaterQualityData.csv (366 samples): field and lab measurements including Flow (m3 s-1), Depth (m), 254 nm field absorbance (AU), field turbidity (NTU), field conductivity (µS cm-1), pH, ammonium (mg L-1), lab pH, lab conductivity, lab turbidity (FTU), 254 nm lab absorbance (AU), Total Suspended Solids (g L-1), NPOC (mg L-1), and 12 pesticides (µg L-1) plus Total pesticides and EU limits.
  - StormWaterQualityData.csv (207 samples): similar variables collected during storm events, with time-stamped data per date/time.
  - HighFrequencySensorDataFlowandSonde.csv (8,332 samples): high-frequency field data including flow (m3 s-1), stage (m), mean velocity (m s-1), total volume (L), depth (m), index velocity (m s-1), area (m2), temperature (°C), plus field and lab sondes measurements (temperature, conductivity, pH, ammonium, turbidity, DO, etc.).
  - HighFrequencyDataOpticalScan.csv (8,364 samples): raw optical scan from TriOS (AU) across 197.976–720.86 nm with DateTime.
  - DailyOpticalScansBlankCorrected.csv (366 samples): blank-corrected daily scans (AU), 200–800 nm, measured every 2 nm; some missing dates.
  - StormOpticalScansBlankCorrected.csv (194 samples): blank-corrected storm scans (AU), 200–800 nm; some missing data points and dates; storm event batch separation noted.
- Units are provided within each file’s description and field definitions.

## Data structure and repository details
- Data organization reflects three temporal scales: hourly high-frequency sensor data, daily measurements, and event-based storm samples, plus spectral scans (field and lab).
- Data are consolidated into six CSV files with detailed field names and unit annotations to support time-series GIS analyses and cross-dataset joins.

## Data quality and limitations
- Gaps due to equipment failure (temperature-related freezes) and measurement errors.
- Turbidity measurements began 10/10/2017, creating an initial data gap for turbidity.
- Daily sampling occasionally extended to 1.5–2 weeks around holidays; storm sampling times may have irregularities due to storm duration and operational constraints.
- Storm optical scans and some storm dates contain missing entries or are organized by batch dates rather than exact calendar alignment.

## Potential GIS applications
- Time-series mapping of water quality and hydrology metrics at a single upstream site with a downstream catchment context.
- Spatial integration with catchment boundaries, land use, rainfall, and storm events to visualize spatial-temporal patterns of turbidity, conductivity, pH, ammonium, and pesticides.
- Linking in-situ sensor data (flow, depth, velocity) with laboratory analyses (NPOC, TSS, pesticides) for integrated water quality assessments.
- Cross-referencing spectral data (UV-Vis scans) with chemical indicators to identify contaminant signatures and water quality changes during storm events.
- Supports development of map-based data products for policy discussions, client reporting, or public-facing dashboards on catchment water quality dynamics.