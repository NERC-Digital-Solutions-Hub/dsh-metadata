# Partial river flow recovery with forest age is rare in the decades following establishment

## Overview
- A dataset produced from a systematic literature review addressing how forest age affects river flow response after forestation.
- Compiles annual river flow changes with forestation, comparing forested catchments to control data, along with rich metadata from primary and secondary sources.
- Authors: Laura Bentley and David A. Coomes (Department of Plant Sciences, University of Cambridge); produced 2018–2019, published 2020.
- Acknowledgement: Bentley, L. & Coomes, D. (2020) Global Change Biology. DOI 10.1111/gcb.14954.

## Data assets and access
- Available via the EIDC catalogue.
- Two associated CSV files:
  - Forestation_RR_Bibliography.csv: bibliographic data for the studies used.
  - Forestation_RR_EffectSize.csv: extracted dataset with effect-size related variables.
- Variable descriptions:
  - Table 1: bibliographic data variables (e.g., Source_ID, Author, Title, Source, Year, DOI).
  - Table 2: effect-size data variables (e.g., Catchment_ID, Area_km2, MAP, Prior_LC, Forest_Type, Establishment, Graphical_Extracted, Modified_Data, Year, P_mm, CQ_mm, TQ_mm, RR_mm, RR_PD, etc.).

## Scope and data content
- Timeframe and search: literature search in Web of Science (1900–Jan 4, 2018).
- Inclusion criteria: studies on forestation effects on river flow over time; comparisons between forested catchments and control data; hydrologically independent catchments; longest time-series when multiple sources exist.
- Study yield: 567 unique data sources screened; 43 unique catchment experiments met strict inclusion criteria.
- Data extraction: for each experiment, four data categories were captured:
  - Catchment descriptors (e.g., area, MAP, prior land cover and use).
  - Treatment descriptors (e.g., forest type, establishment year).
  - Experiment descriptors (e.g., treatment duration, control data method).
  - Experimental data (e.g., time since first planting, area forested per year, control and forested river flow, precipitation, hydrological year).
- Forest age handling: calculated as an area-weighted mean to reflect non-uniform establishment.
- Data provenance: primary sources and, where applicable, data from papers reviewed by Farley et al. (2005).
- Data extraction methods: where needed, data from figures were digitized (PlotDigitizer).

## Data processing and calibration
- Climate data: when not reported, precipitation and climate metrics (CRU TS4.3) were extracted for each catchment location.
- Catchment geography: extents digitized; if unavailable for some cases, a representative circle of equal area was used; in one case, data were taken directly from the catchment location.
- Data cleaning and alignment: control river flow data were sometimes calibrated to be comparable with forested data using linear regression against precipitation or forested river flow, depending on study design.
- Calibration and correction details: Table 4 outlines four calibration regimes (single catchment or paired catchments; with or without pre-forestation data) and the calibration/prediction methods used to adjust control data; the regression approaches are selected based on the highest adjusted R^2.
- Data quality and limitations: data extraction from graphs introduces potential measurement error; some adjustments rely on historic relationships between precipitation and river flow.

## Access, usage, and citation
- Data usage: dataset designed to support analyses of how forest age influences river flow response post-forestation.
- Citation: Bentley, L. & Coomes, D. (2020) Partial river flow recovery with forest age is rare in the decades following establishment. Global Change Biology. DOI 10.1111/gcb.14954.
- Original sources and metadata are documented in the two CSV files; additional methodological details are described in the associated publication and Tables 1–4 within the dataset documentation.