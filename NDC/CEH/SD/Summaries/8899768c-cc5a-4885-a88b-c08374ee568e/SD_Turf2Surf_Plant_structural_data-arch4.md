# Details of data structure for the dataset Plant structural measurements in North Wales and Northwest England (2013 and 2014) as detailed in the table Turf2Surf_Plant_structural_data.csv

## Overview
- Supplement to the Turf2Surf WP2 supporting documentation; describes the data structure for Plant structural measurements in North Wales and Northwest England (2013–2014).
- Related datasets share the first 9 columns and include plant aboveground/belowground biomass (Conwy catchment, 2013–2014), soil carbon (Conwy, 2013–2014), soil physical/chemical/biological data (Conwy, 2013–2014), and plant physiological data (North Wales & NW England, 2013, 2014, 2016).
- The structure is kept consistent across related files to enable easy combination and cross-dataset analyses.

## Core data structure and common columns
- The datasets share the first 9 columns:
  - A: Site Number (unique identifier)
  - B: Habitat
  - C: Habitat Description
  - D: Site name
  - E: Ecosystem Component (plant, soil, or roots)
  - F: Plant species (for plant components) or NA (for soil/root)
  - G: Plot number (1–4)
  - H: Replicate number (used when measurements are not co-located with plots)
  - I: Soil depth interval (for soil/root components)
- Missing values are indicated as NA (e.g., restricted soil depths, limited replicates, or outliers).
- Some sites were sampled for non-plant data (e.g., soil) but not for plant structural data; those data are available in related datasets.
- The consistent structure facilitates combining datasets across components and years.

## Variable naming conventions and examples
- Variable names begin with indicators of transformation or data origin:
  - r: square-root transformed data (e.g., rBcov, rc1SLAob)
  - c1: subordinate species excluded (or included if not present)
  - c: subordinate species included
- Suffixes db or ob indicate data origin:
  - db: database mean trait values only
  - ob: measured trait values for dominants substituted for database means
- Example decoding: rc1LDMCob
  - r: square-root transformed
  - c1: subordinate species excluded
  - LDMC: Leaf Dry Matter Content
  - ob: measured traits for dominants included
- The dataset includes 22 additional columns (J–W, X–AE) and 155 rows for the extended NPP-related data described below.

## Extended NPP-related data (additional columns)
- The dataset adds 22 columns and 155 rows for extended measurements (labels J, K, L, M, N, O, P–AE):
  - J: NPP (Net Primary Production), unit: g dry biomass m^-2 yr^-1
  - K: lnNPP (natural log of NPP)
  - L: rcht (square-root transformed canopy height)
  - M: rcht1 (square-root transformed canopy height, subordinate species excluded)
  - N: rBcov (square-root transformed bryophyte cover)
  - O: rBcov1 (square-root transformed bryophyte cover, subordinate species excluded)
  - P: rc1LDMCdb (LDMC, database values only, broken out as square-root transformed cover)
  - Q: rc1LDMCob (LDMC, measured traits for dominants included)
  - R, S, T, U, V, W: additional SLA/LDMC combinations with db/ob variants (transformed)
  - X–AE: untransformed cover variants for LDMC and SLA with subordinate species excluded or included
- The 22 columns describe transformed and db/ob variants for key traits such as LDMC, SLA, and related covers, enabling nuanced analyses and cross-checks with database means versus on-site measurements.
- NA indicates measurements not performed for that site within these extended variables.

## Data quality, coverage, and integration notes
- Temporal scope: plant structural data (2013–2014); additional plant biomass, soil, and physiological data span 2013–2014 (with 2016 for some plant physiology).
- Some sites lack data for certain components (e.g., plant data absent but soil data present); structure allows these gaps without breaking joins across datasets.
- Data are designed to be easily combined, using the common 9-column core as the join key, with extended trait columns (J–AE) providing richer, trait-level detail.
- Missing depths, limited replicates, and outliers are flagged as NA, signaling data quality considerations during analysis.
- Some trait values derive from published databases (db) or from measured values substituted for dominants (ob), enabling traceability of data provenance and methodological differences.

## Provenance, scope, and governance considerations for Data Leaders
- Clear metadata on sampling context (site, habitat, plot, replicate) and depth intervals supports data discoverability and reproducibility.
- The explicit coding scheme (transforms, inclusion/exclusion of subordinate species, and db vs ob origins) supports reproducible data processing and transparent analytics.
- The dataset is structured to support cross-dataset analyses across plant structure, biomass, soil properties, and plant physiology, aligning with data governance goals around interoperability, discoverability, and reusability.
- Where to source updates or additional columns (e.g., continued NPP or trait measurements) should follow the same 9-core-column schema to maintain joinability across datasets.