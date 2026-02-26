# Overview

- A dataset from a continuous trial of a decentralised low-maintenance drinking water treatment system (DWTS) in the UK, focusing on sensing, treatment, and quality monitoring for a PAqua 1000D-2 unit within the NINJA-DWTP installation at the University of the West of England, Bristol.
- Part of a UK-India Water Quality project to develop and pilot sensing and treatment technologies for monitoring and improving drinking water quality.

## Scope and purpose (GIS relevance)

- Provides spatially contextual water treatment and quality data suitable for map-based visualisation and spatial analysis.
- Aimed at long-term operation monitoring and rapid diagnostics, with data suitable for temporal GIS (time-enabled maps) and data fusion with other spatial datasets.

## System and sampling locations (spatial context)

- Three sampling locations within the DWTS:
  - Raw water ( RW ) from a modified artificial water body on campus.
  - Header tank ( HT ) after Turbidex pre-filtration but before the PAqua-WPU.
  - Potable water ( PW ) pipeline after the treatment unit.
- Raw water sampling site coordinates: N 51° 29' 56", W 2° 32' 39".
- System components include PAqua 1000D-2 WPU, ECAS biocidal dosing, 50 µm pre-filter, 0.02 µm ultrafiltration membranes, and a 100 L treated water tank. Ancillary settlement tanks and Turbidex filters reduce input load.

## Data collection and telemetry (temporal/spatial data)

- Telemetry via Grundfos Remote Management, with in-line sensors (s::can, Messtechnik GmbH) for remote diagnostics and monitoring.
- Key operational telemetry (file 1) captured on a 5-minute window:
  - Flow rate (min, max, average) in m3/hr.
  - Ultrafiltration transmembrane pressure (TMP) average.
  - ORP (min, max, average) in mV.
  - Free chlorine concentration (min, max, average) in ppm.
- Data collection frequency and aggregation suitable for time-series GIS analysis and event detection (e.g., backwash cycles, TMP thresholds).

## Water sampling and quality analysis (procedures)

- Sampling regime:
  - 11-week field trial from 25 November 2019 to 10 February 2020, with weekly sampling (two campus closure weeks noted).
  - Samples analysed by Wessex Water Scientific Centre (UKAS-accredited) following ISO 17025 standards.
- Parameters and suites:
  - Regulatory drinking water quality indicators measured at all locations (Table 3 in the document), including microbiological indicators (E. coli, coliforms, Clostridium perfringens, Enterococci, plate counts) and physicochemical metrics (pH, turbidity, conductivity, colour, alkalinity, TOC, sulfate, orthophosphate, chloride, silica, various metals).
  - Extended analyses (metals, hydrocarbons, pesticides, PAHs) tested less frequently (Table 4).
  - Sampling regimes include Full, Standard, and Basic suites, with corresponding parameter coverage.
- Data structure notes:
  - Each of the three sampling points (raw water, header tank, potable water) has its own data summary file (files 2–4) with detailed parameter lists, units, regulatory limits (DWI limits), and standard methods.

## Trial design and data structure (files and columns)

- File 1: 1_DWTS_operational-parameters.csv
  - 11 columns:
    - Date_Time; Flow_min; Flow_max; Flow_average; TMP_average; ORP_min; ORP_max; ORP_average; FCl_min; FCl_max; FCl_average
  - Description: 5-minute-averaged operational telemetry, recorded by Grundfos Remote Management.
- File 2: 2_DWTS_RawWater_data-summary.csv
  - 85 columns, including:
    - Date, Time
    - Microbiological: Coliforms_37, E-coli_37, Coliforms_44, E-coli_44, Count_2day_37, Count_3day_22, C-perfringens, Enterococci
    - Physicochemical: pH, Colour_spec, Colour_est, Turbidity, EC, T_hardness, Non-CaCO3_hardness, Alkalinity, TOC, SO4, PO4_3-, Cl, Si, NH4, NO2, NO3, F, CN, FOG, Ca, Mg, Na, K, Al, Mn, Fe, Cu, Zn, As, B, Cr, Sb, Ba, Cd, Pb, Ni, Hg, Se, Benzene, 1-2-DCE, DCM, 1-1-2-TCFE, Chloroform, etc., plus numerous trace contaminants and pesticide/PAH indicators.
  - Includes DWI limits and standard methods for each parameter where applicable.
- File 3: 3_DWTS_HeaderTank_data-summary.csv
  - 77 columns, similar parameter structure as File 2 but for header tank data.
- File 4: 4_DWTS_Potable_data-summary.csv
  - 85 columns, similar parameter structure as File 2 but for potable water data.
- Data notes:
  - Some parameters have missing values (NA) due to sampling plan variations and parameter selection.
  - Essential operational data is included; other telemetry data may be condensed in the Grundfos system and not used for performance assessment.

## Data quality and limitations (for GIS data integration)

- Incomplete coverage: not all parameters measured at every time point or location; sampling regime varied by parameter suite.
- Missing values identified as NA; some data gaps during campus closures.
- Ancillary data (beyond essential parameters) may be captured by the Grundfos system but not included in the four summaries.
- Designed for regulatory compliance assessment and broader water-quality profiling, with extensive lists of metals, hydrocarbons, pesticides, PAHs, and other contaminants.

## GIS potential and applications

- Spatial mapping of sampling locations and trajectories of water quality along the DWTS flow path (RW → HT → PW).
- Time-enabled maps and dashboards combining:
  - Telemetry: flow, TMP, ORP, and free chlorine over time.
  - Water-quality parameters at each location (microbiological, chemical, and physical properties).
  - Alerts and events (e.g., TMP thresholds triggering enhanced cleaning or backwash timing).
- Data fusion opportunities:
  - Overlay with external spatial datasets (water sources, infrastructure, land use) to analyze drivers of water quality.
  - Visualise correlations between input water quality (RW) and treated output (PW) and identify critical control points.
- Typical GIS outputs:
  - Point features for RW, HT, PW with time-series attribute layers.
  - Flow-path lines with attribute data from telemetry (volume, pressure, and chlorine/ORP trends).
  - The three sampling locations can be used to create transects or spatial dashboards showing degradation/remediation along the treatment train.

## References

- Clayton, G.E., Thorn, R.M.S., Reynolds, D.M., 2019. Development of a novel off-grid drinking water production system integrating electrochemically activated solutions and ultrafiltration membranes. J. Water Process Eng.
- Drinking Water Inspectorate (DWI), 2010. The Water Supply (Water Quality) Regulations 2010.