# Details of data structure for the dataset Plant structural measurements in North Wales and Northwest England (2013 and 2014) as detailed in the table Turf2Surf_Plant_structural_data.csv

- Purpose and context
  - Supplement to the supporting documentation for Turf2Surf data series (Turf2Surf_WP2_Supporting_documentation.rtf).
  - Documents the data structure for Plant structural measurements in North Wales and Northwest England (2013 and 2014) and related datasets.
  - Aimed at enabling data combination and consistent analysis across related datasets.

- Datasets sharing a common structure
  - The following datasets share the first 9 columns:
    - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
    - Plant aboveground and belowground standing biomass in the Conwy catchment (2013 and 2014)
    - Soil carbon data in the Conwy catchment (2013 and 2014)
    - Soil physical, chemical and biological measurements in the Conwy catchment (2013 and 2014)
    - Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)
    - Plant aboveground and belowground standing biomass in the Conwy catchment (2013 and 2014)
  - This shared structure facilitates merging and cross-dataset analyses.

- Common columns (A–I)
  - Column A: Unique Site Number (as in Table 1 of the supporting documentation).
  - Column B: Habitat.
  - Column C: Habitat Description.
  - Column D: Site name.
  - Column E: Ecosystem Component (plant, soil, or roots).
  - Column F: If Component is Plant, the plant species; otherwise NA.
  - Column G: Plot number (1–4 possible).
  - Column H: Replicate number (used when co-located measurements vary by dominant species).
  - Column I: Soil depth interval (for soil and roots components).

- Missing data and sampling notes
  - Missing values marked as NA (e.g., restricted depths, limited replicates, or outliers).
  - Some sites were not sampled for plant structural data but were sampled for soil or physiological data (and can be found in the related datasets).
  - Structure kept consistent across files to ease combination and comparison.

- Naming conventions and data derivation (variables)
  - Variable names may begin with r to indicate square-root transformed data.
  - c1 indicates subordinate species excluded; c indicates subordinate species included.
  - Suffixes db or ob indicate data derivation:
    - db = database mean values only.
    - ob = measured values for the two highest-cover species substituted for database means.
  - Example: rc1LDMCob = square-root transformed (rc) + subordinate species excluded (c1) + Leaf Dry Matter Content (LDMC) + observed/measured traits for dominants substituted (ob).

- Trait data and computations
  - Mean abundance-weighted trait values (x_jk) for SLA and LDMC computed per NPP sampling plot within each site.
  - Uses either raw percentage cover or square-root transformed cover values (p_ijk) for species i in plot j, site k.
  - Trait values (τ_ijk) come from replicated measurements on dominants or from published databases; if dominants’ traits are measured, they may be substituted for database means (ob).

- Additional columns beyond the first 9 (NPP-related data)
  - The dataset includes 22 additional columns and 155 rows.
  - J: NPP (Annual aboveground net primary production) - units: g dry biomass m^-2 yr^-1.
  - K: lnNPP - units: g dry biomass m^-2 yr^-1; description: natural log of NPP.
  - L: rcht - canopy height, square-root transformed - units: cm.
  - M: rcht1 - canopy height with subordinate species excluded - units: cm.
  - N: rBcov - Bryophyte cover, square-root transformed - units: % (0.5).
  - O: rBcov1 - Bryophyte cover, subordinate species excluded - units: % (0.5).
  - P–AE (multiple columns): various LDMC and SLA measures under different derivation schemes (db vs ob; rc1, c1, c, etc.), with both transformed and untransformed forms where applicable.
  - Examples include:
    - rc1LDMCdb, rc1LDMCob
    - rc1SLAdb, rc1SLAob
    - rcLDMCdb, rcLDMCob
    - rcSLAdb, rcSLAob
    - c1LDMCdb, c1LDMCob
    - c1SLAdb, c1SLAob
    - cLDMCdb, cLDMCob
    - cSLAdb, cSLAob
  - X–AE denote transformed or untransformed cover measures and trait values, with naming reflecting the combination of (transformation, exclusion, trait, and data source).
  - NA values indicate sites where that measurement was not performed.

- Data provenance and usage
  - Structured to support integration with related Turf2Surf datasets and facilitate monitoring of environmental health and policy performance over time.
  - Standardized fields and explicit derivation rules enable transparent re-use and cross-site analyses.
  - Data should be stored and uploaded to the appropriate data portals as part of routine environmental data management.

- Practical notes for analysts
  - Carefully decode variable names to understand transformations, inclusion/exclusion of subordinate species, and whether values are from databases or measured dominants.
  - Expect incomplete data across sites for some variables; plan analyses accordingly (e.g., use NA-aware methods or imputation where appropriate).
  - The shared first-9-column structure supports merging across plant, soil, and physiological datasets for comprehensive environmental assessments.