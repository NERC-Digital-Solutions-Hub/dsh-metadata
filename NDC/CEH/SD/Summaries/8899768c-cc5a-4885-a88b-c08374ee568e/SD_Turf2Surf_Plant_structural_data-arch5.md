# Plant structural measurements in North Wales and Northwest England (2013 and 2014)

## Overview
- Supplemental documentation for Turf2Surf data series; details the data structure for Plant structural measurements (North Wales and Northwest England, 2013–2014) as described in Turf2Surf_Plant_structural_data.csv.
- Notes that several related datasets share the first 9 columns, enabling cross-dataset combination and consistent metadata.

## Shared data structure across related datasets
- All share the first 9 columns:
  - A: Site Number (unique identifier)
  - B: Habitat
  - C: Habitat Description
  - D: Site name
  - E: Ecosystem Component (plant, soil, roots)
  - F: If plant, the species; otherwise NA
  - G: Plot number (1–4)
  - H: Replicate number (used when measurements are not co-located with plots)
  - I: Soil depth interval (for soil/roots components)
- Some sites were sampled for non-plant data (e.g., soil or physiological data) but not for plant structural data; structure is kept consistent to ease data merging.
- Missing values are indicated as NA, reflecting restricted depths, limited replicates, outliers, or non-sampled components.
- The dataset design aims to support easy combination across files despite partial sampling.

## Data naming conventions and trait derivation
- Variable names carry prefixes/suffixes indicating transformations and sampling decisions:
  - Beginning characters indicate transformations or exclusions (e.g., r = square-root transformed; c1 = subordinate species excluded; c = included).
  - Ending characters denote data sources for trait values: db = database means; ob = observed measured values for the two dominants substituted for database means.
- Example decoding: rc1LDMCob = square-root transformed, subordinate species excluded, Leaf Dry Matter Content, observed dominants’ trait values substituted.

## Trait data and data processing notes
- Mean abundance-weighted trait values (x_jk) for SLA and LDMC are computed for each NPP plot j within site k, using either raw or square-root transformed cover values.
- Trait values for each species are based on measured traits for dominants or sourced from published databases when not measured for dominants.
- The dataset includes 22 additional columns and 155 rows (specific to the described subset).

## Measurements, units, and additional columns
- The dataset contains a series of columns (J through AE) detailing additional measurements and derived metrics:
  - J: NPP – Annual aboveground net primary production; Unit: g dry biomass m^-2 yr^-1
  - K: lnNPP – Natural log of NPP
  - L, M: Canopy height (rcht, rcht1) with square-root transformations
  - N, O: Bryophyte cover (rBcov, rBcov1) with square-root transformations
  - P–AE: Various trait-related columns for LDMC and SLA (db vs ob; transformed vs untransformed; for both leaf-level and cover-based representations)
- Each column’s description specifies whether it reflects database values only or observed/measured values, and whether the data are square-root transformed or untransformed.
- NA in these columns indicates measurements not performed for that site.

## Data governance and usability considerations
- The structure supports interoperability and combined analyses across multiple related datasets (plant structure, biomass, soil properties, physiology) by maintaining consistent first-9-column schema.
- Clear encoding of data provenance (db vs ob) and transformation status enhances data discoverability, reproducibility, and appropriate reuse.
- Missing or restricted data are explicitly indicated, guiding dataset curators and data stewards in data completeness assessments and in communicating limitations to users.