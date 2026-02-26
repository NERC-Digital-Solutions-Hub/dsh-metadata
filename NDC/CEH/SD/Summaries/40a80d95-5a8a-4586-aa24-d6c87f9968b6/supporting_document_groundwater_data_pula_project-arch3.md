# PULA Groundwater data folder

- The dataset comprises 25 files with in situ groundwater measurements in the Gaborone catchment, Botswana, collected May 2017–June 2018 by a collaboration between the Botswana Department of Water Affairs, the Botswana International University of Science and Technology, and the University of Aberdeen.
- Purpose: to understand long-term groundwater response to the 2016–2017 floods, assess spatial variability, and evaluate wider impacts of extreme rainfall and flooding on water quality, within a region of diverse geology and land use. This work is part of the NERC-funded PULA project.

## Experimental design and sampling regime

- Two measurement strategies were employed:
  - Strategy 1 (near-monthly, spatial mapping): 22 boreholes across the catchment measured for groundwater depth, pH, temperature, electrical conductivity, and total dissolved solids; 149 measurement occasions across 41 days, yielding 456 measurements by parameter.
  - Strategy 2 (high-temporal-resolution, 5-minute timeseries): 3 boreholes with automatic dataloggers capturing groundwater depth, temperature, and electrical conductivity; 861,816 measurements (324,353 GWD, 324,376 T, 213,087 EC) over roughly a year.
- Sampling locations were selected to cover spatial variability and practical access considerations.
- The near-monthly campaigns were concentrated around flood-drought-flood cycles.

## Collection methods and field instrumentation

- Strategy 1: manual in situ measurements
  - Groundwater depth: Hydrotechnik dipmeter (top of borehole casing as reference).
  - pH, temperature, EC, TDS: pumped grab samples using HI-98129 portable tester.
- Strategy 2: high-frequency automatic measurements
  - Groundwater depth (GWD), temperature, EC: Solinst Leveloggers (2 with LTC for GWD/T/EC, 1 with LT for GWD/T).
  - Raw head values were converted to freshwater depth via barometric compensation and depth corrections using Strategy 1 data and linear interpolation.
- Calibration and units:
  - GWD (Strategy 1): m, 0.01 m resolution, factory calibration (dipmeter).
  - GWD (Strategy 2): m, 0.001 m resolution, manual dipmeter for calibration.
  - pH: unitless; T: °C; EC: µS/cm; TDS: ppm. Device-level calibrations included factory or standard solutions as appropriate.
- Data download timings: eight occasions (8 Aug 2017; 11–12 Sep 2017; 9–10 Nov 2017; 20 Nov 2017; 25 Nov 2017; 17–18 Jan 2018; 16–17 Mar 2018; 9–11 Jun 2018).

## Data processing and quality control

- Strategy 2 data underwent barometric compensation using a Barologger at Otse-ramotswa landfill BH2, with subsequent depth corrections to align with Strategy 1 measurements.
- All data were checked for obvious measurement errors (including field notebook entries and anomalous log records); erroneous records were deleted.
- Data processing ensured alignment of high-frequency and near-monthly data streams, with clear documentation of processing steps and calibration decisions.

## Data structure and content

- Data are provided as CSV files in two categories:
  - Strategy 1 files: PULA_GW_level_physicochem_***.csv (22 files)
    - Columns: measurement date, measurement time, groundwater depth (m), pH, temperature (°C), EC (µS/cm), TDS (ppm).
  - Strategy 2 files: PULA_GW_timeseries_***.csv (3 files)
    - Columns: measurement date, time (hh:mm:ss), groundwater depth (m), temperature (°C), EC (µS/cm, when available).
- Borehole details (Table 1) include names, coordinates, measurement periods, frequency, and measured parameters (e.g., some boreholes with automatic dataloggers; others with manual sampling).

## Spatial coverage and borehole context

- Measurements span boreholes distributed around the Gaborone Reservoir catchment, capturing diversity in physiography, geology, and land use.
- Strategy 1 provides broad spatial coverage with multiple parameters; Strategy 2 provides dense temporal resolution at a subset of wells.

## Relevance to environmental health monitoring and governance

- Demonstrates a dual-structure monitoring approach: broad, multi-parameter snapshots at regular intervals plus high-frequency time series for selected sites.
- Supports data provenance and reproducibility through:
  - Transparent instrumentation choices and calibration references.
  - Barometric and depth-correction procedures to ensure comparability across time scales.
  - Explicit quality control steps and documentation of data gaps.
- Highlights practical governance considerations for monitoring frameworks:
  - Data gaps and incomplete time series due to logistics and equipment reliability.
  - The need for metadata completeness to facilitate dataset verification and reuse.
  - The trade-off between publicly sharing detailed measurement data and operational constraints, and the importance of data management standards at the source.

## Key limitations and challenges

- Near-monthly Strategy 1 datasets are incomplete due to logistical constraints and occasional equipment issues.
- Some parameters are only available where dataloggers were installed, leading to uneven EC data across boreholes.
- Data transformation steps (e.g., barometric correction, depth interpolation) introduce processing requirements that must be clearly documented for reuse.