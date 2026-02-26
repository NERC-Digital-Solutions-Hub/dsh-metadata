# Supporting documentation for 15-Animal_Feed_Stable.csv

- This document provides metadata for the 15-Animal_Feed_Stable.csv dataset, which records concentrations of multiple elements in animal feed samples collected at various locations and associated feeding regimes.
- Key purpose is to enable data quality assessment, proper interpretation of concentrations, and integration into map-based data products for GIS analyses.

## Purpose and scope

- Describes the data fields, including sample identifiers (Animal), sampling context (Location, Feeding), and measured chemical concentrations.
- Focuses on stable element concentrations in the total diet on a dry mass basis, with accompanying uncertainty and detection-limit information.
- Supports map-based visualization and spatial analysis when combined with location geometry.

## Key variables and data structure

- Identifying fields
  - Animal: general type of animal
  - Location: name of location where the sample was collected
  - Feeding: description of the feeding regimes
- Measured elements (concentration in mg per kg dry mass unless noted)
  - Cs_mg/kg_dm
  - Sr_mg/kg_dm
  - K_mg/kg_dm
  - Na_mg/kg_dm
  - Ca_mg/kg_dm
  - Mg_mg/kg_dm
  - P_mg/kg_dm
  - Pb_mg/kg_dm
  - U_mg/kg_dm
  - Th_mg/kg_dm
- Associated quality and detection fields (for each element)
  - Unc_[element]_mg/kg_dm: Uncertainty (quadratic propagation) of the concentration
  - Detection_Limit_[element]_mg/kg_dm: Detection limit for the concentration
  - Notes indicate: if a concentration value is blank, the measurement was below the detection limit
- Special formatting notes
  - Na_mg/kg_dm section and several Unc_Na_mg/kg_dm and Detection_Limit_Na_mg/kg_dm fields include atypical labeling (e.g., numeric prefixes) in some entries, indicating potential formatting inconsistencies to resolve during data cleaning
  - Some entries explicitly state “Where blank, then concentration was below the detection limit” for detection-limit fields

## Data quality and interpretation notes

- Non-detects: Blank values in concentration fields indicate concentrations below the detection limit; corresponding Unc and Detection_Limit fields provide context where available.
- Measurement uncertainty: Unc_[element] fields provide the uncertainty associated with each concentration value.
- Detection limits: Detection_Limit_[element] fields indicate the threshold below which measurements are not detected; blank detection-limit fields imply the value is above detection limit.
- Data standardization needs: Units are consistently mg/kg dry mass, but irregular naming in some Na-related fields suggests a need for careful parsing and standardization before GIS integration.

## GIS usage guidance

- Spatial integration
  - Location provides a textual location name to be joined with a spatial layer (e.g., a shapefile or geodatabase) containing coordinates for mapping.
  - A separate spatial join is required to map samples to precise coordinates; Location alone is not a geometry.
- Visualization strategies
  - Map concentrations by element (e.g., Cs, Sr, K, Na, Ca, Mg, P, Pb, U, Th) across locations.
  - Use color scales or graduated symbols for concentration values; consider separate layers per element or interactive toggles.
  - Represent uncertainty with transparency or error bars where appropriate; use Detection_Limit fields to classify non-detects.
- Data conditioning for maps
  - Standardize units to mg/kg dry mass if needed.
  - Convert or harmonize Na-related fields due to inconsistent labeling to ensure all Na data are correctly interpreted.
  - Create flags for non-detects (e.g., concentration = null or a dedicated non-detect indicator) using the detection-limit rules.
  - Document data provenance and processing steps when creating spatial products.

## Recommendations and best practices

- Data cleaning
  - Normalize field names and ensure consistent handling of Na-related entries.
  - Validate that all concentration, Unc, and Detection_Limit fields align correctly for each element per row.
- Metadata and provenance
  - Capture the sampling context (Animal, Location, Feeding) alongside measurements to enable context-aware GIS analyses.
  - Maintain a data quality sheet describing how non-detects and uncertainties were derived.
- GIS workflows
  - Join the dataset to a spatial layer by Location, then create element-specific thematic maps.
  - Use detection limits to annotate non-detect observations and communicate data limits clearly in maps and reports.
- Communication with end-users
  - Provide clear legend explanations for concentration ranges, detection limits, and uncertainty.
  - Document any data cleaning steps and assumptions made during the GIS processing pipeline.