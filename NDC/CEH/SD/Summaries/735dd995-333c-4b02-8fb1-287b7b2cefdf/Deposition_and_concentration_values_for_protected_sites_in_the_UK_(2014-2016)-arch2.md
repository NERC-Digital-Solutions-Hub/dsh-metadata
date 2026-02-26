# UK Acidifying and Eutrophying Atmospheric Pollutants Supporting information

- Purpose and scope
  - Documents the CBED deposition and PCM concentration modelling approach used to map wet/dry deposition and pollutant concentrations to UK protected sites (SAC, SPA, SSSI).
  - Provides 3-year means for 2014–2016, with site-specific min, max, and area-weighted/grid-average values to support assessment of environmental health and policy performance over time.
  - Outputs are aligned with ecosystem types ( Moorland, Forest/Woodland) and grid averages to enable ecosystem-specific exceedance analyses and comparisons.

- Modelling approaches
  - CBED (Concentration Based Estimated Deposition)
    - Produces 5x5 km resolution maps of wet and dry deposition for sulfur, oxidised and reduced nitrogen, and base cations, based on air concentrations and precipitation data from UK networks (UKEAP).
    - Wet deposition derived from precipitation plus occult deposition to vegetation; separation of anthropogenic vs total components using sea-salt ratios.
    - Dry deposition uses gas and PM deposition to five land-cover categories (forest, moorland, grassland, arable, urban) and applies to relevant habitats (mooring to non-woodland, forest to woodland).
    - Includes orographic enhancement factors; inter-annual variability tempered by using rolling 3-year means.
    - Outputs include ecosystem-specific results (moorland, forest) and grid-average deposition.
  - PCM (Pollution Climate Mapping)
    - Produces 1x1 km grid background maps of pollutant concentrations (NOx, NO2, SO2, PM, etc.) with additional road-side values.
    - Used for scenario assessment, population exposure calculations, and supporting TEN applications; run per pollutant with base-year and projection models.

- Spatial data processing workflow
  - Step 1: Create a UK-wide 5x5 km grid, clip to SAC/SPA/SSSI boundaries, and merge with the 3-year CBED output (2014–2016) to create a UK protected sites CBED dataset; repeat for 1x1 km NOx and SO2 concentration data from PCM.
  - Step 2: For each protected site, generate minimum, maximum, and grid-average deposition/concentration values by SQL querying the gridded data; grid average is area-weighted within the site using grid square area.

- Data outputs and structure
  - CBED-derived data
    - 3-year means for deposition (nitrogen and sulfur species) and concentrations (NH3, NOx, SO2) at site level and grid level.
    - Datasets capture multiple deposition components (NH3/NH4, NO2/NO3, SO2/SO4) for forests and moorlands, plus grid-average values.
  - PCM-derived concentration data
    - Annual concentration values aggregated to 3-year rolling means, with 1x1 km grid resolution and 5x5 km grid summaries.
  - Datasets and columns (examples)
    - Dataset 1–3: 5x5 km grid deposition by ecosystem (forest/moorland) and grid-average; site metadata (SITEAREA, CENTROID_X/Y, COUNTRY, DESIGNATION, YEAR) and deposition components (NH3_NH4, NO2_NO3, SO2_SO4_NM).
    - Dataset 4–6: Concentrations (NH3, NOx, SO2) by 1x1 km grid; site metadata; YEAR; CONC values.
    - Dataset 7–12: Minimum, maximum, and average deposition/concentration values by site (forest and moorland) and grid-average, across 5x5 km or 1x1 km resolutions as applicable.
  - Units and conversions
    - Deposition values: keq ha-1 year-1; convert to kg S ha-1 year-1 (multiply by 16) or kg N ha-1 year-1 (multiply by 14) as needed.
    - Concentrations: µg m-3.
  - Data completeness
    - NaN values indicate missing data in originating pollutant datasets.

- Quality assurance and provenance
  - Methods align with government QA standards; extensive peer review and involvement in Defra model inter-comparison exercises (Carslaw 2011).
  - Documentation, version control, and central storage of code; mass-balance checks and cross-year consistency checks.
  - Results published in peer-reviewed literature; overseen by senior responsible officers.

- Access, references, and supporting information
  - Data and supporting information are linked to UK-AIR/ Defra resources and the UK pollutant deposition portal.
  - Key references include methodological and observational studies underpinning CBED and PCM (e.g., Holme Moss, Great Dun Fell studies) and related reviews (RoTAP, inter-comparison reports).

- Practical implications for analysts
  - Provides standardized, 3-year averaged deposition and concentration datasets for UK protected sites, enabling trend analysis and policy performance assessment.
  - Supports cross-site comparisons and ecosystem-specific exceedance assessments (moorland vs forest).
  - Underlying data and outputs are designed for reuse and integration with other environmental datasets, facilitating broader analyses beyond the immediate CBED/PCM outputs.