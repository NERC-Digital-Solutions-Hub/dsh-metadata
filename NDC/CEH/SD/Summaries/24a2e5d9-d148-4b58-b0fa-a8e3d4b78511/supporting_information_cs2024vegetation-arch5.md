# Countryside Survey vegetation plots 2024

## Overview
- Countryside Survey is the UK’s ongoing audit of countryside natural resources, conducted since 1978 to track changes over time.
- A rolling survey program was adopted in 2019, with 2024 marking the first year of the second five-year cycle.
- The program captures multiple measures (soil, vegetation, habitats, landscape features) to enable ecosystem-level analysis; in 2024, the focus includes five point plots in each 1km square plus additional linear landscape feature plots where appropriate, and soil sampling aligned with adjacent plots.
- The aim is to collect data on ~500 1km squares per five-year cycle to detect spatial and temporal changes cost-effectively.

## Design and rolling program
- Sample design: 500 x 1km squares randomly selected per cycle, stratified by the Land Classification of Great Britain; around 100 squares visited annually.
- Exclusions: squares with more than 75% urban land or more than 90% sea are excluded.
- Time series rationale: the 1978 squares are retained to maximize long-running time series; additional squares surveyed first in 1990 are added to strengthen coverage.
- Rolling cycle: repeats every five years (2019–2023 first cycle; 2024 marks the start of the second cycle).
- Field scope: 2019–2023 cycles focused on soil and vegetation; 2024 additions include boundary, roadside, streamside, and hedgerow plots (dominant species in England), with soil sampling methods harmonized to adjacent plots.

## Methods and quality assurance
- Data collection: field surveys conducted by trained botanical survey teams using standard protocols (Smart et al., 2024); extensive pre-surveys and ongoing supervision ensure consistency.
- Training and QA: rigorous training; 10% of plots re-surveyed for quality assurance; QA analyses conducted by the same assessor since 1990 to ensure comparability and validation against JNCC habitat classifications.
- Documentation and standards: field data are documented in a field handbook (Smart et al., 2024) and linked to environmental zone and habitat classifications.

## Data products and file structure
- Two CSV data files are provided:
  - UKCEHCS_VEGETATION_PLOTS_2024.csv (Vegetation Plot - Plot Information)
    - Contains plot-level information: YEAR, SQUARE_ID, PLOT_TYPE (B boundary, H hedgerow, R roadside, S streamside), PLOT_ID, land classification codes (LC07, LC07_NUM), environmental zones (ENV_ZONE_2007, EZ_DESC_07), COUNTRY, COUNTY, and plot-specific attributes (PLOT_BH, PLOT_PH, trees, canopy/shrub height, and plot-type dependent fields).
  - UKCEHCS_VEGETATION_PLOT_SPECIES_2024.csv (Vegetation Plot - Species List)
    - Contains species data for each plot: YEAR, SQUARE_ID, PLOT_ID, PLOT_TYPE, species identifiers (BRC_NUMBER) and names (BRC_NAMES), nesting data (NEST_LEVEL), cover metrics (ZERO_COVER, FIRST_COVER, TOTAL_COVER), and notes on nomenclature.
- Nomenclature: plant names follow Stace (1997).
- Map and data confidence: Figure 1 provides a map of 2024 1km squares (distribution shown for confidentiality).

## Variables, codes, and relationships
- Plot and site coding: LC07 and LC07_NUM (ITE Land Classification 2007), ENV_ZONE_2007 with EZ_DESC_07, habitat and land classification references linked to broader IJCC and habitat schemes.
- Plot types reflect landscape context: B (boundary), H (hedgerow), R (roadside/verge), S (streamside).
- Data relationships: integrates with ITE Land Classification, Biodiversity Broad Habitat classifications, and related Countryside Survey documentation, with extensive references to methodology and supporting datasets (field handbook, statistical reports, and historical CS publications).

## Practical considerations for data governance
- Time-series integrity: rolling five-year cycle ensures ongoing comparability across years; long-running 1978 squares provide extended time series.
- Data quality and provenance: standardized protocols, comprehensive QA, and careful plot-location validation support data reliability for reuse in policy and research.
- Access and documentation: dataset is accompanied by detailed metadata, methodological references, and a field handbook (Smart et al., 2024) to aid interpretation and reuse.
- Limitations and caveats: data reflect a rotating sample of squares with annual visitation targets; 2024 includes additional plot types (linear features) that may affect cross-year comparability and require attention when aggregating across cycles.