# Derwent X-ray powder diffraction (XRD) Sediment Fingerprinting

## Overview
- Study area: River Derwent Catchment, Yorkshire, UK
- Purpose: use X-ray powder diffraction (XRD) to fingerprint sediment mineralogy and support source attribution

## Methods and Data Collection
- Sample types: grab samples from different soil types and instream sediment related to bars and banks
- Field processing: samples dried, sieved, and powdered
- Instrument: Bruker D8 XRD
- Analytical approach: qualitative phases analysis to identify minerals present
- Quality control: XRD machine calibrated; data provided as raw outputs (not phase-table processed)

## Data Structure and Contents
- Data format: CSV with 2 theta values and counts
- Site and location data: each row identifies a sample site (e.g., Lower Rye u/s Derwent confluence River 1) with X and Y coordinates
- Sample naming convention: Derwent_XRD_SedimentFingerprinting_(n) and variants (e.g., (1,1), (2,0), etc.)
- Coverage: numerous sites across the catchment, including riverine, floodplain, and bank/soil locations (e.g., Jugger Howe Soil series, Spital Beck, The Beck, Black Beck, Elvington, etc.)
- Data scope: raw mineralogical signal per site via 2 theta vs. counts; no pre-identified mineral phases included in the dataset

## Data Quality and Calibration
- Calibration: instrument calibrated
- Data status: raw diffraction counts without phase-table interpretation
- Documentation note: some sections of the data listing appear garbled or truncated, but the core structure and coordinates are present

## Using the Data for Analysis
- Primary use: derive mineralogical fingerprints for sediment at each site, enabling provenance and source attribution analyses
- Analytical steps required:
  - Process raw 2 theta vs. count data to identify mineral phases (compare with standard reference patterns)
  - Link mineral fingerprints to potential sediment sources across sites
  - Integrate with spatial (coordinates) and site metadata for spatial provenance modeling
- Outputs to expect: site-level mineralogical profiles, potential correlations between geology/soil type and sediment mineralogy, and basis for source apportionment models

## Limitations and Considerations
- Dependence on additional processing to identify minerals (dataset is raw)
- Spatial completeness and site coverage may affect representativeness for catchment-wide fingerprinting
- Some data entries show formatting issues; careful data cleaning may be required before analysis
- No temporal information or hydrological context provided within the dataset