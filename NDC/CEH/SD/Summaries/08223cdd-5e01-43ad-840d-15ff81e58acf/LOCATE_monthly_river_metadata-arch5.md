# Land Ocean Carbon Transfer (LOCATE) Monthly river sampling dataset

## Overview
- Multidisciplinary NERC project involving National Oceanography Centre, British Geological Survey, Centre for Ecology and Hydrology, Plymouth Marine Laboratory, with assistance from several universities and the Environment Agency.
- Aim: improve understanding of the flow of carbon from land into the ocean; this dataset focuses on land-to-river transfer (a companion dataset covers estuaries).
- Temporal and spatial scope: monthly sampling in 41 rivers across England, Scotland, and Wales from January to December 2017, with additional samples in November 2016; rivers selected to reflect different land-use types.
- Focus: geographical and seasonal variation in carbon fluxes; data collected at fixed sites, enabling cross-river comparisons and modelling inputs.

## Sampling Design and Procedures
- Sampling cadence: monthly at fixed sites, typically within a 2–3 day window each month; Dorset Stour not sampled in all months initially; coordination managed by Andy Tye (BGS).
- Experimental design shift: after a test phase, sampling sites moved to HMS sites to facilitate data integration, with EA data contributing to the modelling dataset.
- River sampling procedure highlights:
  - In-field sampling of salinity, electrical conductivity (SEC), temperature; some measurements taken in situ; sample bottles prepared and labeled in the field.
  - Samples stored in dark, cool boxes or freezers; depth sampled around 0–30 cm, mid-channel when possible.
  - Field forms completed, photos taken upstream and downstream (not submitted to EIDC but available).
  - Use of gloves and standardized collection practices to minimize contamination.
  - Sequence of sample collection designed to minimize artefacts; samples transported to institutes for specific analyses.

## Parameters and Analytes
- Measured and/or collected parameters include:
  - Physical/chemical: temperature, SEC, salinity, pH, alkalinity.
  - Nutrients: NH4-N, NO3-N, PO4-P, total nitrogen (TN), total phosphorus (TP), non-particulate organic carbon (NPOC), total dissolved carbon (TDC).
  - Organic matter and carbon: dissolved organic matter fluorescence (fDOM), absorbance, particulate organic carbon (POC), particulate organic nitrogen (PON), 13C, 15N.
  - Particulates and isotopes: POC and PON isotopes; 13C and 15N measurements.
- Molecular analyses: additional samples collected for molecular analyses to be reported separately.

## Sample Handling, Laboratory Analysis, and QC
- Sample division for analyses:
  - Particulates (POC, PON, 13C, 15N) sent to NOC.
  - Nutrients sent to CEH Lancaster.
  - pH and alkalinity to CEH Lancaster.
  - Fluorescence and absorbance to BGS Wallingford.
- Field blanks:
  - Initial field blanks used to test filter batches; not implemented at every site.
  - MQ water blanks prepared and processed by the groups responsible for subsequent analyses (BGS for fluorescence; CEH Lancaster for nutrients; NOC for POC).
- Instrumentation and methods (selected):
  - Nutrients: NH4-N, NO3-N, PO4-P measured with specified instruments (SEAL_AQ2, DIONEX_ICS2000) and methods; LODs provided.
  - Carbon and nitrogen concentrations and isotopes: measured using Flash EA 1112 with Conflo III to DeltaPlus XP; δ13C and δ15N calibrated against USGS standards (USGS40, USGS41a).
  - Quality control: ISO 17025-based methods; analyses treated as accredited for QA purposes; long-term precision metrics provided for standards (C, δ13C, N, δ15N).
  - Fluorescence and absorbance: Varian Cary Eclipse and Varian Cary 60 spectrophotometer; blanks and quinine standards used; PARAFAC modelling performed in Matlab (DOMFluor).
- Data quality assurance:
  - Approximately 5% of samples audited per run; CEH Lancaster participates in Aquacheck program for measurement accuracy.

## Data Structure, Metadata, and River Information
- River information and land cover:
  - Land cover data derived from 2015 CEH Land Cover Map (LCM 2015).
  - Calculated variables include catchment area, peat soil extent, various habitat/land-cover types, freshwater and other water body extents, and indicators such as base flow index (BFI), carbonate rocks, mean altitude.
  - Additional variables cover arable land, dry/wet habitats, various woodland types, urban areas, and rainfall (standardised annual rainfall 1961–1990).
  - Each catchment has associated identifiers and codes (e.g., NRFA code) used for linking to other datasets.
- Columns in the data file (highlights):
  - Core metadata: River_code, Date, Trip_number, Sampling_time_GMT, River_sample_ID, weather, sampler_comments.
  - Sample volumes and filtration: Number_filters_used, Volume_filtered_for_RNA, Volume_filtered_for_POC, Volume_Filtered_ml.
  - Measurements: Temperature (°C), Conductivity (µS/cm), Salinity (ppt), pH (RAW_WATER), Alkalinity (RAW_WATER), various nutrient concentrations (NH4-N, NO3-N, PO4-P), NPOC, TDC, TN, TP, PARAFAC loading components, fluorescence indices (OHNO/HIX, McKnight ratio, betalpha), absorbance (absorbance for 254 and 340 nm).
  - Isotopes and particulates: POC_delta_13C, POC_13C atom percent, PON_delta_15N, PON_15N atom percent, POC and PON masses and concentrations.
  - PARAFAC and EEM metrics: component loadings and qualitative sample comments.
  - RAW vs FILTERED data fields for each analyte, with corresponding units and method references.
- Documentation and data lineage:
  - Clear notes on sampling site changes for data integration; companion estuary dataset; planning for incorporation into modelling datasets with EA data.
  - Emphasis on data provenance, traceability, and consistency across laboratories and instruments.

## Data Management, Access, and Stewardship Considerations
- Governance: coordinated across multiple institutions with standardized sampling protocols, metadata, and QC procedures to ensure data quality and comparability.
- Standards and provenance: analyses conducted under ISO 17025-inspired methods; calibration against international reference materials; explicit documentation of analytical methods, units, and detection limits.
- Data sharing and reuse:
  - Dataset structured to support broad sharing and integration into carbon flux modelling and land-to-ocean transfer studies.
  - Companion datasets and model-ready data elements (e.g., EMS-compatible variables, PARAFAC/EEM outputs) facilitate reuse by data users and other researchers.
- Annotations for data stewards:
  - The dataset provides extensive metadata, a comprehensive variable list, and field procedures to aid governance, discovery, and repository deposit.
  - Documentation supports updates and traceable data improvements, including laboratory changes, site relocations, and methodology notes.