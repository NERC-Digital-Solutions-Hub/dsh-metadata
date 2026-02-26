# This document is a supplement to the supporting documentation for data series detailed in: Turf2Surf_WP2_Supporting_documentation.rtf

- Purpose and scope
  - Provides data-structure details for Turf2Surf datasets (plant, soil, and physiological measurements) collected in North Wales and Northwest England (2013–2016).
  - Aims to clarify how data are organized to facilitate combination, reuse, and scrutiny in monitoring frameworks.

- Datasets described and shared structure
  - Plant structural measurements (North Wales & NW England, 2013–2014)
  - Plant aboveground and belowground standing biomass in the Conwy catchment (2013–2014)
  - Soil carbon data in the Conwy catchment (2013–2014)
  - Soil physical, chemical and biological measurements in the Conwy catchment (2013–2014)
  - Plant physiological measurements in North Wales & NW England (2013, 2014, 2016)
  - All datasets share the first 9 columns to enable cross-dataset integration:
    - Column A: Site Number
    - Columns B–D: Habitat, Habitat Description, Site name
    - Column E: Ecosystem Component (plant, soil, or roots)
    - Column F: If Component is Plant, the plant species; otherwise NA
    - Columns G–H: Plot number and Replicate number
    - Column I: Soil depth interval (for soil and roots)
  - Missing values indicated as NA; some sites are sampled for some data types but not others. Structure kept consistent to ease data combination.

- Metadata, naming conventions, and data provenance
  - Variable names encode data transformations and inclusion/exclusion rules:
    - Leading characters indicate transformation: r = square-root transformed data; untransformed otherwise
    - Subordinate species handling: c1 = subordinate species excluded; c = included
    - Trailing suffixes indicate data origin or substitution: db = database trait values only; ob = measured traits for the two dominant species substituted for database means
  - Example: rc1LDMCob = square-root transformed Leaf Dry Matter Content, subordinate species excluded, measured traits for dominants included
  - These conventions support traceability of how trait values were derived and make datasets comparable across sites and studies

- Trait calculation and data integration
  - Mean abundance-weighted trait values (x_jk) are computed per plot per site using either raw or square-root transformed cover values
  - Trait values (τ_ijk) come from replicated measurements on dominants or from published databases
  - The dataset includes 22 additional columns beyond the initial 9, totaling 155 rows, to capture derived metrics and transformed trait data

- Columns and derived metrics
  - J: NPP (annual aboveground net primary production) in g dry biomass m^-2 yr^-1
  - K: lnNPP (natural log of NPP)
  - L, M: canopy height (square-root transformed; with and without subordinate species excluded)
  - N, O, P, Q, R, S, T, U, V, W, X, Y, Z, AA, AB, AC, AD, AE: various transformed and untransformed trait and cover metrics
    - Examples include bryophyte cover (rBcov, rBcov1), LDMC (LDMCdb, LDMCob, c1LDMCdb, c1LDMCob), SLA (SLA variants), and related transformations
  - NA entries indicate that a given site did not have the corresponding measurement

- Data availability and governance notes
  - NA denotes measurements not performed for a site
  - Designed to support integration across data files while clearly indicating data gaps, aiding transparency and governance for monitoring frameworks

- Relevance for monitoring framework authors
  - Demonstrates a standardized data structure that enhances data sharing, consistency, and cross-study synthesis
  - Addresses common governance challenges: metadata clarity, data provenance, transform/tracking rules, and explicit data gaps
  - Facilitates transparent reporting, quality checks, and the presentation of findings through consistent formats (e.g., reports, charts, dashboards)