# River Wensum Water Quality Data (2010 - 2016)

## Overview
- 899 river water samples collected between Oct 2010 and Sep 2016.
- Sampling at 20 sites: 17 tributary outlets and 3 main river sites across the River Wensum catchment.
- Sampling roughly monthly; samples taken from the centre of the channel in 1 L acid pre-washed bottles.
- Samples transported in cool boxes and stored at 4°C within 5 hours to minimize degradation.

## Sampling Design
- Spatial coverage: 20 sampling sites distributed across the catchment (Figure 1 shows locations).
- Temporal coverage: approximately monthly sampling over the 6-year period.

## Laboratory Analysis and Quality Assurance
- Analyses conducted within five days of collection by the UEA Science Analytical Facilities.
- Analyte groups: nutrients, carbon, major ions, and total suspended solids (TSS).
- Quality assurance: use of certified reference materials; instrument accuracy and precision checks; reanalysis if tolerances were not met; manual data screening prior to acceptance.

## Data Content and Variables
- Metadata and measurements are documented across two tables:
  - Table 1: Metadata for measured variables, including:
    - Location/time: latitude, longitude (decimal degrees); date/time (yyyy/mm/dd:hh:mm).
    - In-situ/derived parameters: pH, electrical conductivity (µS/cm), ion concentrations (e.g., Ca, Mg, Na, K, Cl−, SO4 2−, PO4 3−, NO3−, NO2−, NH4 +, etc.), alkalinity (CaCO3), bicarbonate (HCO3−), carbonate (CO3 2−), silicate (Si), trace elements (B, Al, Fe, Mn).
    - Carbon and nitrogen/phosphorus species: Total Carbon (TC), Total Organic Carbon (TOC), Total Nitrogen (TN), Total Dissolved Nitrogen (TDN), Total Particulate Nitrogen (TPN), Total Particulate Phosphorus (TPP), Total Dissolved Phosphorus (TDP), Total Reactive Phosphorus (TRP), Total Phosphorus (TP), dissolved/inorganic forms (NO3−, NO2−, NH4 +, TSS, etc.).
    - Units and analytical notes: specific units for each parameter; long-term precision, accuracy, and detection limits where provided.
    - Data quality indicators: ion balance error, sums of cations/anions, and other calculated fields where applicable.
  - Table 2: Instrumentation used by UEA Science Analytical Facilities, including:
    - Metrohm 855 robotic titro sampler.
    - Agilent ICP-OES Vista Pro.
    - Dionex ICS2000 Ion Chromatography.
    - Skalar San ++ Autoanalyser.
    - Skalar Formacs CA15 TOC TN analyser.

## Spatial-Temporal Coverage
- Timeframe: October 2010 to September 2016.
- Cadence: approximately monthly sampling.
- Geography: 20 sites within the River Wensum catchment (17 tributaries + 3 main river sites).

## Data Quality, Provenance, and Usage
- Data subject to QA procedures: calibration checks, reference materials, repeat measurements, and manual checks before acceptance.
- Instrumental details provide context for data interpretation and comparability across parameters.
- The dataset supports GIS-based analysis of spatial and temporal trends in water quality, enabling visualization of nutrient, carbon, major ion, and TSS patterns across the catchment.

## GIS Considerations and Applications
- Suitable for map-based visualization of spatial gradients and site-specific time-series.
- Coordinate data are in decimal degrees; ensure consistent CRS when integrating with other GIS layers.
- Many parameters include detailed metadata (precision, accuracy, detection limits) that should be considered when performing spatial or temporal analyses.
- Potential outputs: thematic maps of contaminant concentrations by site and time, cross-site comparisons, and trend analyses across the 6-year period.