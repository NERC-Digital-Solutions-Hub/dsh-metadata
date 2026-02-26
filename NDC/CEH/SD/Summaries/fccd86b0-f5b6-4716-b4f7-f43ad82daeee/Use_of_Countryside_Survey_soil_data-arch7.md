# Countryside Survey Soils 2007: Method development, power analyses and protocols.

- Overview
  - Document describes the sampling design, measurement methods, statistical considerations, and data structure for Countryside Survey (CS) soils data, focusing on 2007 sampling and its relation to earlier surveys (1978, 1998).

- Sampling design and location
  - Years and squares:
    - 1978 and 1998: the same 256 CS squares were sampled.
    - 2007: soils sampled from all 591 CS squares.
  - Sampling units:
    - Within each CS square, 5 x-plots are randomly spaced; x-plots are not replicates due to potential land-use and soil-type variation.
  - Plot relocation:
    - X-plots may be relocated over time (e.g., land use change, access issues). Each location has a unique repeat identifier (e.g., 2RPT1). Same identifier indicates the same location, though precise sampling points may shift ~2–3 m around a permanently marked 2 m × 2 m plot.
  - Data coverage:
    - 2007 included measurements from all 591 squares, with some measurements not made on all samples.

- Field sampling and measurements
  - Sampling depth and method:
    - Top 15 cm of soil are sampled (8 cm for invertebrates); 1998/2007 used soil cores hammered in and extracted; 1978 used a soil pit.
    - Some cores could not be fully collected due to stones or shallow soils.
    - 2007 included core dimension measurements and photographs for selected cores.
  - Measurements by year:
    - 1978: laboratory measurements limited to pH and loss-on-ignition (LOI).
    - 1990: some soil mapping conducted.
    - 1998 and 2007: multiple cores per x-plot; different cores carry different measurements (see Table 1).
    - Bulk density measured in 2007 (not via ISO whole-core method).
  - Data release notes:
    - Some data (indicated with asterisk) were released only after the Soils Report published November 2009.
  - Core sampling details:
    - Data tables show measurements across various core types (e.g., black and white cores with differing depths and IDs).

- Data structure and coverage
  - Measurements and cores:
    - Measurements include pH (in water and CaCl2), LOI, %C, %N, bulk density, core dimensions, depth of organic layer, texture, soil moisture, Olsen P, and metals.
    - Some measurements apply to all 591 squares; others apply to original 256 squares or only to specific x-plots within squares.
  - Temperature, pH sampling, and other chemistry were not consistently performed by soil horizon; samples were homogenised prior to pH/LOI analyses.
  - Documentation and methods:
    - Full description and implications of methods are available in Emmett et al. (2008).
  - National vs. local estimates:
    - Analyses may involve weighting by land-class structure to yield national estimates; ignoring land classes yields stock/change estimates not accounting for class structure.

- Statistical considerations for GIS analyses
  - Data structure implications:
    - Use mixed models with square as a random factor to account for multiple x-plots per CS square (up to 5).
  - Sampling design implications:
    - CS is design-based and spatial structure is not always the primary interest; a dispersed set of observations often improves regional precision and coverage.
  - Analysis guidance:
    - Consider land-class structure in analyses; consult CEH prior to analysis and review CS publications for context and prior usage of the data.
  - Data integration cautions:
    - Data from different years and different core types may not be directly comparable without harmonisation; certain measurements may be missing for some plots or years.
  - Data availability:
    - A substantial portion of detailed measurements became available only after the 2009 Soils Report.

- References
  - Emmett, BA, et al. Countryside Survey Soils 2007: Method development, power analyses and protocols. Centre for Ecology and Hydrology Project No. C03042/ DEFRA Contact No. CR0334.