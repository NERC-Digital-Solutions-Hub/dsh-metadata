# Aluminum, FORM = Dissolved.

## Overview
- Comprehensive metadata and value-driven description for a long-term waterquality dataset containing dissolved analytes and hydrological data from field sites (notably Lower Hafren/L Upper Hafren catchments, with locations such as Lancaster, Wallingford, Bangor) collected between 2007 and 2009.
- Contains 30+ chemical constituents (e.g., aluminum, ammonium, arsenic, cadmium, chloride, nitrate, nitrite, sulfate, metals, nutrients, and related species) with standardized fields for form, determinations, units, detection limits, sampling windows, and analytical methods.
- Includes derived hydrological metrics (area-weighted stream flow and rainfall, hourly water fluxes) and time-alignment rules for precipitation and runoff data.

## Data structure and key fields
- For each analyte: 
  - Form (e.g., dissolved), DETERMINAND (the chemical species), UNITS, LQDC (level/quality detection), QUOTE TO (target reporting value), START/END dates, LOCATION OF ANALYSIS, ANALYTICAL METHOD QC DATA QUALIFIER, FILTRATION, PRESERVATION METHOD, METHOD, COMMENT.
  - Examples of analytes covered: Al, NH4-N, Sb, As, Ba, Be, B, Br, Cd, Cs, Ca, Ce, Cl, Cr, Co, Cu, DOC, Fe, F, Gran alkalinity, I, La, Pb, Li, Mg, Mn, Mo, Ni, NO3-N, NO2-N, pH, K, Pr, Rb, Sc, Se, Si, Na, Sr, SO4, SO4_by_ICP, S, TDN, Sn, Ti, W, U, V, Zn, plus area-weighted and flow-related metrics.
- Hydrological data:
  - Area weighted stream flow (mm/15min), Area weighted rainfall (mm), Stream flow (cumecs), Rainfall (mm), Date, Time, Hourly water fluxes (mm/hr), and derived time bases.
  - Sampling times: volume-weighted times; precipitation sampling windows defined as 7-hour intervals; notes on autosampler changes and their effect on time stamping.

## Analytical methods and QA
- Measurement techniques include:
  - Inductively Coupled Plasma Mass Spectrometry (ICP-MS) and Optical Emission Spectrometry (ICP-OES) for metals.
  - Ion chromatography (IC) for chloride, nitrate, nitrite, bromide, sulfate.
  - Automated colorimetry for ammonium (Berthelot reaction) and related tests.
  - Total organic carbon (TOC) via thermal oxidation and conductivity detection.
  - pH by electrometric method; conductivity by a lab meter.
- Sample handling:
  - Filtration: PALL Lifesciences AcroCap Filter with 0.45 µm membrane.
  - Preservation: acidification to 1% with high-purity nitric acid (or storage at 4°C, dark).
  - Start/End dates indicate analysis window coverage.
- Analytical QC:
  - QC data qualifiers and specific codes (1–5) linked to ISO 17025 accreditation status and proficiency testing.
  - Data qualifiers 10–12 indicate raw data, near-detection limits, or patterns requiring caution.
  - SOPs and procedure references (e.g., SOP 3115b, SOP 3504) are provided for traceability.

## Derived data and time handling
- Hydrology-to-chemistry integration:
  - Conversion formulas between stream flow (cumecs) and rainfall-derived rainfall depth (mm/15min) based on catchment areas:
    - mm/15min = cumecs × 0.9 / catchment area (km^2)
    - cumecs = mm/15min × (catchment area) / 0.9
  - Catchment areas given for site pairs (Lower Hafren and Upper Hafren).
- Time stamping:
  - For stream samples: date/time indicates sampling moment.
  - For precipitation samples: begin of the 7-hour interval.
  - Volume-weighted sampling times used to align precipitation and runoff data.
  - Auto-sampler timing adjustments noted (shift from 7 PM to 12 Noon on a changeover date).
- Data presentation:
  - Outputs are designed for clear reporting (reports, maps, charts) and are intended to be stored/uploaded to appropriate data portals.

## Data quality codes and qualifiers
- Analytical Method QC Codes:
  - 1–5 reflect various levels of QA validation, including ISO 17025 accreditation status and interlaboratory proficiency.
- Data Qualifier Codes:
  - 10: Raw instrument data; not rounded.
  - 11: Data at or below detection limit.
  - 12: Raw data with unusual patterns; treated with caution.

## Temporal and spatial scope
- Timeframe: primary data span from 6-Mar-2007 to 27-Jan-2009, with various analyte start/end windows.
- Locations: analysis conducted at Lancaster and Wallingford, with field analysis and data processing involving Lower Hafren (LHF), Upper Hafren (UHF), and field/stream measurement sites; some data designated as field-calculated or field-analyzed.

## Purpose and use
- Aimed at demonstrating environmental condition and policy performance over time using standardized, QA-controlled data.
- Outputs intended for clear communication through reports/maps and for integration with other datasets to enhance dataset value.
- Facilitates data sharing by documenting underlying methods, QC, and time-base conventions for reuse and scrutiny.

## Challenges and opportunities for Analysts
- Increase dataset value through integration with additional relevant datasets (e.g., climatic, land-use, or ecological indicators) rather than single-use analyses.
- Improve accessibility by enabling broader access to underlying data and metadata, supporting reproducibility and policy evaluation.