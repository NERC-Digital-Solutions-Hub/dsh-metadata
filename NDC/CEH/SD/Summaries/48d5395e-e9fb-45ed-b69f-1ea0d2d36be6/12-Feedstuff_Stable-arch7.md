# Supporting documentation for 12-Feedstuff_Stable.csv

## Overview
- Metadata description for the 12-Feedstuff_Stable.csv dataset.
- Captures per-sample information: identifier, sample type/description, collection location, collection date, and sample size.
- Includes multi-element measurements for stable elements (Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th) on a dry mass basis, plus uncertainty and detection limit fields.
- Units: concentrations in mg/kg dry mass; sample_size in g fresh matter; Collection_Date in dd-mm-yyyy.
- Some fields include notes indicating values below detection limit; there are formatting inconsistencies in some field names.

## Dataset Structure and Key Fields
- Core metadata fields:
  - Sample_Code (unique sample identifier)
  - Sample_Type (general description of the sample group)
  - Location (location name where the sample was collected)
  - Sample_Description (part of the organism analysed)
  - Collection_Date (date of collection; dd-mm-yyyy)
  - Sample_size (amount of sample analyzed; units: g fresh matter)
- Measurements (per element):
  - Cs_mg/kg_dm, Unc_Cs_mg/kg_dm, Detection_Limit_Cs_mg/kg_dm
  - Sr_mg/kg_dm, Unc_Sr_mg/kg_dm, Detection_Limit_Sr_mg/kg_dm
  - K_mg/kg_dm, Unc_K_Mg/kg_dm, Detection_Limit_K_mg/kg_dm
  - Na_mg/kg_dm, Unc_Na_mg/kg_dm, Detection_Limit_Na_mg/kg_dm
  - Ca_mg/kg_dm, Unc_Ca_Mg/kg_dm, Detection_Limit_Ca_mg/kg_dm
  - Mg_mg/kg_dm, Unc_Mg_mg/kg_dm, Detection_Limit_Mg_mg/kg_dm
  - P_mg/kg_dm, Unc_P_mg/kg_dm, Detection_Limit_P_mg/kg_dm
  - Pb_mg/kg_dm, Unc_Pb_mg/kg_dm, Detection_Limit_Pb_mg/kg_dm
  - U_mg/kg_dm, Unc_U_mg/kg_dm, Detection_Limit_U_mg/kg_dm
  - Th_mg/kg_dm, Unc_Th_mg/kg_dm, Detection_Limit_Th_mg/kg_dm
- Notes on data quality fields:
  - Unc_* fields represent combined uncertainty (where provided)
  - Detection_Limit_* fields indicate the detection limit; blank values typically mean below detection limit
  - Some field names contain typographical inconsistencies (e.g., Unc_K_Mg/kg_dm) that may require normalization

## Temporal and Spatial Dimensions
- Spatial: Location field provides a place name; no explicit coordinates included in this documentation.
- Temporal: Collection_Date is recorded per sample; format dd-mm-yyyy.
- GIS implication: geocode Location values to obtain coordinates; consider linking to a spatial reference layer for mapping.

## Measurements, Units, and Quality Flags
- Concentrations are reported on a dry mass basis (mg/kg_dm).
- Sample_size is given in g fresh matter (distinct from the dry-mass basis used for concentrations).
- Below-detection-limit values are indicated by blank Unc or detection-limit fields; handle as left-censored data in analyses/maps.
- Some inconsistencies in field naming and formatting may require data cleaning prior to ingestion into GIS workflows.

## Data Quality and Standardization Considerations for GIS
- Data may originate from multiple sources with non-uniform standards.
- Missing data at appropriate resolutions; some elements may have no reported value or uncertainty.
- Ingested data should be harmonized (unit normalization, field-name standardization) before geospatial analysis.
- Address formatting issues in field names to prevent import errors (e.g., unify capitalizations and remove typos).

## GIS Use Scenarios and Best Practices
- Mapping possibilities:
  - Visualize element concentrations by Location using color scales or graduated symbols.
  - Create time-enabled maps if Collection_Date data are available across samples.
  - Separate maps by element or create a multi-element dashboard.
- Handling detection limits and uncertainties:
  - Mark below-detection-limit values explicitly (e.g., using a symbol or annotation).
  - Consider representing Unc_* as an uncertainty layer or as error bars where appropriate.
- Data preparation tips:
  - Geocode Location to coordinates; add a spatial layer for mapping.
  - Clean and standardize field names (e.g., Cs_mg/kg_dm, Sr_mg/kg_dm) for consistent GIS imports.
  - Maintain a metadata appendix describing data provenance and processing steps.

## Challenges and Limitations
- Data distributed across multiple sources; may lack standardized metadata across fields.
- Missing or censored data (below DL) complicate quantitative mapping and analysis.
- Absence of explicit coordinates requires geocoding, which may introduce spatial uncertainty.
- Inconsistent field naming requires careful data cleaning prior to GIS use.

## Practical Next Steps for GIS Analysts
- Geocode Location values to obtain coordinates; attach to a spatial feature layer.
- Normalize and clean column names and units to a consistent schema.
- Compile a per-sample dataset with coordinates, collection date, sample size, and element measurements.
- Create element-specific maps (or a dashboard) showing concentrations with uncertainty and DL indicators.
- Document data provenance and any assumptions used to handle below-detection values in the GIS product.