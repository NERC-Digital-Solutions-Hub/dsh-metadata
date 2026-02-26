# Details of data structure for the dataset Plant structural measurements in North Wales and Northwest England (2013 and 2014) as detailed in the table Turf2Surf_Plant_structural_data.csv

- Overview
  - Supplement to the supporting documentation for Turf2Surf data series.
  - Describes the data structure for Plant structural measurements (North Wales and Northwest England, 2013 and 2014) and related datasets.
  - Aims to facilitate combining related datasets by keeping a common structure.

- Datasets sharing the first 9 columns
  - Plant structural measurements in North Wales and Northwest England (2013 and 2014)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014)
  - Soil carbon data in the Conwy catchment in North Wales (2013 and 2014)
  - Soil physical, chemical and biological measurements in the Conwy catchment in North Wales (2013 and 2014)
  - Plant physiological measurements in North Wales and Northwest England (2013, 2014 and 2016)
  - Plant aboveground and belowground standing biomass measurements in the Conwy catchment in North Wales (2013 and 2014)
  - NA values indicate missing data due to restricted depths, limited replicates, or other sampling limits.

- Key shared columns (A–I)
  - A: Site Number (unique identifier; as introduced in Table 1 of supporting documentation)
  - B: Habitat
  - C: Habitat Description (more detailed)
  - D: Site name
  - E: Ecosystem Component (plant, soil, or roots)
  - F: If Component is 'Plant', species name; otherwise 'NA'
  - G: Plot number (1–4)
  - H: Replicate number (used when photosynthesis measurements were not co-located with plots)
  - I: Soil depth interval (for soil and roots components)

- Data completeness and structure
  - Missing values indicated as 'NA' (data not available)
  - Some sites sampled for soil or physiological data but not for plant structural data (and vice versa)
  - Structure kept similar across related files to ease combining datasets

- Variable naming conventions and data transformations
  - Beginning characters indicate data transformations or inclusion rules (e.g., square-root transformed, r; subordinate species exclusion; c1 vs c)
  - End-of-name indicators denote data origin:
    - db: database mean trait values only
    - ob: measured trait values substituted for the two dominant species in each plot
  - Examples:
    - rc1LDMCob: square-root transformed Leaf Dry Matter Content, subordinate species excluded, measured traits for dominants included
    - rc1SLAdb: square-root transformed Specific Leaf Area, subordinate species excluded, database values only
  - Many variables reflect derived metrics based on species' trait values and plot-level cover data

- Trait data and calculations
  - Mean abundance-weighted trait values (x_jk) for SLA and LDMC computed per NPP sampling plot j within site k
  - Uses either raw percentage cover or square-root transformed cover (pijk) for species i in plot j at site k
  - Trait values (τ_ijk) come from replicated measurements on dominants or from published databases if not dominants
  - The dataset includes 22 additional columns (beyond the first 9) and 155 rows

- Key variables and measurements included (selected examples)
  - J: NPP (annual aboveground net primary production) — units: g dry biomass m^-2 yr^-1
  - K: lnNPP — natural log of NPP
  - L: rcht — canopy height (square-root transformed)
  - M: rcht1 — canopy height (square-root transformed, subordinate species excluded)
  - N / O: rBcov / rBcov1 — bryophyte cover (square-root transformed)
  - P / Q: rc1LDMCdb / rc1LDMCob — LDMC (square-root transformed; subordinate species excluded; database or measured dominants)
  - R / S / T / U / V / W: SLA and LDMC related metrics (subordinate species excluded or dominants included; database or observed values)
  - NA indicates sites where certain measurements were not performed

- Notes on usage
  - The structure enables straightforward merging with related datasets (soil, biomass, physiological measurements)
  - Care should be taken with NA values and the db/ob distinctions when aggregating or imputing traits
  - Applies to data from the Conwy catchment in North Wales and broader North Wales and Northwest England regions (years 2013 and 2014, with some 2016 data in related datasets)