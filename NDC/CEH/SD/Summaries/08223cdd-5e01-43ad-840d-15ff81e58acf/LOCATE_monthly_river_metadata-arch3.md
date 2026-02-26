# Land Ocean Carbon Transfer (LOCATE) Monthly river sampling dataset

## Overview
- Multidisciplinary NERC project aimed at understanding how carbon moves from land to the ocean, focusing on flow from land to rivers; companion estuary dataset exists.
- Involves multiple UK institutions (National Oceanography Centre, British Geological Survey, Centre for Ecology and Hydrology, Plymouth Marine Laboratory, and universities) with coordination to collect and integrate data.
- Dataset covers 41 rivers across England, Scotland, and Wales, with monthly sampling during 2017 (and November 2016 for a trial), designed to capture geographic and seasonal variation in carbon fluxes.
- Rivers selected to reflect diverse land-use types; sampling coordination aimed at data integration, with a shift to HMS sites to improve dataset compatibility with EA modelling data.

## Data collected and parameters
- Core riverine measurements: temperature, specific electrical conductivity (SEC), salinity, pH, alkalinity, nutrients (NH4-N, NO3-N, PO4-P, total nitrogen, total phosphorus), dissolved/particulate carbon and nitrogen (NPOC, TDC, POC, PON), and stable isotopes (13C, 15N).
- Additional optics and colour proxies: dissolved organic matter fluorescence (fDOM) and absorbance.
- Molecular analyses planned for separate reporting.
- Particulates and nutrient/pH/alkalinity samples collected and analyzed at designated laboratories; various QA steps embedded.

## Sampling design and field procedures
- Monthly sampling at fixed river sites throughout 2017 (with most within tight 2–3 day windows per month); one site (Dorset Stour) began in April 2017.
- Field sampling performed with careful handling to preserve sample integrity (dark storage, coolers/freezers, field forms, weather/river condition notes, and photos upstream/downstream when possible).
- Sampling protocol includes standardized bottle types and volumes for different analyses, stepwise handling to avoid contamination, and sub-sampling in the field for various analyses.
- A subset of sites migrated to HMS sites to enhance data integration with EA datasets.

## Quality assurance and data governance
- Field blanks implemented selectively (not at every site) to test batch cleanliness for each sample type; blanks managed by the respective analytical groups.
- Routine QA/QC includes approximately 5% of samples checked per run; CEH Lancaster participates in Aquacheck for measurement accuracy.
- Analyses conducted under UKAS ISO 17025-like standards; analyses treated as accredited where applicable, with explicit calibration materials and reference standards for isotopes.
- Long-term precision benchmarks provided for QC standards (e.g., carbon, nitrogen, δ13C, δ15N) to ensure data reliability.
- Instrumentation and calibration details documented to support traceability and reproducibility, including isotope ratio mass spectrometry setups and fluorescence/absorbance instrumentation.

## Laboratory instrumentation and analytical methods
- Isotopes and elemental analysis: Flash EA 1112 coupled to isotope ratio mass spectrometer (Conflo III); δ13C and δ15N normalized to USGS reference materials.
- Carbon/Nitrogen concentrations and isotopes measured per specified UKAS ISO 17025 methods; results reported as mass percentages and isotope ratios.
- Fluorescence and absorbance measurements: Varian Cary Eclipse (fluorescence) and Varian Cary 60 UV–vis (absorbance); blank and quinine sulfate standards used for QA; PARAFAC modelling for fluorescence components (via Matlab DOMFluor).
- Absorbance data collected across 200–800 nm; Raman units used for fluorescence results; absorbance units in cm^-1.

## Data structure, content, and river context
- Data file columns include site identifiers, date, sampling time, volumes filtered, temperature, conductivity, salinity, various nutrient concentrations (NH4-N, NO3-N, PO4-P, TN, TP), alkalinity, pH, NPOC, TDC, POC/PON, isotopic data (δ13C, δ15N), fluorescence/absorbance metrics, PARAFAC components, and QA/QC flags.
- Detailed metadata on sampling conditions, weather, river flow/level, and field notes are captured to accompany measurements.
- River catchment and landscape context drawn from CEH Land Cover Map (LCM 2015) and related datasets, including:
  - Catchment area, standardised rainfall, peat soil presence, arable/horticulture, various habitat types (bog, grasslands, woodlands), freshwater extent, and land cover class mappings.
  - Hydrological and geological context: Base Flow Index (BFI), carbonate rock presence, mean altitude.
- Derived and contextual variables prepared to support interpretation of carbon and nutrient fluxes in relation to land cover and catchment characteristics.

## Data accessibility and integration
- Outputs are designed to support monitoring frameworks and policy evaluation, providing clear data lineage from field collection through laboratory analyses to derived variables and catchment context.
- A companion estuary dataset exists, and broader integration is planned with partner datasets (e.g., EA modelling datasets) to enhance interpretation and policy-relevant analyses.
- Some results (e.g., molecular analyses) are planned for reporting separately, indicating staged data release and use.

## Practical relevance for monitoring frameworks
- Demonstrates a structured, standardized approach to monitoring riverine carbon and nutrient fluxes across multiple catchments, enabling cross-site comparability.
- Emphasizes robust QA/QC, metadata richness, and traceable instrumentation/calibration, aligning with governance needs for data quality, transparency, and reproducibility.
- Provides a comprehensive data schema and rich environmental context to inform policy evaluation, environmental health assessments, and future monitoring design.
- Highlights governance considerations, including data sharing practices, transparency of underlying data, and explicit decisions on data integration across organisations to overcome silos.