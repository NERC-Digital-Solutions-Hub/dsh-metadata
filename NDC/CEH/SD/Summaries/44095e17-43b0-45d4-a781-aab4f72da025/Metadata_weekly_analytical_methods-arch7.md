# LOCATION OF ANALYTICAL DATA PRE-CONCENTRATION PRIOR TO ANALYSIS TO IMPROVE

- A comprehensive environmental chemistry dataset covering dissolved constituents in surface and ground waters, plus related hydrological inputs, collected across a Welsh catchment area.
- Documents detailed pre-concentration and analytical workflows, including filtration, preservation, and instrumental methods (ICP-OES, ICP-MS, IC, autoanalyzers, AAS, etc.).

## Purpose and scope (GIS-relevant context)

- Designed to enable map-based exploration of spatial and temporal patterns in dissolved chemicals, with accompanying hydrological context (rainfall, runoff, streamflow).
- Includes derived variables that support spatial analyses, such as area-weighted runoff from catchment-scale flow data.

## Spatial coverage and sites

- Catchment-scale network around Plynlimon with multiple sampling locations:
  - Lower Hore (Site A)
  - Upper Hore (Site D)
  - Tanllwyth (Site K)
  - Lower Hafren (Site B)
  - Upper Hafren (Site G)
- Catchment areas (approximate) for flow-to-runoff conversions:
  - Lower Hore: 3.172 km2
  - Upper Hore: 1.62 km2
  - Tanllwyth: 0.916 km2
  - Lower Hafren: 3.58 km2
  - Upper Hafren: 1.22 km2
- Data are suitable for GIS integration with location/geometry context and site-specific attribute fields.

## Temporal coverage

- Serial measurements spanning 1983–2007 (with varying end dates by analyte).
- Time stamps distinguish sample types:
  - Stream and borehole samples: grab at reported time
  - Input samples (Rainfall, Throughfall, Stemflow, Cloud): time-integrated over intervals
- Volume-weighted sampling times and year-mean sampling are calculated to support temporally aligned analyses.

## Analytes and data structure

- Broad suite of chemical species (example categories):
  - Major ions and trace elements (e.g., Al, NH4-N, Cl, NO3-N, SO4, Cr, Cu, Fe, Zn, U, etc.)
  - Dissolved organic carbon and nitrogen (DOC, DON, TDN)
  - Nutrients and related parameters (pH, conductivity, alkalinity, etc.)
  - Temperature and time data for contextual GIS analyses
- For each analyte: common fields include
  - Form (Dissolved)
  - Determinand (element/ion)
  - Units (ug/L, mg/L, etc.)
  - Location of analysis (laboratory)
  - Analytical method (ICP-OES, ICP-MS, IC, Autoanalyzer, etc.)
  - Filtration and preservation details
  - Pre-concentration and processing notes (e.g., evaporation, acidification)
  - Detection limits (LQDC) and quoting ranges
  - Data quality qualifiers (QC data qualifiers and codes)
  - Start/End dates for data series (time-bounded availability)

## Pre-concentration and analytical methods

- Multiple pre-concentration approaches documented per analyte (e.g., evaporation, dilution to 20 mL, infrared evaporation).
- Preservation strategies vary by analyte and period; common theme is maintaining sample integrity until analysis.
- Analytical methods span:
  - Inductively Coupled Plasma Optical Emission Spectrometry (ICP-OES)
  - Inductively Coupled Plasma Mass Spectrometry (ICP-MS)
  - Ion chromatography (IC) for chloride, nitrate, sulphate, fluoride
  - Automated colorimetry and Technicon Autoanalyzers for some nutrients and nitrogen species
  - Gravimetric approaches and other specialized procedures for some parameters
- QC codes indicate accreditation status and method reliability (ISO17025-related notes).

## Data quality and QC indicators

- Data Quality (QC) codes describe instrument and method context, including interlaboratory checks and accreditation status.
- Data Qualifier codes identify data reliability, raw data status, and potential method-change impacts.
- Some data flagged as lower confidence during method transitions; users should consult qualifiers for interpretation.

## Hydrology and data integration

- Hydrological conversions enable GIS-based runoff analysis:
  - Convert streamflow (m3/s or cumecs) to area-weighted runoff (mm/15 min) using catchment area.
  - Back-convert runoff (mm/15 min) to streamflow (cumecs) when needed.
- Volume-weighted sampling and timing considerations provide guidance for temporal GIS analyses, especially when aligning precipitation inputs with runoff responses.
- Cloud catch, rainfall, throughfall, and hourly rainfall data are integrated into the dataset, with explicit notes on how sampling times are determined.

## Sampling methodology and timing details

- Sampling types and timing rules:
  - Stream and borehole samples: grab at the specified time.
  - Input samples (Rainfall, Throughfall, Stemflow, Cloud): time-integrated; sampling window defined by intervals between successive sample times.
- Volume-weighted sampling time is calculated by weighting rainfall-hours with AWS-derived rainfall, using fallback AWSs when records are missing.
- The documentation provides guidance on calculating year-mean sampling and how to treat sampling gaps.

## Practical guidance for GIS use

- Data are well-suited to GIS projects requiring:
  - Spatially distributed water chemistry mapping across catchments
  - Temporal trend analysis by site and analyte
  - Hydrological context integration via area-weighted runoff and flow-conversion components
- Important to incorporate:
  - Analyte-specific units, LQDC, and quote ranges for accurate symbolization
  - Data qualifier codes to filter or weight data by reliability
  - Sampling type and time-stamp rules for accurate temporal alignment
  - Catchment-area data for hydrological derivations and runoff calculations

## Limitations and caveats

- Time coverage and analytical methods vary by analyte; many series end earlier than 2007.
- Method changes and accreditation status can affect data comparability; QC qualifiers should be consulted.
- Derived hydrological variables (area-weighted runoff) rely on accurate catchment areas and flow data; ensure proper alignment with site codes and timestamps.

## Data provenance and access notes

- Data analyzed at multiple laboratories (e.g., Wallingford, Lancaster, Staylittle) with explicit method descriptions.
- QC and documentation sections describe method validation and accreditation considerations.
- The dataset includes explicit conversion formulas and site-specific catchment information to support reproducible GIS analyses.